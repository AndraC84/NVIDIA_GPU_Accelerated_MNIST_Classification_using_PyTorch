GPU Capstone Project – MNIST Image Classification with PyTorch

Overview

This project was developed as the final Capstone Project for the CUDA at Scale for the Enterprise specialization.

The objective is to demonstrate the use of GPU acceleration for deep learning by training and evaluating a neural network on the MNIST handwritten digit dataset using PyTorch. The project compares CPU and GPU execution times while maintaining high classification accuracy.




Project Objectives

- Train a neural network to classify handwritten digits from the MNIST dataset.
- Compare training performance on CPU and GPU.
- Evaluate model accuracy on unseen test data.
- Visualize predictions and the confusion matrix.
- Save the trained model for future inference.




Technologies Used

- Python 3
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab
- NVIDIA CUDA GPU




Dataset

The project uses the MNIST Handwritten Digits dataset provided by the "torchvision.datasets" package.

The dataset contains:

- 60,000 training images
- 10,000 testing images
- Grayscale images (28 × 28 pixels)
- 10 classes (digits 0–9)

The dataset is downloaded automatically when the notebook is executed.




Neural Network Architecture

The implemented neural network is a simple feed-forward classifier composed of fully connected layers with ReLU activation functions.

The model was trained using:

- CrossEntropyLoss
- Adam Optimizer
- Mini-batch training with DataLoader




GPU Acceleration

The notebook automatically detects whether CUDA is available.

If an NVIDIA GPU is detected, the model and data are transferred to the GPU for accelerated training. Otherwise, execution automatically falls back to the CPU.

This allows a direct comparison between CPU and GPU execution times.




Project Outputs

After execution, the following files are generated:

- "results.csv" – Performance metrics
- "predictions.png" – Sample predictions
- "confusion_matrix.png" – Confusion matrix visualization
- "mnist_gpu_model.pth" – Trained PyTorch model




Repository Structure

project/
│
├── mnist_gpu.ipynb
├── README.md
├── requirements.txt
├── results.csv
├── predictions.png
├── confusion_matrix.png
├── mnist_gpu_model.pth
├── presentation.pdf
└── screenshots/





Installation

Install the required packages:

pip install -r requirements.txt




Running the Project

Open the notebook:

mnist_gpu.ipynb

Execute all cells in order.

The notebook will:

1. Detect GPU availability.
2. Download the MNIST dataset.
3. Train the neural network.
4. Evaluate model performance.
5. Compare CPU and GPU execution times.
6. Generate output files.
7. Save the trained model.



Results

The project demonstrates that GPU acceleration significantly reduces training time while maintaining high classification accuracy.

Performance metrics, prediction samples, and the confusion matrix are automatically generated and included in this repository.



Learning Outcomes

This project demonstrates practical knowledge of:

- GPU-accelerated deep learning
- CUDA-enabled execution with PyTorch
- Neural network training and evaluation
- Performance benchmarking
- Data visualization
- Model serialization and reuse



Author

Capstone Project developed as part of the CUDA at Scale for the Enterprise specialization using Python, PyTorch, and NVIDIA GPU acceleration.

