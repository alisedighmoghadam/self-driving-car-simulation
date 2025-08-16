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
data/
 ├─ IMG/                 # Collected training images
 │   └─ driving_log.csv  # Driving data

models/
 └─ model.h5             # Trained CNN model

.gitignore               # Git ignore file
README.md                # Project documentation
data_test.ipynb          # Notebook for testing data
environment.yml          # Conda environment setup file
model.ipynb              # Notebook for model building/training
requirements.txt         # Python package dependencies
TestSimulation.py        # load the model and run the program
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

```bash
# 1. Download Anaconda (Nano version) from https://www.anaconda.com/

# 2. Launch the Anaconda shell

# 3. Create the environment from environment.yml
conda create --name .venv --file environment.yml

# 4. Activate the environment (if not auto-activated)
conda activate .venv

# 5. Run the simulation script (loads models/model.h5 and starts server)
python test_simulation.py

# 6. Open the simulator in **Autonomous Mode** and watch the car drive itself.
```

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
