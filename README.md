# Mosquito Species Classification – Robustness Analysis

This project explores the robustness of deep learning models for mosquito species classification under input noise perturbations. Specifically, we analyse how Gaussian noise affects model predictions and feature representations (embeddings) across three architectures:

- **EfficientNet (CNN)**
- **ResNet (CNN)**
- **Swin Transformer**

While model accuracy is commonly reported, this project emphasises *embedding stability*, i.e., how the internal representations shift when inputs are perturbed, and how this correlates with performance.

---


- **notebooks/** – Contains 8 Jupyter notebooks detailing environment setup, data preprocessing, model training, noise robustness experiments, and embedding analysis.  
- **configs/** – Holds `config.yaml`, which defines image sizes, batch sizes, learning rates, noise levels, and normalization constants.  


---

## Key Highlights

- Gaussian noise is applied at test time to evaluate model robustness.
- Embeddings are extracted before classification layers and compared using cosine similarity.
- Accuracy and embedding stability are visualised across noise levels.
- Correlations between embedding drift and performance provide insights into architectural robustness.

---

## Notes

- Datasets (`images.zip`) and pretrained models are not included due to size constraints; instructions to generate them are provided in the notebooks.
- The project ensures reproducibility using fixed seeds and deterministic data loaders.
