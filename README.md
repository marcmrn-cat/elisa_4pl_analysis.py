# elisa_4pl_analysis.py
This repository contains an automated Python pipeline designed to process, analyze, and visualize 96-well plate ELISA (Enzyme-Linked Immunosorbent Assay) data. It replaces manual spreadsheet calculations with a robust, reproducible, and highly customizable script utilizing a Four-Parameter Logistic (4PL) regression model. 
        Key Features
- Smart Quality Control (QC) Filter: Automatically evaluates the Coefficient of Variation (CV) of standard triplicates. If the CV exceeds a user-defined threshold (e.g., 15%), the algorithm automatically identifies and drops the outlier, rescuing the measurement by utilizing the optimal duplicate.
- Automated 4PL Curve Fitting: Utilizes scipy.optimize to generate highly accurate non-linear calibration curves, calculating the R^2 value to ensure model reliability.
- Paired/Kinetic Analysis: Automatically detects time-point markers (e.g., "t1" and "t2") in sample IDs to compute absolute differences and percentage changes in biomarker concentrations over time.
- Publication-Ready Visualizations: Generates high-quality calibration curves distinguishing between pure triplicates and rescued duplicates, along with paired sample trend lines.
Modular Configuration: All experimental variables (plate layout, standard concentrations, dilution factors) are isolated in a configuration dictionary, allowing researchers to use the script without modifying the core logic.
        Dependencies
This script requires Python 3.x and the following standard scientific libraries:
- pandas (Data manipulation and Excel I/O)
- numpy (Numerical operations)
- scipy (4PL mathematical optimization)
- matplotlib (Data visualization)
        How to Use
- Clone the repository to your local machine.
- Open elisa_4pl_analysis.py and modify the CONFIG block at the top of the script to match your specific plate layout and standard concentrations.
- Run the script from your terminal:
