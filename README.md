# Neural Network Backpropagation Implementation

## Overview
A complete implementation of a 3-layer neural network autoencoder (8-3-8 architecture) built from scratch using NumPy. The network learns to reproduce 8 one-hot encoded vectors through dimensionality compression, demonstrating custom backpropagation and gradient descent optimization.

## Architecture
- **Input Layer:** 8 neurons (one-hot encoded vectors)
- **Hidden Layer:** 3 neurons with sigmoid activation (compression bottleneck)
- **Output Layer:** 8 neurons with sigmoid activation (reconstruction)
- **Loss Function:** Binary Cross-Entropy (BCE)
- **Optimization:** Gradient Descent with early stopping

## Key Features
- **Pure NumPy implementation** - No high-level ML frameworks
- **Fully vectorized operations** - Efficient matrix computations
- **Custom backpropagation** - Chain rule implementation from first principles
- **Early stopping** - Automatic termination at 100% accuracy
- **Comprehensive visualization** - 3D hidden space representations, weight heatmaps, and training curves
- **Mathematical documentation** - Complete derivation of backpropagation gradients

## Implementation Details

### Training Process
1. **Forward Propagation:** Compute predictions through network layers
2. **Loss Computation:** Binary Cross-Entropy measures reconstruction error
3. **Backpropagation:** Compute gradients using chain rule (∂J/∂W, ∂J/∂b)
4. **Parameter Update:** Gradient descent (θ = θ - α·∇θ)
5. **Early Stopping:** Halt when 100% classification accuracy achieved

### Hyperparameters
- Learning rate: 0.1
- Maximum epochs: 8000
- Weight initialization: Random normal (×0.5)
- Bias initialization: Zeros

## Files
- `backpropagation_implementation.ipynb` - Main implementation notebook
- `Backpropagation_Mathematical_Derivation.md` - Complete mathematical derivation with dimensions
- `Assignment description.md` - Project setup and theoretical background
- `requirements.txt` - Python dependencies (NumPy, Matplotlib)

## Usage
```bash
# Install dependencies
pip install -r requirements.txt

# Run Jupyter notebook
jupyter notebook backpropagation_implementation.ipynb
```

## Results
The network successfully learns the identity function, achieving:
- **Perfect accuracy:** 100% classification on all 8 training examples
- **Rapid convergence:** Typically within 1000-2000 epochs
- **Dimensionality reduction:** 8D → 3D → 8D with zero information loss
- **Unique representations:** Each input mapped to distinct 3D coordinate in hidden space

## Mathematical Insights
- **BCE + Sigmoid simplification:** Output gradient reduces to elegant form (A₂ - y)
- **Information bottleneck:** 3 continuous values sufficient for 8 discrete classes (exceeds theoretical log₂(8) = 3 bits)
- **Weight interpretation:** W₁ encodes, W₂ decodes the compressed representation
- **Hidden space structure:** 8 training examples linearly separable in 3D space

## Visualizations
The notebook generates comprehensive analyses:
- 3D scatter plot of hidden layer activations
- Weight matrix heatmaps (W₁, W₂)
- Training loss convergence curves
- Activation pattern heatmaps
- 2D projections of hidden space

## Author
Implemented as part of Advanced Computational and Machine Learning coursework.

## License
Educational use only.
