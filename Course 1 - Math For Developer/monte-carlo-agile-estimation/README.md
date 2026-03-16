# Monte Carlo Simulation for Agile Estimation

This project is part of the Softuni Software Development AI and Machine Learning Upskill program and aims to demonstrate the understanding and gained knowledge in mathematics and Python during the course. The chosen topic can hopefully be used as a means for improvement in my current work environment, based on the end results. 

**Disclaimer**: This project was developed with the assistance of AI tools (Claude by Anthropic), used to support code consistency, improve written language, and aid in documentation clarity. All logic, design decisions and implementations remain the work of the author - as do any wrong decisions, conclusions, misinterpretations, or questionable life choices made along the way.

### Problem Statement
A big challenge I am facing on a daily basis in my work environment is frequently providing unrealistic ETAs by giving single point estimates that ignore the inherent variability in software development work. This leads to missed deadlines, stakeholder frustration and poor planning. Current estimation approaches(story points, t-shirt sizing, etc.) fail to capture the uncertainty or provide confidence intervals. 

### Objective
Can Monte Carlo simulation produce less misleading delivery forecasts than point estimates for high-variance software work — and under what conditions does it break down?

Note: the question is not whether probabilistic forecasting is theoretically superior (it is), but whether it produces calibrated, useful predictions given the data constraints of a real team.

## Data
Real anonymized cycle time data exported from Jira, representing completed software integration tickets. Data files are in the `/data` folder.

### Project Structure
1. Problem Defition - `01_problem_definition.ipynb`
2. Monte Carlo Simulation - `02_monte_carlo_simulation.ipynb`

### What Is Not Covered
The following are identified as valuable but outside the scope of this project:
- Sensitivity analysis on parameters
- Validation on larger sample sizes to confirm P85/P95 stability
- Temporal drift detection: rolling window approach for teams whose composition has changed

## How to Use
> **Important**: Both notebooks must be executed sequentially, cell by cell, from top to bottom. Cells depend on variables and functions defined in earlier cells running them out of order will cause errors.

### Recommended Execution Order
1. Open and run `01_problem_definition.ipynb` from top to bottom
2. Open and run `02_monte_carlo_simulation.ipynb` from top to bottom

PyMC will display a compiler warning on first run if `g++` is not available. This does not affect results PyMC falls back to a Python implementation with a minor performance cost. 

### Dependencies
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [pandas](https://pandas.pydata.org/)
- [PyMC](https://www.pymc.io/)
- Mathematical references are cited inline in each notebook