# Evaluation of Creativity: A Reading List

![papers](https://img.shields.io/badge/papers-152-blue) ![metadata](https://img.shields.io/badge/metadata-verified%20against%20arXiv%20%2B%20OpenAlex-brightgreen) ![updated](https://img.shields.io/badge/updated-2026--10--16-lightgrey) ![license](https://img.shields.io/badge/list-CC0--1.0-informational)

**152 papers on how creativity is evaluated**: the instruments, the human protocols, the automatic metrics, the model judges, the benchmarks, and the frameworks that decide whether any of them measure what they claim.


## Legend

| Mark | Meaning |
| :-: | --- |
| ★★★ | The evaluation of creativity is the object of study, it proposes, validates or critiques a test, metric, rubric, judge, benchmark or framework |
| ★★ | Evaluation is a main axis of the paper, but its goal is something else, it applies an existing instrument, or reports a creativity measure as evidence for a different claim |
| ★ | Listed for framing or lineage only, collected under [Adjacent and background reading](#adjacent-and-background-reading) |

Each entry also carries **Side**: *Original* for human-creativity science and classical computational creativity, *LLM* for work on generative language models, so the two traditions can be read against each other.

## Start here

Eight papers that between them cover the whole argument:

- **[Social psychology of creativity: A consensual assessment technique](https://doi.org/10.1037/0022-3514.43.5.997)** (1982, Journal of Personality and Social Psychology (1982)): the consensual assessment technique: the protocol every automatic method is still validated against
- **[A Standardised Procedure for Evaluating Creative Systems: Computational Creativity Evaluation Based on What it is to be Creative](https://doi.org/10.1007/s12559-012-9156-1)** (2012, Cognitive Computation (2012)): SPECS: evaluate a system against a stated definition of creativity, not a fixed checklist
- **[Some Empirical Criteria for Attributing Creativity to a Computer Program](https://doi.org/10.1007/s11023-007-9066-2)** (2007, Minds and Machines (2007)): Ritchie's criteria — the first attempt to say what evidence would license calling a program creative
- **[Automating creativity assessment with SemDis: An open platform for computing semantic distance](https://doi.org/10.3758/s13428-020-01453-w)** (2021, Behavior Research Methods 53:757–780): the semantic-distance scorer that made automated originality scoring routine
- **[Beyond semantic distance: Automated scoring of divergent thinking greatly improves with large language models](https://doi.org/10.1016/j.tsc.2023.101356)** (2023, Thinking Skills and Creativity (2023)): where LLM-based scoring of divergent thinking overtook distributional metrics
- **[Art or Artifice? Large Language Models and the False Promise of Creativity](https://doi.org/10.1145/3613904.3642731)** (2024, CHI 2024): the TTCW rubric, and the finding that expert judges separate human from model writing
- **[Rethinking Creativity Evaluation: A Critical Analysis of Existing Creativity Evaluations](https://doi.org/10.18653/v1/2026.eacl-long.297)** (2026, EACL 2026): the critical audit of what existing creativity evaluations actually measure
- **[Measuring what Matters: Construct Validity in Large Language Model Benchmarks](https://doi.org/10.52202/085713-0590)** (2025, NeurIPS 2025 Datasets & Benchmarks Track): construct validity in benchmarks generally, the frame the rest of the list needs

## Contents

- [A. Psychometric tests and their machine adaptations](#a-psychometric-tests-and-their-machine-adaptations): 27 papers
- [B. Human judgment protocols](#b-human-judgment-protocols): 14 papers
- [C. Automatic metrics](#c-automatic-metrics): 26 papers
- [D. Model judges and reward models](#d-model-judges-and-reward-models): 17 papers
- [E. Benchmarks and evaluation suites](#e-benchmarks-and-evaluation-suites): 22 papers
- [F. Evaluation frameworks and construct validity](#f-evaluation-frameworks-and-construct-validity): 28 papers
- [G. Process and co-creation measurement](#g-process-and-co-creation-measurement): 6 papers
- [H. Interpretability of the evaluation mechanism](#h-interpretability-of-the-evaluation-mechanism): 3 papers
- [Adjacent and background reading](#adjacent-and-background-reading): 9 papers
- [Contributing](#contributing)
- [License](#license)

## A. Psychometric tests and their machine adaptations

Instruments that score creative *potential* from constrained-response tasks — divergent-thinking
fluency, flexibility and originality, associative reach, convergent insight. The Original entries
are the measurement tradition (Guilford, Torrance, Mednick, the Divergent Association Task) together
with the validity literature that keeps it honest; the LLM entries run those same instruments on
models, almost always scoring the model's responses with the human norming protocol. The recurring
hazard is construct drift: a test normed on human respondents does not automatically retain its
validity when the respondent may have seen the items during pre-training.

*27 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★ | 1950 | [Creativity](https://doi.org/10.1037/h0063487) | J. P. Guilford | American Psychologist 5(9):444–454 (1950) | Original | [DOI 10.1037/h0063487](https://doi.org/10.1037/h0063487) |
| ★★★ | 1962 | [The associative basis of the creative process](https://doi.org/10.1037/h0048850) | Sarnoff A. Mednick | Psychological Review (1962) | Original | [DOI 10.1037/h0048850](https://doi.org/10.1037/h0048850) |
| ★★★ | 1966 | Torrance Tests of Creative Thinking | E. Paul Torrance | Test manual — Personnel Press, Princeton NJ | Original | No DOI — Personnel Press, 1966 |
| ★★ | 1967 | [The Nature of Human Intelligence](https://gwern.net/doc/iq/1967-guilford-thenatureofhumanintelligence.pdf) | J. P. Guilford | Book — McGraw-Hill, New York | Original | [ISBN 978-0070251359](https://gwern.net/doc/iq/1967-guilford-thenatureofhumanintelligence.pdf) |
| ★★★ | 2021 | [Forward flow and creative thought: Assessing associative cognition and its role in divergent thinking](https://doi.org/10.1016/j.tsc.2021.100859) | Roger E. Beaty, Daniel C. Zeitlen, Brendan S. Baker et al. | Thinking Skills and Creativity (2021) | Original | [DOI 10.1016/j.tsc.2021.100859](https://doi.org/10.1016/j.tsc.2021.100859) |
| ★★★ | 2021 | [Naming unrelated words predicts creativity](https://doi.org/10.1073/pnas.2022340118) | Jay A. Olson, Johnny Nahas, Denis Chmoulevitch et al. | Proceedings of the National Academy of Sciences (2021) | Original | [DOI 10.1073/pnas.2022340118](https://doi.org/10.1073/pnas.2022340118) |
| ★★ | 2022 | [Putting GPT-3's Creativity to the (Alternative Uses) Test](https://arxiv.org/abs/2206.08932) | Claire Stevenson, Iris Smal, Matthijs Baas et al. | ICCC 2022 (13th Int. Conf. on Computational Creativity) | LLM | [arXiv:2206.08932](https://arxiv.org/abs/2206.08932) |
| ★★★ | 2022 | [Semantic Distance and the Alternate Uses Task: Recommendations for Reliable Automated Assessment of Originality](https://doi.org/10.1080/10400419.2022.2025720) | Roger E. Beaty, Dan Richard Johnson, Daniel C. Zeitlen et al. | Creativity Research Journal (2022) | Original | [DOI 10.1080/10400419.2022.2025720](https://doi.org/10.1080/10400419.2022.2025720) |
| ★★ | 2023 | [Best humans still outperform artificial intelligence in a creative divergent thinking task](https://doi.org/10.1038/s41598-023-40858-3) | Mika Koivisto, Simone Grassini | Scientific Reports (2023) | LLM | [DOI 10.1038/s41598-023-40858-3](https://doi.org/10.1038/s41598-023-40858-3) |
| ★★★ | 2023 | [Large Language Models are Fixated by Red Herrings: Exploring Creative Problem Solving and Einstellung Effect using the Only Connect Wall Dataset](https://doi.org/10.52202/075280-0246) | Saeid Naeini, Raeid Saqur, Mozhgan Saeidi et al. | NeurIPS 2023 Datasets & Benchmarks Track | LLM | [DOI 10.52202/075280-0246](https://doi.org/10.52202/075280-0246) |
| ★★★ | 2024 | [The creative psychometric item generator: a framework for item generation and validation using large language models](https://arxiv.org/abs/2409.00202) | Antonio Laverghetta, Simone Luchini, Averie Linell et al. | CREAI 2024 workshop | LLM | [arXiv:2409.00202](https://arxiv.org/abs/2409.00202) |
| ★★ | 2024 | [The current state of artificial intelligence generative language models is more creative than humans on divergent thinking tasks](https://doi.org/10.1038/s41598-024-53303-w) | Kent F. Hubert, Kim N. Awa, Darya L. Zabelina | Scientific Reports (2024) | LLM | [DOI 10.1038/s41598-024-53303-w](https://doi.org/10.1038/s41598-024-53303-w) |
| ★★ | 2025 | [A large-scale comparison of divergent creativity in humans and large language models](https://doi.org/10.1038/s41562-025-02331-1) | Dawei Wang, Difang Huang, Haipeng Shen et al. | Nature Human Behaviour (2025) | LLM | [DOI 10.1038/s41562-025-02331-1](https://doi.org/10.1038/s41562-025-02331-1) |
| ★★★ | 2025 | [Assessing and Understanding Creativity in Large Language Models](https://doi.org/10.1007/s11633-025-1546-4) | Yunpu Zhao, Rui Zhang, Wenyi Li et al. | Machine Intelligence Research (2025) | LLM | [DOI 10.1007/s11633-025-1546-4](https://doi.org/10.1007/s11633-025-1546-4) |
| ★★ | 2025 | [Divergent thinking is linked with convergent thinking; implications for models of creativity](https://doi.org/10.1080/13546783.2025.2485059) | Bruce S. Rawlings, Daisy Chetwynd-Talbot, Erin Husband et al. | Thinking & Reasoning (2025) | Original | [DOI 10.1080/13546783.2025.2485059](https://doi.org/10.1080/13546783.2025.2485059) |
| ★★★ | 2025 | [Envisioning the Future of Creative Thinking Assessment](https://doi.org/10.1002/jocb.70036) | Mathias Benedek, Roger E. Beaty | The Journal of Creative Behavior (2025) | Original | [DOI 10.1002/jocb.70036](https://doi.org/10.1002/jocb.70036) |
| ★★ | 2025 | [Generative artificial intelligence models outperform students on divergent and convergent thinking assessments](https://doi.org/10.1038/s41598-025-21398-4) | Vikram Arora, Alex Thabane, Sameer Parpia et al. | Scientific Reports (2025) | LLM | [DOI 10.1038/s41598-025-21398-4](https://doi.org/10.1038/s41598-025-21398-4) |
| ★★★ | 2025 | [Has the creativity of large-language models peaked? An analysis of inter- and intra-LLM variability](https://doi.org/10.1016/j.yjoc.2025.100113) | Jennifer Haase, Paul H. P. Hanel, Sebastian Pokutta | Journal of Creativity 5(2):100113 (2025) | LLM | [DOI 10.1016/j.yjoc.2025.100113](https://doi.org/10.1016/j.yjoc.2025.100113) |
| ★★ | 2025 | [Human Creativity in the Age of LLMs: Randomized Experiments on Divergent and Convergent Thinking](https://doi.org/10.1145/3706598.3714198) | Harsh Kumar, Jonathan Vincentius, Ewan Jordan et al. | CHI 2025 | LLM | [DOI 10.1145/3706598.3714198](https://doi.org/10.1145/3706598.3714198) |
| ★★ | 2025 | [Large language models show both individual and collective creativity comparable to humans](https://doi.org/10.1016/j.tsc.2025.101870) | Luning Sun, Yuzhuo Yuan, Yuan Yao et al. | Thinking Skills and Creativity (2025) | LLM | [DOI 10.1016/j.tsc.2025.101870](https://doi.org/10.1016/j.tsc.2025.101870) |
| ★★★ | 2025 | [Measuring Combinatorial Creativity in Large Language Models and Humans](https://arxiv.org/abs/2509.21043) | Samuel Schapiro, Akshay K. Jagadish, Alexi Gladstone et al. | arXiv preprint (no published version found) | LLM | [arXiv:2509.21043](https://arxiv.org/abs/2509.21043) |
| ★★★ | 2025 | [S-DAT: A Multilingual, GenAI-Driven Framework for Automated Divergent Thinking Assessment](https://arxiv.org/abs/2505.09068) | Jennifer Haase, Paul H. P. Hanel, Sebastian Pokutta | AIES 2025 (AAAI/ACM Conf. on AI, Ethics and Society) | LLM | [DOI 10.1609/aies.v8i2.36622](https://doi.org/10.1609/aies.v8i2.36622) |
| ★★★ | 2026 | [AlphaContext: An Evolutionary Tree-based Psychometric Context Generator for Creativity Assessment](https://arxiv.org/abs/2604.18398) | Yixuan Wang, Yue Huang, Hong Qian et al. | ACL 2026 (Main) | LLM | [DOI 10.48448/wk53-ck51](https://doi.org/10.48448/wk53-ck51) |
| ★★★ | 2026 | [Assessing the Creativity of Large Language Models: Testing, Limits, and New Frontiers](https://arxiv.org/abs/2605.13450) | Samuel Schapiro, Alexi Gladstone, Jonah Black et al. | arXiv preprint (no published version found) | LLM | [arXiv:2605.13450](https://arxiv.org/abs/2605.13450) |
| ★★★ | 2026 | [Beyond Divergent Creativity: A Human-Based Evaluation of Creativity in Large Language Models](https://doi.org/10.18653/v1/2026.findings-eacl.138) | Kumiko Nakajima, Jan Zuiderveld, Sandro Pezzelle | Findings of EACL 2026 | LLM | [DOI 10.18653/v1/2026.findings-eacl.138](https://doi.org/10.18653/v1/2026.findings-eacl.138) |
| ★★★ | 2026 | [CREATE: Testing LLMs for Associative Creativity](https://arxiv.org/abs/2603.09970) | Manya Wadhwa, Tiasa Singha Roy, Harvey Lederman et al. | arXiv preprint (no published version found) | LLM | [arXiv:2603.09970](https://arxiv.org/abs/2603.09970) |
| ★★ | 2026 | [Divergent Creativity in Humans and Large Language Models](https://doi.org/10.1038/s41598-025-25157-3) | Antoine Bellemare-Pepin, François Lespinasse, Philipp Thölke et al. | Scientific Reports (2026) | LLM | [DOI 10.1038/s41598-025-25157-3](https://doi.org/10.1038/s41598-025-25157-3) |

[↑ Contents](#contents)

## B. Human judgment protocols

Procedures that turn expert or lay opinion into a reliable score,Amabile's consensual assessment
technique, product-semantic rating scales, the rubric-based Torrance Test of Creative Writing. These
remain the criterion every automatic method is validated against, which makes rater selection, rater
expertise and inter-rater agreement first-order concerns rather than implementation details.

*14 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★★ | 1982 | [Social psychology of creativity: A consensual assessment technique](https://doi.org/10.1037/0022-3514.43.5.997) | Teresa M. Amabile | Journal of Personality and Social Psychology (1982) | Original | [DOI 10.1037/0022-3514.43.5.997](https://doi.org/10.1037/0022-3514.43.5.997) |
| ★★★ | 1986 | [Analyzing Creative Products: Refinement and Test of a Judging Instrument](https://doi.org/10.1002/j.2162-6057.1986.tb00426.x) | Susan P. Besemer, Karen E. O'Quin | Journal of Creative Behavior 20(2):115–126 (1986) | Original | [DOI 10.1002/j.2162-6057.1986.tb00426.x](https://doi.org/10.1002/j.2162-6057.1986.tb00426.x) |
| ★★★ | 2023 | [A Confederacy of Models: a Comprehensive Evaluation of LLMs on Creative Writing](https://doi.org/10.18653/v1/2023.findings-emnlp.966) | Carlos Gómez-Rodríguez, Paul Williams | Findings of EMNLP 2023 | LLM | [DOI 10.18653/v1/2023.findings-emnlp.966](https://doi.org/10.18653/v1/2023.findings-emnlp.966) |
| ★★★ | 2024 | [Are Large Language Models Capable of Generating Human-Level Narratives?](https://doi.org/10.18653/v1/2024.emnlp-main.978) | Yufei Tian, Tenghao Huang, Miri Liu et al. | EMNLP 2024 | LLM | [DOI 10.18653/v1/2024.emnlp-main.978](https://doi.org/10.18653/v1/2024.emnlp-main.978) |
| ★★★ | 2024 | [Art or Artifice? Large Language Models and the False Promise of Creativity](https://doi.org/10.1145/3613904.3642731) | Tuhin Chakrabarty, Philippe Laban, Divyansh Agarwal et al. | CHI 2024 | LLM | [DOI 10.1145/3613904.3642731](https://doi.org/10.1145/3613904.3642731) |
| ★★ | 2024 | [Can LLMs Generate Novel Research Ideas? A Large-Scale Human Study with 100+ NLP Researchers](https://arxiv.org/abs/2409.04109) | Chenglei Si, Diyi Yang, Tatsunori Hashimoto | arXiv preprint (no published version found) | LLM | [arXiv:2409.04109](https://arxiv.org/abs/2409.04109) |
| ★★ | 2024 | [Generative AI enhances individual creativity but reduces the collective diversity of novel content](https://doi.org/10.1126/sciadv.adn5290) | Anil Rajnikant Doshi, Oliver Hauser | Science Advances (2024) | LLM | [DOI 10.1126/sciadv.adn5290](https://doi.org/10.1126/sciadv.adn5290) |
| ★★ | 2024 | [Pron vs Prompt: Can Large Language Models already Challenge a World-Class Fiction Author at Creative Text Writing?](https://arxiv.org/abs/2407.01119) | Guillermo Marco, Julio Gonzalo, Ramón del Castillo et al. | EMNLP 2024 | LLM | [arXiv:2407.01119](https://arxiv.org/abs/2407.01119) |
| ★★ | 2024 | [Small Language Models can Outperform Humans in Short Creative Writing: A Study Comparing SLMs with Humans and LLMs](https://arxiv.org/abs/2409.11547) | Guillermo Marco, Luz Rello, Julio Gonzalo | COLING 2025 | LLM | [arXiv:2409.11547](https://arxiv.org/abs/2409.11547) |
| ★★★ | 2024 | [The Unlikely Duel: Evaluating Creative Writing in LLMs through a Unique Scenario](https://arxiv.org/abs/2406.15891) | Carlos Gómez-Rodríguez, Paul Williams | CAEPIA 2024 (XIX Conf. of the Spanish Assoc. for AI) | LLM | [arXiv:2406.15891](https://arxiv.org/abs/2406.15891) |
| ★★★ | 2025 | [Evaluating Creative Short Story Generation in Humans and Large Language Models](https://arxiv.org/abs/2411.02316) | Mete Ismayilzada, Claire Stevenson, Lonneke van der Plas | ICCC 2025 | LLM | [arXiv:2411.02316](https://arxiv.org/abs/2411.02316) |
| ★★ | 2026 | [AI Delivers Creative Output but Struggles with Thinking Processes](https://arxiv.org/abs/2503.23327) | Man Zhang, Ying Li, Yang Peng et al. | Thinking Skills and Creativity (2026) | LLM | [DOI 10.1016/j.tsc.2026.102196](https://doi.org/10.1016/j.tsc.2026.102196) |
| ★★★ | 2026 | [Capabilities and Evaluation Biases of Large Language Models in Classical Chinese Poetry Generation: A Case Study on Tang Poetry](https://doi.org/10.18653/v1/2026.findings-acl.836) | Bolei Ma, Yina Yao, Anna-Carolina Haensch | Findings of ACL 2026 | LLM | [DOI 10.18653/v1/2026.findings-acl.836](https://doi.org/10.18653/v1/2026.findings-acl.836) |
| ★★ | 2026 | [Contemporary AI lacks the imagination to diverge or negate in science](https://arxiv.org/abs/2606.08251) | Honglin Bao, Siyang Wu, Xiao Liu et al. | arXiv preprint (no published version found) | LLM | [arXiv:2606.08251](https://arxiv.org/abs/2606.08251) |

[↑ Contents](#contents)

## C. Automatic metrics

Scoring functions computed from the artefact with no judge in the loop: semantic distance, divergent
semantic integration, n-gram and corpus-attribution novelty, embedding diversity, homogenisation
measures. Cheap and reproducible, and therefore the layer where measurement artefacts accumulate,
response length, elaboration and retrieval ability all leak into scores reported as originality.
Several 2025–26 entries here are explicitly critiques of the metrics listed above them.

*26 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★★ | 2019 | [Predicting Humorousness and Metaphor Novelty with Gaussian Process Preference Learning](https://doi.org/10.18653/v1/p19-1572) | Edwin Simpson, Erik-Lân Do Dinh, Tristan Miller et al. | ACL 2019 | Original | [DOI 10.18653/v1/p19-1572](https://doi.org/10.18653/v1/p19-1572) |
| ★★★ | 2021 | [Automating creativity assessment with SemDis: An open platform for computing semantic distance](https://doi.org/10.3758/s13428-020-01453-w) | Roger E. Beaty, Dan Richard Johnson | Behavior Research Methods 53:757–780 | Original | [DOI 10.3758/s13428-020-01453-w](https://doi.org/10.3758/s13428-020-01453-w) |
| ★★★ | 2023 | [Beyond semantic distance: Automated scoring of divergent thinking greatly improves with large language models](https://doi.org/10.1016/j.tsc.2023.101356) | Peter Organisciak, Selçuk Acar, Denis Dumas et al. | Thinking Skills and Creativity (2023) | Original | [DOI 10.1016/j.tsc.2023.101356](https://doi.org/10.1016/j.tsc.2023.101356) |
| ★★★ | 2023 | [Divergent semantic integration (DSI): Extracting creativity from narratives with distributional semantic modeling](https://doi.org/10.3758/s13428-022-01986-2) | Dan Richard Johnson, James C. Kaufman, Brendan S. Baker et al. | Behavior Research Methods 55:3726–3759 | Original | [DOI 10.3758/s13428-022-01986-2](https://doi.org/10.3758/s13428-022-01986-2) |
| ★★★ | 2023 | [Multilingual semantic distance: Automatic verbal creativity assessment in many languages](https://doi.org/10.1037/aca0000618) | John D. Patterson, Hannah Meghan Merseal, Dan Richard Johnson et al. | Psychology of Aesthetics Creativity and the Arts (2023) | Original | [DOI 10.1037/aca0000618](https://doi.org/10.1037/aca0000618) |
| ★★★ | 2024 | [How Much Retrieval Ability Is in Originality?](https://doi.org/10.1002/jocb.659) | Selina Weiss, Benjamin Goecke, Oliver Wilhelm | Journal of Creative Behavior (2024) | Original | [DOI 10.1002/jocb.659](https://doi.org/10.1002/jocb.659) |
| ★★ | 2025 | [AI Suggestions Homogenize Writing Toward Western Styles and Diminish Cultural Nuances](https://doi.org/10.1145/3706598.3713564) | Dhruv Agarwal, Mor Naaman, Aditya Vashistha | CHI 2025 | LLM | [DOI 10.1145/3706598.3713564](https://doi.org/10.1145/3706598.3713564) |
| ★★★ | 2025 | [AI as Humanity's Salieri: Quantifying Linguistic Creativity of Language Models via Systematic Attribution of Machine Text against Web Text](https://arxiv.org/abs/2410.04265) | Ximing Lu, Melanie Sclar, Skyler Hallinan et al. | NAACL 2025 | LLM | [arXiv:2410.04265](https://arxiv.org/abs/2410.04265) |
| ★★★ | 2025 | [Automated Creativity Evaluation for Large Language Models: A Reference-Based Approach](https://doi.org/10.18653/v1/2025.findings-emnlp.1171) | Ruizhe Li, Chiwei Zhu, Benfeng Xu et al. | Findings of EMNLP 2025 | LLM | [DOI 10.18653/v1/2025.findings-emnlp.1171](https://doi.org/10.18653/v1/2025.findings-emnlp.1171) |
| ★★★ | 2025 | [Death of the Novel(ty): Beyond n-Gram Novelty as a Metric for Textual Creativity](https://arxiv.org/abs/2509.22641) | Arkadiy Saakyan, Najoung Kim, Smaranda Muresan et al. | ICLR 2026 | LLM | [arXiv:2509.22641](https://arxiv.org/abs/2509.22641) |
| ★★★ | 2025 | [Deep Associations, High Creativity: A Simple yet Effective Metric for Evaluating Large Language Models](https://arxiv.org/abs/2510.12110) | Ziliang Qiu, Renfen Hu | EMNLP 2025 | LLM | [DOI 10.18653/v1/2025.emnlp-main.550](https://doi.org/10.18653/v1/2025.emnlp-main.550) |
| ★★ | 2025 | [Galton's Law of Mediocrity: Why Large Language Models Regress to the Mean and Fail at Creativity in Advertising](https://arxiv.org/abs/2509.25767) | Matt Keon, Aabid Karim, Bhoomika Lohana et al. | arXiv preprint (no published version found) | LLM | [arXiv:2509.25767](https://arxiv.org/abs/2509.25767) |
| ★★★ | 2025 | [Literature-Grounded Novelty Assessment of Scientific Ideas](https://arxiv.org/abs/2506.22026) | Simra Shahid, Marissa Radensky, Raymond Fok et al. | SDP 2025 workshop (Scholarly Document Processing) | LLM | [DOI 10.18653/v1/2025.sdp-1.9](https://doi.org/10.18653/v1/2025.sdp-1.9) |
| ★★★ | 2025 | [Measuring LLM Novelty As The Frontier Of Original And High-Quality Output](https://arxiv.org/abs/2504.09389) | Vishakh Padmakumar, Chen Yueh-Han, Jane Pan et al. | arXiv preprint (no published version found) | LLM | [arXiv:2504.09389](https://arxiv.org/abs/2504.09389) |
| ★★★ | 2025 | [MuseScorer: Idea Originality Scoring At Scale](https://doi.org/10.18653/v1/2025.emnlp-main.1009) | Ali Sarosh Bangash, Krish Veera, Ishfat Abrar Islam et al. | EMNLP 2025 | LLM | [DOI 10.18653/v1/2025.emnlp-main.1009](https://doi.org/10.18653/v1/2025.emnlp-main.1009) |
| ★★★ | 2025 | [Task-Dependent Evaluation of LLM Output Homogenization: A Taxonomy-Guided Framework](https://arxiv.org/abs/2509.21267) | Shomik Jain, Jack Lanchantin, Maximilian Nickel et al. | arXiv preprint (no published version found) | LLM | [arXiv:2509.21267](https://arxiv.org/abs/2509.21267) |
| ★★★ | 2026 | ["I've Seen How This Goes": Characterizing Diversity via Progressive Conditional Surprise](https://arxiv.org/abs/2606.01811) | Matthew Khoriaty, David Williams-King, Shi Feng | ICML 2026 workshop on Generative AI, Creativity and Human-AI Co-Creation (non-archival) | LLM | [arXiv:2606.01811](https://arxiv.org/abs/2606.01811) |
| ★★★ | 2026 | [Automated Creativity Evaluation of Language Models Across Open-Ended Tasks](https://doi.org/10.48448/vhwv-n411) | Min Sen Tan, Zachary Kit Chun Choy, Syed Ali Redha Alsagoff et al. | ACL 2026 (Main Conference) | LLM | [DOI 10.48448/vhwv-n411](https://doi.org/10.48448/vhwv-n411) |
| ★★★ | 2026 | [Before and After Temperature: A Distributional View of Creative LLM Generation](https://arxiv.org/abs/2606.01451) | V. S. Raghu Parupudi, Harsha Ponnada, Aditi Kaushal et al. | arXiv preprint (no published version found) | LLM | [arXiv:2606.01451](https://arxiv.org/abs/2606.01451) |
| ★★ | 2026 | [Large language models are homogeneously creative](https://doi.org/10.1093/pnasnexus/pgag042) | Emily Wenger, Yoed Nissan Kenett | PNAS Nexus (2026) | LLM | [DOI 10.1093/pnasnexus/pgag042](https://doi.org/10.1093/pnasnexus/pgag042) |
| ★★★ | 2026 | [Spoiler Alert: Narrative Forecasting as a Metric for Tension in LLM Storytelling](https://arxiv.org/abs/2604.09854) | Peiqi Sui, Yutong Zhu, Tianyi Cheng et al. | COLM 2026 | LLM | [arXiv:2604.09854](https://arxiv.org/abs/2604.09854) |
| ★★★ | 2026 | [StructSim: Measuring Idea Similarity at Scale Through Structural Representation](https://arxiv.org/abs/2609.34046) | Yaqing Yang, Vikram Mohanty, Mei-Xi Chia et al. | arXiv preprint (no published version found) | LLM | [arXiv:2609.34046](https://arxiv.org/abs/2609.34046) |
| ★★★ | 2026 | [Surprisal and Metaphor Novelty Judgments: Moderate Correlations and Divergent Scaling Effects Revealed by Corpus-Based and Synthetic Datasets](https://arxiv.org/abs/2601.02015) | Omar Momen, Emilie Sitter, Berenike Herrmann et al. | EACL 2026 (Main) | LLM | [arXiv:2601.02015](https://arxiv.org/abs/2601.02015) |
| ★★★ | 2026 | [The Effect of Idea Elaboration on the Automatic Assessment of Idea Originality](https://doi.org/10.1145/3811427.3811453) | Umberto Domanti, Moritz Mock, Sergio Agnoli et al. | AVI 2026 | LLM | [DOI 10.1145/3811427.3811453](https://doi.org/10.1145/3811427.3811453) |
| ★★★ | 2026 | [The Limits of Automatic Evaluation of Creativity in Large Language Models](https://arxiv.org/abs/2608.23705) | Alessandro Tutone, Giorgio Franceschelli, Mirco Musolesi | arXiv preprint (no published version found) | LLM | [arXiv:2608.23705](https://arxiv.org/abs/2608.23705) |
| ★★★ | 2026 | [Using Poly-Encoders for Computationally Efficient Automated Creativity Assessment](https://arxiv.org/abs/2608.26165) | Sam Grouchnikov, Phillip Gregory, Jiho Noh | AIED 2026 (Lecture Notes in Computer Science) | LLM | [DOI 10.1007/978-3-032-29755-6_32](https://doi.org/10.1007/978-3-032-29755-6_32) |

[↑ Contents](#contents)

## D. Model judges and reward models

Language models used as the scorer rather than the subject: LLM-as-a-judge pipelines, creativity
reward models, and the bias literature that has grown around them, position bias, verbosity,
shortcut bias, scoring bias. The fastest-moving family and the one with the thinnest validity base,
so the critiques are listed alongside the methods rather than separately. No Original-side
counterpart exists, which is itself the argument these critiques make.

*17 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★★ | 2025 | [Automating chemosensory creativity assessment with large language models](https://doi.org/10.1016/j.foodqual.2025.105599) | Qian Janice Wang, Robert Pellegrino | Food Quality and Preference (2025) | LLM | [DOI 10.1016/j.foodqual.2025.105599](https://doi.org/10.1016/j.foodqual.2025.105599) |
| ★★★ | 2025 | [Beyond Correctness: Evaluating Subjective Writing Preferences Across Cultures](https://arxiv.org/abs/2510.14616) | Shuangshuang Ying, Yunwen Li, Xingwei Qu et al. | arXiv preprint (no published version found) | LLM | [arXiv:2510.14616](https://arxiv.org/abs/2510.14616) |
| ★★★ | 2025 | [Bridging the Creativity Understanding Gap: Small-Scale Human Alignment Enables Expert-Level Humor Ranking in LLMs](https://doi.org/10.18653/v1/2025.findings-emnlp.884) | Kuan Lok Zhou, Jiayi Chen, Siddharth Suresh et al. | Findings of EMNLP 2025 | LLM | [DOI 10.18653/v1/2025.findings-emnlp.884](https://doi.org/10.18653/v1/2025.findings-emnlp.884) |
| ★★ | 2025 | [Can Large Language Models Outperform Non-Experts in Poetry Evaluation? A Comparative Study Using the Consensual Assessment Technique](https://doi.org/10.48448/whrs-et52) | Association for Computational Linguistics 2025, brown, dan, Goes, Fabricio et al. | EMNLP 2025 | LLM | [DOI 10.48448/whrs-et52](https://doi.org/10.48448/whrs-et52) |
| ★★★ | 2025 | [Curiosity-Driven LLM-as-a-judge for Personalized Creative Judgment](https://arxiv.org/abs/2510.05135) | Vanya Bannihatti Kumar, Divyanshu Goyal, Akhil Eppa et al. | arXiv preprint (no published version found) | LLM | [arXiv:2510.05135](https://arxiv.org/abs/2510.05135) |
| ★★★ | 2025 | [Evaluating and Enhancing Large Language Models for Novelty Assessment in Scholarly Publications](https://doi.org/10.18653/v1/2025.aisd-main.5) | Ethan Lin, Zhiyuan Peng, Yi Fang | AISD @ ACL 2025 (Workshop on AI and Scientific Discovery) | LLM | [DOI 10.18653/v1/2025.aisd-main.5](https://doi.org/10.18653/v1/2025.aisd-main.5) |
| ★★ | 2025 | [Leveraging Large Models to Evaluate Novel Content: A Case Study on Advertisement Creativity](https://doi.org/10.18653/v1/2025.emnlp-main.1072) | Zhaoyi Joey Hou, Adriana Kovashka, Xiang Lorraine Li | EMNLP 2025 | LLM | [DOI 10.18653/v1/2025.emnlp-main.1072](https://doi.org/10.18653/v1/2025.emnlp-main.1072) |
| ★★★ | 2025 | [The Silent Judge: Unacknowledged Shortcut Bias in LLM-as-a-Judge](https://arxiv.org/abs/2509.26072) | Arash Marioriyad, Mohammad Hossein Rohban, Mahdieh Soleymani Baghshah | NeurIPS 2025 Workshop: Reliable ML from Unreliable Data | LLM | [arXiv:2509.26072](https://arxiv.org/abs/2509.26072) |
| ★★★ | 2026 | [Creativity Bias: How Machine Evaluation Struggles with Creativity in Literary Translations](https://arxiv.org/abs/2605.13596) | Kyo Gerrits, Rik van Noord, Ana Guerberof Arenas | EAMT 2026 | LLM | [arXiv:2605.13596](https://arxiv.org/abs/2605.13596) |
| ★★★ | 2026 | [Decoupled Analysis-Judging: An Automated Creativity Evaluator Using LLMs in Complex Multi-step Creativity Tasks](https://arxiv.org/abs/2609.03432) | Xiangyu Wang, Jin Wu, Xiaoyu Li et al. | EMNLP 2026 | LLM | [arXiv:2609.03432](https://arxiv.org/abs/2609.03432) |
| ★★★ | 2026 | [DeepInstructor: An Agentic AI Instructor for Experience-Driven Idea Evaluation](https://arxiv.org/abs/2609.22104) | Rongcan Pei, Fang Guo, Qinglin Qi et al. | arXiv preprint (no published version found) | LLM | [arXiv:2609.22104](https://arxiv.org/abs/2609.22104) |
| ★★★ | 2026 | [LitBench: A Benchmark and Dataset for Reliable Evaluation of Creative Writing](https://doi.org/10.18653/v1/2026.eacl-long.362) | Daniel Fein, Sebastian Russo, Violet Xiang et al. | EACL 2026 | LLM | [DOI 10.18653/v1/2026.eacl-long.362](https://doi.org/10.18653/v1/2026.eacl-long.362) |
| ★★★ | 2026 | [Old Ideas, Novel Problems: The Instability of LLM-Based Novelty Evaluation](https://arxiv.org/abs/2610.02022) | Noy Sternlicht, Simra Shahid, Peter Jansen et al. | arXiv preprint (no published version found) | LLM | [arXiv:2610.02022](https://arxiv.org/abs/2610.02022) |
| ★★★ | 2026 | [Rethinking Creativity Evaluation: A Critical Analysis of Existing Creativity Evaluations](https://doi.org/10.18653/v1/2026.eacl-long.297) | Li-Chun Lu, Miri Liu, Pin-Chun Lu et al. | EACL 2026 | LLM | [DOI 10.18653/v1/2026.eacl-long.297](https://doi.org/10.18653/v1/2026.eacl-long.297) |
| ★★★ | 2026 | [The Judge Is Not Its Twin: Post-training makes a model's writing more predictable but barely moves its taste, as a judge, toward predictable writing](https://arxiv.org/abs/2609.32196) | Arman Nik Khah, Arvin Bahreini | arXiv preprint (no published version found) | LLM | [arXiv:2609.32196](https://arxiv.org/abs/2609.32196) |
| ★★★ | 2026 | [When Reasoning Supervision Hurts: TTCW-Based Long-Form Literary Review Generation](https://arxiv.org/abs/2605.20364) | Jinlong Liu, Mohammed Bahja, Mark Lee | arXiv preprint (no published version found) | LLM | [arXiv:2605.20364](https://arxiv.org/abs/2605.20364) |
| ★★★ | 2026 | [Why Large Language Models and Humans Converge and Diverge in Evaluating Creativity](https://doi.org/10.48550/arXiv.2607.22218) | Pengzhao Lyu, Yeun Joon Kim, Hanlin Xiao et al. | arXiv preprint (no published version found) | LLM | [DOI 10.48550/arXiv.2607.22218](https://doi.org/10.48550/arXiv.2607.22218) |

[↑ Contents](#contents)

## E. Benchmarks and evaluation suites

Fixed task suites with released data against which models are compared, constraint-controlled story
writing, creative code generation, physical and real-world problem solving, scientific ideation,
humour, linguistic diversity. The entries differ mainly in what they hold constant.

*22 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★ | 2024 | [Getting Serious about Humor: Crafting Humor Datasets with Unfunny Large Language Models](https://doi.org/10.18653/v1/2024.acl-short.76) | Zachary Horvitz, Jingru Chen, Rahul Aditya et al. | ACL 2024 (Short Papers) | LLM | [DOI 10.18653/v1/2024.acl-short.76](https://doi.org/10.18653/v1/2024.acl-short.76) |
| ★★ | 2024 | [MacGyver: Are Large Language Models Creative Problem Solvers?](https://doi.org/10.18653/v1/2024.naacl-long.297) | Yufei Tian, Abhilasha Ravichander, Lianhui Qin et al. | NAACL 2024 | LLM | [DOI 10.18653/v1/2024.naacl-long.297](https://doi.org/10.18653/v1/2024.naacl-long.297) |
| ★★ | 2025 | [A Comparative Approach to Assessing Linguistic Creativity of Large Language Models and Humans](https://doi.org/10.1016/j.procs.2025.09.250) | Anca Dinu, Andra-Maria Florescu, Alina Resceanu | KES 2025; Procedia Computer Science 270:1292–1301 | LLM | [DOI 10.1016/j.procs.2025.09.250](https://doi.org/10.1016/j.procs.2025.09.250) |
| ★★★ | 2025 | [Benchmarking Language Model Creativity: A Case Study on Code Generation](https://doi.org/10.18653/v1/2025.naacl-long.141) | Yining Lu, Dixuan Wang, Tianjian Li et al. | NAACL 2025 | LLM | [DOI 10.18653/v1/2025.naacl-long.141](https://doi.org/10.18653/v1/2025.naacl-long.141) |
| ★★★ | 2025 | [Benchmarking Linguistic Diversity of Large Language Models](https://doi.org/10.1162/tacl.a.47) | Yanzhu Guo, Guokan Shang, Chloé Clavel | TACL 2025 | LLM | [DOI 10.1162/tacl.a.47](https://doi.org/10.1162/tacl.a.47) |
| ★★★ | 2025 | [Creativity Benchmark: A benchmark for marketing creativity for large language models](https://arxiv.org/abs/2509.09702) | Ninad Bhat, Kieran Browne, Pip Bingemann | arXiv preprint (no published version found) | LLM | [arXiv:2509.09702](https://arxiv.org/abs/2509.09702) |
| ★★★ | 2025 | [CS4: Measuring the Creativity of Large Language Models Automatically by Controlling the Number of Story-Writing Constraints](https://arxiv.org/abs/2410.04197) | Anirudh Atmakuru, Jatin Nainani, Rohith Siddhartha Reddy Bheemreddy et al. | EMNLP 2025 | LLM | [arXiv:2410.04197](https://arxiv.org/abs/2410.04197) |
| ★★★ | 2025 | [CreBench: Human-Aligned Creativity Evaluation from Idea to Process to Product](https://arxiv.org/abs/2511.13626) | Kaiwen Xue, Chenglong Li, Zhonghong Ou et al. | AAAI 2026 | LLM | [arXiv:2511.13626](https://arxiv.org/abs/2511.13626) |
| ★★ | 2025 | [Evaluating the Creativity of LLMs in Persian Literary Text Generation](https://doi.org/10.18653/v1/2025.findings-emnlp.796) | Armin Tourajmehr, Mohammad Reza Modarres, Yadollah Yaghoobzadeh | Findings of EMNLP 2025, pp. 14762–14774 | LLM | [DOI 10.18653/v1/2025.findings-emnlp.796](https://doi.org/10.18653/v1/2025.findings-emnlp.796) |
| ★★★ | 2025 | [IdeaBench: Benchmarking Large Language Models for Research Idea Generation](https://arxiv.org/abs/2411.02429) | Sikun Guo, Amir Hassan Shariatmadari, Guangzhi Xiong et al. | KDD 2025 | LLM | [DOI 10.1145/3711896.3737419](https://doi.org/10.1145/3711896.3737419) |
| ★★★ | 2025 | [Societal Impacts Research Requires Benchmarks for Creative Composition Tasks](https://arxiv.org/abs/2504.06549) | Judy Hanwen Shen, Carlos Guestrin | ICLR 2025 Workshop on Bidirectional Human-AI Alignment (BiAlign) | LLM | [arXiv:2504.06549](https://arxiv.org/abs/2504.06549) |
| ★★★ | 2026 | [AGC-Bench: Measuring Artificial General Creativity](https://arxiv.org/abs/2607.01152) | Roger Beaty, Vijeta Deshpande, Clin K. Y. Lai et al. | arXiv preprint (no published version found) | LLM | [arXiv:2607.01152](https://arxiv.org/abs/2607.01152) |
| ★★★ | 2026 | [ALPS: Measuring Valid Creativity in Large Language Models with Mathematical Construction](https://arxiv.org/abs/2608.15979) | Eric Xie, Wenqian Ye, Aidong Zhang | arXiv preprint (no published version found) | LLM | [arXiv:2608.15979](https://arxiv.org/abs/2608.15979) |
| ★★ | 2026 | [Beyond One Path: Evaluating and Enhancing Divergent Thinking in Interactive LLM Agents](https://arxiv.org/abs/2605.28465) | Jihyeong Park, Ingeol Baek, Jeonghyun Park et al. | arXiv preprint (no published version found) | LLM | [arXiv:2605.28465](https://arxiv.org/abs/2605.28465) |
| ★★ | 2026 | [Can LLM Agents Discover? Evaluating Creativity on ML Engineering Tasks](https://arxiv.org/abs/2608.30047) | Shitanshu Bhushan, Yunxiang Zhang, Lu Wang | COLM 2026 | LLM | [arXiv:2608.30047](https://arxiv.org/abs/2608.30047) |
| ★★★ | 2026 | [CreativityBench: Evaluating Agent Creative Reasoning via Affordance-Based Tool Repurposing](https://arxiv.org/abs/2605.02910) | Cheng Qian, Hyeonjeong Ha, Jiayu Liu et al. | arXiv preprint (no published version found) | LLM | [arXiv:2605.02910](https://arxiv.org/abs/2605.02910) |
| ★★★ | 2026 | [CreativityPrism: A Cross-Domain Evaluation Framework for Large Language Model Creativity](https://arxiv.org/abs/2510.20091) | Zhaoyi Joey Hou, Bowei Alvin Zhang, Yining Lu et al. | Transactions on Machine Learning Research (06/2026) | LLM | [arXiv:2510.20091](https://arxiv.org/abs/2510.20091) |
| ★★★ | 2026 | [CresOWLve: Benchmarking Creative Problem-Solving Over Real-World Knowledge](https://arxiv.org/abs/2604.03374) | Mete Ismayilzada, Renqing Cuomao, Daniil Yurshevich et al. | COLM 2026 | LLM | [arXiv:2604.03374](https://arxiv.org/abs/2604.03374) |
| ★★★ | 2026 | [Evaluating LLMs' Divergent Thinking Capabilities for Scientific Idea Generation with Minimal Context (LiveIdeaBench)](https://doi.org/10.1038/s41467-026-70245-1) | Kai Ruan, Xuan Wang, Jixiang Hong et al. | Nature Communications (2026) | LLM | [DOI 10.1038/s41467-026-70245-1](https://doi.org/10.1038/s41467-026-70245-1) |
| ★★★ | 2026 | [Is Imagination Derived from Hallucination? A Cross-Taxonomy Evaluation of Imagination and Hallucination in Large Language Models](https://arxiv.org/abs/2609.22152) | Zixuan Tang, Hongzong Li, Shuxin Zhuang et al. | arXiv preprint (no published version found) | LLM | [arXiv:2609.22152](https://arxiv.org/abs/2609.22152) |
| ★★★ | 2026 | [LLM Jaggedness Unlocks Scientific Creativity](https://arxiv.org/abs/2605.10574) | Shray Mathur, J. Anibal Boscoboinik, Esther H. R. Tsai et al. | arXiv preprint (no published version found) | LLM | [arXiv:2605.10574](https://arxiv.org/abs/2605.10574) |
| ★★★ | 2026 | [QUIET: A Multi-Blank Cascaded Story Cloze Benchmark for LLM Creative Generation Capability](https://arxiv.org/abs/2605.25955) | Bo Zou, Chao Xu | arXiv preprint (no published version found) | LLM | [arXiv:2605.25955](https://arxiv.org/abs/2605.25955) |

[↑ Contents](#contents)

## F. Evaluation frameworks and construct validity

The pre-LLM theory of how to evaluate a creative *system* rather than an artefact, Wiggins'
descriptive framework, Ritchie's empirical criteria, Colton's creative tripod, FACE/IDEA,
Jordanous's SPECS, together with the modern construct-validity critiques that rediscover the same
problems in benchmark form. This is the family the LLM literature most often skips, and the only one
where Original work still outnumbers LLM work.

*28 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★★ | 2006 | [A preliminary framework for description, analysis and comparison of creative systems](https://doi.org/10.1016/j.knosys.2006.04.009) | Geraínt A. Wiggins | Knowledge-Based Systems (2006) | Original | [DOI 10.1016/j.knosys.2006.04.009](https://doi.org/10.1016/j.knosys.2006.04.009) |
| ★★★ | 2007 | [Some Empirical Criteria for Attributing Creativity to a Computer Program](https://doi.org/10.1007/s11023-007-9066-2) | Graéme Ritchie | Minds and Machines (2007) | Original | [DOI 10.1007/s11023-007-9066-2](https://doi.org/10.1007/s11023-007-9066-2) |
| ★★★ | 2008 | [Creativity versus the perception of creativity in computational systems](https://cdn.aaai.org/Symposia/Spring/2008/SS-08-03/SS08-03-003.pdf) | Simon Colton | AAAI Spring Symposium on Creative Intelligent Systems 2008 | Original | [PDF](https://cdn.aaai.org/Symposia/Spring/2008/SS-08-03/SS08-03-003.pdf) |
| ★★★ | 2010 | [Evaluating creativity in humans, computers, and collectively intelligent systems](https://doi.org/10.5555/1854969.1854977) | Mary Lou Maher | DESIRE '10: Creativity and Innovation in Design | Original | [DOI 10.5555/1854969.1854977](https://doi.org/10.5555/1854969.1854977) |
| ★★★ | 2011 | [Computational creativity theory: The FACE and IDEA descriptive models](https://computationalcreativity.net/iccc2011/proceedings/the_foundational/colton_1_iccc11.pdf) | Simon Colton, John Charnley, Alison Pease | ICCC 2011 (2nd Int. Conf. on Computational Creativity) | Original | [PDF](https://computationalcreativity.net/iccc2011/proceedings/the_foundational/colton_1_iccc11.pdf) |
| ★★★ | 2011 | [On impact and evaluation in computational creativity: a discussion of the Turing Test and an alternative proposal](https://www.thepaintingfool.com/archive/papers/pease_aisb11.pdf) | Alison Pease, Simon Colton | AISB 2011 Symposium on AI and Philosophy | Original | [PDF](https://www.thepaintingfool.com/archive/papers/pease_aisb11.pdf) |
| ★★★ | 2012 | [A Standardised Procedure for Evaluating Creative Systems: Computational Creativity Evaluation Based on What it is to be Creative](https://doi.org/10.1007/s12559-012-9156-1) | Anna Jordanous | Cognitive Computation (2012) | Original | [DOI 10.1007/s12559-012-9156-1](https://doi.org/10.1007/s12559-012-9156-1) |
| ★★★ | 2018 | [Evaluating Computational Creativity](https://doi.org/10.1145/3167476) | Carolyn Lamb, Daniel G. Brown, Charles L. A. Clarke | ACM Computing Surveys (2018) | Original | [DOI 10.1145/3167476](https://doi.org/10.1145/3167476) |
| ★★★ | 2019 | [Evaluating Evaluation: Assessing Progress and Practices in Computational Creativity Research](https://doi.org/10.1007/978-3-319-43610-4_10) | Anna Jordanous | Computational Synthesis and Creative Systems (Springer) (2019) | Original | [DOI 10.1007/978-3-319-43610-4_10](https://doi.org/10.1007/978-3-319-43610-4_10) |
| ★★★ | 2024 | [Creativity and Markov Decision Processes](https://arxiv.org/abs/2405.14966) | Joonas Lahikainen, Nadia M. Ady, Christian Guckelsberger | ICCC 2024 (15th Int. Conf. on Computational Creativity) | LLM | [arXiv:2405.14966](https://arxiv.org/abs/2405.14966) |
| ★★ | 2024 | [SciMON: Scientific Inspiration Machines Optimized for Novelty](https://doi.org/10.18653/v1/2024.acl-long.18) | Qingyun Wang, Doug Downey, Heng Ji et al. | ACL 2024 | LLM | [DOI 10.18653/v1/2024.acl-long.18](https://doi.org/10.18653/v1/2024.acl-long.18) |
| ★★★ | 2025 | [Assessing the Capabilities of LLMs in Humor:A Multi-dimensional Analysis of Oogiri Generation and Evaluation](https://arxiv.org/abs/2511.09133) | Ritsu Sakabe, Hwichan Kim, Tosho Hirasawa et al. | arXiv preprint (no published version found) | LLM | [arXiv:2511.09133](https://arxiv.org/abs/2511.09133) |
| ★★★ | 2025 | [Ideometrics: a scientific approach to generating, evaluating, and prioritising ideas](https://doi.org/10.7189/jogh.15.04360) | Igor Rudan, Aziz Sheikh | Journal of Global Health (2025) | Original | [DOI 10.7189/jogh.15.04360](https://doi.org/10.7189/jogh.15.04360) |
| ★★★ | 2025 | [Measuring what Matters: Construct Validity in Large Language Model Benchmarks](https://doi.org/10.52202/085713-0590) | Andrew M. Bean, Ryan Othniel Kearns, Angelika Romanou et al. | NeurIPS 2025 Datasets & Benchmarks Track | LLM | [DOI 10.52202/085713-0590](https://doi.org/10.52202/085713-0590) |
| ★★★ | 2025 | [The Geometry of Creative Variability: How Credal Sets Expose Calibration Gaps in Language Models](https://arxiv.org/abs/2509.23088) | Esteban Garces Arias, Julian Rodemann, Christian Heumann | UncertaiNLP 2025 workshop @ EMNLP | LLM | [DOI 10.18653/v1/2025.uncertainlp-main.5](https://doi.org/10.18653/v1/2025.uncertainlp-main.5) |
| ★★★ | 2026 | [Are Semantic Networks Associated with Idea Originality in Artificial Creativity? A Comparison with Human Agents](https://arxiv.org/abs/2602.02048) | Umberto Domanti, Lorenzo Campidelli, Sergio Agnoli et al. | CHI 2026 | LLM | [arXiv:2602.02048](https://arxiv.org/abs/2602.02048) |
| ★★★ | 2026 | [Assessing LLMs' mathematical abilities requires understanding the various mechanisms of mathematical creativity](https://arxiv.org/abs/2608.16118) | Silvère Gangloff | arXiv preprint (no published version found) | LLM | [arXiv:2608.16118](https://arxiv.org/abs/2608.16118) |
| ★★★ | 2026 | [Beyond Reproduction: A Paired-Task Framework for Assessing LLM Comprehension and Creativity in Literary Translation](https://arxiv.org/abs/2604.18169) | Ran Zhang, Steffen Eger, Arda Tezcan et al. | Findings of ACL 2026 | LLM | [DOI 10.18653/v1/2026.findings-acl.2030](https://doi.org/10.18653/v1/2026.findings-acl.2030) |
| ★★★ | 2026 | [Calibrated Surprise: An Information-Theoretic Account of Creative Quality](https://arxiv.org/abs/2604.26269) | Bo Zou, Chao Xu | arXiv preprint (no published version found) | LLM | [arXiv:2604.26269](https://arxiv.org/abs/2604.26269) |
| ★★ | 2026 | [Can LLM generate interesting mathematical research problems?](https://arxiv.org/abs/2603.18813) | Xiaoyang Chen, Xiang Jiang | arXiv preprint (no published version found) | LLM | [arXiv:2603.18813](https://arxiv.org/abs/2603.18813) |
| ★★★ | 2026 | [CLIN: an Objective Framework for Evaluating Creativity in Short Persian Literary Text](https://arxiv.org/abs/2608.30754) | Mohammad Reza Modarres, Armin Tourajmehr, Yadollah Yaghoobzadeh et al. | Findings of EMNLP 2026 | LLM | [arXiv:2608.30754](https://arxiv.org/abs/2608.30754) |
| ★★★ | 2026 | [DEFINED: A Data-Efficient Computational Framework for Fine-Grained Creativity Assessment in Debate Scenarios](https://arxiv.org/abs/2606.07226) | Tongzhou Yu, Mingjia Li, Hong Qian et al. | KDD 2026 | LLM | [DOI 10.1145/3770855.3817874](https://doi.org/10.1145/3770855.3817874) |
| ★★★ | 2026 | [Evaluating LLM Creativity through Long-Tail Performance](https://arxiv.org/abs/2610.12998) | Yichen Wang, Tenghao Huang, Vishakh Padmakumar et al. | arXiv preprint (no published version found) | LLM | [arXiv:2610.12998](https://arxiv.org/abs/2610.12998) |
| ★★★ | 2026 | [HindSight: Evaluating LLM-Generated Research Ideas via Future Impact](https://arxiv.org/abs/2603.15164) | Bo Jiang | arXiv preprint (no published version found) | LLM | [arXiv:2603.15164](https://arxiv.org/abs/2603.15164) |
| ★★★ | 2026 | [Measuring Creativity in the Age of Generative AI: Distinguishing Human and AI-Generated Creative Performance in Hiring and Talent Systems](https://arxiv.org/abs/2604.19799) | Yigal Rosen, Ilia Rushkin | arXiv preprint — presented at BIG.AI@MIT 2026 | LLM | [arXiv:2604.19799](https://arxiv.org/abs/2604.19799) |
| ★★★ | 2026 | [On the Creativity of AI Agents](https://arxiv.org/abs/2604.13242) | Giorgio Franceschelli, Mirco Musolesi | arXiv preprint (no published version found) | LLM | [arXiv:2604.13242](https://arxiv.org/abs/2604.13242) |
| ★★★ | 2026 | [POEMetric: The Last Stanza of Humanity](https://arxiv.org/abs/2604.03695) | Bingru Li, Han Wang, Hazel Wilkinson | ICLR 2026 | LLM | [arXiv:2604.03695](https://arxiv.org/abs/2604.03695) |
| ★★★ | 2026 | [The Proxy Presumption: From Semantic Embeddings to Valid Social Measures](https://arxiv.org/abs/2605.07409) | Baishi Li, Ta Yu, Kelvin J. L. Koa et al. | ACL 2026 (Oral) | LLM | [DOI 10.18653/v1/2026.acl-long.1048](https://doi.org/10.18653/v1/2026.acl-long.1048) |

[↑ Contents](#contents)

## G. Process and co-creation measurement

Measurement aimed at the *process* rather than the finished artefact: human–AI co-creation studies
and their interaction instruments, idea-evolution and collective-diversity experiments, and the
question of whether a generation-time parameter such as temperature tracks any creativity measure at
all. Methods whose object is *raising* a creativity score rather than measuring one are in [Adjacent
and background reading](#adjacent-and-background-reading).

*6 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★ | 2022 | [CoAuthor: Designing a Human-AI Collaborative Writing Dataset for Exploring Language Model Capabilities](https://doi.org/10.1145/3491102.3502030) | Mina Lee, Percy Liang, Qian Yang | CHI 2022 | LLM | [DOI 10.1145/3491102.3502030](https://doi.org/10.1145/3491102.3502030) |
| ★★ | 2023 | [Co-Writing Screenplays and Theatre Scripts with Language Models: An Evaluation by Industry Professionals](https://doi.org/10.1145/3544548.3581225) | Piotr Mirowski, Kory W. Mathewson, Jaylen Pittman et al. | CHI 2023 | LLM | [DOI 10.1145/3544548.3581225](https://doi.org/10.1145/3544548.3581225) |
| ★★ | 2024 | [Characterising the Creative Process in Humans and Large Language Models](https://doi.org/10.48550/arXiv.2405.00899) | Surabhi S Nath, Peter Dayan, Claire E. Stevenson | arXiv preprint (no published version found) | LLM | [DOI 10.48550/arXiv.2405.00899](https://doi.org/10.48550/arXiv.2405.00899) |
| ★★ | 2024 | [Is Temperature the Creativity Parameter of Large Language Models?](https://arxiv.org/abs/2405.00492) | Max Peeperkorn, Tom Kouwenhoven, Dan Brown et al. | ICCC | LLM | [arXiv:2405.00492](https://arxiv.org/abs/2405.00492) |
| ★★ | 2025 | [A Systematic Review of Human-AI Co-Creativity](https://doi.org/10.48550/arXiv.2506.21333) | Singh, Saloni, Koen V. Hindriks, Dirk Heylen et al. | arXiv preprint (no published version found) | LLM | [DOI 10.48550/arXiv.2506.21333](https://doi.org/10.48550/arXiv.2506.21333) |
| ★★ | 2025 | [How AI Ideas Affect the Creativity, Diversity, and Evolution of Human Ideas: Evidence From a Large, Dynamic Experiment](https://doi.org/10.1145/3715928.3737481) | Joshua Ashkinaze, Julia Mendelsohn, Li Qiwei et al. | Creativity & Cognition 2025 (ACM C&C) | LLM | [DOI 10.1145/3715928.3737481](https://doi.org/10.1145/3715928.3737481) |

[↑ Contents](#contents)

## H. Interpretability of the evaluation mechanism

Interpretability is a separate line of work and most of it is not about evaluation. The three
entries kept here are the ones that bear on the evaluation mechanism itself: what a model's internal
states do when it is asked to *judge* creativity, and whether the representations a creativity test
is supposed to probe are the ones actually engaged. Work that steers internals to make output more
creative belongs to the generation side and is not listed.

*3 papers*

| Focus | Year | Paper | Authors | Venue | Side | ID |
| :-: | :-: | --- | --- | :-: | :-: | --- |
| ★★ | 2022 | [Modeling the Remote Associates Test as Retrievals from Semantic Memory](https://doi.org/10.1111/cogs.13145) | Jule Schatz, Steven J. Jones, John E. Laird | Cognitive Science (2022) | Original | [DOI 10.1111/cogs.13145](https://doi.org/10.1111/cogs.13145) |
| ★★ | 2024 | [Steering Large Language Models to Evaluate and Amplify Creativity](https://arxiv.org/abs/2412.06060) | Matthew Lyle Olson, Neale Ratzlaff, Musashi Hinck et al. | NeurIPS 2024 Workshop on Creativity & Generative AI (Spotlight) | LLM | [arXiv:2412.06060](https://arxiv.org/abs/2412.06060) |
| ★★ | 2026 | [Large Language Models Align with the Human Brain during Creative Thinking](https://arxiv.org/abs/2604.03480) | Mete Ismayilzada, Simone A. Luchini, Abdulkadir Gokce et al. | COLM 2026 | LLM | [arXiv:2604.03480](https://arxiv.org/abs/2604.03480) |

[↑ Contents](#contents)

## Adjacent and background reading

These works are regularly cited in creativity-evaluation work and a reader will meet them, but in each case the paper's own object of study is something else most often *producing* more creative output rather than measuring it.

- **[Brainstorm, then Select: a Generative Language Model Improves Its Creativity Score](https://openreview.net/forum?id=8HwKaJ1wvl)**: Douglas Summers-Stay, Clare R. Voss, Stephanie M. Lukin, 2023, AAAI-23 Workshop on Creative AI across Modalities (OpenReview) · [PDF](https://openreview.net/forum?id=8HwKaJ1wvl)  
  A generate-then-filter method that improves a model's score on an existing creativity test.

- **[Quality-Diversity through AI Feedback](https://arxiv.org/abs/2310.13032)**: Herbie Bradley, Andrew Dai, Hannah Teufel et al., 2023, arXiv preprint (no published version found) · [arXiv:2310.13032](https://arxiv.org/abs/2310.13032)  
  Uses an LLM as the quality-and-diversity critic inside a search loop. The critic is a means to better generation, not an evaluation instrument offered for reuse.

- **[Representing creative thought: A representational similarity analysis of creative idea generation and evaluation](https://doi.org/10.1016/j.neuropsychologia.2023.108587)**: Heath E. Matheson, Yoed Nissan Kenett, Courtney R. Gerver et al., 2023, Neuropsychologia (2023) · [DOI 10.1016/j.neuropsychologia.2023.108587](https://doi.org/10.1016/j.neuropsychologia.2023.108587)  
  A representational-similarity analysis of idea generation and evaluation in the brain. The construct it illuminates is the one the tests in Section A try to capture, but the paper measures neural patterns, not creative products.

- **[Infini-gram: Scaling Unbounded n-gram Language Models to a Trillion Tokens](https://arxiv.org/abs/2401.17377)**: Jiacheng Liu, Sewon Min, Luke Zettlemoyer et al., 2024, COLM 2024 (spotlight) · [arXiv:2401.17377](https://arxiv.org/abs/2401.17377)  
  The paper's object is an n-gram indexing engine over a trillion tokens, not a creativity measure. It is here because the linguistic-creativity attribution work in Section C is built on top of it.

- **[LLM Discussion: Enhancing the Creativity of Large Language Models via Discussion Framework and Role-Play](https://arxiv.org/abs/2405.06373)**: Li-Chun Lu, Shou-Jen Chen, Tsung-Min Pai et al., 2024, COLM 2024 · [arXiv:2405.06373](https://arxiv.org/abs/2405.06373)  
  A multi-agent prompting framework that raises creativity scores; the scores are borrowed from Section A rather than examined.

- **[Turning Up the Heat: Min-p Sampling for Creative and Coherent LLM Outputs](https://arxiv.org/abs/2407.01082)**: Minh Nhat Nguyen, Andrew Baker, Clement Neo et al., 2024, ICLR 2025 (Oral) · [arXiv:2407.01082](https://arxiv.org/abs/2407.01082)  
  A decoding method. Creativity scores appear as the evidence that it works, which is the opposite direction from the rest of the list.

- **[Creative Beam Search: LLM-as-a-Judge For Improving Response Generation](https://arxiv.org/abs/2405.00099)**: Giorgio Franceschelli, Mirco Musolesi, 2024, ICCC 2024 · [arXiv:2405.00099](https://arxiv.org/abs/2405.00099)  
  Uses LLM-as-a-judge inside decoding to pick among candidates. Closest of the nine to being an evaluation paper, but the contribution is the generation procedure.

- **[Modifying Large Language Model Post-Training for Diverse Creative Writing](https://arxiv.org/abs/2503.17126)**: John Joon Young Chung, Vishakh Padmakumar, Melissa Roemmele et al., 2025, arXiv preprint (no published version found) · [arXiv:2503.17126](https://arxiv.org/abs/2503.17126)  
  A training-side intervention for diverse creative writing, reported through diversity measures.

- **[Collective creativity in hybrid societies](https://doi.org/10.48550/arXiv.2609.02620)**: Mason Youngblood, Katie Mudd, Manuel Anglada-Tort et al., 2026, arXiv preprint (no published version found) · [DOI 10.48550/arXiv.2609.02620](https://doi.org/10.48550/arXiv.2609.02620)  
  A position paper on how mixed human–machine groups produce ideas collectively. It frames a measurement problem rather than defining a measure.

[↑ Contents](#contents)

## Contributing

Additions are welcome. To keep the list's one useful property — that its metadata is right — please include with any proposed entry:

1. the canonical identifier (arXiv ID or DOI), not just a URL;
2. the venue of record, or an explicit statement that it is an unpublished preprint;
3. the full author list as the primary index gives it;
4. which section it belongs in, which focus tier, and whether it is Original or LLM side.

Entries whose venue cannot be confirmed from arXiv or OpenAlex will be marked unconfirmed rather than rejected.
## License

The list itself — the selection, structure, annotations and metadata — is released under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/): use it without attribution. The papers it points to are the property of their authors and publishers; links go to publisher pages or author-posted preprints.
