## CSE366LAB07

## Objective
To build, train, and evaluate a Convolutional Neural Network (CNN) for image classification using the Caltech-101 dataset. Students will also learn to apply Explainable AI (XAI) techniques, specifically Grad-CAM, to visualize model decision-making.

## Key Observations:
* Top-5 Accuracy: EfficientNet-B0 achieved the highest Top-5 accuracy (97%), followed by ResNet50 (95%) and VGG19 (92%).
* Class-Specific Performance: Classes like "Faces," "Leopards," and "Motorbikes" achieved near-perfect accuracy across all models, while classes like "Ant," "Lobster," and "Platypus" struggled due to limited samples.
* Validation Loss: EfficientNet-B0 had the lowest validation loss (0.5366), indicating better generalization compared to VGG19 and ResNet50.
* Training Time: ResNet50 took significantly longer to train.


## Grad-CAM Insights
### Model-Specific Analysis:
* VGG19: Focuses on object contours and textures. For example, in car images, it highlights wheels and body shape.
* ResNet50: Attends central object regions. For instance, for animals, it focuses on the head/body rather than the background.
* EfficientNet-B0: Shows scattered attention patterns, often highlighting unexpected regions (e.g., background elements).
### Common Patterns:
* All models struggle with small objects.
* Background elements sometimes receive more attention than foreground objects.
* Best performance observed on high-contrast, centered objects.
