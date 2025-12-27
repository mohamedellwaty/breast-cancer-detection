Authors 
Project Team Members 
Mohamed Eslam Ellwaty 
• Contributions: Gui and data loader optimization 

Adam Mohamed Foda 
• Contributions: Prediction pipeline and transform builder 

Taspih  
• Contributions: Custom CNN model design  

Asseel 
• Contributions: Data preprocessing functions (remove_corrupted_images, split_dataset) 

Toqa  
• Contributions: Training loop, evaluation metrics, and optimization 

Project Overview 
This project implements a deep learning system for classifying breast medical images 
as Benign or Malignant using a custom Convolutional Neural Network (CNN). The system includes both a 
training pipeline and a user-friendly GUI for inference. 

Features 
• Automated Data Pipeline: Preprocessing, corruption removal, and dataset splitting 
• Custom CNN Architecture: Optimized for 50x50 medical images 
• Data Augmentation: Extensive transformations to improve generalization 
• Class Balancing: Weighted sampling for imbalanced datasets 
• User-Friendly GUI: Built with CustomTkinter for easy image classification 
• Model Persistence: Save/load trained models with metadata 
• Performance Metrics: Training/validation/test accuracy and loss tracking 

Data Augmentation 
Training transformations include: 
• Random horizontal/vertical flips (50%) 
• Random rotation (±30°) 
• Random grayscale (25%) 
• Color jitter (brightness, contrast, saturation, hue) 
• Random autocontrast (25%) 
• Normalization (ImageNet statistics) 

Model Architecture 
The custom CNN (CNN_Manual_50) features: 
• Input: 50×50 RGB images 
• Convolutional Layers: 4 conv layers with BatchNorm and ReLU 
• Pooling: Max pooling for spatial downsampling 
• Regularization: Dropout (0.25, 0.5) for overfitting prevention 
• Fully Connected: 512-unit hidden layer 
• Output: 2-class classification (Benign/Malignant) 

Training Configuration 
• Image Size: 50×50 pixels 
• Augmentation: Random flips, rotation, color jitter, grayscale 
• Normalization: ImageNet mean/std 
• Batch Size: 128 
• Optimizer: AdamW with weight decay (1e-4) 
• Learning Rate: 0.001 
• Epochs: 10 
• Loss Function: Cross Entropy with class balancing 

Analysis 
Strengths: 
1. Excellent Convergence: Model improved consistently over all epochs 
2. High Final Accuracy: 88.60% test accuracy is strong for imaging 
3. Good Generalization: Test accuracy (88.60%) matches validation accuracy (88.63%) 
4. No Overfitting: Training and validation metrics remain close 
5. Clean Dataset: No corrupted images detected 

GUI Features 
• Dark/Light Mode: Customizable theme 
• Image Preview: Thumbnail display 
• One-Click Prediction: Instant classification results 
• Confidence Scores: Probability-based predictions 
• Error Handling: User-friendly error messages 
