# Comprehensive Intelligent Traffic Analysis System 🚦🚙
This repository hosts a state-of-the-art, multi-domain Deep Learning project focused on intelligent traffic analysis, autonomous decision-making, and anomaly detection. By fusing cutting-edge Computer Vision, Natural Language Processing (NLP), Reinforcement Learning (RL), and Time-Series Forecasting, this project provides a holistic approach to understanding, predicting, and optimizing urban traffic environments.

## Key Features & Methodologies

Our system is broken down into several specialized AI sub-systems:

### 1.Computer Vision & Object Tracking (YOLOv8 & DeepSORT)
- **Object Detection**: Utilizing pre-trained YOLOv8 and YOLO26s models to accurately detect vehicles, pedestrians, and traffic infrastructure in high-resolution video feeds.
- **UAV Integration**: Support for the UAVDT (Unmanned Aerial Vehicle Benchmark Object Detection and Tracking) dataset, enabling the system to process drone-captured footage for aerial traffic surveillance.
- **Tracking**: Continuous vehicle tracking across frames to extract trajectories and movement patterns.

### 2.Anomaly Detection (Variational Autoencoders)
- **Unsupervised Learning**: Implementation of a Variational Autoencoder (VAE) to learn the standard distribution of traffic behavior.
- **Dataset Integration**: Evaluated on the standard UCSD Anomaly Dataset (UCSDped2) to accurately flag anomalous behaviors, accidents, or illegal traffic maneuvers without relying on labeled anomaly data.

### 3.Time-Series Forecasting (LSTM Networks)
- **Traffic Flow Prediction**: Utilizing Long Short-Term Memory (LSTM) recurrent neural networks to predict future traffic density and flow based on historical data.
- **PEMS08 Dataset**: Trained and validated on the PEMS08 dataset, a standard benchmark for complex traffic network forecasting.

### 4.Reinforcement Learning for Traffic Control (PPO & SUMO)
- **Intelligent Traffic Lights**: A custom reinforcement learning agent trained using Proximal Policy Optimization (PPO) from the Stable-Baselines3 library.
- **SUMO Integration**: The agent interacts directly with the SUMO (Simulation of Urban MObility) environment to dynamically adjust traffic light phases, significantly reducing vehicle wait times and improving overall throughput compared to static baseline systems.

### 5.Natural Language Processing (BERT)
- **Incident Report Classification**: Fine-tuned BERT (Bidirectional Encoder Representations from Transformers) model for classifying textual data related to traffic incidents (e.g., social media reports, emergency logs) into critical and non-critical categories.

## 📁 Project Structure

- **`notebooks/`**: Core Jupyter Notebooks containing the implementations.
  - `dlproj.ipynb`: Main project integration.
  - `yolo.ipynb`: YOLO implementation for object detection.
  - `vae.ipynb`: Variational Autoencoder (VAE) for anomaly detection.
  - `bert.ipynb`: NLP implementation using BERT.
  - `traffic_rl_sumo.ipynb`: Reinforcement Learning for traffic using SUMO.
- **`data/`**: Ignored by git. Expected to contain raw datasets (uavdt, PEMS08, UCSD) and video files.
- **`models/`**: Ignored by git. Expected to contain `.pt`, `.zip` pre-trained models.
- **`outputs/`**: Ignored by git. Contains tensorboard logs, plots, and tracked results.
- **`configs/`**: Configuration files (e.g., SUMO networks).

*(Note: Data, outputs, and model weight directories are excluded from version control via `.gitignore` to keep the repository lightweight.)*

## 🛠 Setup & Installation

1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd <repo-name>
   ```

2. **Create a virtual environment (recommended):**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Populate Ignored Folders:**
   Ensure you have downloaded the required datasets (UCSD, PEMS08, UAVDT) into the `data/` directory and any base weights into the `models/` directory prior to running the notebooks.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
