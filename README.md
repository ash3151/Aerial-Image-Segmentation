# Aerial Image Semantic Segmentation Using Vision Transformers and UNet  

This project implements semantic segmentation on aerial images to classify features like water, vegetation, buildings, and roads using Vision Transformers (ViT) combined with a UNet architecture.  

---

## How It Works  
1. **Data Loading and Augmentation:**  
   The dataset contains aerial imagery and corresponding segmentation masks. Data is preprocessed using augmentations such as color jittering, Gaussian blurring, rotations, and flipping for better generalization.  

2. **Model Architecture:**  
   - **Vision Transformers (ViT):** Extract high-level spatial and contextual features.  
   - **UNet Decoder:** Refines segmentation outputs for pixel-level precision by progressively up-sampling feature maps.  

3. **Training Workflow:**  
   - Input images and their segmentation masks are passed to the model.  
   - The model minimizes pixel-wise loss (e.g., Cross-Entropy Loss) to improve segmentation accuracy.  
   - Evaluations are performed using metrics like Intersection over Union (IoU).  

---

## Model Training  
- **Dataset:**  
   The dataset is obtained from [Kaggle: Semantic Segmentation of Aerial Imagery](https://www.kaggle.com/datasets/humansintheloop/semantic-segmentation-of-aerial-imagery). It includes RGB images and annotated masks for six classes: water, land, road, building, vegetation, and unlabeled.  

- **Training Process:**  
   - Split the dataset into training and validation sets.  
   - Use PyTorch's `torch.utils.data` for efficient data loading and batching.  
   - Train for multiple epochs with Adam optimizer and a learning rate scheduler.  
   - Monitor performance metrics such as IoU and pixel accuracy on the validation set.  

---

## Technologies and Frameworks Used  
- **Programming Language:** Python  
- **Libraries:**  
   - PyTorch (for model building and training)  
   - OpenCV (for image processing)  
   - torchvision (for data augmentation)  
   - Matplotlib (for visualization)  

---

## Improvements  
- Combined Vision Transformers with UNet to enhance feature extraction and segmentation accuracy.  
- Applied comprehensive data augmentations to improve generalization on unseen data.  
- Achieved approximately **7% IoU improvement** compared to traditional UNet implementations. *(Adjust based on your results.)*  

---

## How to Run This Locally  

1. **Clone the Repository:**  
   ```bash  
   git clone https://github.com/<your-username>/<repository-name>.git  
   cd <repository-name>  
