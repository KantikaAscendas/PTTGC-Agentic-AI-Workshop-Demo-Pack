# PTTGC Agentic AI Workshop Demo Pack

Hands-on workshop examples for **MATLAB Online**, using MATLAB Live Scripts and synthetic engineering data.

[![Open in MATLAB Online](https://www.mathworks.com/images/responsive/global/open-in-matlab-online.svg)](https://matlab.mathworks.com/open/github/v1?repo=KantikaAscendas/PTTGC-Agentic-AI-Workshop-Demo-Pack&file=01_GageRR_MaterialTesting.mlx)

## Before the workshop

- Sign in to MATLAB Online with your MathWorks account.
- Use MATLAB **R2026b or later** for the guided Gage R&R Analyzer and DOE Explorer app activities.
- Ensure your account has access to **Statistics and Machine Learning Toolbox**. MATLAB Online availability and toolbox access depend on your license.
- The repository includes all CSV data needed for the two demos.

## Start in MATLAB Online

1. Click **Open in MATLAB Online** above to copy this repository into your MATLAB Online environment and open Demo 01.
2. Set MATLAB's **Current Folder** to the downloaded repository folder, containing both the Live Scripts and the `data` folder. The scripts locate data with `fullfile(pwd,"data")`.
3. Open the desired **`.mlx` Live Script**. Run sections from top to bottom using **Run Section**. Read the notes and discuss the embedded agent prompts as you go.
4. Complete the app activities described in the Live Script. Running the code sections does not automatically perform the interactive app steps.
5. For Demo 02, open `02_DOE_PolymerPellet.mlx` from the same repository folder.

The agent prompts are discussion prompts for an AI assistant; the scripts themselves do not connect to an AI service.

**Download alternative:** On GitHub, choose **Code > Download ZIP**, extract it, and upload the two `.mlx` files and the entire `data` folder into one folder in MATLAB Drive. Open that folder in MATLAB Online before running a demo.

## Workshop demos

| Demo | Live Script | Open directly |
| --- | --- | --- |
| 01 - Gage R&R for material testing | [01_GageRR_MaterialTesting.mlx](01_GageRR_MaterialTesting.mlx) | [Open Demo 01 in MATLAB Online](https://matlab.mathworks.com/open/github/v1?repo=KantikaAscendas/PTTGC-Agentic-AI-Workshop-Demo-Pack&file=01_GageRR_MaterialTesting.mlx) |
| 02 - DOE for polymer pellet development | [02_DOE_PolymerPellet.mlx](02_DOE_PolymerPellet.mlx) | [Open Demo 02 in MATLAB Online](https://matlab.mathworks.com/open/github/v1?repo=KantikaAscendas/PTTGC-Agentic-AI-Workshop-Demo-Pack&file=02_DOE_PolymerPellet.mlx) |

### Demo 01 - Gage R&R for material testing

Explore repeatability and reproducibility in synthetic tensile-strength measurements. Load the data, compare part/operator patterns, and use **Gage R&R Analyzer** to review measurement variation.

Data: [data/gage_rr_material_testing.csv](data/gage_rr_material_testing.csv)

App variable mapping:

- Part: `PartID`
- Operator: `Operator`
- Measurement: `TensileStrength` (MPa)
- `Repeat` identifies repeated measurements.

Launch the app from **Apps**, or enter `gageRRAnalyzer` in the Command Window. Discuss the suitability of the study design, including destructive material testing, before applying the workflow to real measurements.

### Demo 02 - DOE for polymer pellet development

Explore a synthetic experiment, visualize melt-flow response, fit a regression model with a temperature/screw-speed interaction, inspect residuals, and discuss experiment planning with **DOE Explorer**.

Data: [data/polymer_pellet_doe.csv](data/polymer_pellet_doe.csv)

- Factors: `MeltTemp_C`, `ScrewSpeed_rpm`, `Additive_wtPct`
- Modeled response: `MeltFlowIndex_g10min`
- Additional recorded response: `PelletStrength_MPa`
- `run` identifies the experiment run.

Launch the app from **Apps**, or enter `doeExplorer` in the Command Window. Follow the Live Script's guided design activity; use the supplied table for the code-based analysis.

## Repository contents

```text
PTTGC-Agentic-AI-Workshop-Demo-Pack/
|-- README.md
|-- 01_GageRR_MaterialTesting.mlx
|-- 02_DOE_PolymerPellet.mlx
`-- data/
    |-- gage_rr_material_testing.csv
    |-- polymer_pellet_doe.csv
    |-- pellet_quality_spc.csv
    `-- catalyst_support_life.csv
```

The complete source data folder is included. The SPC and catalyst-life CSV files are additional workshop datasets; this repository currently contains Live Scripts for Demos 01 and 02.

## Troubleshooting

- **CSV file not found:** Check that the Current Folder contains `data` and keep the folder name lowercase.
- **App or function unavailable:** Check your MATLAB release and Statistics and Machine Learning Toolbox access using `ver`.
- **GitHub does not display the Live Script:** Open it in MATLAB Online using the links above, or download it and open it in MATLAB.
- **Results differ from saved output:** Run sections in order to refresh the outputs in your own session.

## About the data

All datasets are synthetic teaching examples. They do not represent PTTGC measurements, operating conditions, specifications, or acceptance limits. Factor ranges illustrate the workflow and are not production recommendations. Review AI-generated code and interpretations before engineering use.

## MathWorks documentation

- [Open GitHub repositories in MATLAB Online](https://www.mathworks.com/help/matlab/matlab_env/open-github-repositories-in-matlab-online.html)
- [Gage R&R Analyzer](https://www.mathworks.com/help/stats/gagerranalyzer-app.html)
- [DOE Explorer](https://www.mathworks.com/help/stats/doeexplorer-app.html)
