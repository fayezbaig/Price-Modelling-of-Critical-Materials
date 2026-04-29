# Note

The scripts, datasets, internal models, generated outputs, and supporting packages related to this project are confidential and are therefore not included in this repository.

This repository is intended only to explain the methodology, workflow, and purpose of the scripts developed for the price modelling of critical materials in Germany.

All automation, forecasting, regression modelling, and scenario-based analysis for this project were performed using Python.

The main purpose of these scripts was to automate the complete price modelling pipeline and generate projected material prices to be used as characterization factors for Life Cycle Assessment (LCA).

No confidential project data, proprietary datasets, internal scripts, or generated results are being shared in this repository.

---

# Project Overview

## Price Modelling of Critical Materials for Germany (Until 2035)

This project focuses on forecasting the future prices of critical raw materials in Germany until 2035 for use in Life Cycle Assessment (LCA).

The materials included in this study are:

- Platinum
- Palladium
- Rhodium
- Lithium
- Nickel
- Cobalt

The goal is to use the projected prices of these materials as characterization factors for LCA, particularly in the context of Fuel Cell Electric Vehicle (FCEV) powertrain demand and supply risk analysis.

The final output of the project is a scenario-based price projection range for each material until 2035.

---

# Modelling Workflow

## Step 1: Baseline Price Prediction using State Space Model (ETS)

A baseline forecast of material prices was created using the State Space Model with Exponential Smoothing (ETS).

This step establishes the historical trend-based future price prediction for each critical material without considering external influencing factors.

The purpose of this step was to generate the reference price trajectory for all materials up to 2035.

---

## Step 2: Regression Integration using OLS

Ordinary Least Squares (OLS) regression was used to integrate the effect of external drivers into the baseline forecast.

The two major influencing factors considered were:

- Demand from FCEV Powertrains
- Supply Risk

This step improves the baseline forecast by incorporating market and geopolitical dependencies that affect critical material pricing.

---

## Step 3: FCEV Powertrain Demand Analysis

The demand impact from Fuel Cell Electric Vehicle (FCEV) powertrains was incorporated into the regression model.

This demand-side analysis helps estimate how increasing demand of FCEV technologies influences the future prices of critical materials.

---

## Step 4: Supply Risk Modelling using WGI Index

Supply risk was modelled using the Worldwide Governance Indicators (WGI) Index, which directly influences material availability and market stability.

The six WGI factors considered are:

1. Voice and Accountability
2. Political Stability and Absence of Violence/Terrorism
3. Government Effectiveness
4. Regulatory Quality
5. Rule of Law
6. Control of Corruption

These governance indicators help estimate geopolitical and supply-chain risks associated with material supply.

---

## Step 5: Scenario-Based Price Projection until 2035

By combining the baseline forecast, FCEV demand effects, and supply risk factors, a scenario-based price projection was generated for each material.

This provides a projected price range rather than a single fixed value, allowing better uncertainty analysis for LCA applications.

The final projected prices are then used as characterization factors for further Life Cycle Assessment studies.

---

# Additional Note

The supporting packages, datasets, scenario assumptions, and generated model outputs used to perform these operations are also confidential and are not included in this repository.
