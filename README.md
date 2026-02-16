# Option-Pricing
# QMC Pricing of Asian Options: Smoothing and Variance Reduction

This project focuses on pricing high-dimensional **Arithmetic Asian Call** and **Binary Digital Asian Options** using advanced numerical integration techniques.

## Project Overview
The pricing of Asian options often involves high-dimensional integrals where standard Quasi-Monte Carlo (QMC) methods fail to achieve optimal convergence due to non-smooth payoffs (kinks and jumps). This implementation addresses these challenges using:

* **Pre-integration (Smoothing):** Analytically integrating along the active subspace to restore $O(N^{-1})$ convergence.
* **Active Subspace Method:** Identifying the dominant direction of variability using gradient covariance matrices.
* **Optimal Drift Importance Sampling (ODIS):** Reducing variance in out-of-the-money (OTM) regimes ($K=120$).
* **Sobol Sequences:** Utilizing scrambled low-discrepancy sequences (RQMC).

## Repository Structure
* `arithmetic_asian_option_final.py`: Implementation and simulation for Arithmetic Asian Call options.
* `digital_asian_option_final.py`: Implementation and simulation for Binary Digital Asian options.
* `Report.pdf`: Detailed theoretical background and analysis of numerical results.
* `plots_arithmetic_asian/`: (Optional) Generated convergence and efficiency plots.

## Methodology
The core of the project is based on the synergy between analytical smoothing and optimized sampling. 
- For **Arithmetic options**, we smooth the "kink" at the strike price.
- For **Digital options**, we integrate the jump discontinuity, transforming it into a smooth Gaussian tail probability.

## Requirements
To run the simulations, you need:
- Python 3.x
- NumPy, Pandas, SciPy, Matplotlib, tqdm

## Authors
- Matteo Burzio
- Luca Civilla
- Francesco Vinciguerra
