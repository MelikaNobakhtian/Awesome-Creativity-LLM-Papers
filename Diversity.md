# Diversity in Creativity: A Reading List

![papers](https://img.shields.io/badge/papers-119-blue) ![metadata](https://img.shields.io/badge/metadata-verified%20against%20arXiv%20%2B%20OpenAlex-brightgreen) ![updated](https://img.shields.io/badge/updated-2026--10--13-lightgrey) ![license](https://img.shields.io/badge/list-CC0--1.0-informational)

**119 papers on the diversity of machine creativity**: how it is defined, how it is measured, how it is lost, and what has been tried to get it back.

A language model asked the same open-ended question a hundred times will often give nearly the same answer, and two different models will often give nearly the same answer as each other. That observation now has a literature: metrics for it, benchmarks that score it, measurements of its spread into human writing and culture, accounts of which training step causes it, and a fast-growing set of fixes. This list collects that literature in the order the argument runs, foundations, measurement, phenomena, causes, remedies, norms, so it can be read front to back rather than searched.


## Legend

| Mark | Meaning |
| :-: | --- |
| ★★★ | Diversity or homogeneity of output is the object of study |
| ★★ | Diversity is a main axis of the paper, but its goal is something else |
| ★ | Listed for framing or lineage only, collected under [Adjacent and background reading](#adjacent-and-background-reading) |


## Start here

Eight papers that between them cover the whole argument:

- **[The Curious Case of Neural Text Degeneration](http://arxiv.org/abs/1904.09751v2)** (2020, ICLR 2020): where the diversity-quality trade-off in decoding was first made precise
- **[Understanding the Effects of RLHF on LLM Generalisation and Diversity](http://arxiv.org/abs/2310.06452v3)** (2024, ICLR 2024): the clearest demonstration that alignment buys capability with variety
- **[Artificial Hivemind: The Open-Ended Homogeneity of Language Models (and Beyond)](http://arxiv.org/abs/2510.22954v2)** (2025, NeurIPS 2025 Datasets & Benchmarks (Oral)): the largest measurement of open-ended homogeneity to date, within and across models
- **[Generative AI enhances individual creativity but reduces the collective diversity of novel content](https://doi.org/10.1126/sciadv.adn5290)** (2024, Science Advances 10(28) (2024)): the human-side result: individual stories get better, the collection gets narrower
- **[AI models collapse when trained on recursively generated data](https://doi.org/10.1038/s41586-024-07566-y)** (2024, Nature 631:755–759 (2024)): what happens when models train on their own output
- **[NoveltyBench: Evaluating Language Models for Humanlike Diversity](http://arxiv.org/abs/2504.05228v4)** (2025, COLM 2025): how to measure diversity in a way that correlates with what people notice
- **[Verbalized Sampling: How to Mitigate Mode Collapse and Unlock LLM Diversity](http://arxiv.org/abs/2510.01171v4)** (2025, arXiv preprint (no published version found)): — the typicality-bias account of mode collapse, plus a prompt-level fix
- **[A Roadmap to Pluralistic Alignment](http://arxiv.org/abs/2402.05070v3)** (2024, ICML 2024): the normative vocabulary — which kind of pluralism a model should even aim for

## Contents

- [A. Foundations: creativity theory and the diversity construct](#a-foundations-creativity-theory-and-the-diversity-construct): 5 papers
- [B. Measuring diversity: metrics](#b-measuring-diversity-metrics): 10 papers
- [C. Benchmarks and evaluation suites](#c-benchmarks-and-evaluation-suites): 10 papers
- [D. Phenomenon: homogenization of model output](#d-phenomenon-homogenization-of-model-output): 13 papers
- [E. Phenomenon: effects on people, culture, and the information ecosystem](#e-phenomenon-effects-on-people-culture-and-the-information-ecosystem): 14 papers
- [F. Self-consuming loops: model collapse and knowledge collapse](#f-self-consuming-loops-model-collapse-and-knowledge-collapse): 8 papers
- [G. Causes and mechanisms](#g-causes-and-mechanisms): 6 papers
- [H. Remedies at inference time: decoding and sampling](#h-remedies-at-inference-time-decoding-and-sampling): 10 papers
- [I. Remedies at inference time: prompting, personas, and steering](#i-remedies-at-inference-time-prompting-personas-and-steering): 12 papers
- [J. Remedies in training and post-training](#j-remedies-in-training-and-post-training): 11 papers
- [K. Open-endedness, quality-diversity, and search](#k-open-endedness-quality-diversity-and-search): 5 papers
- [L. Pluralism, safety, and the diversity-quality trade-off](#l-pluralism-safety-and-the-diversity-quality-trade-off): 10 papers
- [Adjacent and background reading](#adjacent-and-background-reading): 5 papers
- [Contributing](#contributing)
- [License](#license)

## A. Foundations: creativity theory and the diversity construct

Where the claim that creativity *requires* variation comes from. These are the works a survey cites to justify treating diversity as a property worth measuring rather than a side effect of sampling.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★★ | 1960 | [Blind variation and selective retentions in creative thought as in other knowledge processes.](https://doi.org/10.1037/h0040373) | Donald T. Campbell | Psychological Review 67(6):380–400 (1960) | [DOI 10.1037/h0040373](https://doi.org/10.1037/h0040373) |
| ★★★ | 1967 | [The Nature of Human Intelligence](https://gwern.net/doc/iq/1967-guilford-thenatureofhumanintelligence.pdf) | J. P. Guilford | Book — McGraw-Hill, New York | [ISBN 978-0070251359](https://gwern.net/doc/iq/1967-guilford-thenatureofhumanintelligence.pdf) |
| ★★ | 1990 / 2004 | The Creative Mind: Myths and Mechanisms | Margaret A. Boden | Book — Weidenfeld & Nicolson, London (1st ed., 1990); 2nd ed. Routledge, 2004 | ISBN 978-0415314534 (2nd ed.) |
| ★★ | 2024 | [On the Creativity of Large Language Models](http://arxiv.org/abs/2304.00008v5) | Giorgio Franceschelli, Mirco Musolesi | AI & Society (2024) | [arXiv:2304.00008](http://arxiv.org/abs/2304.00008v5) |
| ★★ | 2024 | [On the stochastics of human and artificial creativity](http://arxiv.org/abs/2403.06996v1) | Solve Sæbø, Helge Brovold | arXiv preprint (no published version found) | [arXiv:2403.06996](http://arxiv.org/abs/2403.06996v1) |

[↑ Contents](#contents)

## B. Measuring diversity: metrics

Metric-level work: n-gram and embedding distance, reference-free diversity scores, syntactic templates, calibration of open-endedness. These papers define the quantity; Section C assembles it into benchmarks.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★★ | 2016 | [A Diversity-Promoting Objective Function for Neural Conversation Models](http://arxiv.org/abs/1510.03055v3) | Jiwei Li, Michel Galley, Chris Brockett et al. | NAACL-HLT 2016 | [arXiv:1510.03055](http://arxiv.org/abs/1510.03055v3) |
| ★★ | 2018 | [Texygen: A Benchmarking Platform for Text Generation Models](http://arxiv.org/abs/1802.01886v1) | Yaoming Zhu, Sidi Lu, Lei Zheng et al. | arXiv preprint — prior draft lists SIGIR 2018 (not confirmed by arXiv/OpenAlex) | [arXiv:1802.01886](http://arxiv.org/abs/1802.01886v1) |
| ★★ | 2019 | [Unifying Human and Statistical Evaluation for Natural Language Generation](https://doi.org/10.18653/v1/n19-1169) | Tatsunori Hashimoto, Hugh Zhang, Percy Liang | NAACL-HLT 2019 | [DOI 10.18653/v1/n19-1169](https://doi.org/10.18653/v1/n19-1169) |
| ★★★ | 2022 | [Measuring and Improving Semantic Diversity of Dialogue Generation](http://arxiv.org/abs/2210.05725v2) | Seungju Han, Beomsu Kim, Buru Chang | Findings of EMNLP 2022 | [arXiv:2210.05725](http://arxiv.org/abs/2210.05725v2) |
| ★★★ | 2022 | [Rethinking and Refining the Distinct Metric](https://doi.org/10.18653/v1/2022.acl-short.86) | Siyang Liu, Sahand Sabour, Yinhe Zheng et al. | ACL 2022 (Short) | [DOI 10.18653/v1/2022.acl-short.86](https://doi.org/10.18653/v1/2022.acl-short.86) |
| ★★★ | 2022 | [Semantic Diversity in Dialogue with Natural Language Inference](https://doi.org/10.18653/v1/2022.naacl-main.6) | Katherine Stasaski, Marti A. Hearst | NAACL 2022 (Main) | [DOI 10.18653/v1/2022.naacl-main.6](https://doi.org/10.18653/v1/2022.naacl-main.6) |
| ★★★ | 2022 | [The Vendi Score: A Diversity Evaluation Metric for Machine Learning](http://arxiv.org/abs/2210.02410v2) | Dan Friedman, Adji Bousso Dieng | arXiv preprint — prior draft lists TMLR 2023 (not confirmed by arXiv/OpenAlex) | [arXiv:2210.02410](http://arxiv.org/abs/2210.02410v2) |
| ★★ | 2023 | [Beyond semantic distance: Automated scoring of divergent thinking greatly improves with large language models](https://doi.org/10.1016/j.tsc.2023.101356) | Peter Organisciak, Selçuk Acar, Denis Dumas et al. | Thinking Skills and Creativity (2023) | [DOI 10.1016/j.tsc.2023.101356](https://doi.org/10.1016/j.tsc.2023.101356) · [PDF](https://www.researchgate.net/publication/363456838_Beyond_Semantic_Distance_Automated_Scoring_of_Divergent_Thinking_Greatly_Improves_with_Large_Language_Models) |
| ★★★ | 2023 | [Pragmatically Appropriate Diversity for Dialogue Evaluation](http://arxiv.org/abs/2304.02812v1) | Katherine Stasaski, Marti A. Hearst | arXiv preprint (no published version found) | [arXiv:2304.02812](http://arxiv.org/abs/2304.02812v1) |
| ★★★ | 2024 | [Detection and Measurement of Syntactic Templates in Generated Text](http://arxiv.org/abs/2407.00211v2) | Chantal Shaib, Yanai Elazar, Junyi Jessy Li et al. | EMNLP 2024 | [arXiv:2407.00211](http://arxiv.org/abs/2407.00211v2) |
| ★★★ | 2024 | [Exploring Precision and Recall to assess the quality and diversity of LLMs](http://arxiv.org/abs/2402.10693v3) | Florian Le Bronnec, Alexandre Verine, Benjamin Negrevergne et al. | ACL 2024 (Main) | [arXiv:2402.10693](http://arxiv.org/abs/2402.10693v3) |
| ★★★ | 2025 | [Benchmarking Linguistic Diversity of Large Language Models](http://arxiv.org/abs/2412.10271v2) | Yanzhu Guo, Guokan Shang, Chloé Clavel | TACL (2025) | [arXiv:2412.10271](http://arxiv.org/abs/2412.10271v2) |
| ★★★ | 2025 | [Evaluating the Diversity and Quality of LLM Generated Content](http://arxiv.org/abs/2504.12522v2) | Alexander Shypula, Shuo Li, Botong Zhang et al. | COLM 2025 | [arXiv:2504.12522](http://arxiv.org/abs/2504.12522v2) |
| ★★★ | 2025 | [Evaluating the Evaluation of Diversity in Commonsense Generation](http://arxiv.org/abs/2506.00514v1) | Tianhui Zhang, Bei Peng, Danushka Bollegala | ACL 2025 (Main) | [arXiv:2506.00514](http://arxiv.org/abs/2506.00514v1) |
| ★★★ | 2025 | [Generation Space Size: Understanding and Calibrating Open-Endedness of LLM Generations](http://arxiv.org/abs/2510.12699v1) | Sunny Yu, Ahmad Jabbar, Robert Hawkins et al. | arXiv preprint (no published version found) | [arXiv:2510.12699](http://arxiv.org/abs/2510.12699v1) |
| ★★ | 2025 | [Measuring AI "Slop" in Text](http://arxiv.org/abs/2509.19163v2) | Chantal Shaib, Tuhin Chakrabarty, Diego Garcia-Olano et al. | arXiv preprint (no published version found) | [arXiv:2509.19163](http://arxiv.org/abs/2509.19163v2) |
| ★★ | 2025 | [Reasoning Path Divergence: A New Metric and Curation Strategy to Unlock LLM Diverse Thinking](http://arxiv.org/abs/2510.26122v2) | Feng Ju, Zeyu Qin, Rui Min et al. | arXiv preprint (no published version found) | [arXiv:2510.26122](http://arxiv.org/abs/2510.26122v2) |
| ★★★ | 2025 | [Standardizing the Measurement of Text Diversity: A Tool and a Comparative Analysis of Scores](http://arxiv.org/abs/2403.00553v3) | Chantal Shaib, Venkata S. Govindarajan, Joe Barrow et al. | AACL 2025 | [arXiv:2403.00553](http://arxiv.org/abs/2403.00553v3) |
| ★★★ | 2025 | [Task-Dependent Evaluation of LLM Output Homogenization: A Taxonomy-Guided Framework](http://arxiv.org/abs/2509.21267v3) | Shomik Jain, Jack Lanchantin, Maximilian Nickel et al. | arXiv preprint (no published version found) | [arXiv:2509.21267](http://arxiv.org/abs/2509.21267v3) |
| ★★ | 2026 | [Death of the Novel(ty): Beyond n-Gram Novelty as a Metric for Textual Creativity](http://arxiv.org/abs/2509.22641v2) | Arkadiy Saakyan, Najoung Kim, Smaranda Muresan et al. | ICLR 2026 | [arXiv:2509.22641](http://arxiv.org/abs/2509.22641v2) |

[↑ Contents](#contents)

## C. Benchmarks and evaluation suites

Task suites and human-study protocols that score models for creativity and diversity end to end, including the divergent-thinking batteries imported from psychology.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★ | 2022 | [Putting GPT-3's Creativity to the (Alternative Uses) Test](http://arxiv.org/abs/2206.08932v1) | Claire Stevenson, Iris Smal, Matthijs Baas et al. | ICCC 2022 (Int. Conf. on Computational Creativity) | [arXiv:2206.08932](http://arxiv.org/abs/2206.08932v1) |
| ★★ | 2023 | [A Confederacy of Models: a Comprehensive Evaluation of LLMs on Creative Writing](http://arxiv.org/abs/2310.08433v1) | Carlos Gómez-Rodríguez, Paul Williams | Findings of EMNLP 2023 | [arXiv:2310.08433](http://arxiv.org/abs/2310.08433v1) |
| ★★★ | 2023 | [Probing the Creativity of Large Language Models: Can models produce divergent semantic association?](http://arxiv.org/abs/2310.11158v1) | Honghua Chen, Nai Ding | Findings of EMNLP 2023 | [arXiv:2310.11158](http://arxiv.org/abs/2310.11158v1) |
| ★★ | 2024 | [Art or Artifice? Large Language Models and the False Promise of Creativity](http://arxiv.org/abs/2309.14556v3) | Tuhin Chakrabarty, Philippe Laban, Divyansh Agarwal et al. | ACM CHI 2024 | [arXiv:2309.14556](http://arxiv.org/abs/2309.14556v3) |
| ★★★ | 2024 | [Can LLMs Generate Novel Research Ideas? A Large-Scale Human Study with 100+ NLP Researchers](http://arxiv.org/abs/2409.04109v1) | Chenglei Si, Diyi Yang, Tatsunori Hashimoto | arXiv preprint (no published version found) | [arXiv:2409.04109](http://arxiv.org/abs/2409.04109v1) |
| ★★ | 2025 | [Assessing and Understanding Creativity in Large Language Models](https://doi.org/10.1007/s11633-025-1546-4) | Yunpu Zhao, Rui Zhang, Wenyi Li et al. | Machine Intelligence Research (2025) | [DOI 10.1007/s11633-025-1546-4](https://doi.org/10.1007/s11633-025-1546-4) |
| ★★ | 2025 | [Benchmarking Language Model Creativity: A Case Study on Code Generation](http://arxiv.org/abs/2407.09007v2) | Yining Lu, Dixuan Wang, Tianjian Li et al. | NAACL 2025 (Long) | [arXiv:2407.09007](http://arxiv.org/abs/2407.09007v2) |
| ★★★ | 2025 | [NoveltyBench: Evaluating Language Models for Humanlike Diversity](http://arxiv.org/abs/2504.05228v4) | Yiming Zhang, Harshita Diddee, Susan Holm et al. | COLM 2025 | [arXiv:2504.05228](http://arxiv.org/abs/2504.05228v4) |
| ★★ | 2026 | [Automated Creativity Evaluation of Language Models Across Open-Ended Tasks](http://arxiv.org/abs/2606.11762v1) | Min Sen Tan, Zachary Kit Chun Choy, Syed Ali Redha Alsagoff et al. | ACL 2026 (Main) | [arXiv:2606.11762](http://arxiv.org/abs/2606.11762v1) |
| ★★★ | 2026 | [Beyond Divergent Creativity: A Human-Based Evaluation of Creativity in Large Language Models](http://arxiv.org/abs/2601.20546v1) | Kumiko Nakajima, Jan Zuiderveld, Sandro Pezzelle | Findings of EACL 2026 | [arXiv:2601.20546](http://arxiv.org/abs/2601.20546v1) |
| ★★★ | 2026 | [CreativityPrism: A Cross-Domain Evaluation Framework for Large Language Model Creativity](http://arxiv.org/abs/2510.20091v3) | Zhaoyi Joey Hou, Bowei Alvin Zhang, Yining Lu et al. | TMLR (06/2026) | [arXiv:2510.20091](http://arxiv.org/abs/2510.20091v3) |
| ★★★ | 2026 | [Divergent creativity in humans and large language models](https://doi.org/10.1038/s41598-025-25157-3) | Antoine Bellemare, François Lespinasse, Philipp Thölke et al. | Scientific Reports 16:1279 (2026) | [DOI 10.1038/s41598-025-25157-3](https://doi.org/10.1038/s41598-025-25157-3) |
| ★★ | 2026 | [LitBench: A Benchmark and Dataset for Reliable Evaluation of Creative Writing](http://arxiv.org/abs/2507.00769v1) | Daniel Fein, Sebastian Russo, Violet Xiang et al. | EACL 2026 (Long) | [arXiv:2507.00769](http://arxiv.org/abs/2507.00769v1) |

[↑ Contents](#contents)

## D. Phenomenon: homogenization of model output

Direct measurements of the effect: one model collapsing onto a few modes, and different models converging on the same ones. The core empirical evidence.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★★ | 2024 | [Creativity Has Left the Chat: The Price of Debiasing Language Models](http://arxiv.org/abs/2406.05587v1) | Behnam Mohammadi | arXiv preprint; also SSRN Electronic Journal (2024) | [arXiv:2406.05587](http://arxiv.org/abs/2406.05587v1) |
| ★★★ | 2024 | [Detecting Mode Collapse in Language Models via Narration](http://arxiv.org/abs/2402.04477v1) | Sil Hamilton | SCALE-LLM 2024 workshop (ACL Anthology 2024.scalellm-1.5) | [arXiv:2402.04477](http://arxiv.org/abs/2402.04477v1) |
| ★★★ | 2024 | [Generative Monoculture in Large Language Models](http://arxiv.org/abs/2407.02209v1) | Fan Wu, Emily Black, Varun Chandrasekaran | arXiv preprint (no published version found) | [arXiv:2407.02209](http://arxiv.org/abs/2407.02209v1) |
| ★★★ | 2024 | [Heads, Tails, and AI Fails: LLMs, Randomness, and Human Judgments](http://arxiv.org/abs/2406.00092v2) | Katherine Van Koevering, Jon Kleinberg | arXiv preprint (no published version found) | [arXiv:2406.00092](http://arxiv.org/abs/2406.00092v2) |
| ★★★ | 2024 | [Understanding the Effects of RLHF on LLM Generalisation and Diversity](http://arxiv.org/abs/2310.06452v3) | Robert Kirk, Ishita Mediratta, Christoforos Nalmpantis et al. | ICLR 2024 | [arXiv:2310.06452](http://arxiv.org/abs/2310.06452v3) |
| ★★★ | 2025 | [Artificial Hivemind: The Open-Ended Homogeneity of Language Models (and Beyond)](http://arxiv.org/abs/2510.22954v2) | Liwei Jiang, Yuanjun Chai, Margaret Li et al. | NeurIPS 2025 Datasets & Benchmarks (Oral) | [arXiv:2510.22954](http://arxiv.org/abs/2510.22954v2) |
| ★★★ | 2025 | [Base Models Beat Aligned Models at Randomness and Creativity](http://arxiv.org/abs/2505.00047v2) | Peter West, Christopher Potts | COLM 2025 | [arXiv:2505.00047](http://arxiv.org/abs/2505.00047v2) |
| ★★★ | 2025 | [Correlated Errors in Large Language Models](http://arxiv.org/abs/2506.07962v1) | Elliot Kim, Avi Garg, Kenny Peng et al. | ICML 2025 | [arXiv:2506.07962](http://arxiv.org/abs/2506.07962v1) |
| ★★★ | 2025 | [Echoes in AI: Quantifying lack of plot diversity in LLM outputs](http://arxiv.org/abs/2501.00273v2) | Weijia Xu, Nebojsa Jojic, Sudha Rao et al. | PNAS 122(35):e2504966122 (2025) | [arXiv:2501.00273](http://arxiv.org/abs/2501.00273v2) |
| ★★★ | 2025 | [Testing English News Articles for Lexical Homogenization Due to Widespread Use of Large Language Models](https://doi.org/10.18653/v1/2025.acl-srw.95) | Sarah Fitterer, Dominik Gangl, Jannes Ulbrich | ACL 2025 | [DOI 10.18653/v1/2025.acl-srw.95](https://doi.org/10.18653/v1/2025.acl-srw.95) |
| ★★★ | 2025 | [Variance reduction in output from generative AI](http://arxiv.org/abs/2503.01033v1) | Yu Xie, Yueqi Xie | arXiv preprint (no published version found) | [arXiv:2503.01033](http://arxiv.org/abs/2503.01033v1) |
| ★★★ | 2025 | [We're Different, We're the Same: Creative Homogeneity Across LLMs](http://arxiv.org/abs/2501.19361v1) | Emily Wenger, Yoed Kenett | arXiv preprint (no published version found) | [arXiv:2501.19361](http://arxiv.org/abs/2501.19361v1) |
| ★★★ | 2026 | [Creative Convergence or Imitation? Genre-Specific Homogeneity in LLM-Generated Chinese Literature](http://arxiv.org/abs/2603.14430v1) | Yuanchi Ma, Kaize Shi, Hui He et al. | arXiv preprint (no published version found) | [arXiv:2603.14430](http://arxiv.org/abs/2603.14430v1) |
| ★★★ | 2026 | [Elias in the Lighthouse, Again? Diagnosing Low Diversity in LLM Stories](http://arxiv.org/abs/2605.26492v1) | Sil Hamilton, David Mimno | arXiv preprint (no published version found) | [arXiv:2605.26492](http://arxiv.org/abs/2605.26492v1) |
| ★★★ | 2026 | [Narrative Flattening: How Post-Training Compresses Thematic, Affective, and Stylistic Variation in LLM Fiction](http://arxiv.org/abs/2605.27878v2) | Zehan Li, Yutong Zhu, Siyang Wu et al. | EMNLP 2026 (Main) | [arXiv:2605.27878](http://arxiv.org/abs/2605.27878v2) |
| ★★ | 2026 | [Rethinking the Evaluation of Alignment Methods: Insights into Diversity, Generalisation, and Safety](http://arxiv.org/abs/2509.12936v1) | Denis Janiak, Julia Moska, Dawid Motyka et al. | EACL 2026 (Student Research Workshop) | [arXiv:2509.12936](http://arxiv.org/abs/2509.12936v1) |
| ★★★ | 2026 | [The Chameleon's Limit: Investigating Persona Collapse and Homogenization in Large Language Models](https://doi.org/10.48550/arxiv.2604.24698) | Yunze Xiao, Vivienne J. Zhang, Chenghao Yang et al. | arXiv preprint (no published version found) | [DOI 10.48550/arxiv.2604.24698](https://doi.org/10.48550/arxiv.2604.24698) |
| ★★★ | 2026 | [The Hitchhiker's Guide to Monoculture: AI Homogenizes Syntax, Not (Necessarily) Semantics](http://arxiv.org/abs/2607.13077v3) | Gordon Burtch | arXiv preprint (no published version found) | [arXiv:2607.13077](http://arxiv.org/abs/2607.13077v3) |

[↑ Contents](#contents)

## E. Phenomenon: effects on people, culture, and the information ecosystem

What happens when homogenized output enters a human population — collective idea diversity, co-writing, cultural and linguistic narrowing, citation and topic monoculture.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★ | 2023 | [Artificial Artificial Artificial Intelligence: Crowd Workers Widely Use Large Language Models for Text Production Tasks](http://arxiv.org/abs/2306.07899v1) | Veniamin Veselovsky, Manoel Horta Ribeiro, Robert West | arXiv preprint (no published version found) | [arXiv:2306.07899](http://arxiv.org/abs/2306.07899v1) |
| ★★ | 2023 | [Machine Culture](http://arxiv.org/abs/2311.11388v2) | Levin Brinkmann, Fabian Baumann, Jean-François Bonnefon et al. | Nature Human Behaviour 7:1855–1868 (2023) | [arXiv:2311.11388](http://arxiv.org/abs/2311.11388v2) |
| ★★ | 2023 | [Which Humans?](https://doi.org/10.31234/osf.io/5b26t) | Mohammad Atari, Mona J. Xue, Peter S. Park et al. | PsyArXiv preprint (no journal version found in OpenAlex) | [DOI 10.31234/osf.io/5b26t](https://doi.org/10.31234/osf.io/5b26t) |
| ★★★ | 2024 | [Competition and Diversity in Generative AI](http://arxiv.org/abs/2412.08610v3) | Manish Raghavan | arXiv preprint (no published version found) | [arXiv:2412.08610](http://arxiv.org/abs/2412.08610v3) |
| ★★★ | 2024 | [Does Writing with Language Models Reduce Content Diversity?](http://arxiv.org/abs/2309.05196v3) | Vishakh Padmakumar, He He | ICLR 2024 | [arXiv:2309.05196](http://arxiv.org/abs/2309.05196v3) |
| ★★★ | 2024 | [Generative AI enhances individual creativity but reduces the collective diversity of novel content](https://doi.org/10.1126/sciadv.adn5290) | Anil Rajnikant Doshi, Oliver Hauser | Science Advances 10(28) (2024) | [DOI 10.1126/sciadv.adn5290](https://doi.org/10.1126/sciadv.adn5290) |
| ★★★ | 2024 | [Homogenization Effects of Large Language Models on Human Creative Ideation](http://arxiv.org/abs/2402.01536v2) | Barrett R. Anderson, Jash Hemant Shah, Max Kreminski | C&C 2024 | [arXiv:2402.01536](http://arxiv.org/abs/2402.01536v2) |
| ★★ | 2024 | [Not All Countries Celebrate Thanksgiving: On the Cultural Dominance in Large Language Models](http://arxiv.org/abs/2310.12481v2) | Wenxuan Wang, Wenxiang Jiao, Jingyuan Huang et al. | ACL 2024 (Long) | [arXiv:2310.12481](http://arxiv.org/abs/2310.12481v2) |
| ★★★ | 2025 | [Homogenizing effect of large language models (LLMs) on creative diversity: An empirical comparison of human and ChatGPT writing](https://doi.org/10.1016/j.chbah.2025.100207) | Kibum Moon, Adam E. Green, Kostadin Kushlev | Computers in Human Behavior: Artificial Humans (2025) | [DOI 10.1016/j.chbah.2025.100207](https://doi.org/10.1016/j.chbah.2025.100207) |
| ★★★ | 2026 | [Aligned but Flattened: Analyzing the Trade-off between Cultural Alignment and Diversity in LLMs](http://arxiv.org/abs/2609.00565v1) | Jingshen Zhang, Shaoyang Xu, Wenxuan Zhang | Findings of EMNLP 2026 | [arXiv:2609.00565](http://arxiv.org/abs/2609.00565v1) |
| ★★★ | 2026 | [Artificial intelligence tools expand scientists’ impact but contract science’s focus](https://doi.org/10.1038/s41586-025-09922-y) | Qianyue Hao, Fengli Xu, Yong Li et al. | Nature 649:1237–1243 (2026) | [DOI 10.1038/s41586-025-09922-y](https://doi.org/10.1038/s41586-025-09922-y) |
| ★★★ | 2026 | [Examining and Addressing Barriers to Diversity in LLM-Generated Ideas](http://arxiv.org/abs/2602.20408v1) | Yuting Deng, Melanie Brucks, Olivier Toubia | arXiv preprint; also SSRN Electronic Journal (2026) | [arXiv:2602.20408](http://arxiv.org/abs/2602.20408v1) |
| ★★ | 2026 | [How Did Writing Change At CHI? Analyzing 44 Years of CHI Writing Before and After the Introduction of Large Language Models](http://arxiv.org/abs/2609.23090v1) | Thomas Kosch, Robin Welsch, Michael Hedderich et al. | arXiv preprint (no published version found) | [arXiv:2609.23090](http://arxiv.org/abs/2609.23090v1) |
| ★★★ | 2026 | [Human diversity fuels collective creativity that large language models cannot simulate or sustain](http://arxiv.org/abs/2607.26899v1) | Mengchen Dong, Hiromu Yakura | arXiv preprint (no published version found) | [arXiv:2607.26899](http://arxiv.org/abs/2607.26899v1) |
| ★★★ | 2026 | [Narrowing the Horizon: Quantifying Topic Saliency Shifts in Generative Monoculture](http://arxiv.org/abs/2609.35302v1) | Oriane Peter, Elena Simperl, Kate Devlin | Findings of EMNLP 2026 | [arXiv:2609.35302](http://arxiv.org/abs/2609.35302v1) |
| ★★★ | 2026 | [When AI Writes, Who Gets Cited? Evidence of Citation Monoculture Across Language Models](http://arxiv.org/abs/2608.19230v1) | Sina Alemohammad, Denghui Zhang, Bolong Tang et al. | arXiv preprint (no published version found) | [arXiv:2608.19230](http://arxiv.org/abs/2608.19230v1) |

[↑ Contents](#contents)

## F. Self-consuming loops: model collapse and knowledge collapse

The feedback-loop literature, kept deliberately small. The statistical-theory branch is large and mostly orthogonal; these are the entries a diversity reader needs, plus the main critiques.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★ | 2024 | [A Note on Shumailov et al. (2024): `AI Models Collapse When Trained on Recursively Generated Data'](http://arxiv.org/abs/2410.12954v2) | Ali Borji | arXiv preprint (no published version found) | [arXiv:2410.12954](http://arxiv.org/abs/2410.12954v2) |
| ★★ | 2024 | [A Tale of Tails: Model Collapse as a Change of Scaling Laws](http://arxiv.org/abs/2402.07043v2) | Elvis Dohmatob, Yunzhen Feng, Pu Yang et al. | ICML 2024 | [arXiv:2402.07043](http://arxiv.org/abs/2402.07043v2) |
| ★★★ | 2024 | [AI models collapse when trained on recursively generated data](https://doi.org/10.1038/s41586-024-07566-y) | Ilia Shumailov, Zakhar Shumaylov, Yiren Zhao et al. | Nature 631:755–759 (2024) | [DOI 10.1038/s41586-024-07566-y](https://doi.org/10.1038/s41586-024-07566-y) |
| ★★ | 2024 | [Is Model Collapse Inevitable? Breaking the Curse of Recursion by Accumulating Real and Synthetic Data](http://arxiv.org/abs/2404.01413v2) | Matthias Gerstgrasser, Rylan Schaeffer, Apratim Dey et al. | arXiv preprint (no published version found) | [arXiv:2404.01413](http://arxiv.org/abs/2404.01413v2) |
| ★★★ | 2024 | [The Curious Decline of Linguistic Diversity: Training Language Models on Synthetic Text](http://arxiv.org/abs/2311.09807v2) | Yanzhu Guo, Guokan Shang, Michalis Vazirgiannis et al. | Findings of NAACL 2024 | [arXiv:2311.09807](http://arxiv.org/abs/2311.09807v2) |
| ★★★ | 2025 | [AI and the Problem of Knowledge Collapse](http://arxiv.org/abs/2404.03502v2) | Andrew J. Peterson | AI & Society (2025) | [arXiv:2404.03502](http://arxiv.org/abs/2404.03502v2) |
| ★★★ | 2025 | [Epistemic diversity across language models mitigates knowledge collapse](http://arxiv.org/abs/2512.15011v3) | Damian Hodel, Jevin D. West | arXiv preprint (no published version found) | [arXiv:2512.15011](http://arxiv.org/abs/2512.15011v3) |
| ★★ | 2025 | [Position: Model Collapse Does Not Mean What You Think](http://arxiv.org/abs/2503.03150v2) | Rylan Schaeffer, Joshua Kazdan, Alvan Caleb Arulandu et al. | arXiv preprint (no published version found) | [arXiv:2503.03150](http://arxiv.org/abs/2503.03150v2) |

[↑ Contents](#contents)

## G. Causes and mechanisms

Why diversity disappears: decoding behaviour, typicality bias, alignment and post-training dynamics, positional effects, the reasoning/creativity tension.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★★ | 2020 | [The Curious Case of Neural Text Degeneration](http://arxiv.org/abs/1904.09751v2) | Ari Holtzman, Jan Buys, Li Du et al. | ICLR 2020 | [arXiv:1904.09751](http://arxiv.org/abs/1904.09751v2) |
| ★★ | 2024 | [Beyond Reverse KL: Generalizing Direct Preference Optimization with Diverse Divergence Constraints](http://arxiv.org/abs/2309.16240v1) | Chaoqi Wang, Yibo Jiang, Chenghao Yang et al. | ICLR 2024 | [arXiv:2309.16240](http://arxiv.org/abs/2309.16240v1) |
| ★★★ | 2024 | [Forcing Diffuse Distributions out of Language Models](http://arxiv.org/abs/2404.10859v2) | Yiming Zhang, Avi Schwarzschild, Nicholas Carlini et al. | arXiv preprint (no published version found) | [arXiv:2404.10859](http://arxiv.org/abs/2404.10859v2) |
| ★★ | 2025 | [Beyond Pass@1: Self-Play with Variational Problem Synthesis Sustains RLVR](http://arxiv.org/abs/2508.14029v4) | Xiao Liang, Zhongzhi Li, Yeyun Gong et al. | arXiv preprint (no published version found) | [arXiv:2508.14029](http://arxiv.org/abs/2508.14029v4) |
| ★★★ | 2025 | [KL-Regularized Reinforcement Learning is Designed to Mode Collapse](http://arxiv.org/abs/2510.20817v1) | Anthony GX-Chen, Jatin Prakash, Jeff Guo et al. | arXiv preprint (no published version found) | [arXiv:2510.20817](http://arxiv.org/abs/2510.20817v1) |
| ★★ | 2025 | [The Entropy Mechanism of Reinforcement Learning for Reasoning Language Models](http://arxiv.org/abs/2505.22617v1) | Ganqu Cui, Yuchen Zhang, Jiacheng Chen et al. | arXiv preprint (no published version found) | [arXiv:2505.22617](http://arxiv.org/abs/2505.22617v1) |
| ★★★ | 2025 | [The Price of Format: Diversity Collapse in LLMs](http://arxiv.org/abs/2505.18949v1) | Longfei Yun, Chenyang An, Zilong Wang et al. | Findings of EMNLP 2025 | [arXiv:2505.18949](http://arxiv.org/abs/2505.18949v1) |
| ★★★ | 2025 | [Token Homogenization under Positional Bias](http://arxiv.org/abs/2508.17126v1) | Viacheslav Yusupov, Danil Maksimov, Ameliia Alaeva et al. | arXiv preprint (no published version found) | [arXiv:2508.17126](http://arxiv.org/abs/2508.17126v1) |
| ★★★ | 2026 | [Fine-Tuning Fixes Mode Collapse and Over-Dispersion in LLMs](http://arxiv.org/abs/2609.16454v1) | Kirill Skobelev, Eric Fithian, X. Y. Han | arXiv preprint (no published version found) | [arXiv:2609.16454](http://arxiv.org/abs/2609.16454v1) |
| ★★ | 2026 | [R-Diverse: Mitigating Diversity Illusion in Self-Play LLM Training](http://arxiv.org/abs/2602.13103v2) | Gengsheng Li, Jinghan He, Shijie Wang et al. | arXiv preprint (no published version found) | [arXiv:2602.13103](http://arxiv.org/abs/2602.13103v2) |
| ★★ | 2026 | [The Reasoning-Creativity Trade-off: Toward Creativity-Driven Problem Solving](http://arxiv.org/abs/2601.00747v1) | Max Ruiz Luyten, Mihaela van der Schaar | arXiv preprint (no published version found) | [arXiv:2601.00747](http://arxiv.org/abs/2601.00747v1) |
| ★★★ | 2026 | [Where does output diversity collapse in post-training?](http://arxiv.org/abs/2604.16027v1) | Constantinos Karouzos, Xingwei Tan, Nikolaos Aletras | arXiv preprint (no published version found) | [arXiv:2604.16027](http://arxiv.org/abs/2604.16027v1) |

[↑ Contents](#contents)

## H. Remedies at inference time: decoding and sampling

Truncation and temperature schemes, minimum Bayes risk, guided and seeded generation. The cheapest interventions, and the ones with the clearest diversity-quality trade-off curves.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★★ | 2018 | [Diverse Beam Search: Decoding Diverse Solutions from Neural Sequence Models](http://arxiv.org/abs/1610.02424v2) | Ashwin K Vijayakumar, Michael Cogswell, Ramprasath R. Selvaraju et al. | AAAI 2018 | [arXiv:1610.02424](http://arxiv.org/abs/1610.02424v2) |
| ★★ | 2024 | [EDT: Improving Large Language Models' Generation by Entropy-based Dynamic Temperature Sampling](http://arxiv.org/abs/2403.14541v2) | Shimao Zhang, Yu Bao, Shujian Huang | arXiv preprint (no published version found) | [arXiv:2403.14541](http://arxiv.org/abs/2403.14541v2) |
| ★★★ | 2024 | [Generating Diverse and High-Quality Texts by Minimum Bayes Risk Decoding](http://arxiv.org/abs/2401.05054v2) | Yuu Jinnai, Ukyo Honda, Tetsuro Morimura et al. | arXiv preprint (no published version found) | [arXiv:2401.05054](http://arxiv.org/abs/2401.05054v2) |
| ★★★ | 2024 | [Improving Diversity of Commonsense Generation by Large Language Models via In-Context Learning](http://arxiv.org/abs/2404.16807v2) | Tianhui Zhang, Bei Peng, Danushka Bollegala | Findings of EMNLP 2024 | [arXiv:2404.16807](http://arxiv.org/abs/2404.16807v2) |
| ★★★ | 2024 | [Is Temperature the Creativity Parameter of Large Language Models?](http://arxiv.org/abs/2405.00492v1) | Max Peeperkorn, Tom Kouwenhoven, Dan Brown et al. | ICCC 2024 (15th Int. Conf. on Computational Creativity) | [arXiv:2405.00492](http://arxiv.org/abs/2405.00492v1) |
| ★★★ | 2025 | [Balancing Diversity and Risk in LLM Sampling: How to Select Your Method and Parameter for Open-Ended Text Generation](http://arxiv.org/abs/2408.13586v2) | Yuxuan Zhou, Margret Keuper, Mario Fritz | ACL 2025 (Long) | [arXiv:2408.13586](http://arxiv.org/abs/2408.13586v2) |
| ★★★ | 2025 | [Control the Temperature: Selective Sampling for Diverse and High-Quality LLM Outputs](http://arxiv.org/abs/2510.01218v1) | Sergey Troshin, Wafaa Mohammed, Yan Meng et al. | COLM 2025 | [arXiv:2510.01218](http://arxiv.org/abs/2510.01218v1) |
| ★★★ | 2025 | [G2: Guided Generation for Enhanced Output Diversity in LLMs](http://arxiv.org/abs/2511.00432v1) | Zhiwen Ruan, Yixia Li, Yefeng Liu et al. | EMNLP 2025 | [arXiv:2511.00432](http://arxiv.org/abs/2511.00432v1) |
| ★★ | 2025 | [Min-p, Max Exaggeration: A Critical Analysis of Min-p Sampling in Language Models](http://arxiv.org/abs/2506.13681v2) | Rylan Schaeffer, Joshua Kazdan, Yegor Denisov-Blanch | arXiv preprint (no published version found) | [arXiv:2506.13681](http://arxiv.org/abs/2506.13681v2) |
| ★★ | 2025 | [Mode-Conditioning Unlocks Superior Test-Time Scaling](http://arxiv.org/abs/2512.01127v1) | Chen Henry Wu, Sachin Goyal, Aditi Raghunathan | arXiv preprint (no published version found) | [arXiv:2512.01127](http://arxiv.org/abs/2512.01127v1) |
| ★★ | 2025 | [Odysseus Navigates the Sirens' Song: Dynamic Focus Decoding for Factual and Diverse Open-Ended Text Generation](http://arxiv.org/abs/2503.08057v2) | Wen Luo, Feifan Song, Wei Li et al. | ACL 2025 (Main) | [arXiv:2503.08057](http://arxiv.org/abs/2503.08057v2) |
| ★★ | 2025 | [Optimizing Temperature for Language Models with Multi-Sample Inference](http://arxiv.org/abs/2502.05234v2) | Weihua Du, Yiming Yang, Sean Welleck | ICML 2025 | [arXiv:2502.05234](http://arxiv.org/abs/2502.05234v2) |
| ★★ | 2025 | [REAL Sampling: Boosting Factuality and Diversity of Open-ended Generation by Extrapolating the Entropy of an Infinitely Large LM](https://doi.org/10.1162/tacl_a_00757) | Haw-Shiuan Chang, Nanyun Peng, Mohit Bansal et al. | TACL (2025) | [DOI 10.1162/tacl_a_00757](https://doi.org/10.1162/tacl_a_00757) |
| ★★★ | 2025 | [SimpleStrat: Diversifying Language Model Generation with Stratification](http://arxiv.org/abs/2410.09038v2) | Justin Wong, Yury Orlovskiy, Michael Luo et al. | NeurIPS 2025 | [arXiv:2410.09038](http://arxiv.org/abs/2410.09038v2) |
| ★★ | 2025 | [Top-H Decoding: Adapting the Creativity and Coherence with Bounded Entropy in Text Generation](http://arxiv.org/abs/2509.02510v2) | Erfan Baghaei Potraghloo, Seyedarmin Azizi, Souvik Kundu et al. | NeurIPS 2025 | [arXiv:2509.02510](http://arxiv.org/abs/2509.02510v2) |
| ★★ | 2025 | [Turning Up the Heat: Min-p Sampling for Creative and Coherent LLM Outputs](http://arxiv.org/abs/2407.01082v8) | Minh Nhat Nguyen, Andrew Baker, Clement Neo et al. | ICLR 2025 (Oral) | [arXiv:2407.01082](http://arxiv.org/abs/2407.01082v8) |
| ★★★ | 2026 | [No Single Best Model for Diversity: Learning a Router for Sample Diversity](http://arxiv.org/abs/2604.02319v3) | Yuhan Liu, Fangyuan Xu, Vishakh Padmakumar et al. | COLM 2026 | [arXiv:2604.02319](http://arxiv.org/abs/2604.02319v3) |
| ★★★ | 2026 | [Optimizing Diversity and Quality through Base-Aligned Model Collaboration](http://arxiv.org/abs/2511.05650v2) | Yichen Wang, Chenghao Yang, Tenghao Huang et al. | ICML 2026 | [arXiv:2511.05650](http://arxiv.org/abs/2511.05650v2) |
| ★★★ | 2026 | [String Seed of Thought: Prompting LLMs for Distribution-Faithful and Diverse Generation](http://arxiv.org/abs/2510.21150v3) | Kou Misaki, Takuya Akiba | ICLR 2026 | [arXiv:2510.21150](http://arxiv.org/abs/2510.21150v3) |

[↑ Contents](#contents)

## I. Remedies at inference time: prompting, personas, and steering

Prompt-level and representation-level interventions: distribution prompting, multi-agent discussion, persona vectors, weight and activation steering.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★ | 2023 | [Diversity of Thought Improves Reasoning Abilities of LLMs](http://arxiv.org/abs/2310.07088v2) | Ranjita Naik, Varun Chandrasekaran, Mert Yuksekgonul et al. | arXiv preprint (no published version found) | [arXiv:2310.07088](http://arxiv.org/abs/2310.07088v2) |
| ★★★ | 2024 | [How Far Can We Extract Diverse Perspectives from Large Language Models?](http://arxiv.org/abs/2311.09799v3) | Shirley Anugrah Hayati, Minhwa Lee, Dheeraj Rajagopal et al. | EMNLP 2024 (Main) | [arXiv:2311.09799](http://arxiv.org/abs/2311.09799v3) |
| ★★ | 2024 | [LLM Discussion: Enhancing the Creativity of Large Language Models via Discussion Framework and Role-Play](http://arxiv.org/abs/2405.06373v4) | Li-Chun Lu, Shou-Jen Chen, Tsung-Min Pai et al. | COLM 2024 | [arXiv:2405.06373](http://arxiv.org/abs/2405.06373v4) |
| ★★ | 2024 | [Steering Large Language Models to Evaluate and Amplify Creativity](http://arxiv.org/abs/2412.06060v1) | Matthew Lyle Olson, Neale Ratzlaff, Musashi Hinck et al. | NeurIPS 2024 Workshop on Creativity & Generative AI (Spotlight) | [arXiv:2412.06060](http://arxiv.org/abs/2412.06060v1) |
| ★★★ | 2025 | [Asking a Language Model for Diverse Responses](http://arxiv.org/abs/2509.17570v1) | Sergey Troshin, Irina Saparina, Antske Fokkens et al. | UncertaiNLP 2025 workshop | [arXiv:2509.17570](http://arxiv.org/abs/2509.17570v1) |
| ★★ | 2025 | [Cooking Up Creativity: Enhancing LLM Creativity through Structured Recombination](http://arxiv.org/abs/2504.20643v2) | Moran Mizrahi, Chen Shani, Gabriel Stanovsky et al. | TACL (accepted; pre-MIT Press version) | [arXiv:2504.20643](http://arxiv.org/abs/2504.20643v2) |
| ★★★ | 2025 | [Exploring and Controlling Diversity in LLM-Agent Conversation](http://arxiv.org/abs/2412.21102v3) | KuanChao Chu, Yi-Pei Chen, Hideki Nakayama | Findings of EMNLP 2025 | [arXiv:2412.21102](http://arxiv.org/abs/2412.21102v3) |
| ★★★ | 2025 | [Multi-Novelty: Improve the Diversity and Novelty of Contents Generated by Large Language Models via inference-time Multi-Views Brainstorming](http://arxiv.org/abs/2502.12700v1) | Arash Lagzian, Srinivas Anumasa, Dianbo Liu | arXiv preprint (no published version found) | [arXiv:2502.12700](http://arxiv.org/abs/2502.12700v1) |
| ★★★ | 2025 | [Multilingual Prompting for Improving LLM Generation Diversity](http://arxiv.org/abs/2505.15229v2) | Qihan Wang, Shidong Pan, Tal Linzen et al. | EMNLP 2025 | [arXiv:2505.15229](http://arxiv.org/abs/2505.15229v2) |
| ★★ | 2025 | [SliderSpace: Decomposing the Visual Capabilities of Diffusion Models](http://arxiv.org/abs/2502.01639v1) | Rohit Gandikota, Zongze Wu, Richard Zhang et al. | ICCV 2025 | [arXiv:2502.01639](http://arxiv.org/abs/2502.01639v1) |
| ★★★ | 2025 | [Verbalized Sampling: How to Mitigate Mode Collapse and Unlock LLM Diversity](http://arxiv.org/abs/2510.01171v4) | Jiayi Zhang, Simon Yu, Derek Chong et al. | arXiv preprint (no published version found) | [arXiv:2510.01171](http://arxiv.org/abs/2510.01171v4) |
| ★★★ | 2026 | [BILLY: Steering Large Language Models via Merging Persona Vectors for Creative Generation](http://arxiv.org/abs/2510.10157v2) | Tsung-Min Pai, Jui-I Wang, Li-Chun Lu et al. | EACL 2026 (Long) | [arXiv:2510.10157](http://arxiv.org/abs/2510.10157v2) |
| ★★★ | 2026 | [Beyond the Hivemind: Escaping LLM Homogeneity via Meta-Persona Anchoring and Sequential Temperature Scaling](http://arxiv.org/abs/2608.02618v1) | Tairan Fu, Javier Conde, Carlos Arriaga et al. | arXiv preprint (no published version found) | [arXiv:2608.02618](http://arxiv.org/abs/2608.02618v1) |
| ★★★ | 2026 | [CreativityNeuro: Steering Language Model Weights to Improve Divergent Thinking and Reduce Mode Collapse](http://arxiv.org/abs/2607.01433v1) | Samuel Schapiro, Core Francisco Park, Felix Sosa et al. | ICML 2026 Workshop on Creativity & Generative AI | [arXiv:2607.01433](http://arxiv.org/abs/2607.01433v1) |
| ★★★ | 2026 | [Geometry of Knowledge Allows Extending Diversity Boundaries of Large Language Models](http://arxiv.org/abs/2507.13874v2) | Mateusz Bystroński, Doheon Han, Nitesh V. Chawla et al. | ACL 2026 Student Research Workshop (published as 'Continuous Context Sampling Allows Extending Diversity Boundaries of Large Language Models') | [arXiv:2507.13874](http://arxiv.org/abs/2507.13874v2) |
| ★★★ | 2026 | [Inducing Sustained Creativity and Diversity in Large Language Models](http://arxiv.org/abs/2603.19519v2) | Queenie Luo, Gary King, Michael Puett et al. | arXiv preprint (no published version found) | [arXiv:2603.19519](http://arxiv.org/abs/2603.19519v2) |

[↑ Contents](#contents)

## J. Remedies in training and post-training

Preference-optimization and reinforcement-learning objectives that make diversity part of the training signal, plus data-selection and layer-restoration approaches.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★★ | 2024 | [GDPO: Learning to Directly Align Language Models with Diversity Using GFlowNets](http://arxiv.org/abs/2410.15096v1) | Oh Joon Kwon, Daiki E. Matsunaga, Kee-Eung Kim | EMNLP 2024 | [arXiv:2410.15096](http://arxiv.org/abs/2410.15096v1) |
| ★★ | 2024 | [GFlowNet Fine-tuning for Diverse Correct Solutions in Mathematical Reasoning Tasks](http://arxiv.org/abs/2410.20147v1) | Ryoichi Takase, Masaya Tsunokake, Yuta Tsuchiya et al. | arXiv preprint (no published version found) | [arXiv:2410.20147](http://arxiv.org/abs/2410.20147v1) |
| ★★ | 2025 | [BARE: Leveraging Base Language Models for Few-Shot Synthetic Data Generation](http://arxiv.org/abs/2502.01697v3) | Alan Zhu, Parth Asawa, Jared Quincy Davis et al. | arXiv preprint (no published version found) | [arXiv:2502.01697](http://arxiv.org/abs/2502.01697v3) |
| ★★★ | 2025 | [Creative Preference Optimization](http://arxiv.org/abs/2505.14442v2) | Mete Ismayilzada, Antonio Laverghetta, Simone A. Luchini et al. | Findings of EMNLP 2025 | [arXiv:2505.14442](http://arxiv.org/abs/2505.14442v2) |
| ★★★ | 2025 | [Diverse Preference Learning for Capabilities and Alignment](http://arxiv.org/abs/2511.08594v1) | Stewart Slocum, Asher Parker-Sartori, Dylan Hadfield-Menell | ICLR 2025 | [arXiv:2511.08594](http://arxiv.org/abs/2511.08594v1) |
| ★★★ | 2025 | [Diverse Preference Optimization](http://arxiv.org/abs/2501.18101v4) | Jack Lanchantin, Angelica Chen, Shehzaad Dhuliawala et al. | arXiv preprint — prior draft lists arXiv (no published version found) | [arXiv:2501.18101](http://arxiv.org/abs/2501.18101v4) |
| ★★★ | 2025 | [Diverse, not Short: A Length-Controlled Data Selection Strategy for Improving Response Diversity of Language Models](http://arxiv.org/abs/2505.16245v4) | Vijeta Deshpande, Debasmita Ghose, John D. Patterson et al. | EMNLP 2025 (Main) | [arXiv:2505.16245](http://arxiv.org/abs/2505.16245v4) |
| ★★★ | 2025 | [Group-Aware Reinforcement Learning for Output Diversity in Large Language Models](http://arxiv.org/abs/2511.12596v1) | Oron Anschel, Alon Shoshan, Adam Botach et al. | EMNLP 2025 (Main) | [arXiv:2511.12596](http://arxiv.org/abs/2511.12596v1) |
| ★★★ | 2025 | [Improving Linguistic Diversity of Large Language Models with Possibility Exploration Fine-Tuning](http://arxiv.org/abs/2412.03343v1) | Long Mai, Julie Carson-Berndsen | Interspeech 2025 | [arXiv:2412.03343](http://arxiv.org/abs/2412.03343v1) |
| ★★★ | 2025 | [Jointly Reinforcing Diversity and Quality in Language Model Generations](http://arxiv.org/abs/2509.02534v1) | Tianjian Li, Yiming Zhang, Ping Yu et al. | arXiv preprint (no published version found) | [arXiv:2509.02534](http://arxiv.org/abs/2509.02534v1) |
| ★★★ | 2025 | [Modifying Large Language Model Post-Training for Diverse Creative Writing](http://arxiv.org/abs/2503.17126v1) | John Joon Young Chung, Vishakh Padmakumar, Melissa Roemmele et al. | COLM 2025 | [arXiv:2503.17126](http://arxiv.org/abs/2503.17126v1) |
| ★★★ | 2025 | [Preserving Diversity in Supervised Fine-Tuning of Large Language Models](http://arxiv.org/abs/2408.16673v2) | Ziniu Li, Congliang Chen, Tian Xu et al. | ICLR 2025 | [arXiv:2408.16673](http://arxiv.org/abs/2408.16673v2) |
| ★★★ | 2026 | [CreativeInstruct: Scalably Teaching LLMs to Balance Quality, Creativity, and Diversity](http://arxiv.org/abs/2608.07460v1) | Ananya Sahu, Mohit Bansal, Elias Stengel-Eskin | arXiv preprint (no published version found) | [arXiv:2608.07460](http://arxiv.org/abs/2608.07460v1) |
| ★★ | 2026 | [DPWriter: Reinforcement Learning with Diverse Planning Branching for Creative Writing](http://arxiv.org/abs/2601.09609v1) | Qian Cao, Yahui Liu, Wei Bi et al. | ACL 2026 (Long) | [arXiv:2601.09609](http://arxiv.org/abs/2601.09609v1) |
| ★★ | 2026 | [DyJR: Preserving Diversity in Reinforcement Learning with Verifiable Rewards via Dynamic Jensen-Shannon Replay](http://arxiv.org/abs/2603.16157v1) | Long Li, Zhijian Zhou, Tianyi Wang et al. | arXiv preprint (no published version found) | [arXiv:2603.16157](http://arxiv.org/abs/2603.16157v1) |
| ★★★ | 2026 | [Not All Layers Need Tuning: Selective Layer Restoration Recovers Diversity](http://arxiv.org/abs/2602.06665v1) | Bowen Zhang, Meiyi Wang, Harold Soh | arXiv preprint (no published version found) | [arXiv:2602.06665](http://arxiv.org/abs/2602.06665v1) |
| ★★★ | 2026 | [Post-training Large Language Models for Diverse High-Quality Responses](http://arxiv.org/abs/2509.04784v3) | Yilei Chen, Souradip Chakraborty, Lorenz Wolf et al. | ICLR 2026 | [arXiv:2509.04784](http://arxiv.org/abs/2509.04784v3) |
| ★★★ | 2026 | [SED-SFT: Selectively Encouraging Diversity in Supervised Fine-Tuning](http://arxiv.org/abs/2602.07464v1) | Yijie Chen, Yijin Liu, Fandong Meng | ACL 2026 (Short) | [arXiv:2602.07464](http://arxiv.org/abs/2602.07464v1) |
| ★★★ | 2026 | [Spectrum Tuning: Post-Training for Distributional Coverage and In-Context Steerability](http://arxiv.org/abs/2510.06084v2) | Taylor Sorensen, Benjamin Newman, Jared Moore et al. | ICLR 2026 | [arXiv:2510.06084](http://arxiv.org/abs/2510.06084v2) |
| ★★★ | 2026 | [UpSkill: Mutual Information Skill Learning for Structured Response Diversity in LLMs](http://arxiv.org/abs/2602.22296v1) | Devan Shah, Owen Yang, Daniel Yang et al. | arXiv preprint (no published version found) | [arXiv:2602.22296](http://arxiv.org/abs/2602.22296v1) |

[↑ Contents](#contents)

## K. Open-endedness, quality-diversity, and search

The quality-diversity and novelty-search branch, where diversity is the optimization target rather than a constraint. Pre-LLM in origin; the LLM entries here inherit its vocabulary.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★ | 2011 | [Abandoning Objectives: Evolution Through the Search for Novelty Alone](https://doi.org/10.1162/evco_a_00025) | Joel Lehman, Kenneth Owen Stanley | Evolutionary Computation 19(2):189–223 (2011; online 2010) | [DOI 10.1162/evco_a_00025](https://doi.org/10.1162/evco_a_00025) |
| ★★ | 2021 | [Flow Network based Generative Models for Non-Iterative Diverse Candidate Generation](http://arxiv.org/abs/2106.04399v2) | Emmanuel Bengio, Moksh Jain, Maksym Korablyov et al. | NeurIPS 2021 | [arXiv:2106.04399](http://arxiv.org/abs/2106.04399v2) |
| ★★ | 2023 | [OMNI: Open-endedness via Models of human Notions of Interestingness](http://arxiv.org/abs/2306.01711v3) | Jenny Zhang, Joel Lehman, Kenneth Stanley et al. | arXiv preprint — prior draft lists ICLR 2024 (not confirmed by arXiv/OpenAlex) | [arXiv:2306.01711](http://arxiv.org/abs/2306.01711v3) |
| ★★★ | 2023 | [Quality-Diversity through AI Feedback](http://arxiv.org/abs/2310.13032v4) | Herbie Bradley, Andrew Dai, Hannah Teufel et al. | arXiv preprint — prior draft lists ICLR 2024 (not confirmed by arXiv/OpenAlex) | [arXiv:2310.13032](http://arxiv.org/abs/2310.13032v4) |
| ★★ | 2024 | [Language Model Crossover: Variation through Few-Shot Prompting](http://arxiv.org/abs/2302.12170v3) | Elliot Meyerson, Mark J. Nelson, Herbie Bradley et al. | ACM Transactions on Evolutionary Learning and Optimization (2024) | [arXiv:2302.12170](http://arxiv.org/abs/2302.12170v3) |
| ★★ | 2024 | [Large Language Models as In-context AI Generators for Quality-Diversity](http://arxiv.org/abs/2404.15794v2) | Bryan Lim, Manon Flageat, Antoine Cully | ALIFE 2024 | [arXiv:2404.15794](http://arxiv.org/abs/2404.15794v2) |
| ★★★ | 2026 | [Parameter-Efficient Neuroevolution for Diverse LLM Generation: Quality-Diversity Optimization via Prompt Embedding Evolution](http://arxiv.org/abs/2605.09781v2) | Dongxin Guo, Jikun Wu, Siu Ming Yiu | arXiv preprint (no published version found) | [arXiv:2605.09781](http://arxiv.org/abs/2605.09781v2) |

[↑ Contents](#contents)

## L. Pluralism, safety, and the diversity-quality trade-off

The normative frame: whose diversity, how much, and at what cost to quality.

| Focus | Year | Paper | Authors | Venue | ID |
| :-: | :-: | --- | --- | --- | --- |
| ★★ | 2023 | [Whose Opinions Do Language Models Reflect?](http://arxiv.org/abs/2303.17548v1) | Shibani Santurkar, Esin Durmus, Faisal Ladhak et al. | ICML 2023 | [arXiv:2303.17548](http://arxiv.org/abs/2303.17548v1) |
| ★★★ | 2024 | [A Roadmap to Pluralistic Alignment](http://arxiv.org/abs/2402.05070v3) | Taylor Sorensen, Jared Moore, Jillian Fisher et al. | ICML 2024 | [arXiv:2402.05070](http://arxiv.org/abs/2402.05070v3) |
| ★★ | 2024 | [Modular Pluralism: Pluralistic Alignment via Multi-LLM Collaboration](http://arxiv.org/abs/2406.15951v2) | Shangbin Feng, Taylor Sorensen, Yuhan Liu et al. | EMNLP 2024 | [arXiv:2406.15951](http://arxiv.org/abs/2406.15951v2) |
| ★★ | 2024 | [PERSONA: A Reproducible Testbed for Pluralistic Alignment](http://arxiv.org/abs/2407.17387v1) | Louis Castricato, Nathan Lile, Rafael Rafailov et al. | arXiv preprint (no published version found) | [arXiv:2407.17387](http://arxiv.org/abs/2407.17387v1) |
| ★★ | 2024 | [Social Choice Should Guide AI Alignment in Dealing with Diverse Human Feedback](http://arxiv.org/abs/2404.10271v2) | Vincent Conitzer, Rachel Freedman, Jobst Heitzig et al. | ICML 2024 (position paper) | [arXiv:2404.10271](http://arxiv.org/abs/2404.10271v2) |
| ★★ | 2024 | [The PRISM Alignment Dataset: What Participatory, Representative and Individualised Human Feedback Reveals About the Subjective and Multicultural Alignment of Large Language Models](http://arxiv.org/abs/2404.16019v2) | Hannah Rose Kirk, Alexander Whitefield, Paul Röttger et al. | NeurIPS 2024 (Datasets & Benchmarks) | [arXiv:2404.16019](http://arxiv.org/abs/2404.16019v2) |
| ★★ | 2024 | [Value Kaleidoscope: Engaging AI with Pluralistic Human Values, Rights, and Duties](http://arxiv.org/abs/2309.00779v2) | Taylor Sorensen, Liwei Jiang, Jena Hwang et al. | AAAI 2024 | [arXiv:2309.00779](http://arxiv.org/abs/2309.00779v2) |
| ★★★ | 2025 | [From Distributional to Overton Pluralism: Investigating Large Language Model Alignment](http://arxiv.org/abs/2406.17692v2) | Thom Lake, Eunsol Choi, Greg Durrett | NAACL 2025 (Main) | [arXiv:2406.17692](http://arxiv.org/abs/2406.17692v2) |
| ★★ | 2025 | [From Noise to Signal to Selbstzweck: Reframing Human Label Variation in the Era of Post-training in NLP](http://arxiv.org/abs/2510.12817v3) | Shanshan Xu, Santosh T. Y. S. S, Barbara Plank | arXiv preprint (no published version found) | [arXiv:2510.12817](http://arxiv.org/abs/2510.12817v3) |
| ★★★ | 2025 | [Understanding the Quality-Diversity Trade-off in Diffusion Language Models](http://arxiv.org/abs/2503.10683v1) | Zak Buzzard | arXiv preprint (no published version found) | [arXiv:2503.10683](http://arxiv.org/abs/2503.10683v1) |
| ★★ | 2026 | [A Roadmap to Impactful Pluralistic Alignment Research](http://arxiv.org/abs/2607.22305v1) | Elinor Poole-Dayan, Jillian Fisher, Atoosa Kasirzadeh et al. | arXiv preprint (no published version found) | [arXiv:2607.22305](http://arxiv.org/abs/2607.22305v1) |
| ★★★ | 2026 | [Growing a tail: Increasing output diversity in large language models](https://doi.org/10.1016/j.mlwa.2026.100951) | Michal Shur‐Ofry, Bar Horowitz-Amsalem, Adir Rahamim et al. | Machine Learning with Applications (2026) | [DOI 10.1016/j.mlwa.2026.100951](https://doi.org/10.1016/j.mlwa.2026.100951) |
| ★★★ | 2026 | [Magic, Madness, Heaven, Sin: LLM Output Diversity is Everything, Everywhere, All at Once](http://arxiv.org/abs/2604.01504v1) | Harnoor Dhingra | arXiv preprint (no published version found) | [arXiv:2604.01504](http://arxiv.org/abs/2604.01504v1) |
| ★★★ | 2026 | [On Epistemic Diversity in Large Language Models](http://arxiv.org/abs/2609.04835v1) | Elisabeth Kirsten, Nicole Krämer, Muhammad Bilal Zafar | arXiv preprint (no published version found) | [arXiv:2609.04835](http://arxiv.org/abs/2609.04835v1) |
| ★★★ | 2026 | [The Homogenization Problem in LLMs: Towards Meaningful Diversity in AI Safety](http://arxiv.org/abs/2601.06116v7) | Ian Rios-Sialer | arXiv preprint (prior draft linked an ICML 2026 virtual page; not confirmed) | [arXiv:2601.06116](http://arxiv.org/abs/2601.06116v7) |

[↑ Contents](#contents)
## Adjacent and background reading

These works are regularly cited in diversity work and a reader will meet them, but in each case the paper's own object of study is something other than output diversity.

- **[Illuminating search spaces by mapping elites](http://arxiv.org/abs/1504.04909v1)** — Jean-Baptiste Mouret, Jeff Clune, 2015, arXiv preprint · arXiv:1504.04909  
  An evolutionary-computation algorithm for filling a behaviour archive. It is the method ancestor of the quality-diversity work in Section K.

- **[Algorithmic monoculture and social welfare](https://doi.org/10.1073/pnas.2018340118)** — Jon M. Kleinberg, Manish Raghavan, 2021, PNAS 118(22) (2021) · DOI 10.1073/pnas.2018340118  
  Monoculture here means many firms applying the same decision rule to the same applicants, and the outcome measure is social welfare, not output variety. Useful as a conceptual precedent for "everyone using one model narrows outcomes"; it measures nothing a diversity metric would recognise.

- **[Having Beer after Prayer? Measuring Cultural Bias in Large Language Models](http://arxiv.org/abs/2305.14456v4)** — Tarek Naous, Michael J. Ryan, Alan Ritter et al., 2024, ACL 2024 (Long) · arXiv:2305.14456  
  Measures Western-entity bias in Arabic cultural contexts. The finding is about *which* culture a model defaults to, not about how many distinct outputs it produces; there is no diversity metric in the paper.

- **[Encouraging Divergent Thinking in Large Language Models through Multi-Agent Debate](http://arxiv.org/abs/2305.19118v4)** — Tian Liang, Zhiwei He, Wenxiang Jiao et al., 2024, EMNLP 2024 (Main) · arXiv:2305.19118  
  The target is reasoning accuracy; "divergent thinking" names the mechanism (debate breaks degeneration-of-thought) rather than a measured quantity. Frequently cited in creativity work.

- **[MaxMin-RLHF: Alignment with Diverse Human Preferences](http://arxiv.org/abs/2402.08925v2)** — Souradip Chakraborty, Jiahao Qiu, Hui Yuan et al., 2024, arXiv preprint · arXiv:2402.08925  
  Aligns to heterogeneous *preferences* across user groups, a fairness objective. Diversity of generated text is neither the goal nor an outcome measure.

[↑ Contents](#contents)

## Contributing

Additions are welcome. To keep the list's one useful property — that its metadata is right — please include with any proposed entry:

1. the canonical identifier (arXiv ID or DOI), not just a URL;
2. the venue of record, or an explicit statement that it is an unpublished preprint;
3. the full author list as the primary index gives it;
4. which section it belongs in, and which focus tier — if diversity is not the object of study, say what is.

Entries whose venue cannot be confirmed from arXiv or OpenAlex will be marked unconfirmed rather than rejected.

## License

The list itself — the selection, structure, annotations and metadata — is released under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/): use it without attribution. The papers it points to are the property of their authors and publishers; links go to publisher pages or author-posted preprints.
