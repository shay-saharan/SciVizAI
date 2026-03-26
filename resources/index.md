---
title: Resources
nav_order: 9
layout: default
---

# Resources

A curated list of papers and publications relevant to AI in scientific and medical visualization.

<!-- 
  HOW TO CONNECT YOUR GOOGLE SHEET:
  1. Open your Google Sheet.
  2. Go to File → Share → Publish to web.
  3. Under "Link", select the sheet tab and choose "Comma-separated values (.csv)".
  4. Click Publish and copy the URL.
  5. Replace YOUR_PUBLISHED_CSV_URL_HERE below with that URL.

  Expected column order in the sheet: Name | Link | Summary
-->

<div id="resources-table-container">
  <p id="resources-loading" style="color: gray; font-style: italic;">Loading resources…</p>
  <table id="resources-table" style="display:none; width:100%; border-collapse:collapse;">
    <thead>
      <tr>
        <th style="text-align:left; padding:8px 12px; border-bottom:2px solid #ccc; white-space:nowrap;">Name</th>
        <th style="text-align:left; padding:8px 12px; border-bottom:2px solid #ccc; white-space:nowrap;">Link</th>
        <th style="text-align:left; padding:8px 12px; border-bottom:2px solid #ccc;">Summary</th>
      </tr>
    </thead>
    <tbody id="resources-tbody"></tbody>
  </table>
  <p id="resources-error" style="display:none; color:#c00;">
    Unable to load resources. Please check that the Google Sheet is published and the URL is correct.
  </p>
</div>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var SHEET_CSV_URL = "https://docs.google.com/spreadsheets/d/e/2PACX-1vSidHu0dxrOgjL8tNKqSZy133_vx627FQt3EJywRIzB1H5HV-adalF3mEeyNJh3jWVwJPmbmIxsv5g-/pub?output=csv";
  // Route through a CORS proxy to avoid browser cross-origin blocks
  var CSV_URL = "https://api.allorigins.win/raw?url=" + encodeURIComponent(SHEET_CSV_URL);

  var loading = document.getElementById("resources-loading");
  var table   = document.getElementById("resources-table");
  var tbody   = document.getElementById("resources-tbody");
  var error   = document.getElementById("resources-error");

  function showError(msg) {
    if (loading) loading.style.display = "none";
    if (error) { error.textContent = msg || "Unable to load resources. Check the sheet is published publicly."; error.style.display = "block"; }
  }

  var xhr = new XMLHttpRequest();
  xhr.open("GET", CSV_URL, true);
  xhr.timeout = 20000;
  xhr.onload = function () {
    if (xhr.status >= 200 && xhr.status < 300) {
      renderCSV(xhr.responseText);
    } else {
      showError("HTTP error " + xhr.status + " fetching the sheet.");
    }
  };
  xhr.onerror   = function () { showError("Network error — cannot reach the Google Sheet."); };
  xhr.ontimeout = function () { showError("Request timed out fetching the Google Sheet."); };
  xhr.send();

  function renderCSV(csv) {
      var rows = parseCSV(csv);
      // Skip header row (row 0)
      for (var i = 1; i < rows.length; i++) {
        var row = rows[i];
        if (row.every(function (c) { return c.trim() === ""; })) continue;
        var name    = row[0] || "";
        var link    = row[1] || "";
        var summary = row[2] || "";

        var tr = document.createElement("tr");
        tr.style.borderBottom = "1px solid #e0e0e0";

        var tdName = document.createElement("td");
        tdName.style.padding = "8px 12px";
        tdName.style.verticalAlign = "top";
        tdName.textContent = name;

        var tdLink = document.createElement("td");
        tdLink.style.padding = "8px 12px";
        tdLink.style.verticalAlign = "top";
        tdLink.style.whiteSpace = "nowrap";
        if (link) {
          var a = document.createElement("a");
          // Ensure link has a protocol
          a.href = /^https?:\/\//i.test(link) ? link : "https://" + link;
          a.target = "_blank";
          a.rel = "noopener noreferrer";
          a.textContent = "View paper";
          tdLink.appendChild(a);
        }

        var tdSummary = document.createElement("td");
        tdSummary.style.padding = "8px 12px";
        tdSummary.style.verticalAlign = "top";
        tdSummary.textContent = summary;

        tr.appendChild(tdName);
        tr.appendChild(tdLink);
        tr.appendChild(tdSummary);
        tbody.appendChild(tr);
      }

    if (tbody.children.length === 0) {
      showError("The sheet appears to be empty or could not be parsed.");
    } else {
      loading.style.display = "none";
      table.style.display = "table";
    }
  }

  // Minimal RFC 4180-compliant CSV parser
  function parseCSV(text) {
    var rows = [];
    var row = [];
    var i = 0;
    var field = "";
    while (i < text.length) {
      var ch = text[i];
      if (ch === '"') {
        i++;
        while (i < text.length) {
          if (text[i] === '"' && text[i + 1] === '"') {
            field += '"'; i += 2;
          } else if (text[i] === '"') {
            i++; break;
          } else {
            field += text[i++];
          }
        }
      } else if (ch === ',') {
        row.push(field); field = ""; i++;
      } else if (ch === '\r' && text[i + 1] === '\n') {
        row.push(field); field = ""; rows.push(row); row = []; i += 2;
      } else if (ch === '\n') {
        row.push(field); field = ""; rows.push(row); row = []; i++;
      } else {
        field += ch; i++;
      }
    }
    if (field || row.length) { row.push(field); rows.push(row); }
    return rows;
  }
});
</script>
