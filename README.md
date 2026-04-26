# 🧪 Statistical Evaluation of Study Methods and Cognitive Focus
## 2³ Full Factorial Experiment

![R](https://img.shields.io/badge/Language-R-276DC3?style=flat&logo=r)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Design%20of%20Experiments-2E75B6)

## 📌 Overview
A **2³ full factorial experiment** investigating how study method, study location, and peer interaction jointly influence **cognitive focus scores** among university students. The study identifies optimal study conditions using rigorous ANOVA-based analysis across all main effects and interaction terms.

---

## 🎯 Research Questions
- Does digital studying outperform traditional methods for cognitive focus?
- Does study location (home vs. library) significantly affect concentration?
- Do interaction effects between these factors matter more than individual effects?
- Which combination of conditions maximizes focus scores?

---

## 🧬 Experimental Design

| Factor | Level -1 | Level +1 |
|--------|----------|----------|
| **A: Study Method** | Traditional (pen & paper) | Digital (tablet/laptop) |
| **B: Location** | Home | Library |
| **C: Peer Interaction** | Solo | Group |

- **Design:** 2³ Full Factorial → 8 treatment combinations
- **Participants:** n = 108 (>95% usable data rate)
- **Response Variable:** Cognitive Focus Score (0–100, standardized test)
- **Replication:** ~13–14 participants per cell

---

## 🔬 Methodology

### 1. Data Collection & Preprocessing
- Recruited 108 participants across all 8 experimental conditions
- Applied IQR-based outlier detection and systematic validation checks
- Achieved >95% usable data rate, reducing inconsistencies by ~20%

### 2. Assumption Checks
- **Normality:** Shapiro-Wilk test on model residuals
- **Homogeneity of Variance:** Levene's test across all factor combinations
- **Independence:** Ensured by randomized assignment

### 3. ANOVA Analysis (Type III SS)
Evaluated all **7 effect terms**:
- 3 Main effects: A, B, C
- 3 Two-way interactions: A×B, A×C, B×C
- 1 Three-way interaction: A×B×C

### 4. Post-hoc Analysis
- **Tukey HSD** for pairwise comparisons
- **Estimated Marginal Means (emmeans)** for interaction interpretation
- Planned contrast: Digital+Group vs Traditional+Solo

---

## 📈 Key Results

| Effect | F-statistic | p-value | Significant? |
|--------|-------------|---------|--------------|
| Study Method (A) | — | < 0.05 | ✅ Yes |
| Location (B) | — | < 0.05 | ✅ Yes |
| Peer Interaction (C) | — | < 0.05 | ✅ Yes |
| A × C (Method × Peers) | — | < 0.01 | ✅ Yes (strongest) |
| A × B × C | — | < 0.05 | ✅ Yes |

### 🏆 Main Finding
> **Digital study methods combined with group settings improved cognitive focus by 15–25% over the Traditional + Solo baseline condition** — the most impactful factor combination identified.

---

## 💡 Recommendations
1. Academic institutions should promote **digital tools** in collaborative environments
2. **Library settings** provide a consistent marginal benefit over home study
3. The **Digital + Group** combination is the optimal study configuration
4. Solo traditional study remains the lowest-performing condition

---

## 🛠️ Tech Stack
- **Language:** R
- **Key Packages:** `tidyverse`, `ggplot2`, `car`, `emmeans`, `agricolae`, `gridExtra`

---

## 🚀 How to Run
```r
# 1. Install required packages
install.packages(c("tidyverse", "ggplot2", "gridExtra",
                   "car", "emmeans", "agricolae"))

# 2. Open factorial_experiment.R in RStudio

# 3. Source the script
source("factorial_experiment.R")
```

---

## 📁 Repository Structure
```
02_factorial_experiment/
│
├── factorial_experiment.R   # Full analysis: design → ANOVA → post-hoc → plots
├── README.md                # This file
└── plots/                   # Output visualizations (generated on run)
```

---

## 📚 References
- Montgomery, D.C. (2017). *Design and Analysis of Experiments* (9th ed.). Wiley.
- R Core Team (2024). *R: A Language and Environment for Statistical Computing*.
- Fox, J. & Weisberg, S. (2019). *An R Companion to Applied Regression* (3rd ed.).
