# KERNEL-DENSITY-ESTIMATION-BASED-DEFENSE-AGAINST-MODEL-POISONING-IN-FEDERATED-LEARNING
A Kernel Density Estimation (KDE)–based defense for federated learning that detects and mitigates model poisoning attacks. Protects the global model by identifying anomalous updates from malicious clients, ensuring secure and robust collaborative training across multiple participants.

Project Overview

This project leverages Artificial Intelligence (AI) in federated learning to build robust models resistant to model poisoning attacks. Using Convolutional Neural Networks (CNNs) and Kernel Density Estimation (KDE), the system trains AI models collaboratively across clients while identifying malicious updates to protect the global model.

AI Highlights
1. Deep Learning with CNNs: Trains AI models on MNIST to classify handwritten digits.
2. Federated Learning: Multiple clients contribute to a global model without sharing raw data.
3. Adversarial Defense: Uses KDE-based anomaly detection to prevent poisoned model updates from degrading AI performance.
4. Visualization: AI-driven metrics show the effectiveness of defense in terms of accuracy and model size.

Repository Structure
KDE/
├── README.md # Project overview and instructions

├── requirements.txt # Python dependencies

├── Main.py # Main AI client script

├── Server.py # Server-side script for AI defense

└── Dataset/ # Folder for mnist.csv (user must add)

Dataset
Requires MNIST dataset in CSV format (mnist.csv).
Place the CSV in a folder named Dataset at the root of the repo.
The AI models in the project are trained on this dataset.
Download link: [Kaggle MNIST CSV](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv) 

Setup
Clone the repository:
git clone <repository-url>

Install dependencies:
pip install -r requirements.txt

Running the Project - 
Start the server: python Server.py

Start the client GUI: python Main.py

In the GUI, follow this workflow:

1. Upload MNIST Dataset → Load data for AI model training
2. Preprocess Dataset → Normalize and split data
3. Upload Genuine Model to Server → Train and send AI model
4. Upload Poison Model to Server → Train poisoned AI model for testing defense
5. Propose KDE & No Defence Accuracy → Compare AI performance with and without KDE defense
6. Extension Model Size Graph → Visualize compression effect on AI model

Notes:
The following files are automatically generated when you run the project:
cnn_weights.hdf5 → Trained genuine CNN weights
poison_weights.hdf5 → Trained poisoned CNN weights
poison_history.pckl → Training history of the poisoned model
Ensure the server is running before uploading models.

→ The system demonstrates how AI can be secured in collaborative, multi-client learning environments.
