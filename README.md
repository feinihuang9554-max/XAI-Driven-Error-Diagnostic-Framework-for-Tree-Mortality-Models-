# XAI-Driven-Error-Diagnostic-Framework-for-Tree-Mortality-Models-
Beyond Global Metrics - Unboxing Model Failures using Residual Attribution

🎙️ Unboxing Model Failures: XAI-Driven Error Attribution for Tree MortalityThis repository contains an explainable AI (XAI) framework designed to diagnose and evaluate tree mortality models. Instead of simply predicting mortality, this project focuses on Residual Analysis—modeling the error ($\epsilon = Obs - Pred$) to identify where and why physical models fail.

🌟 Core ConceptIn Earth System Science, a model that is "right for the wrong reasons" is a liability. This project utilizes machine learning and game-theory-based interpretability (SHAP) to perform a "diagnostic autopsy" on model residuals. By explaining the error, we identify missing physical processes (e.g., vapor pressure deficit thresholds or compound drought stress) that current models fail to represent.

🛠️ Methodology & XAI PipelineThe framework follows a multi-stage diagnostic pipeline:
1. Data Preprocessing: 
Automated filtering of numerical climate drivers and handling of missing data through density-based thresholding.
2. Error Modeling:
Using Random Forest (RF) to fit the residuals. RF excels at capturing the non-linear "failure patterns" of the original model.
3. Global Interpretation:
Feature Importance ranking to identify the primary drivers of model systematic bias.
5. Directional Attribution:
SHAP (Shapley Additive Explanations) to quantify whether a driver leads to model under-estimation (missed mortality) or over-estimation (false alarms).
6. Physical Thresholds: PDP & ICE Plots to identify the specific environmental tipping points (e.g., critical soil moisture) where model accuracy breaks down.
7. Interaction Discovery:
SHAP Dependence Plots to reveal how compound stresses (e.g., high Temp + low Precip) interact to amplify model error.

Huang, Feini
feini.huang@uv.es
fhuang@bgc-jena.mpg.de
