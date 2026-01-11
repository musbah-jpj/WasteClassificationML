# Resource Efficient Waste Classification for Smart Recycling

## Description
An image-based waste classification system using transfer learning to categorize waste into cardboard, glass, metal, paper, plastic, and trash.

## Models Used
- ResNet18 (transfer learning, training & evaluation)
- MobileNetV2 (lightweight model for deployment)

## Methodology
- Image preprocessing and train + test split
- PyTorch is used to refine pretrained CNNs.
- Accuracy and confusion matrices are used for evaluation.
- Robustness testing under noisy and out-of-distribution inputs

## Results
- GPU inference latency is similar across models although MobileNetV2 reduces the number of parameters by approximately 80% when compared to ResNet18; 
- Because of their visual resemblance, thin plastic materials are often mistaken for paper.
- Thin plastic materials are frequently misclassified as paper due to visual similarity

## Limitations
- The model may struggle with out-of-distribution inputs (e.g., plastic bags, small plastic objects), highlighting dataset bias. 
- A proof can be seen of this in the third sample file, where it predicts Beads, as Paper, instead of Plastic, due to close % match.

## Usage
- The trained MobileNet model can be used to classify new images by loading the saved weights and running inference on input images.
