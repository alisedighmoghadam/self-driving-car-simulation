# Self-Driving Car Simulation

## 📌 Project Overview

This project implements a Convolutional Neural Network (CNN) model to control a self-driving car in a simulation environment.  
The model predicts steering angles from front camera images to keep the vehicle on the road.  
The simulator used is provided by Udacity/Nvidia.

---

## 🚀 Features

- Data collection from simulator (center camera images + steering data)
- Data augmentation (flipping, brightness adjustment, zoom, panning, rotation)
- Image preprocessing (cropping, YUV conversion, resizing, normalization, Gaussian blur)
- CNN model based on Nvidia architecture
- Training and evaluation scripts with loss/accuracy plots
- Testing the trained model in the simulator

---

## 📂 Project Structure

```
project-root/
│── data/                  # Collected images & driving_log.csv
│── src/                   # Python scripts (training, preprocessing, testing)
│── requirements.txt       # Python dependencies
│── README.md              # Project documentation
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash
git clone https://github.com/yourusername/self-driving-car-simulation.git
cd self-driving-car-simulation
```

### 2️⃣ Create virtual environment and install dependencies

#### Mac/Linux

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

#### Windows (PowerShell)

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

#### Windows (Command Prompt)

```cmd
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

✅ **Note:** Make sure the virtual environment is active before running any Python scripts.  
You can check by running:

```bash
which python    # Mac/Linux
where python    # Windows
```

If the path points to `.venv`, it’s active.

---

## 🏎 Running the Project

### **Data Collection**

1. Launch the simulator and select **Training Mode**.
2. Drive along the track (both directions) to collect images and steering data.
3. Save the session — data will be stored as `IMG/` (images) and `driving_log.csv`.

### **Training the Model**

```bash
python src/train.py
```

### **Testing the Model**

1. Run the testing script:

```bash
python src/TestSimulation.py
```

2. Open the simulator in **Autonomous Mode** and watch the car drive itself.

---

## 📦 Dependencies

See [`requirements.txt`](requirements.txt) for the full list.

Main libraries include:

- **TensorFlow/Keras** – Deep learning framework
- **OpenCV & Pillow** – Image processing
- **Pandas & NumPy** – Data handling
- **Matplotlib & Seaborn** – Visualization
- **Flask** – Communication with simulator during testing

---

## 📜 License

This project is for educational purposes under the DPS920 course (Summer 2025).
