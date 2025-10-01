# AIRL Internship Coding Assignment

## Repository Structure
- `q1.ipynb` - Vision Transformer implementation for CIFAR-10 classification
- `q2.ipynb` - Text-driven image segmentation using SAM 2
- `README.md` - This file

## Q1: Vision Transformer on CIFAR-10

### How to Run in Colab
1. Open `q1.ipynb` in Google Colab
2. Enable GPU runtime (Runtime → Change runtime type → GPU)
3. Run all cells sequentially
4. Model will train and display test accuracy

### Best Model Configuration
- Image Size: 32x32
- Patch Size: 4x4
- Layers: 8
- Hidden Dimension: 256
- MLP Size: 512
- Heads: 8
- Dropout: 0.1
- Optimizer: AdamW
- Learning Rate: 0.001
- Augmentations: RandomCrop, HorizontalFlip, ColorJitter

### Results
| Model | Test Accuracy |
|-------|---------------|
| ViT   |     94.2%     |

## Q2: Text-Driven Image Segmentation with SAM 2

### How to Run in Colab
1. Open `q2.ipynb` in Google Colab
2. Run all cells (includes automatic installation)
3. Upload an image when prompted
4. Enter text prompt for segmentation
5. View segmented output with mask overlay

### Pipeline Description
1. Load input image and text prompt
2. Use GroundingDINO for text-to-bounding box conversion
3. Pass bounding boxes to SAM 2 for mask generation
4. Overlay segmentation mask on original image

### Limitations
- Dependent on text prompt clarity and specificity
- May struggle with fine details or transparent objects
- Performance varies with object size and background complexity
