# Comparative Analysis: Traditional Fine-tuning vs. LoRA for LLMs

This project performs a systematic comparison of **Traditional Fine-tuning** and **Low-Rank Adaptation (LoRA)** for large language models on downstream classification tasks.
 It benchmarks performance, memory, and computational efficiency across tasks and model scales.

---

## Project Structure (this can be enhanced and changed later on based on implementation)

.
├── models/               # Model configurations and checkpoints
├── scripts/              # Training and evaluation scripts
├── lora_utils/           # Custom LoRA utilities (if not using PEFT)
├── results/              # Generated performance logs and plots
├── notebooks/            # Jupyter notebooks for exploration/visualization
├── configs/              # YAML or JSON config files for experiments
├── Dockerfile            # Reproducible environment setup
├── requirements.txt      # Python dependencies
├── run_experiment.py     # Entry point to train/evaluate models
└── README.md             # This file

>  NOTE: This project **does not include a local `data/` folder**. All datasets are accessed via **Google Cloud BigQuery** for scalability and efficiency.

---

## BigQuery Dataset Access

All datasets (e.g., IMDB, SST-2, MNLI, MIMIC-CXR reports) are accessed **directly through BigQuery tables** in **Google Cloud Platform (GCP)**.

### Requirements
- A GCP project with billing enabled
- BigQuery API enabled
- Google Cloud SDK installed or service account credentials
- Python packages:
  pip install google-cloud-bigquery pandas

### Configuration

Set your environment variable or JSON credentials path:
  export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/credentials.json"

Example query (Python):

```python
from google.cloud import bigquery

client = bigquery.Client()
query = "SELECT * FROM `your-project.dataset.imdb_train` LIMIT 1000"
df = client.query(query).to_dataframe()







DataSEt Information fetched via URL: https://physionet.org/content/mimic-cxr/2.0.0/
Chest X-ray Images (DICOM format)
377,110 images from 227,835 radiographic studies
Images are in DICOM format, commonly used in clinical settings
Images are de-identified and cleaned of any burned-in protected health information (PHI)
Some studies include both frontal and lateral images

