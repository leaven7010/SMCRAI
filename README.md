Here's an English version of the `README.md` file for your GitHub project:

```markdown
# Multi-Planar Medical Image Fusion System (Traverse + Sagittal)

This project provides an automated system for lesion detection, classification, and fusion decision-making using traverse and sagittal medical images. It includes object detection, image classification, multi-planar fusion models, and complete prediction examples for both DICOM and JPG formats.

## Project Structure

```
├── tra_objectdetection.ipynb      # Traverse object detection model training (RetinaNet)
├── tra_classification.ipynb       # Traverse classification model training (ConvNeXt)
├── sag.ipynb                      # Sagittal plane model training
├── tra_sag_fusion.ipynb           # Traverse + Sagittal fusion model training (Logistic Regression)
├── demo_dcm.ipynb                 # Single-patient prediction demo for DICOM files
├── demo_jpg.ipynb                 # Single-patient prediction demo for JPG files
└── model_weights/                 # Pre-trained model weights
    ├── retinanet.pth              # Traverse object detection weights
    ├── convnext.pth               # Traverse classification weights
    └── logistic_lasso_3factors_convnext.pkl  # Fusion model weights (Logistic + Lasso)
```

## Model Description

### 1. Traverse Analysis
- **Object Detection**: RetinaNet-based for lesion localization
- **Classification**: ConvNeXt-based for lesion classification

### 2. Sagittal Analysis
- Model architecture detailed in `sag.ipynb` for sagittal feature extraction

### 3. Fusion Model
- Logistic Regression with Lasso regularization integrating:
  - Traverse detection confidence
  - Traverse classification results
  - Sagittal features
- Final output: Combined disease risk prediction

## Requirements

- Python 3.8+
- PyTorch 1.10+
- torchvision
- pandas, numpy, scikit-learn
- opencv-python, matplotlib
- pydicom (for DICOM parsing)
- jupyter


## Important Notes

- DICOM files require the `pydicom` library. Ensure your data follows standard medical imaging formats (e.g., CT or MRI).
- Input image sizes must match the dimensions used during training (see preprocessing sections in each notebook).
- The fusion model expects three input features in the exact order as used during training.

## Citation & Acknowledgments

If this project contributes to your research, please consider citing or acknowledging it.  
(Add paper or project background information as needed)

## Author

- Zhehuang Li / Henan Cancer Hospital 
- Email: zlyylizhehuang4413@zzu.edu.cn

## License

This English version maintains all the technical details while being ready for an international GitHub audience. You can customize the author, license, and repository URL sections as needed.
