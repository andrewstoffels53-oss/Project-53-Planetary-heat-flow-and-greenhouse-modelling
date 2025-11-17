# Project-53-Planetary-heat-flow-and-greenhouse-modelling
An Investigation into Simplified Planetary Radiative Transfer Models for Planetary Energy Balances
# Planetary Energy Balance Modelling  
CHE4045Z Project 53 · University of Cape Town (2025)  
**Authors:** Andrew Stoffels · Henry Zhang  
**Supervisor:** Kyle Abrahams  

---

##  Project Overview
This repository contains the code, models, and supporting files for the CHE4045Z research project on **planetary energy balance models**, focusing on simplified approaches for predicting the **surface temperature** of terrestrial exoplanets.

The objective of this project is to explore:
- How different assumptions in energy balance models influence predictive accuracy  
- Which parameters are essential vs. non-essential  
- How outgoing longwave radiation (OLR) can be approximated  
- How planetary characteristics (albedo, composition, stellar radiation, etc.) affect heat balance  
- How model complexity can be increased stepwise while maintaining accuracy  

The final outcome is a **simple-but-accurate energy balance model** that balances computational simplicity with scientific realism.

---

## 🧪 Features & Components

### **1. Energy Balance Model Implementations**
Includes multiple versions of the planetary energy balance model:
- 0-D blackbody approximation  
- Greybody greenhouse model  
- Linear OLR approximation (North, 1981)  
- Polynomial OLR approximations  
  - Haqq-Misra (2018)  
  - Williams & Kasting (1997)  
  - Batalha (2016)  
  - Raymond (2010 – humidity-dependent)  
- Ice–albedo feedback options  
- Cloud masking considerations (Fauchez et al., 2019)

Each model folder corresponds to a different **complexity tier**, allowing stepwise comparison.

---

## Data
This project uses the **INARA synthetic exoplanet dataset**, containing:
- Stellar temperature & radius  
- Semi-major axis  
- Planetary surface pressure & temperature  
- Atmospheric composition  
- Mean surface albedo  
- Full planetary and stellar spectral curves  

Source:  
Zorzan et al. (2025), *Machine Learning-ready Dataset for Exoplanet Atmospheric Retrieval*.

**Note:** Only the portion of data relevant to this analysis is included here.

---

##  Method Summary
A structured pipeline is used to evaluate each model:

1. **Build simplest possible energy balance model**  
2. Incrementally replace one assumption at a time  
3. Evaluate each change using:  
   - RMSE  
   - R²  
   - Parity plots  
   - Bias analysis  
   - T-tests / Mann-Whitney U (normality-dependent)  
4. Keep only assumptions that *meaningfully* improve predictive accuracy  
5. Perform sensitivity analysis on the final model  

---

##  Repository Structure

