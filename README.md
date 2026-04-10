# Shared Neuroanatomical Backbone Discovery via Importance Inversion Transfer (IIT)

Official implementation of the **Importance Inversion Transfer (IIT)** logic, an explainable AI (XAI) framework designed to identify the shared neuroanatomical foundations between Alzheimer’s (AD) and Parkinson’s (PD) diseases.

This computational pipeline provides the empirical evidence required to validate the **Neurodegenerative Elderly Syndrome (NES)** hypothesis by isolating stable structural anchors within the aging brain.

## Overview
Traditional machine learning approaches in clinical neuroscience focus on **discriminative hallmarks**—features that maximize the separation between cohorts. While effective for differential diagnosis, this logic inherently obscures the invariant structural core of neurodegeneration. 

The **IIT mechanism** inverts this paradigm. It prioritizes **Structural Anchors**: regional volumes that remain invariant across different disease manifolds (AD and PD) but deviate significantly from the healthy baseline. This approach isolates the "pathological trunk" shared by both disorders before phenotypic bifurcation occurs.

## Repository Structure
The complete analytical pipeline is integrated into a single, well-documented Jupyter Notebook:
- `IIT_Backbone_Discovery_Neurodegeneration.ipynb`

### Analytical Pipeline

#### Module 1 — Volumetric Characterization & IIT Discovery
*   **Inductive Benchmarking**: Leakage-free diagnostic assessment using a multi-seed protocol (10 independent realizations) and an ensemble of optimized architectures (Random Forest, Gradient Boosting, Logistic Regression).
*   **Anchor Discovery**: Implementation of the **IIT Score**, which integrates Borda rank neutrality, Spearman rank consistency ($\rho=1.0$), and physiological normalization via the Healthy group variance.

#### Module 2 — Statistical Validation & High-Fidelity Visualization
*   **Inferential Profiling**: Comprehensive statistical audit using the Kruskal-Wallis H-test and Dunn’s post-hoc with Bonferroni correction. 
*   **Clinical Signatures**: Differentiation between **Master Anchors** (true phenotypic invariance) and **Transition Pillars** (synchronized patterns with diverging magnitudes).
*   **Nature-Ready Viz**: Automated generation of high-resolution (600 DPI) distribution plots with statistical significance annotations.

## Installation
To set up the environment and run the analysis, clone this repository and install the required dependencies:

```bash
git clone https://github.com/danielecaligiore/IIT-Backbone-Discovery.git
cd IIT-Backbone-Discovery
pip install -r requirements.txt
```

## Data Availability
The analysis presented in the associated paper utilizes data derived from the ADNI (Alzheimer’s Disease Neuroimaging Initiative) and PPMI (Parkinson’s Progression Markers Initiative) repositories.

- Access to raw data must be requested through their respective portals: adni.loni.usc.edu and ppmi-info.org.
- Standardized volumetric datasets should be formatted as detailed in the notebook preprocessing cell.

## Contact
**Daniele Caligiore**  
National Research Council of Italy (CNR), Institute of Cognitive Sciences and Technologies (ISTC) 
Email: daniele.caligiore@istc.cnr.it
