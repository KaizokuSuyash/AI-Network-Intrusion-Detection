# AI Network Intrusion Detection System

A machine learning project exploring network traffic classification for DDoS detection, with an optional LLM-assisted explanation layer.

This project combines a **Random Forest classifier** with a Streamlit interface to examine network traffic samples and explore how machine learning can support intrusion detection. An optional Grok API integration provides natural-language explanations of predictions.

## Overview

Network intrusion detection involves identifying traffic patterns that may indicate malicious activity. This project focuses on DDoS-related traffic using a subset of the CIC-IDS2017 dataset.

The application provides a practical environment for exploring traffic classification, model predictions, and AI-assisted interpretation.

### Core components

- **Traffic classification:** Random Forest machine learning model.
- **Dataset:** CIC-IDS2017 traffic data supplied as a CSV file.
- **Interactive interface:** Streamlit application.
- **Packet simulation:** Select a sample from the available test data and inspect its classification.
- **Optional AI explanations:** Grok API integration for natural-language explanations.

The classifier's prediction and the LLM's explanation serve different purposes. An explanation is not independent evidence that an attack occurred.

## How the application works

1. **Load the data** — the application uses the available CIC-IDS2017 CSV dataset.
2. **Train the classifier** — initiate model training through the application interface.
3. **Select a traffic sample** — use the packet simulation feature to inspect a sample from the test data.
4. **Review the prediction** — examine whether the model classifies the sample as benign or DDoS.
5. **Explore an explanation** — optionally use the Grok integration to obtain a natural-language explanation.

## Technology stack

| Component | Technology |
|---|---|
| Language | Python |
| Machine learning | scikit-learn, Random Forest |
| Data processing | pandas, NumPy |
| Interface | Streamlit |
| AI-assisted explanations | Grok API, optional |
| Dataset | CIC-IDS2017 subset |

## Project structure

The main files documented in this repository are:

```text
AI-Network-Intrusion-Detection/
├── app.py
├── requirements.txt
├── Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv
└── README.md
```

## Getting started

### Prerequisites

- Python 3.8 or newer
- pip
- Git

### 1. Clone the repository

```bash
git clone https://github.com/KaizokuSuyash/AI-Network-Intrusion-Detection.git
cd AI-Network-Intrusion-Detection
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Linux:

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Start the application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal if the browser does not open automatically.

> The commands above assume the repository contains the documented entry point and dependency file. The application has not been independently tested as part of this README update.

## Dataset

The project uses `Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv`, a subset associated with the CIC-IDS2017 intrusion detection dataset.

The dataset contains network traffic records used to explore benign and DDoS classification. Its presence in the repository does not imply that the model has been validated against all attack types or real-time production traffic.

Dataset reference: [Canadian Institute for Cybersecurity — CIC-IDS2017](https://www.unb.ca/cic/datasets/ids-2017.html)

## Configuration and API usage

The Grok integration is optional and is intended to provide explanations of model predictions.

- Keep API keys out of source code and Git commits.
- Supply credentials through the application's supported runtime input or a local environment configuration.
- Do not share API keys in screenshots, logs, or public issue reports.
- The application should remain usable without the optional integration only to the extent supported by its implementation.

## Scope and limitations

This is an academic project and an environment for experimenting with machine learning-based network traffic classification.

- A model prediction is not a guarantee that traffic is malicious or benign.
- Results depend on the dataset, selected features, preprocessing, and training procedure.
- Performance on a dataset does not establish effectiveness on unseen real-world network traffic.
- LLM-generated explanations may be incomplete or incorrect and should not be treated as security evidence.
- The project should not be considered a production-ready intrusion detection or prevention system without further validation.

## Possible future improvements

- Add reproducible evaluation metrics and a confusion matrix.
- Document feature preprocessing and the train/test split.
- Add automated tests for data handling and prediction logic.
- Include screenshots of the running application and representative outputs.
- Improve dataset management so large data files do not need to be stored directly in Git history.

These are potential improvements, not features claimed to be implemented.

## Project context

Developed as a university cybersecurity project to explore the intersection of traditional machine learning and LLM-assisted interpretation.

**Author:** [KaizokuSuyash](https://github.com/KaizokuSuyash)

---

*If you use or extend this project, review the dataset's terms and the licenses of its dependencies before redistribution.*
