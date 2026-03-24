# Configuration Files

This folder contains configuration files for the mosquito classification robustness project.

---

## config.yaml

The configuration file defines all essential hyperparameters and settings required to run the experiments. Key sections:

### 1. Data
```yaml
data:
  image_size: 192
  train_split: 0.8
  test_split: 0.2

normalization:
  mean: [0.485, 0.456, 0.406]
  std:  [0.229, 0.224, 0.225]

normalization:
  mean: [0.485, 0.456, 0.406]
  std:  [0.229, 0.224, 0.225]

model:
  freeze_backbone: true
  train_last_layer_only: true

noise:
  sigmas: [0.0, 0.05, 0.1, 0.15, 0.2]
