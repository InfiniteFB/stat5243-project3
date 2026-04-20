# STAT-GR5243 Project 3: A/B Test on Voice Interaction in Yiliu

**Yiliu** is a web app designed by our group where users speak to an AI to generate "memory cards" — essentially an AI-assisted oral autobiography tool. We are testing two voice interaction modes via A/B Testing. In Version A (Control), the microphone stays open, and the system automatically detects the end of a turn after two seconds of silence. In Version B (Treatment), users press and hold a large button to speak and release it when finished. Our core hypothesis is that Version B will encourage users to tell longer, more complete stories without being interrupted, leading to higher-quality memory cards. Real users are randomly assigned to one of the two versions via a public link, and all interaction events are logged on the backend.

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Required packages: `scipy`, `pingouin`, `statsmodels`, `pandas`, `numpy`, `matplotlib`
```
import sys
!{sys.executable} -m pip install pandas numpy scipy matplotlib seaborn pingouin
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
 
## Project Structure

```
STATGR5243-Project1/
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
