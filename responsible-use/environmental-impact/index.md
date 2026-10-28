---
title: Environmental Impact
parent: Responsible Use
nav_order: 5
layout: default
---

# Environmental Impact

<div class="notice" style="border-left: 4px solid #369E88; background: #f2f8f6; padding: 1rem 1.25rem; margin: 1.5rem 0;">

This section examines the environmental footprint of AI across its major operational and material pathways, including model training, inference, AI infrastructures, computational variation across modalities, and the impacts of AI hardware. Together these insights provide the foundation for sustainable AI use, with the following section exploring the role of developers in reducing the environmental cost of AI design and outlining how individuals can mitigate downstream effects through mindful use and practical everyday strategies. 

</div>

AI workflows can require significant compute, energy, and infrastructure resources depending on model size and usage patterns. This is an important topic that helps AI users weigh whether the benefits of generative tools justify their costs. However, past research shows that these choices are rarely as simple as deciding whether AI use is “good” or “bad.” Education on environmental impact remains limited overall, which restricts informed judgment and prevents people across disciplines from accessing the knowledge and resources needed to adopt not only responsible but also sustainable practices in the growing wave of AI (Jansen et al., 2026).

Additionally, AI is used across a wide range of disciplines, each with its own context and patterns of integration, even where some overlap exists. As a result, field-specific guidance is essential. In biomedical communication, for example, the environmental demands of AI must be understood alongside existing computational practices, where high-performance computing systems already support extensive data storage and petaflop-processing. (Kovatch et al., 2020). In terms of large computing environments such as Minerva, substantial energy consumption and infrastructure requirements long predate generative AI (Kovatch et al., 2020). As a result, AI tools introduce a continuous processing load to an already demanding ecosystem, heavily compounding existing project-based computing burdens. This section aims to provide a meaningful analysis of the underlying factors that shape the environmental impact of AI (training, inference, data centers, and more) and to outline how these effects can be understood and navigated across diverse contexts.

## Training AI Models 

The environmental cost of AI spans several interconnected components, one of the most significant being the substantial computational power required to train modern AI models. While advances in specialized hardware and training techniques have enabled dramatic improvements in accuracy, these gains come with proportionally higher financial and environmental costs due to the energy intensive nature of large-scale model training (Strubell et al., 2019). For example, GPT‑4 was estimated to consume 50–70 GWh of electricity over a 100‑day training period, nearly 50 times more than GPT‑3 (Aczel et al., 2026). 

>  As noted by Aczel et al. (2026), “60 GWh of electricity is equivalent to the annual residential electricity consumption of 460,000 people in Sub‑Saharan Africa.

Additionally, the energy required to train these models is predominantly generated from traditional fossil fuels, which remains the most cost‑effective source of energy in many regions and therefore a major contributor of AI‑related carbon emissions. (Z. Li et al., 2025). 

Moreover, AI training requires high-performance accelerators rather than general purpose chips. Unlike CPUs, modern AI models depend on specialized hardware such as GPUs and TPUs, which draw significantly more power and generate substantial heat during operation (Aczel et al., 2026). This increased thermal output necessitates intensive cooling systems, with many data centers using water-based methods such as evaporative cooling where water consumption scales directly with heat output. Given that training keeps GPUs operating at full capacity for prolonged intervals (any amount of time from weeks to months), cooling systems must run continuously, driving substantially higher cumulative water consumption compared to typical non-training operations (Barnett-Itzhaki, 2026). As a result, water-based cooling can place additional pressure on local water infrastructures, especially in regions already facing scarcity (P. Li et al., 2025). 

> CPU: A Central Processing Unit (CPU) is the computer’s main processor or the “brain” responsible for most operations, including arithmetic, logic, and input/output (Nikolic et al., 2022). It contains a Control Unit that translates instructions into binary and an Arithmetic Logic Unit (ALU) that carries out those instructions, performing tens of operations per cycle.
> GPU: A Graphics Processing Unit (GPU) is a chip that works with the CPU to process 2D and 3D images more efficiently than a CPU and can perform thousands of operations per cycle (Nikolic et al., 2022). While initially designed for graphics tasks, high-end GPUs have emerged as excellent accelerators for AI training and inference. 
> TPU: A Tensor Processing Unit (TPU) was developed by Google and is primarily used to accelerate tensor calculations in artificial intelligence, machine learning and deep learning (Nikolic et al., 2022). TPUs are able to perform four Trillion Operations Per Second (TOPS).

## AI Inference 

Inference is a term used to describe the process of using trained AI models to produce predictions or conclusions in response to user input. Although it requires fewer resources per operation than training, inference occurs continuously (everytime a prompt is submitted). The massive scale of inference burdened by the widespread and growing use of AI systems, accounts for 80-90% of AI’s total computing power (Podder et al., 2026). This imbalance is evident in GPT-4, whose cumulative carbon emissions from 121 days of inference match those produced during its entire training run (Podder et al., 2026). These trends illustrate the environmental burden of AI as it shifts towards high volume inference, making the sustainability of routine prompting a central concern. 

A number of emerging tools can offer estimates of the energy use, carbon emissions, water consumption, and other resource impacts linked to various AI models. One such example is EcoLogits, whose calculator estimates these impacts at the stage of daily inference. This calculator operates by using available information from generative AI providers to approximate variables such as model parameter counts and applies a bottom-up methodology that begins with assessing the environmental impacts of individual computational components before scaling upward to effects at the software level (CodeCarbon, n.d.). It is important to note that these estimates rely on publicly available information and inferred parameter counts, the results should be interpreted as approximations rather than precise measurements of environmental impact. Regardless, EcoLogits remains a useful tool that helps bridge the current transparency gap when direct reporting from AI providers is unavailable. 

## Data Centers

The concerns with training AI models are amplified when these systems are deployed within large-scale data centers. The addition of AI workloads significantly increases computational intensity, leading to increased energy use and therefore environmental strain. Estimates show that AI operations alone could produce 24-44 million metric tons of CO₂ annually within a decade (Chouksey et al., 2025). This challenge is compounded by the rapid expansion of new facilities, which require about 10-40 times more energy than data centers built before 2015, reflecting both higher computational density and increased cooling requirements (Privette et al., 2026). Water use in data center cooling varies widely, with facilities evaporating roughly 1-9 L of water for every kWh of server energy, a range shaped by local climate conditions and the type of cooling technologies employed. 

Another environmental concern relates to land use, as data centers are physical infrastructure that impose a substantial burden on the landscapes where they are built. The development of large AI facilities frequently converts peri-urban, agricultural land, and other available spaces into specialized industrial areas, displacing existing uses and locking regions into long-term spatial commitments (Hlabisa, 2025). Consequently, the construction of this infrastructure limits ecological flexibility and contributes to regional capacity limits. Although the discourse on data centers and biodiversity remains limited, researchers such as Hlabisa (2025) highlight the role of AI operations in accelerating habitat fragmentation and intensifying stress on local ecosystems.

It remains difficult to assess the full environmental impact of data centers, especially with lack of transparency by their operators and AI-based companies. Several major firms acknowledge that AI is driving large increases in electricity use, water consumption, and other resource needs, yet very few provide an effective overview that isolates the environmental cost of AI operations especially when the cost is complicated by many interconnected factors (De Vries-Gao, 2025). For example, in the case of data centers, current reporting practices only provide broad estimates for total data center emissions and water use, without identifying how much of that footprint is specifically attributable to AI workloads. This gap exists due to the lack of detailed information centered around how AI systems are being operated or the amount of power these systems consume within individual facilities (De Vries-Gao, 2025). Environmental assessments typically rely on knowing a data center's location, energy consumption, and characteristics of its local electric grid, hence making transparency in operations key for precise evaluation. 

This challenge is further compounded by the fact that the environmental impact of electricity itself varies significantly across regions. For example, countries dominated by hydropower, such as Brazil, often exhibit significantly lower carbon intensity but substantially higher water and land footprints (Aczel et al., 2026). These differences mean that identical AI workloads can have a vastly different environmental impact depending on where they are run. As a result, without knowing the specific locations of AI operations, researchers cannot accurately determine the true carbon, water, or land impacts associated with large-scale AI systems. Overall, transparency is essential because it enables meaningful mitigation strategies and informed policy development, allowing AI technologies to advance in a responsible and sustainable manner. 

## Environmental Costs Across AI Output Modalities

From previous passages, it is understood that the structure and infrastructure supporting AI generates a substantial environmental cost. However, there is another dimension that requires examination which is the variation between different AI output modalities. The energy required to generate an output is not uniform, advances in AI have shifted the field from single modality systems to multimodal models like CLIP, DALL-E, and GPT-4V (Gautan, 2023). Because these models perform computations across images, audio, and video, they require substantially more processing and therefore more energy than traditional text-based inference. 

In terms of scaling, compared to a basic text classification, which depending on the model and hardware spans anywhere from a mwh to kWh in terms of energy consumption, a ChatGPT style prompt uses about 200 times more energy (Zschache & Hartwig, 2026; Aczel et al., 2026). Similarly an AI-generated image uses around 2000 times more, and a short video can require roughly 200,000 times more ( Aczel et al., 2026). Multimodal AI models are hence difficult to evaluate consistently, given the substantial variation in energy use across modalities. These values can change significantly depending on the length and richness of the media generated by different models. For example, upscale models like Lumina can significantly increase the energy cost of AI-generated images (Aczel et al., 2026). 

An additional consideration is re-prompting, which involves submitting a new prompt (with some alterations) in order to ensure that the AI output meets the required standard. This technique is difficult to quantify, as there is no fixed number of iterations that guarantees improvement, however, it can be qualitatively assessed through the gradual refinement of the output toward completion. This is an essential topic as repeated re-prompting increases the total number of inference cycles performed, adding to the overall energy consumption associated with AI-generated content. This concern can also be amplified by considering the growing number of tasks operationalized by AI systems. At scale, these repeated interactions have the potential to significantly compound the environmental burden. Moreover, given the substantial variability in how AI tools are used across contexts, assessing the true environmental cost of AI remains a persistent challenge. 

## Hardware Manufacturing 

As briefly mentioned, AI models utilize specialized hardware (GPUs and TPUs), the production of these devices carries significant environmental implications. Modern GPUs contain heavy metals including but not limited to arsenic, mercury, lead, cadmium, and others that are classified as hazardous (Falk et al., 2026). These materials pose severe risks to ecosystems that absorb the long-term buildup of metal contaminants, as well as to people in mining zones due to potential water contamination. Although the quantity of hazardous material in a single GPU itself is small, large-scale AI training requires thousands of units and hence the cumulative burden of metal extraction, processing, and eventual e-waste disposal becomes significant (Falk et al., 2026). 

## Socioecological Impacts of E-Waste 

Due to increased device consumption, limited recycling capacity, and short product life cycles, it has been estimated that global e-waste will increase to 80 million tons by 2030, outcompeting documented recycling practices by almost five-fold (Christensen, 2025). Due to this increasing demand, the availability of high-performance computing power is constrained, with global chip production being unable to keep up with the pace of consumption across both consumer electronics and AI infrastructure (Lohn et al., 2021). The semiconductor company Nvidia currently supplies the majority of AI accelerators, reporting 37% of its revenue in 2021 from the datacenter market, a percentage that is increasing to support large-scale AI workloads (Lohn et al., 2021). This concentration of demand places pressure on manufacturing, hardware turnover, and rapid growth of electronic waste. 

>  It is estimated that by 2030, total e-waste generated by AI infrastructure will be comparable to annually discarding around 250 Eiffel Towers (Aczel et al., 2026).

Metal contamination is a serious concern with much of this e-waste being illicitly exported to countries such as China, Ghana, and India, where unsafe dumping and processing poses severe health risks to surrounding communities (Christensen, 2025). The seepage of hazardous materials such as cadmium, mercury, and lead from landfills has impacted all levels of the community. Impacts range from lead poisoning in children, to health issues among workers that burn plastics to recover metal (such as copper), to broader public exposure through contaminated drinking water and the inhalation of toxic fumes (Christensen, 2025). These harms are intensified by unsafe e-waste processing practices, including particles released by the burning of hardware and the use of oxidizing acids to extract valuable metals, processes that contaminate soil, threaten plant and microbial life, and contribute to biomagnification across food chains (Quinto et al., 2025). Ultimately highlighting another key element, the impact of AI is not confined to indirect pressures such as land use or carbon emissions, it also develops as direct harm to human health, underscoring the socioecological consequences embedded in the lifecycle of AI hardware. 

## Additional Factors

While earlier sections have outlined several major sources of environmental burden, it is important to recognize that the impact of generative AI is far more complex. There are numerous points across the AI lifecycle where additional energy is required to maintain smooth and reliable operation, extending well beyond the training and deployment of models. One such example is idle machine energy. To keep AI systems continuously available, production environments maintain reserved computing capacity that can respond to unexpected events (Elsworth et al., 2025). Even when this capacity is not active, it remains powered on, thereby consuming additional energy. 

Another factor to consider is efficiency, particularly within data centers. Because these facilities are not fully efficient, they incur additional energy costs. This is reflected in the Power Usage Effectiveness (PUE) metric, which accounts for the energy required to run supporting systems such as power conversion equipment and other overhead operations (Elsworth et al., 2025). Collectively, these considerations highlight the need to investigate the environmental burden of AI systems with a holistic perspective.

> Overall, there are a lot of components that contribute to the harmful effects of artificial intelligence tools. Every step of the process from large-scale model training to everyday inference produces measurable energy, carbon, water and material impacts. Given the scale and trajectory of these systems, it is essential to consider how sustainable AI practices can mitigate these effects and promote more responsible development and individual use. 

## Sustainable AI Practices

The sustainability of AI is an important topic, highlighting the need for greater transparency and consistent, effective policy frameworks. This section examines sustainability from the large‑scale practices involved in designing, training, and powering AI systems to the smaller, everyday choices users make that collectively influence AI’s environmental footprint.

### Developing AI Systems

AI systems are rapidly developing, there is a continual drive to create newer, more specialized models suited for an expanding range of sectors. However, as this technology expands, so does the need for techniques within AI research and development that can alleviate the significant environmental burden of the AI lifecycle. 

### Model Optimization

AI training is an energy intensive process due to the length and complexity of the training process, and various tests and parameters that increase its computational cost. As a result, model optimization is a major goal for those pursuing sustainable AI. Pruning is a technique that removes parameters and thus reduces model size (along with resources for training and inference) leading to lower energy consumption (Tabbakh et al., 2024). Similarly, using efficient algorithms which reduce the complexity of mathematical operations, or the introduction of transfer learning which reuses pre-trained general models. By working over existing models, transfer learning substantially reduces the computational workload and therefore energy consumption associated with developing AI systems (Tabbakh et al., 2024). However, these techniques introduce a trade-off in model accuracy, where gains in efficiency sometimes come at the expense of reduced predictive accuracy. This requires developers to balance sustainability benefits with acceptable accuracy thresholds. 

Given that lower-precision models reduce energy consumption, another technique that could be employed is quantization. Similar to model compression, this is a newer method that has been shown to offload the energy cost of AI systems by up to 50% without a significant loss in performance (Esho et al., 2026). Simply put, this technique reduces high-precision model parameters into lower-bit formats (i.e., from a 32-bit floating-point to an 8-bit), thereby decreasing the computational and memory requirements during training and inference (Khan et al., 2025). However, while using less-precise numbers does make AI models significantly smaller, it can also introduce small errors and is not suitable for tasks that require very detailed calculations (Khan et al., 2025). Developers therefore need to consider who will use the model and whether the reduced precision will still meet their needs. Overall, this reduction method is promising, especially as the field of AI looks for more sustainable ways to lower energy use while still meeting a good standard of performance. 

### Renewable Energy

Fossil fuels remain a major percentage of energy use for AI operations, and expanding the current use of renewable energy sources such as solar, wind, and other low-carbon technologies offers several benefits for sustainable data centers. Integrating renewable energy into AI infrastructure planning also enables more purposeful land use, co-locating data centers with renewable generation can encourage land use strategies that align technological growth with sustainable operations (Tabbakh et al., 2024). However, there are issues with location optimization leading to concerns about long-term sustainability as data centers become concentrated in areas with abundant renewable energy (Bolón-Canedo et al., 2024).

### Mindful Use at the Individual Level

AI is a tool that has shown significant potential in many different sectors. Continued use will require long-term sustainability, which can begin on a local scale by adopting mindful usage practices. 

#### Evaluating Necessity

Before discussing how to use this technology more efficiently, it is important to  acknowledge that not using AI at all is also a legitimate response to its environmental cost. There is a very real tension between embracing AI’s capabilities and recognizing that choosing not to engage is itself a meaningful form of environmental responsibility. In light of this tension, a key shift involves the integration of critical assessment practices. One of the major changes is integrating critical assessment practices to determine when AI use is genuinely necessary rather than merely convenient, a move supported by authors such as Emma Christensen (2025), who offers reflective prompts for practitioners. For example “Is using generative AI to translate a text instead of hiring a proofreader worth the energy consumption?” This can be implemented on a personal level, as part of an individual’s approach to  sustainable and responsible AI use.

This evaluation can also extend to right model sizing, ensuring that when AI is used, the chosen model is proportionate to the task rather than being unnecessarily larger. Although larger systems typically achieve the highest performance, this corresponds with increased environmental costs. Hence, researchers such as Haase et al. (2026) showcase how smaller models frequently deliver comparable results for many daily tasks whether it be summarizing information, drafting emails, etc., thereby consuming less energy and offering meaningful reductions in overall cost of use. Models such as Gemma-3 and Phi-4 do not reach the same performance as GPT-4o but still provide consistent and reliable outputs with a significantly lower energy footprint (Haase et al., 2026). This highlights the importance of selecting a model that is proportionate to the task rather than defaulting to the largest available option. Even small shifts in model choice can reduce unnecessary computation and represents a practical step towards more sustainable AI use. 

### Local Models vs. Cloud Inference

One topic that remains difficult to fully contextualize is the difference between inference in local devices (often called edge devices) versus cloud data centers and how this informs the choices of the general public. Although the exact impact varies depending on usage patterns, deployment methods, and several other parameters, researchers such as Li et al. (2025) have attempted to model how inference workloads differ between these two systems. An important aspect in relation to edge devices is that they cannot run advanced models without modification (i.e., quantization to fit within processing constraints) making energy use during inference significantly lower (Li et al., 2025). This leads to their greatest downside, the inability to handle highly complex computations that typically require the scale and precision of cloud platforms. 

Additionally, because AI models run locally, the environmental impact associated with transmitting data to distant cloud servers is eliminated, further improving energy efficiency (Li et al., 2025). These models also avoid many of the environmental pressures associated with large-scale data centers, including intensive cooling requirements, short hardware lifespans, and the substantial energy needed to keep cloud servers operating continuously (Li et al., 2025). Moreover, the work of Li et al. (2025) determined that edge devices can reduce carbon emissions and water consumption by nearly 80%. This highlights how local inference can be more sustainable for everyday, low-energy tasks. However, it is important to emphasize that local models still produce a measurable impact and some forms such as federated learning (training directly on user model) requires many rounds of on-device computation, increasing carbon emissions (Wu et al., 2021). As a result, consumers need to be more conscious of which platform they select, but also of when and how they choose to use AI technologies, as every form of utilization carries an environmental cost.

### Efficient Prompting Practices

Another change involves prompt engineering, given the environmental concerns associated with inference energy, it is important to ensure optimized prompting that reduces AI energy consumption. It has been estimated that effective prompting has the ability to reduce greenhouse gas emissions by around 32-48%, making it critical for lowering the environmental footprint of everyday AI use (Podder et al., 2026). Research by Podder et al., (2026) has highlighted different practices that users can employ to ensure energy efficient usage, some of these key strategies are listed below.

Variational prompting: asking AI for more than one solution to avoid continuous prompt reiteration. 

> Goal: to simplify and interpret the information presented in the abstract of a complex research paper.
> Example: “Provide three interpretations of this abstract: one suited for a non-professional reader, one for a student in the field, and one for a practitioner.”

Avoiding terminological ambiguities: ensuring the use of effective language to prevent generating irrelevant responses. 

> When abbreviating phrases such as “technical design document” into TDD, it becomes difficult to determine the exact meaning. The same abbreviation can also refer to “test-driven development” or “tentative delivery date,” and while this ambiguity may not always cause issues in highly specific prompts, being intentional about sentence structure can help avoid misunderstanding that lead to repeated re-prompting (Podder et al., 2026). Clear phrasing reduces the likelihood of misinterpretation and supports efficient more energy conscious interactions with AI technologies.

Specifying response length: longer responses directly increase energy use, specifying the desired length helps the model produce concise and relevant answers. 

> Goal: to write a concise, business appropriate email to a supervisor. 
> Example: “Generate a professional email asking for clarification on the following topic: _ in under three sentences.”

## Attribution

Author(s): Sania Khurshid

Editor(s): Derek Ng, Shehryar (Shay) Saharan, Nick Woolridge

## References 

Aczel, M., Chamanara, S., Matin, M., Farsi, A., Marwala, T., & Madani, K. (2026). The environmental cost of AI’s energy use: carbon, water and land footprints. https://doi.org/10.53328/inr26rma002

Barnett-Itzhaki, Z. (2026). The water footprint of artificial intelligence: Emerging solutions and governance imperatives. Water Research (Oxford), 299, Article 125866. https://doi.org/10.1016/j.watres.2026.125866

Bolón-Canedo, V., Morán-Fernández, L., Cancela, B., & Alonso-Betanzos, A. (2024). A review of green artificial intelligence: Towards a more sustainable future. Neurocomputing, 599, 128096. https://doi.org/10.1016/j.neucom.2024.128096

Chouksey, A., Rajan, A. K., Gurjar, V., Tiwari, R., & Mishra, P. K. (2025). The green paradox: The climate, environmental, and sustainability implications of artificial intelligence. Global Environmental Change Advances, 6, 100029. https://doi.org/10.1016/j.gecadv.2025.100029

Christensen, E. (2025). The socio-ecological costs of AI: Toward socially responsible and sustainable communication practices. Public Relations Inquiry. https://doi.org/10.1177/2046147x251377853

CodeCarbon. (n.d.). EcoLogits Calculator. https://calculator.ecologits.ai/

De Vries-Gao, A. (2025). The carbon and water footprints of data centers and what this could mean for artificial intelligence. Patterns, 7(1), 101430. https://doi.org/10.1016/j.patter.2025.101430

Elsworth, C., Huang, K., Patterson, D., Schneider, I., Sedivy, R., Goodman, S., Townsend, B., Ranganathan, P., Dean, J., Vahdat, A., Gomes, B., & Manyika, J. (2025). Measuring the environmental impact of delivering AI at Google Scale. arXiv (Cornell University). https://doi.org/10.48550/arxiv.2508.15734

Esho, E. O., Akinyelu, A. A., & Dinis, M. a. P. (2026). Sustainable generative AI and quantum computing: review assessment on the environmental impact of generative AI and quantum technologies. Frontiers in Sustainability, 7. https://doi.org/10.3389/frsus.2026.1726832

Falk, S., Corrêa, N. K., Luccioni, S., Biber-Freudenberger, L., & Van Wynsberghe, A. (2026). From computation to environmental cost the resource burden of artificial intelligence. Communications Earth & Environment, 7(1). https://doi.org/10.1038/s43247-026-03537-5

Gautam, S. (2023). Bridging multimedia modalities: enhanced multimodal AI understanding and intelligent agents. INTERNATIONAL CONFERENCE ON MULTIMODAL INTERACTION, 695–699. https://doi.org/10.1145/3577190.3614225

Haase, J., Klessascheck, F., Mendling, J., & Pokutta, S. (2026). Sustainability via large language model right-sizing. IEEE Transactions on Sustainable Computing, 1–14. https://doi.org/10.1109/tsusc.2026.3697261

Hlabisa, S. (2025). The ecology of artificial intelligence: energy, water, materials, and land limits of digital systems. Carbon Neutral Systems, 1(1). https://doi.org/10.1007/s44438-025-00018-8

Khan, T., Motie, S., Kocak, S. A., & Raza, S. (2025). Optimizing large language models: metrics, energy efficiency, and case study insights. arXiv (Cornell University). https://doi.org/10.48550/arxiv.2504.06307

Kovatch, P., Gai, L., Cho, H. M., Fluder, E., & Jiang, D. (2020). Optimizing High-Performance Computing Systems for Biomedical Workloads. IEEE Int Symp Parallel Distrib Process Workshops Phd Forum, 2020, 183–192. https://doi.org/10.1109/ipdpsw50202.2020.00040

Li, P., Islam, M. J., & Ren, S. (2025). A Case Study of Environmental Footprints for Generative AI Inference: Cloud versus Edge. ACM SIGMETRICS Performance Evaluation Review, 53(2), 21–26. https://doi.org/10.1145/3764944.3764950

Li, P., Yang, J., Islam, M. A., & Ren, S. (2025). Making AI Less “Thirsty.” Communications of the ACM, 68(7), 54–61. https://doi.org/10.1145/3724499

Li, Z., Xing, Y., Shao, X., Zhong, Y., & Su, Y. H. (2025). Transitioning the energy landscape: AI’s role in shifting from fossil fuels to renewable energy. Energy Economics, 149, 108729. https://doi.org/10.1016/j.eneco.2025.108729

Lohn, A. J., Musser, M., & Center for Security and Emerging Technology. (2021). AI and Compute. In CSET Issue Brief. https://cset.georgetown.edu/wp-content/uploads/AI-and-Compute-How-Much-Longer-Can-Computing-Power-Drive-Artificial-Intelligence-Progress_v2.pdf

Nikolic, G. S., Dimitrijevic, B. R., Nikolic, T. R., & Stojcev, M. K. (2022). A survey of three types of processing units: CPU, GPU and TPU. 2022 57th International Scientific Conference on Information, Communication and Energy Systems and Technologies (ICEST), 1–6. https://doi.org/10.1109/icest55168.2022.9828625

Privette, A. P., Barros, A., & Cai, X. (2026). Data centers water footprint: the need for more transparency. AGU Advances, 7(2). https://doi.org/10.1029/2025av002140

Podder, S., Date, H., & Murthy, S. (2026). Green prompt engineering for sustainable generative AI. Environmental Science and Ecotechnology, 30, 100684. https://doi.org/10.1016/j.ese.2026.100684

Strubell, E., Ganesh, A., & McCallum, A. (2019, July). Energy and policy considerations for deep learning in NLP. In Proceedings of the 57th annual meeting of the association for computational linguistics (pp. 3645-3650). 

Tabbakh, A., Amin, L. A., Islam, M., Mahmud, G. M. I., Chowdhury, I. K., & Mukta, M. S. H. (2024). Towards sustainable AI: a comprehensive framework for Green AI. Discover Sustainability, 5(1). https://doi.org/10.1007/s43621-024-00641-4

Wu, C., Raghavendra, R., Gupta, U., Acun, B., Ardalani, N., Maeng, K., Chang, G., Behram, F. A., Huang, J., Bai, C., Gschwind, M., Gupta, A., Ott, M., Melnikov, A., Candido, S., Brooks, D., Chauhan, G., Lee, B., Lee, H. S., . . . Hazelwood, K. (2021). Sustainable AI: environmental implications, challenges and opportunities. arXiv (Cornell University). https://doi.org/10.48550/arxiv.2111.00364
