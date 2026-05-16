# BigData Architecture

**OpenClassrooms — Data Scientist Path | Project 8** (July – August 2023)

> Note: project deliverables (notebook, presentation) are in French.

## Sector
AgriTech · Food Industry

## Tech Stack
- Jupyter Notebook
- Python: PySpark
- AWS: EC2, S3, EMR

## Keywords
BigData, distributed computing, cloud infrastructure, machine cluster, PySpark

## Context
An AgriTech startup is building a mobile app that identifies fruits from a photo. Once in production, the volume of images to process will grow rapidly, creating new requirements in terms of storage and compute infrastructure that a single machine cannot handle.

## Mission
Design and test a first version of the BigData architecture needed to scale data processing to large volumes, based on an existing notebook left by a former intern.

> The goal of this project is **not** to train a classification model, but to validate that the architecture can handle the preprocessing and feature extraction pipeline at scale.

## Deliverables
- `notebook.ipynb` — PySpark scripts for the full preprocessing pipeline, executable on the cloud cluster
- `presentation.pdf` — presentation slides (in French)

## Methodology

1. **Local validation**
   - Run and validate the PySpark script locally before moving to the cloud:
     - Image data cleaning
     - Feature extraction via transfer learning (MobileNetV2)
     - Dimensionality reduction (PCA)
     - Store transformed data

2. **AWS infrastructure setup**
   - Create AWS account with budget alerts
   - Create an S3 bucket for data storage
   - Configure an EMR cluster

3. **Cloud execution**
   - Launch the EMR cluster
   - Connect to the master node via SSH tunnel
   - Execute the notebook from JupyterHub hosted on the cluster
   - Verify output stored in S3

## Skills
- Identifying and configuring cloud services for a BigData use case
- Parallelising data processing with PySpark
- Setting up and running a managed machine cluster on AWS EMR

## Data Source
[Kaggle — Fruits 360](https://www.kaggle.com/moltean/fruits)
