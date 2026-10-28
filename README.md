# Mutual Information-Based Functional Connectivity Matrices and CNN-XGB Ensemble for Differentiating Alzheimer's Disease and Frontotemporal Dementia Using EEG Signals

Official repository for the paper: **"Mutual Information-Based Functional Connectivity Matrices and CNN-XGB Ensemble for Differentiating Alzheimer's Disease and Frontotemporal Dementia Using EEG Signals"**.

---

## 📌 Abstract
**Alzheimer's disease (AD)** and **frontotemporal dementia (FTD)** disrupt complex brain functional connectivity networks. Traditional linear methods like spectral coherence or Phase Locking Value (PLV) often miss the irregular, non-linear neural dynamics caused by synaptic degradation. 

This study introduces a novel framework utilizing **Mutual Information (MI)-based Functional Connectivity Matrices (FCMs)** integrated into a **Convolutional Neural Network and Extreme Gradient Boosting (CNN-XGB)** ensemble pipeline. Resting-state multi-channel EEG signals from 88 participants (36 AD, 23 FTD, and 29 Healthy Controls) were evaluated under both **eyes-closed** and **eyes-open** conditions. 

### Key Performance Highlights:
* **Eyes-Closed State:** Reached **97.97% Accuracy**, 97.92% Precision, 97.89% Recall, and 97.91% F1-score (a **15–16% improvement** over a standalone CNN).
* **Eyes-Open State:** Reached **96.47% Accuracy**, 96.23% Precision, 96.22% Recall, and 96.22% F1-score (a **31–37% improvement** over a standalone CNN).
* **Computational Efficiency:** Reduced diagnostic processing and inference time from over 45 minutes (traditional deep networks) to **less than 15 minutes**, making it highly viable for clinical environments.


---

## 📊 Experimental Results

### Performance Summary (5-Fold Cross-Validation)

| Model Architecture | Dataset Condition | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) |
| :--- | :--- | :---: | :---: | :---: | :---: |
| Standalone CNN | Eyes-Closed | 82.82 | 86.46 | 83.75 | 82.65 |
| **Proposed CNN-XGB** | **Eyes-Closed** | **97.97** | **97.92** | **97.89** | **97.91** |
| Standalone CNN | Eyes-Open | 64.82 | 74.34 | 63.29 | 59.32 |
| **Proposed CNN-XGB** | **Eyes-Open** | **96.47** | **96.23** | **96.22** | **96.22** |

### Benchmark Against Existing Literature (Same OpenNeuro Dataset)

| Study / Authors | Core Feature | Model Backbone | Processing Time | Classification Accuracy |
| :--- | :--- | :--- | :---: | :---: |
| Jiang et al. | Coherence | CNN | $\geq$ 45 mins | 94.32% |
| Lalawat et al. | PLV | CNN | $\geq$ 45 mins | 95.76% |
| Aljanabi et al. | Coherence | ResNet | $\geq$ 45 mins | 99.33% |
| **This Study** | **Mutual Information** | **CNN-XGB Ensemble** | **< 15 mins** | **97.97%** |

---

## 🧠 Explainable AI & Network Visualizations

* **Alzheimer's Disease (AD):** Reveals widespread, prominent interhemispheric bilateral coupling across frontal ($F_{p1}$-$F_{p2}$), central, and parietal networks during resting states, masking severe posterior/occipital drop-offs when eyes are opened.
* **Frontotemporal Dementia (FTD):** Displays highly compartmentalized, asymmetric intra-hemispheric frontotemporal loops ($F_{p1}$-$F_7$, $F_{p2}$-$F_8$) reflecting focal cortical degeneration.

---

## 📂 Data & Code Repository Structure

### Public Datasets
The datasets utilized in this research are available publicly on the OpenNEURO repository:
* 🌐 [OpenNEURO: Eyes-Closed EEG Dataset](https://openneuro.org)
* 🌐 [OpenNEURO: Eyes-Open EEG Dataset](https://openneuro.org)




### Acknowledgments
The authors express their gratitude to **Multimedia University (MMU), Malaysia**, for providing high-performance computing facilities and digital resources. We also sincerely thank the medical and research teams at the **2nd Department of Neurology, AHEPA General University Hospital of Thessaloniki, Greece**, for making their clinical experimental datasets publicly available.
