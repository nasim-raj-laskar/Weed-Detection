# Weed Detection

## Dataset

**DeepWeeds Dataset**: 17,509 RGB images (256×256px) across 9 classes with significant class imbalance (Snake Weed: 42.9%, others: 5.8-10.9%).

**Classes**: Chinee Apple, Lantana, Parkinsonia, Parthenium, Prickly Pear, Rubber Vine, Siam Weed, Snake Weed, Negative.

## Model Used
### 1. MobileNetV2 + Attention

### Architecture
- **Backbone**: MobileNetV2 (ImageNet pre-trained)
- **Enhancement**: Spatial/channel attention mechanisms
- **Input**: 224×224×3
- **Parameters**: 3.8M (1.2M trainable)
- **Model Size**: 42 MB

### Performance Metrics
- **Training Accuracy**: 96.31%
- **Validation Accuracy**: 86.81%
- **Test Accuracy**:82.27%
- **Test Loss**:72.63%
- **FLOPs**: 585M

### Training Configuration
- **Optimizer**: Adam (lr=0.001)
- **Batch Size**: 32
- **Epochs**: 100
- **Loss**: Categorical Crossentropy
- **Regularization**: Dropout (0.3), L2 (1e-4)
- **Strategy**: 3-phase progressive unfreezing

