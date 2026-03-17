# Embedded-NeuroEthics-Toolkit

![Status](https://img.shields.io/badge/Status-Work_in_Progress-orange)
![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Focus](https://img.shields.io/badge/Focus-NeuroAI_Governance-success)

*An open-source Python framework for translating high-level NeuroRights and AI Act requirements into quantifiable product quality metrics for Brain-Computer Interfaces (BCIs) and NeuroAI foundation models.**

# Mission: Quality over Neuroethics
Currently, Neuro-rights and AI Ethics frameworks are too abstract to be implemented by engineers. They rely on high-level declarations rather than technical standards. **Embedded-NeuroEthics-Toolkit (ENET)** bridges this gap. 

Our core philosophy: **Mental privacy breaches and algorithmic biases in BCIs should not be treated merely as "ethical concerns" but as actionable Product Defects.** By using specific quality metrics and risk assessments across the entire AI lifecycle, we can embed ethical and legal compliance directly into the technical design.

# The Problem: Liability Gaps in NeuroAI
As Foundation Models are increasingly used to decode brain signals (e.g., EEG-to-Text), several critical legal and ethical gaps emerge:
1. **The Hallucination Liability Gap ("Lie by Design"):** If a foundation model hallucinates while decoding brain signals and the BCI interface presents this hallucination as the user's actual thought or intent, who is liable? 
2. **Mental Privacy as a Product Defect:** High risks of "algorithmic shadows." Extracting excessive brain data beyond the intended functionality is a security and privacy defect.
3. **The Non-Medical BCI Blindspot:** If a BCI is not classified as a Medical Device (MDR/SaMD) but collects sensitive neural data, there is a massive liability gap for the manufacturer, especially regarding the EU AI Act classification for "mind reading."

# Core Modules (Under Development)

The toolkit consists of Python-based modules designed for AI auditors, DPOs, and BCI developers to evaluate NeuroAI systems:

## 1. `AI_Act_BCI_Classifier`
An automated decision-tree module to classify BCI systems under the EU AI Act.
* Evaluates whether non-medical "mind-reading" operations fall under *High-Risk* or *Prohibited* AI practices.
* Identifies regulatory gaps when the BCI hardware manufacturer did not train the underlying foundation model used for signal decoding.

## 2. `Hallucination_Liability_Scorer`
A risk assessment calculator for foundation models used in neuro-decoding.
* Compares the model's confidence scores against the UI/UX presentation.
* Flags "Lie by Design" scenarios where low-confidence decoded signals are presented as absolute user intent, defining thresholds for product liability.

## 3. `Mental_Privacy_Validator`
A data minimization and privacy impact assessment tool.
* Measures the ratio of collected raw neural data vs. required features for the specific task.
* Quantifies "algorithmic shadows" and outputs a `Privacy_Defect_Score`.

# Theoretical Framework & Papers
This toolkit is the practical implementation of the theoretical frameworks developed in the following papers:
* *Quality over Neuroethics: Who is responsible for “mind reading”?* (Presented at INS Neuroethics Meeting 2026).
* *Lie by Design: AI Hallucinations as the Product Liability Gap.* (Working Paper).
* *Mental Privacy Violations as Product Defects in AI Systems.* (Working Paper).

# Roadmap
- [x] Conceptual framework design
- [ ] Release `AI_Act_BCI_Classifier` beta script
- [ ] Release `Mental_Privacy_Validator` metrics logic
- [ ] Integration with ISO 42001 and NIST AI RMF guidelines for BCI
