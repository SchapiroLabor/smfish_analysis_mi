# Analysis of RNASCOPE data for human myocardial infarction samples

This repository contains analysis of RNAscope data for human myocardial infarction (MI) samples for [Kuppe, Ramirez et al 2022](https://www.biorxiv.org/content/10.1101/2020.12.08.411686v1%20%20).

Docker containers used to run tools for this analysis can be found under the following links:

* Mesmer: https://hub.docker.com/r/vanvalenlab/deepcell-applications
* RS-FISH: https://hub.docker.com/repository/docker/wuennemannflorian/rs_fish
* Jupyter-Scipy: https://hub.docker.com/r/jupyter/scipy-notebook

## Scripts

 * [segment_nuclei_rnascope_images.sh](./segment_nuclei_rnascope_images.sh)           : Used to segment nuclei from RNAscope images and compute centroid positions for nuclear masks.
 * [count_spots.run_rsfish.sh](./count_spots.run_rsfish.sh)                           : Run RS-FISH on all .tif images in folder and count RNA spots.
 * [count_spots_for_CMs.Rmd](./count_spots_for_CMs.Rmd)                               : Count spots per image for quantification of NPPB and ANKDR1 signal relative to TNNT2.
 * [assign_spots_to_nuclei.Macrophages.Rmd](./assign_spots_to_nuclei.Macrophages.Rmd) : Assign spots from RS-FISH to closest nuclei positions to assign positive cell counts for markers.

