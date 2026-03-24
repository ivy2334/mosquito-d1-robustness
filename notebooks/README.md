# Notebooks Overview

This folder contains all Jupyter notebooks used in the mosquito classification robustness project. The notebooks are designed to be executed sequentially for reproducibility and clarity.

---

## Notebook Summary

1. **00_setup_and_config.ipynb**
   - Mounts Google Drive and sets up paths.
   - Loads configuration file (`config.yaml`) and installs dependencies.

2. **01_data_loading_and_split.ipynb**
   - Unzips dataset and explores training/testing images.
   - Defines data transformations, splits training data into train/validation sets.

3. **02_model_setup.ipynb**
   - Creates deterministic PyTorch `DataLoader` objects.
   - Ensures reproducibility via fixed seeds and worker initialisation.
  
     
4. **03_training.ipynb**
   - Defines architectures: EfficientNet, ResNet, Swin Transformer.
   - Freezes backbone layers, trains only classifier head.
   - Saves trained models for evaluation.

5. **04_noisy.ipynb**
   - Adds Gaussian noise at test time.
   - Evaluates models on noisy inputs and records accuracy per noise level.

6. **05_embeddings.ipynb**
   - Extracts embeddings from each model.
   - Computes cosine similarity between clean and noisy embeddings to measure stability.

7. **06_metricval.ipynb**
   - Computes and visualises both cosine similarity and L2 drift of embeddings.
   - Plots stability metrics vs noise levels for all models.

8. **07_final.ipynb**
   - Visualises correlation between embedding stability and accuracy.
   - Plots trends and computes Pearson correlation coefficients.

---

## Notes

- All experiments use consistent seeds for deterministic results.
- Embedding stability and accuracy correlations provide insight beyond standard evaluation metrics.
