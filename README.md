# Leveraging LLMs in Coal Mining Incidents Reporting

## Introduction

Repository for Massive Data Institute with Professor Robin Dillon-Merrill Spring 2024. Using LLMs to compare and classify near miss events from minor events 


## Main Directories

- **input/**: Contains data used for the project
  - `labeled_accidents_injuries_2000-2018.xlsx`: Human-labeled coal mining incidents, contain main columns of Narratives and Label. Labels of Minor Events or Near miss with previous training to labelers
  - `raw_accidents_injuries_2000-2018.xlsx`: Raw data for 60,000+ coal mining incidents, containing Narrative column

- **output/**: Contains outputs, graphs and images of the project
  - `near-miss-vote.png`: Vote comparison between Human labelers and OpenAI with 2 different temperatures (variability of responses)

- **documentation/**: Contains papers, data dictionaries and references to guide research structure
  - `2024 conference paper final final.pdf`: How AI Can Help Learn Lessons from Incident Reporting Systems
  - `Coal Labeling Qualtrics instructions.docx`: Labeling instructions given to human labelers 
  - `lm_hackers.ipynb`: Notebook that explains how LLMs and word embeddings work from Professor Jeremy Howard
  - `Madsen_et_al-2016-Risk_Analysis.pdf`: Airline Safety Improvement Through Experience with Near-Misses: A Cautionary TaleNotebook for RAG pipeline experiments.

- **poster/**: Contains Jupyter notebooks for various experiments and analyses.
  - `HollandSoto_IncidentsAndLLMs_Spring2024.pdf`: Poster presented at MDI Spring 2024 Showcase

- **RiskyBusiness.ipynb**: Jupyternotebook with the main code base for the project

## Data

The dataset being used comes from the United States Department of Labor, Mine Safety and Health Administration (MSHA). This dataset contains 60,971 accidents in coal mines in the United States from 2000 to 2019. Please follow this link, to reference our dataset. [MSHA Fatality Reports](https://www.msha.gov/data-and-reports/fatality-reports/search)

## Findings

- LLMs with an identical instruction prompt cannot replicate human-like judgment
- The temperature parameter helps identify and prioritize more critical events
- Better results might be achieved by employing fine-tuning techniques on different models

## Conclusion

While the comparison between human judgement and the responses of LLMs is still quite stark overall, the speed of LLMs is unmatched. The human responses took weeks to compile, but an LLM can be queried with thousands of prompts in a matter of minutes. Many parameters, including temperature, and many other factors about the prompt can also be adjusted to condition the response of LLMs, but humans are much less deterministic and disciplined. While much research and experimentation is yet to be done, these results clearly indicate that LLMs in their current state are far from a drop-in replacement for human assessment
of risk.