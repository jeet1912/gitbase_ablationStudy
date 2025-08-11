# Comparative Analysis: Traditional Fine-tuning vs. LoRA for Microsoft's GIT-Base 

This project performs a systematic comparison of **Traditional Fine-tuning** and **Low-Rank Adaptation (LoRA)** for large language models on downstream classification tasks.
 It benchmarks performance, memory, and computational efficiency across tasks and model scales.

This repository contains code and data for fine-tuning vision-language models on the MIMIC-CXR dataset using different training strategies including full fine-tuning, LoRA (Low-Rank Adaptation), and ablation studies.

# Project Structure
📁 code/

Contains the main implementation files for different fine-tuning approaches:

mimic_cxr.ipynb - Main notebook for MIMIC-CXR dataset processing and model training
mimic_cxr_ablation.ipynb - Ablation study experiments comparing different model components
mimic_cxr_fft.ipynb - Full Fine-Tuning (FFT) implementation and experiments

📁 comparisiondiagrams/

Visualization and comparison materials:

mimic_cxr_comparisionCharts_L... - Comparison charts and diagrams for different training methods and results

📁 data/

Dataset files and data splits:

sampled_5000_per_label.csv - Balanced dataset with 5000 samples per label for training
test_split.csv - Test dataset split for final evaluation
train_split.csv - Training dataset split
val_split.csv - Validation dataset split for model selection

📁 fftresults/

Full Fine-Tuning experiment results:

fftTest_target_modules_ablation... - Test results from FFT target modules ablation study
ffttrain_target_modules_ablatio... - Training results from FFT target modules ablation study

📁 loraResults/

LoRA (Low-Rank Adaptation) experiment results:

lora_target_modules_ablation_r... - Results from LoRA target modules ablation experiments

Getting Started

Data Preparation: Use the CSV files in the data/ folder to load the MIMIC-CXR dataset splits
Model Training:

For full fine-tuning: Run mimic_cxr_fft.ipynb
For LoRA training: Use mimic_cxr.ipynb with LoRA configurations
For ablation studies: Execute mimic_cxr_ablation.ipynb


Results Analysis: Check the respective results folders (fftresults/ and loraResults/) for experiment outputs
Visualization: Use files in comparisiondiagrams/ to generate comparison charts

Experiment Types

Full Fine-Tuning (FFT): Complete model parameter updating
LoRA: Efficient fine-tuning using low-rank matrix decomposition
Ablation Studies: Systematic analysis of different model components and target modules

# Dataset Information
The project uses the MIMIC-CXR dataset with a balanced sampling approach (5000 samples per label) and standard train/validation/test splits for robust evaluation.

