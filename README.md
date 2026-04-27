# Adaptive Threat Modeling in AI-Enabled Cyber-Physical Systems
**A Data-Driven Framework for Predictive Security Assurance**

> **Authors:** Hussain Haidary (23UCS596) & Ishwi Dhanuka (23UCS599)  
> **Advisor:** Dr. Ashish Kumar Dwivedi  
> **Institution:** The LNM Institute of Information Technology (LNMIIT), Jaipur  

---

## Project Description
In the age of Industry 4.0, the intersection of IT and OT technologies has made CPS vulnerable to complex cyber-attacks. Static intrusion detection systems based on signature recognition have proven insufficient in detecting sophisticated threats in today's heterogeneous and ever-evolving industrial network environments.

This research proposes a Predictive Security Assurance Framework designed specifically for the industrial edge. By leveraging spatiotemporal features, our hybrid AI engine effectively identifies volumetric assaults while exposing any hidden stealthy attacks (e.g., Man-In-The-Middle, Fingerprinting attacks).

### Innovations:
* **Spatiotemporal Design:** Our proprietary hybrid **1D-CNN & LSTM** model captures spatial anomalies at the moment and slow, subtle behavior drifts over time.
* **Dynamic Learning Process:** An adaptive learning loop identifies low-confidence predictions as new zero-day attacks, storing them for future weight update training.
* **Real-Time Edge Deployment Capability:** Our FP32 PyTorch framework is automatically optimized to 8-bit integers, delivering a **0.12 MB model size (4x compression)** suitable for PLC inference within microseconds.
---

## Dataset: Edge-IIoTset
The model has been trained and tested on the extremely realistic **Edge-IIoTset (2022)** dataset, which includes telemetry data collected from a 7-layer CPS testbed.
* **Attributes:** 61 diverse attributes (extended to 82 through one-hot encoding) including various protocols such as MQTT, Modbus, and HTTP.
* **Labels:** 14 categories of attacks + 1 category of Benign (Normal).

**Data Availability Note:** Due to restrictions imposed by GitHub on file size, the actual dataset is not available in this repository. You may obtain the complete dataset from Kaggle.
---

## Repository Structure

Code output
Generated README.txt

```text
├── .gitignore
├── README.md
├── EDA_plots/
│   ├── class_distribution.png  
|   └── tsne_clusters.png
├── Model_architecture/
|   └── PSCTM.png
├── Model_report/
│   ├── confusion_matrix.png  
|   └── inference_report_readable.txt            
├── Report/
│   └── CTMAS.pdf
├── notebooks/
|   └── edgeiiot.ipynb 
└── quantized_model/
    └── adaptive_edge_engine.pt  
```
---
## 🚀 Getting Started

### Prerequisites
* Python 3.8+
* PyTorch
* Pandas, NumPy, Scikit-Learn
* Matplotlib, Seaborn

### Installation & Execution
1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/Adaptive-Threat-Modeling-CPS.git](https://github.com/YOUR_USERNAME/Adaptive-Threat-Modeling-CPS.git)
   cd Adaptive-Threat-Modeling-CPS```
2. Download the Edge-IIoTset from Kaggle and place the CSV files in a local /data directory.
3. Open notebooks/edgeiiot.ipynb in Jupyter or Google Colab.
4. Run the notebook sequentially to reproduce the Exploratory Data Analysis (t-SNE), train the hybrid CNN-LSTM engine, and execute the simulated Adaptive Edge Inference loop.
---
## Performance Highlights
- Weighted F1-Score: 1.00
- Macro F1-Score: 0.98 across all 15 highly imbalanced classes.
- Stealth Detection: 0.92 Recall on camouflaged MITM and Fingerprinting attacks.
---
## Future Work
Our research roadmap includes expanding this framework with Federated Learning for decentralized threat intelligence, Blockchain & Fully Homomorphic Encryption (FHE) to secure gradient updates against poisoning, and Explainable AI (XAI) layers (SHAP/LIME) to provide plant operators with transparent, human-readable threat rationales.
