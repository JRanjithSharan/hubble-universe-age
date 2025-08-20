# 🌌 Predicting the Hubble Parameter and Age of the Universe using Type Ia Supernovae

This repository contains my research project completed during the **India Space Academy (ISA) Summer School 2025**.  
The project uses **Type Ia supernovae as standard candles** to predict the **Hubble constant (H₀)** and estimate the **age of the Universe**, based on observational data from the **Pantheon+SH0ES dataset**.

---

## 🔭 Project Overview
Type Ia supernovae are considered "standard candles" in cosmology because of their consistent intrinsic luminosity.  
By comparing their apparent brightness to expected absolute brightness, we can estimate distances and construct the **Hubble diagram** (distance modulus vs. redshift).

Using this dataset and statistical fitting, the project:
- Measures the **Hubble constant (H₀)** from supernova data  
- Estimates the **age of the Universe** by integrating cosmological equations  
- Compares results across different redshift ranges  
- Evaluates residuals to validate the cosmological model  

---
## ⚙️ Required Libraries
- numpy  
- pandas  
- matplotlib  
- scipy  
- astropy  

---

## 📊 Methodology

### 1. Load Dataset
- Used the **Pantheon+SH0ES Type Ia supernova sample**.  
- Extracted relevant columns: redshift (`zHD`), distance modulus (`MU_SH0ES`), and uncertainties.  

### 2. Preprocess Data
- Removed missing values.  
- Converted extracted columns into **NumPy arrays** for efficient analysis.  

### 3. Plot the Hubble Diagram
- Plotted **distance modulus vs. redshift** to form the Hubble diagram.  
- Applied logarithmic scaling on the redshift axis for clarity.  

### 4. Fit Cosmological Model
- Applied **non-linear least-squares fitting** using `scipy.optimize.curve_fit`.  
- Estimated parameters:  
  - **Hubble constant (H₀)**  
  - **Matter density parameter (Ωₘ)**  

### 5. Estimate Universe Age
- Used the **Friedmann equation** with numerical integration (`scipy.integrate.quad`).  
- Derived the **age of the Universe** based on best-fit cosmological parameters.  

### 6. Residual Analysis
- Computed residuals between observed and fitted values.  
- Validated that **Type Ia supernovae** behave as reliable standard candles.  

---

## 📈 Results
- Best-fit **Hubble constant (H₀): ~72.97 ± 0.17 km/s/Mpc**  
- Estimated **age of the Universe: ~12.36 billion years**  
- Residual analysis confirmed consistency with the **ΛCDM cosmological model**.  

> Results differ from **Planck 2018 data** and **Riess et al. (2021) SH0ES measurements** because of **Hubble Tension**.  

---

## 📑 References
- Pantheon+SH0ES Supernova Data Release: [Dataset](https://github.com/PantheonPlusSH0ES/DataRelease)  
- Astropy Documentation: [Astropy](https://docs.astropy.org/)  
- Hu, J. P., Zhu, Y. Z., Chen, Y. Y., & Wang, B. (2023). Testing the cosmological principle with the Pantheon+ sample and the region-fitting method. Astronomy & Astrophysics. arXiv:2310.11727 
  
