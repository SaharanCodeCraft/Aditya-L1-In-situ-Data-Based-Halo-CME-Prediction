📖 Overview

This project was developed as part of the Bharatiya Antariksh Hackathon 2025 (ISRO).
The objective is to predict Halo Coronal Mass Ejections (CMEs) in real time using in-situ particle and plasma data from the SWIS-ASPEX payload onboard Aditya-L1.

Unlike traditional CME detection methods that rely on remote imaging, this approach leverages time-series solar wind parameters (proton density, bulk speed, temperature, dynamic pressure, etc.) to identify precursor signatures of Halo CMEs, providing earlier and more reliable warnings for space weather preparedness.

🚀 Key Features

Machine Learning Pipeline: Random Forest classifier trained on 1M+ labeled samples.

Data Preprocessing:

Unified multi-source data into HDF5 format.

Rolling-window feature engineering (gradients, averages, dynamic pressure).

Anomaly handling and time-series continuity fixes.

Performance:

~80% overall classification accuracy.

High reliability in detecting non-CME quiet periods (Recall: 0.96).

Demonstrated potential for 30–60 min early warnings of Earth-directed CMEs.

Tech Stack

Languages: Python

Libraries: NumPy, pandas, Scikit-learn, h5py

ML Model: Random Forest

Data Handling: HDF5 (time-aligned streams), rolling-window features, anomaly handling

Project Structure:
├── data/                # Preprocessed datasets / sample inputs
├── notebooks/           # Jupyter notebooks for experiments & EDA
├── src/                 # Core ML pipeline scripts
│   ├── preprocessing.py # Data cleaning & feature engineering
│   ├── train.py         # Training script (Random Forest model)
│   ├── evaluate.py      # Model evaluation & metrics
│   └── utils.py         # Helper functions
├── results/             # Accuracy reports, metrics, plots
└── README.md            # Project documentation

How to run->

1.Clone the Repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

2.Install Dependencies
pip install -r requirements.txt

3.Run Preprocessing
python src/preprocessing.py

4.Train the Model
python src/train.py

5.Evaluate Results
python src/evaluate.py


Results->

Accuracy: ~80%

Non-CME Recall: 0.96 (very strong at filtering quiet periods)

CME Detection Recall: 0.04 (baseline, with scope for sensitivity improvements)

Weighted F1 Score: 0.72
