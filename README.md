# Awesome Creativity × LLM Papers

![lists](https://img.shields.io/badge/lists-2%20of%206-blue) ![papers](https://img.shields.io/badge/papers-~200%20unique-blue) ![metadata](https://img.shields.io/badge/metadata-verified%20against%20arXiv%20%2B%20OpenAlex-brightgreen) ![updated](https://img.shields.io/badge/updated-2026--10--13-lightgrey) ![license](https://img.shields.io/badge/list-CC0--1.0-informational)

Curated reading lists on **creativity in large language models**: how it is measured, how varied it is, and how it relates to the science of human creativity.

Most work on LLM creativity borrows its tools from psychology and computational creativity, such as the Alternate Uses Task, the Remote Associates Test, and expert rating protocols. It rarely asks whether those tools still measure the same thing when the test-taker is a model. These lists put the original creativity-science literature next to the LLM literature so the two can be read against each other. They are the working bibliography for a series of surveys on creativity and LLMs.

## The lists

| List | What it covers | Papers | Status |
| --- | --- | :-: | --- |
| [**Evaluation**](Evaluation.md) | How creativity is evaluated: psychometric tests, human judgment, automatic metrics, model judges, benchmarks, and frameworks for checking whether any of them measure what they claim | 103 | Available |
| [**Diversity**](Diversity.md) | How diverse machine output is, how that diversity is measured, how it is lost through alignment and homogenization, and what has been tried to recover it | 119 | Available |
| Interpretability and machine neuroaesthetics | What models represent internally about emotion, style, form, novelty and creativity | | Coming |
| Analogy | Analogical reasoning and analogy as a creative mechanism, from structure-mapping to LLMs | | Coming |
| Figurative language, poetry and literature | Metaphor, humor, poetry, story generation and co-writing | | Coming |
| Theory of creativity | Foundational theories and how LLM research uses (or ignores) them | | Coming |


### Evaluation, by section

| Section | Papers |
| --- | :-: |
| [A. Psychometric tests and their machine adaptations](Evaluation.md#a-psychometric-tests-and-their-machine-adaptations) | 24 |
| [B. Human judgment protocols](Evaluation.md#b-human-judgment-protocols) | 9 |
| [C. Automatic metrics](Evaluation.md#c-automatic-metrics) | 15 |
| [D. Model judges and reward models](Evaluation.md#d-model-judges-and-reward-models) | 10 |
| [E. Benchmarks and evaluation suites](Evaluation.md#e-benchmarks-and-evaluation-suites) | 14 |
| [F. Evaluation frameworks and construct validity](Evaluation.md#f-evaluation-frameworks-and-construct-validity) | 13 |
| [G. Process and co-creation measurement](Evaluation.md#g-process-and-co-creation-measurement) | 6 |
| [H. Interpretability of the evaluation mechanism](Evaluation.md#h-interpretability-of-the-evaluation-mechanism) | 3 |
| [Adjacent and background reading](Evaluation.md#adjacent-and-background-reading) | 9 |

### Diversity, by section

| Section | Papers |
| --- | :-: |
| [A. Foundations: creativity theory and the diversity construct](Diversity.md#a-foundations-creativity-theory-and-the-diversity-construct) | 5 |
| [B. Measuring diversity: metrics](Diversity.md#b-measuring-diversity-metrics) | 10 |
| [C. Benchmarks and evaluation suites](Diversity.md#c-benchmarks-and-evaluation-suites) | 10 |
| [D. Phenomenon: homogenization of model output](Diversity.md#d-phenomenon-homogenization-of-model-output) | 13 |
| [E. Phenomenon: effects on people, culture, and the information ecosystem](Diversity.md#e-phenomenon-effects-on-people-culture-and-the-information-ecosystem) | 14 |
| [F. Self-consuming loops: model collapse and knowledge collapse](Diversity.md#f-self-consuming-loops-model-collapse-and-knowledge-collapse) | 8 |
| [G. Causes and mechanisms](Diversity.md#g-causes-and-mechanisms) | 6 |
| [H. Remedies at inference time: decoding and sampling](Diversity.md#h-remedies-at-inference-time-decoding-and-sampling) | 10 |
| [I. Remedies at inference time: prompting, personas, and steering](Diversity.md#i-remedies-at-inference-time-prompting-personas-and-steering) | 12 |
| [J. Remedies in training and post-training](Diversity.md#j-remedies-in-training-and-post-training) | 11 |
| [K. Open-endedness, quality-diversity, and search](Diversity.md#k-open-endedness-quality-diversity-and-search) | 5 |
| [L. Pluralism, safety, and the diversity-quality trade-off](Diversity.md#l-pluralism-safety-and-the-diversity-quality-trade-off) | 10 |
| [Adjacent and background reading](Diversity.md#adjacent-and-background-reading) | 5 |

## How to read a list

Each list opens with **Start here**, about eight papers that cover its main argument. After that, sections run in the order the argument does, so a list can be read from start to finish.

Every entry has:

- **Focus.** ★★★ means the topic is the paper's object of study. ★★ means it is a main axis, but the paper's goal is something else. ★ marks framing or lineage, and those papers are collected under *Adjacent and background reading*.
- **Side** (Evaluation list). *Original* means human-creativity science or classical computational creativity, and *LLM* means work on generative language models.
- **Year, authors, venue and a canonical ID** (DOI or arXiv). The metadata is checked against arXiv and OpenAlex. Preprints without a confirmed published version are labeled as such.

## Contributing

Suggestions are welcome through an issue or a pull request. With each proposed paper, please include:

1. a DOI or arXiv ID, not just a URL;
2. the venue of record, or a note that it is an unpublished preprint;
3. the author list as the primary index gives it;
4. the list and section it belongs in, its focus tier, and (for Evaluation) its side.

Each list's own Contributing section has its scope rules.

## Citation

A survey based on these lists is in preparation. A citation entry will be added here when it is available.

## License

The lists (selection, structure, annotations and metadata) are released under [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). The papers belong to their authors and publishers. Links point to publisher pages or author-posted preprints.

Maintained by [Melika Nobakhtian](https://github.com/MelikaNobakhtian).
