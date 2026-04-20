# STAT-GR5243 Project 3: A/B Test on Voice Interaction in Yiliu

This project investigates how two different voice interaction modes affect user engagement and satisfaction in an AI‑powered journaling app.  
- **Control (VAD)**: Voice Activity Detection – turn ends automatically after 2 seconds of silence.  
- **Treatment (PTT)**: Push‑to‑Talk – user holds a button to speak and releases to submit.

We analyzed data from 51 active users over a three‑day period, focusing on:
- Number of memory cards generated
- Number of conversation turns
- User satisfaction (1–5 stars)
- Exploratory metrics (e.g., characters per turn, completion rate, press duration)

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Required packages: `scipy`, `pingouin`, `statsmodels`, `pandas`, `numpy`, `matplotlib`
```
import sys
!{sys.executable} -m pip install pandas numpy scipy matplotlib seaborn pingouin
```
```bash
git clone https://github.com/InfiniteFB/stat5243-project3.git
cd stat5243-project3
```

## 📌 Overview

This project investigates how two different voice interaction modes affect user engagement and satisfaction in an AI‑powered journaling app.  
- **Control (VAD)**: Voice Activity Detection – turn ends automatically after 2 seconds of silence.  
- **Treatment (PTT)**: Push‑to‑Talk – user holds a button to speak and releases to submit.

We analyzed data from 51 active users over a three‑day period, focusing on:
- Number of memory cards generated
- Number of conversation turns
- User satisfaction (1–5 stars)
- Exploratory metrics (e.g., characters per turn, completion rate, press duration)

---

## 🧪 Experimental Design

- **Randomization**: Deterministic assignment based on `md5(user_id) mod 2` at first visit.
- **Data Collection**: 128 recording sessions, April 17–19, 2026.
- **Privacy**: All user IDs hashed (SHA‑256 + salt); only aggregated statistics exported.
- **Statistical Methods**:
  - Welch’s t‑test (unequal variances)
  - Mann‑Whitney U test
  - Bootstrap 95% confidence intervals
  - Cohen’s d effect size
  - Fisher’s exact test (completion rates)
 
## 🔧 Reproducing the Analysis

To reproduce the analysis and results presented in this project:

1. **Clone the repository**
   ```bash
   git clone https://github.com/InfiniteFB/stat5243-project3.git
   cd stat5243-project3
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

4. **Run the analysis**
   - Open `yiliu analysis.ipynb`
   - Click `Kernel` → `Restart & Run All`
 
## Project Structure

```
STATGR5243-Project1/
├── data_raw/                      # Raw data collected from our application
│   ├── ab_session_summary.csv
│   └── ab_user_summary.csv
├── yiliu analysis.ipynb           # Data analysis programming
├── Project_3 Report.pdf           # Project report
├── requirements.txt               # Python dependencies
└── README.md
```


## 👥 Contributors

- Junye Chen (jc6636)
- Yuxuan Ji (yj2924)
- Gujie Li (gl2957)
- Kaicheng Li (kl3728)
