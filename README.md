# **India Test Batting Simulation – England Tour (2025)**

This repository contains a pre-series tactical analytics project that evaluates the expected performance of India’s Test top-order batters for the upcoming tour of England. The analysis uses region-wise segmentation, spin vs seam dismissal profiling, and a Monte Carlo simulation framework to generate probabilistic series forecasts.

---

## **Project Context**

The project was built to answer a forward-looking question:  
**How might India's transitioning Test batting lineup fare in seam-dominant English conditions?**

Rather than relying solely on raw historical averages, this analysis integrates multiple layers of context:

- Regionally segmented batting metrics (SENA vs Subcontinent)
- Seam vs spin dismissal distributions
- Tactical vulnerability indicators
- Monte Carlo simulations with strike rate penalties for seam threat

By combining data engineering, simulation modeling, and visual storytelling, the project attempts to forecast not just form but *fit*—whether each batter’s skillset aligns with the challenge at hand.

---

## **What's Included**

- `india_vs_eng.ipynb`: Final Jupyter Notebook with analysis, visualizations, and commentary  
- `/india_vs_eng.py`: Full end-to-end Python script with data wrangling, metric engineering, simulation logic, and visualizations
- `/Images`: Output plots and charts used for communication and storytelling  
- `/data`: Cleaned and labeled CSV files for each batter  
- `README.md`: Project documentation and methodological overview

---

## **Monte Carlo Simulation Engine**

A log-normal distribution is used to model the natural skew in Test innings. For each batter, we simulate **1,000 Test innings** using their region-specific career averages:

- **Balls Faced** modeled using log-normal distributions with player-specific volatility indices  
- **Strike Rate** modeled using normal distributions  
- **Score = (Balls Faced × SR) / 100**

We then apply a **Seam Threat Penalty**, based on each batter’s historical dismissal rate and average against pace in SENA countries. This penalty is implemented at the strike rate level to simulate pressure against a seam-heavy England bowling attack.

---

## **Metrics Analyzed**

Each batter is evaluated across:

- Runs, Average, Strike Rate, and Balls Per Dismissal (SENA vs Subcontinent)  
- Seam vs Spin Dismissal Percentage (in SENA)  
- Average vs Seam / vs Spin (in SENA)  
- Projected Score Distribution (Monte Carlo Simulation)  
- Cumulative Run Forecast across a 10-innings Test series  

---

## **Visualizations**

- **Grouped Bar Charts**: Regional runs and balls per dismissal  
- **Stacked Bar Chart**: Seam vs spin dismissal percentages  
- **Heatmap**: Batting average vs seam/spin in SENA  
- **Distribution Plots**: Monte Carlo score simulations per batter  
- **Line Plot**: Cumulative projected runs over a 10-innings Test series  

These visualizations aim to blend tactical insight with statistical clarity, enabling pre-series performance forecasting at a scouting level.

---

## **Batters Profiled**

- **Shubman Gill**  
- **Yashasvi Jaiswal**  
- **KL Rahul**  
- **Rishabh Pant**
- **Karun Nair** *(EDA only, since he hasn't played an away test for India, but might be a great player to look out for, best average against pace out of all 6, albeit with a small sample size)*
- **Nitish Kumar Reddy** *(dark horse candidate with strong domestic red-ball credentials and a great Australia series under his belt)*

---

## **Contact**

If you'd like to explore this further, collaborate, or discuss cricket analytics and simulation modeling, feel free to reach out:

- [LinkedIn](https://www.linkedin.com/in/aaditpahuja)  
- 📧 aaditpahuja@gmail.com
