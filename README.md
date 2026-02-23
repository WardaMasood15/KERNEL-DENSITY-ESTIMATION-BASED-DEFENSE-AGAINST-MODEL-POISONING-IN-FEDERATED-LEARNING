# KDE-Based Defense in Federated Learning 🔐

A *Kernel Density Estimation (KDE)–based defense mechanism* for Federated Learning that detects and mitigates model poisoning attacks. The system protects the global model by identifying anomalous updates from malicious clients, ensuring secure and robust collaborative training across multiple participants.

---

## Project Overview

This project leverages *Artificial Intelligence (AI)* and *Federated Learning (FL)* to build deep learning models that are resilient to model poisoning attacks.

Using *Convolutional Neural Networks (CNNs)* and *Kernel Density Estimation (KDE)*, the system:

* Trains models collaboratively across multiple clients
* Detects malicious or poisoned model updates
* Prevents adversarial updates from degrading global model performance
* Maintains accuracy and robustness in distributed environments

The implementation demonstrates how AI systems can be secured in collaborative, multi-client learning environments.

---

## AI Highlights

* *Deep Learning with CNNs*
  Trains CNN models on the MNIST dataset to classify handwritten digits.

* *Federated Learning Architecture*
  Multiple clients train locally and send model updates to a central server without sharing raw data.

* *KDE-Based Adversarial Defense*
  Uses Kernel Density Estimation to detect anomalous (poisoned) client updates before aggregation.

* *Attack Simulation*
  Includes poisoned model training to test robustness of the defense mechanism.

* *Visualization & Metrics*
  Displays accuracy comparison between:

  * No Defense
  * KDE Defense
    Also visualizes model size and performance trends.

---

## Repository Structure


KDE/
├── README.md              # Project overview and instructions
├── requirements.txt       # Python dependencies
├── Main.py                # Client-side GUI application
├── Server.py              # Server-side script implementing KDE defense
├── Dataset/
│   └── mnist.csv          # MNIST dataset in CSV format (user must add)
├── cnn_weights.hdf5       # Generated genuine CNN weights (auto-created)
├── poison_weights.hdf5    # Generated poisoned CNN weights (auto-created)
├── poison_history.pckl    # Training history of poisoned model (auto-created)
└── graphs/                # Accuracy and model size visualizations (generated)


---

## Dataset

This project requires the *MNIST dataset in CSV format (mnist.csv)*.

### Dataset Setup:

1. Download MNIST dataset in CSV format from: [Kaggle MNIST CSV](https://www.kaggle.com/oddrationale/mnist-in-csv)  
2. Create a folder named:


Dataset/


3. Place mnist.csv inside the Dataset/ folder at the root of the repository.

The CNN models in this project are trained using this dataset.

---

## Requirements

Install the required dependencies:

bash
pip install -r requirements.txt


Typical dependencies include:

* TensorFlow / Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Pickle

---

## Setup Instructions

### 1️⃣ Clone the Repository

bash
git clone https://github.com/yourusername/KDE.git
cd KDE


### 2️⃣ Install Dependencies

bash
pip install -r requirements.txt


---

## Running the Project

### Step 1: Start the Server

bash
python Server.py


The server initializes the global model and activates the KDE-based defense mechanism.

---

### Step 2: Start the Client GUI

Open a new terminal and run:

bash
python Main.py


---

## GUI Workflow

Follow this sequence inside the client interface:

1. *Upload MNIST Dataset*
   Load data for AI model training.

2. *Preprocess Dataset*
   Normalize and split dataset for CNN training.

3. *Upload Genuine Model to Server*
   Train and send legitimate model updates.

4. *Upload Poison Model to Server*
   Train a poisoned model to simulate adversarial attack.

5. *Propose KDE & No Defense Accuracy*
   Compare model performance:

   * With KDE defense
   * Without defense

6. *Extension Model Size Graph*
   Visualize the compression and size comparison of models.

---

## Automatically Generated Files

The following files are created automatically when running the project:

* cnn_weights.hdf5 → Trained genuine CNN model weights
* poison_weights.hdf5 → Trained poisoned CNN model weights
* poison_history.pckl → Training history of poisoned model

⚠️ Ensure the server is running before uploading models from the client GUI.

---

## Security Demonstration

This project demonstrates:

* How model poisoning attacks affect federated learning
* How KDE can detect anomalous updates
* How defensive aggregation preserves global model integrity
* How AI systems can be secured in distributed environments
