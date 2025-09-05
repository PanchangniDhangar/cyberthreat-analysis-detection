# Cyber Security Traffic Analysis & IDS

[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://www.python.org/)    
[![Pandas](https://img.shields.io/badge/Pandas-latest-blue)](https://pandas.pydata.org/)      
[![Matplotlib](https://img.shields.io/badge/Matplotlib-latest-orange)](https://matplotlib.org/)     
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)  

## Overview
The Cyber Security Traffic Analysis project performs exploratory data analysis (EDA), anomaly detection, and supervised classification on network traffic logs. It provides insights into:

- Network traffic patterns and volumes  
- Suspicious vs normal traffic distribution  
- Top source countries and destination ports  
- Anomaly detection using Isolation Forest  
- Supervised classification with Random Forest for heuristic suspicious traffic detection  
- Feature importance and precision-recall analysis  

The project is built using Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, and XGBoost.

## Features
- **Traffic Summary & EDA:** Distribution of traffic volumes, top sources/destinations, protocol breakdown  
- **Anomaly Detection:** Isolation Forest-based unsupervised anomaly scoring and visualization  
- **Supervised IDS Classification:** Random Forest classifier for predicting suspicious traffic  
- **Visualizations:** PCA projections, confusion matrix, feature importance, precision-recall curves  
- **Inline Analysis:** All figures are generated within the notebook for comprehensive insight  

## Installation
Clone the repository:

```bash
git clone git@github.com:PanchangniDhangar/cyberthreat-analysis-detection.git
cd cyberthreat-analysis-detection
```
Install dependencies:

```bash
pip install -r requirements.txt
```
### Required Packages
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- openpyxl / xlsxwriter

### Usage
Ensure your dataset `CloudWatch_Traffic_Web_Attack.csv` is in the project directory or in one of the following paths:

- `/mnt/data/CloudWatch_Traffic_Web_Attack.csv`
- `/content/CloudWatch_Traffic_Web_Attack.csv`
- `/content/drive/MyDrive/CloudWatch_Traffic_Web_Attack.csv`

Run the notebook:

```bash
jupyter notebook Cyber_Security_Traffic_Analysis.ipynb
```
## Data
`CloudWatch_Traffic_Web_Attack.csv` contains network traffic logs with columns such as:

- `src_ip`, `dst_ip`: Source and destination IP addresses  
- `src_ip_country_code`: Source country  
- `dst_port`: Destination port  
- `bytes_in`, `bytes_out`: Traffic volume  
- `protocol`: Protocol type  
- `rule_names`, `detection_types`, `observation_name`: Detection rule or label information  
- `is_suspicious`: Optional labeled suspicious traffic (0/1)  
- `creation_time`, `end_time`, `time`: Timestamp columns  

The notebook handles normalization, cleaning, label heuristics, and feature aggregation.

## Visualizations
The notebook produces:

- Traffic volume distributions (`bytes_in`, `bytes_out`)  
- Top source countries and destination ports  
- Traffic type distribution (suspicious vs non-suspicious)  
- PCA projection of traffic features  
- Anomaly score distribution and top anomalies  
- Precision-recall vs threshold, cumulative feature importance  
- Confusion matrix and class balance for supervised IDS  

All figures are generated inline for analysis.

## Screenshots
<img width="861" height="473" alt="output" src="https://github.com/user-attachments/assets/940f749e-b4e6-4667-9fc7-ac5c32a1deb8" />
<img width="842" height="396" alt="3" src="https://github.com/user-attachments/assets/2d36da92-b854-47df-a81d-bdd28c4bacd6" />
<img width="833" height="396" alt="2" src="https://github.com/user-attachments/assets/0a5f5ac0-9e12-4c8d-af33-a1ac969aa227" />
<img width="451" height="396" alt="4" src="https://github.com/user-attachments/assets/9ad20ddf-c850-4f9d-b6cc-bc73ca8a327c" />

## License
This project is licensed under the MIT License.

## Contributing
Contributions are welcome! Please submit pull requests or open issues for bugs, feature requests, or improvements.

## Contact
For any questions or support, reach out to Panchangni at panchangnidhangar@gmail.com.
