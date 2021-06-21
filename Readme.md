[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4284486.svg)](https://doi.org/10.5281/zenodo.4284486)

# Branch-chamber-fluxes

A python notebook to merge data from branch chambers located in a dought-exposed and experimentally irrigated plot in Yatir forest, with gas concentrations of H<sub>2</sub>O and CO<sub>2</sub> measured using the LI-COR LI-7000 and LI-840a infrared gas analysers combined into a novel gas exchange measurement system. Data is gathered as follows:

1. Gas concentrations of CO<sub>2</sub> and H<sub>2</sub>O: LI-COR LI-7000 infrared gas analyser (IRGA)
2. Auxiliary data: All collected into a Campbell CR1000 datalogger

There are 2 notebooks in this project, and the data is organised as follows:
1. Raw data is in folder *01_raw_chamber_data*, and logfiles are in *00_additional_data*
2. **01_chambers_v1.00.ipynb**: This calculates corrected data in the folder *02_preprocessed_chamber_data*. Data is organsed like this:
   * *raw_qc*: Fully corrected data at the raw temporal resolution
   * *1min*: Means per chamber and measurement period of the last 30-60 measurements in 2s intervals, with calculated fluxes.
   * *1h*: Hourly means per plot
3. **02_final_corrections_v0.1.ipynb**: This adds one last layer of corrections, removing some remaining bad data from the 1min (per chamber) files. Outputs are stored in *03_processed_data*.

## Dependencies

The following python packages are required to read the FLIR files:

  - Pandas
  - Numpy
  - Scipy

## How to Cite

Jonathan D. Muller, Itay Oz. (2021). Branch-chamber-fluxes: Tool to calculate gas fluxes from branch chambers.  DOI: 10.5281/zenodo.4284486  (URL:
<https://doi.org/10.5281/zenodo.4284486>), Python notebook

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4284486.svg)](https://doi.org/10.5281/zenodo.4284486)

## License

This software is distributed under the GNU GPL version 3

