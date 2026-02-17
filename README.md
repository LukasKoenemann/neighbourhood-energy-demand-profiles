# neighbourhood-energy-demand-profiles

**Data for:** *Design of decentralized energy systems using an artificial neural network-based dispatch concept*

This repository contains the time series data and system configurations used in the research paper "Design of decentralized energy systems using an artificial neural network-based dispatch concept".

---

## 📘 Overview

The dataset provides representative time series for three decentralized energy system (DES) topologies of increasing complexity. It includes:

- demand profiles
- weather data
- price signals

All time series are aggregated into typical periods using the **Time Series Aggregation Module (TSAM)**.

---

## 🔧 Case Study Topologies

Each case corresponds to a different DES configuration:

### Case Study 1 – Industrial Electrical Supply
- **Focus:** Variable energy demand charges and battery dispatch.
- **Components:** PV system, Li-ion battery (B), grid connection (EG), industrial load (ED).
- **Key data:** Normalized PV profiles, electrical demand, time-dependent grid prices.

### Case Study 2 – Residential Multi‑Energy System (Heat & Power)
- **Focus:** Sector coupling and thermal storage management.
- **Components:** All from Case 1 plus air-source heat pump (HP), electric boiler (EB), heat storage (HS), heating demand (HD).
- **Key data:** Ambient temperature (for COP) and space‑heating/hot‑water demand.

### Case Study 3 – Advanced Multi‑Energy System (Heat, Cold & Power)
- **Focus:** Flexible demands and triple‑sector integration.
- **Components:** Case 2 plus compression chiller (CC), cold storage (CS), electro‑mobility (EM), refrigerator warehouse (RW), cooling demand (CD).
- **Key data:** Solar radiation, cooling demand, EV occupancy/charging profiles.

---

## 🗂 Data Structure

All files are stored in CSV format and organised by annual time series for each profile and the corresponding calculated typical periods as described in the manuscript.

```
data/            

 case_study_1/ 
   yearly_timeseries/
   ├─ electrical_demand[1].unscaled_power.csv   # [timestamp, electrical_load]
   ├─ electrical_grid.market_price.csv   # [timestamp, electrical_price]
   ...
   └─ photovoltaic[1].normalized_power.csv   # [timestamp, normalized photovoltaic power]
   typcial_periods/
   ├─ data.csv # [timestamp, electrical_load, electrical_price, normalized photovoltaic power, ...]

case_study_2/ 
...
```

### Typical Periods & Aggregation
Original annual profiles have been reduced to **6 typical days (24 h each)** to lower computational effort while preserving seasonal characteristics. Representation factors ($n_{occ,p}$) are given in Appendix A of the paper.

---

## 📎 Citation

If you use this data or the associated framework, please cite:

> Koenemann, Lukas and Bensmann, Astrid and Gerster, Johannes and Hanke-Rauschenbach, Richard, Design of decentralized energy systems using an artificial neural network-based dispatch concept. Available at SSRN: https://ssrn.com/abstract=5480445 or http://dx.doi.org/10.2139/ssrn.5480445

---

## 📄 License

This data is licensed under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.
