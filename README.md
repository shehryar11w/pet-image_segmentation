# Image Segmentation — U-Net

A **U-Net** built manually from scratch for semantic image segmentation, trained on the **Oxford-IIIT Pet** dataset's trimap masks (background / pet / boundary — 3 classes).

## Contents

| Notebook | Description |
|---|---|
| `model.ipynb` | Full pipeline: loads `OxfordIIITPet` (with segmentation trimaps) via `torchvision`, builds a manual encoder-decoder U-Net (`nn.Module`), trains with a combined Cross-Entropy + Dice loss, evaluates with mean IoU, and visualizes predicted masks against ground truth. |

## Features

- Manually implemented U-Net (encoder/decoder with skip connections)
- Combined **Cross-Entropy + Dice loss**
- **Mean IoU** evaluation metric
- Experiment tracking with Weights & Biases (W&B)
- Prediction visualization against ground-truth masks

## Technologies

- Python
- PyTorch / TorchVision
- Weights & Biases (W&B)
- Matplotlib

## Getting Started

```bash
git clone https://github.com/shehryar11w/carvana-image_segmentation.git
cd carvana-image_segmentation
pip install torch torchvision wandb matplotlib
```

Open `model.ipynb` in Jupyter or VS Code and run. The dataset downloads automatically via `torchvision`.

## Learning Outcomes

- Building an encoder-decoder segmentation network with skip connections from scratch
- Dice loss and combined loss functions for segmentation
- Evaluating segmentation quality with mean IoU

## License

Educational / personal use.
