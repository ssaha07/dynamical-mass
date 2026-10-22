# Estimating the Dynamical Mass of a Galaxy Cluster

Python-based analysis of galaxy-cluster observations from the Sloan Digital Sky Survey (SDSS). The project investigates galaxy redshifts and velocity distribution to estimate the cluster's dynamical mass and luminous mass.

## Objectives
- Retrieve and inspect photometric and spectroscopic galaxy data from SDSS.
- Handle repeated observations and retain a consistent record per object.
- Examine redshift distributions and identify likely cluster members.
- Apply a 3-sigma outlier-filtering procedure and estimate the cluster's systemic redshift.
- Calculate velocity dispersion and estimate dynamical mass using the virial approach.
- Estimate luminous mass from photometric measurements and compare it with dynamical mass.
- Visualise the data and discuss the implications and limitations of the estimates.

## Data
The SDSS data are not included in this repository. Obtain the data from the [SDSS website](https://www.sdss.org/) or the relevant SkyServer query, and place the downloaded file in `data/`. Do not commit large files or data that you are not permitted to redistribute.

Record the query, data-release version, retrieval date, selected sky position, redshift limits, and column definitions in your notebook or report so the analysis can be reproduced.

## Repository layout
```text
data/       # Local input data; see data/README.md
notebooks/  # Analysis notebook(s)
figures/    # Exported plots
results/    # Summary results and tables
requirements.txt
```

## Setup
Python 3.10 or later is recommended. Create and activate a virtual environment, then install dependencies:

```bash
python -m venv .venv
# Windows PowerShell: .venv\Scripts\Activate.ps1
# macOS/Linux: source .venv/bin/activate
python -m pip install -r requirements.txt
```

Open the project notebook with Jupyter Lab or Jupyter Notebook. Update any file paths to match the local SDSS data file.

## Reported results
The submitted project report records the following outputs; these should be reproduced from the final notebook before treating the repository as a fully verified release:

- Mean cluster redshift: approximately `0.08007`
- Velocity dispersion: approximately `1317.22 km/s`
- Cluster diameter: approximately `0.56837 Mpc`
- Dynamical mass: approximately `3.32 × 10^14 solar masses`
- Luminous mass in the r-band analysis: approximately `1.02 × 10^13 solar masses`

These values depend on the selected sample, assumptions, and calculations. Consult the notebook and project report for methodology and limitations.

## Limitations
The virial estimate assumes the selected galaxies represent a gravitationally bound system in approximate dynamical equilibrium. Membership cuts, projection effects, data quality, and the luminous-mass conversion can affect the result.

## References
- Sloan Digital Sky Survey: https://www.sdss.org/
- NumPy: https://numpy.org/doc/
- pandas: https://pandas.pydata.org/docs/
- Matplotlib: https://matplotlib.org/stable/
- SciPy: https://docs.scipy.org/doc/scipy/
- Astropy: https://docs.astropy.org/

## Author
Name: Shamayita Saha
