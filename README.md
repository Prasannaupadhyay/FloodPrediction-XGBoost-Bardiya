FloodPrediction-XGBoost-Bardiya
This repository contains the code and documentation for a flood prediction system developed for the Bardiya region of Nepal. The system leverages rainfall data from NASA's IMERG dataset, covering the monsoon season from June 1 to August 31, 2023, to forecast flood events. It utilizes the XGBoost algorithm implemented across three configurations: single-thread CPU, multi-thread CPU, and GPU acceleration, enabling a comparative analysis of training time, accuracy, and resource efficiency.

Features
Data Preprocessing: Includes feature engineering (rolling sums, lag features, temporal and statistical metrics) and synthetic flood label generation based on rainfall thresholds.
Model Training: Employs XGBoost with parallel computing techniques to optimize performance.
Evaluation: Achieves up to 98% accuracy and an AUC of 0.9970, with the multi-thread CPU configuration offering the best efficiency.
Analysis: Investigates potential data leakage from synthetic labels and suggests mitigation strategies.
Installation
Clone the repository: git clone https://github.com/your-username/FloodPrediction-XGBoost-Bardiya.git
Install dependencies: pip install -r requirements.txt (create a requirements.txt file with pandas, xgboost, matplotlib, seaborn, numpy, etc.).
Ensure dataset bardiya_rainfall_2023_06_08.csv is in the root directory.
Usage
Run the main script: python main.py (create a main.py file to orchestrate data loading, preprocessing, and model training).

Results
CPU Parallel: 0.1488s, AUC 0.9963, Efficiency 6.6967
CPU Single: 0.1640s, AUC 0.9963, Efficiency 6.0760
GPU: 0.3474s, AUC 0.9970, Efficiency 2.8697
Future Work
Integrate topographic and hydrological data.
Validate with real flood records.
Enhance feature selection to reduce leakage.
Contributions
Feel free to fork, improve, or submit issues/pull requests. Contributions are welcome!
