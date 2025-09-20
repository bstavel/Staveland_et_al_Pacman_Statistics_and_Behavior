# Pacman Behavioral Analyses

## Overview

Analysis scripts (mostly in R) for the behavior and statistical analysis of the PacMan project. While [Staveland_et_al_Pacman_Neural_Analyses](https://github.com/bstavel/Staveland_et_al_Pacman_Neural_Analyses) has the python scripts for analyses that are (nearly) only brain data, these analyses include both pure behavioral analyses and both brain/behavior models.

## Repository Structure

### R/
This folder holds all of the helper functions that are used throughout the analyses. The functions are sourced at the beginning of each .Rmd file. 

### matlab_helpers/
This folder holds the matlab helper functions that are used to convert the `.mat` files from our WashU site to a csv with MNI coordinates for each subject
- `washu_to_mni.m`: This file converts the washu coordinates to MNI coordinates.

### analysis/
This folder holds all of the analyses for the paper. Each subfolder corresponds to a different analysis group.

#### anatomical_plotting
This folder holds the scripts for creating the MNI coordinate CSV files.
- `create_mni_csv.Rmd`: This script creates a CSV file with the MNI coordinates for each electrode.

#### attack
This folder holds the analyses related to ghost attacks. (Figure 5 analyses)
- `fig5_left_vs_right_mfg.Rmd`: This script creates the plots for the left vs. right MFG activity during ghost attacks.
- `fig5_right_mfg_models_and_figures.Rmd`: This script runs the models and creates the plots for the right MFG activity during ghost attacks.
- `limbic_theta_during_attack.Rmd`: This script runs the models and creates the plots for the limbic theta activity during ghost attacks.
- `mfg_hfa_attack.Rmd`: This script runs the models for the MFG HFA activity during ghost attacks.

#### behavior
This folder holds the behavioral modeling and plotting. (Figure 1 analyses)
- `brms_behavioral_modeling.Rmd`: This script runs the Bayesian models of the behavior.
- `figure_1_behave_plots.Rmd`: This script creates the plots for Figure 1.
- `normative_behavior_new_sample.Rmd`: This script runs the normative behavior analyses on a new sample of subjects.
- `normative_behavior.Rmd`: This script runs the normative behavior analyses for the pilot subjects.

#### cleaning_ieeg_behavior
This folder holds the scripts for cleaning and combining the behavioral data for each subject.
- `cleaning_behave_SUBJECT.Rmd`: These scripts clean the behavioral data for each subject.
- `combine_ieeg_subs_behavior.Rmd`: This script combines the cleaned behavioral data for all subjects.

#### clinical
This folder holds the exploratory analyses of the clinical cohort. (Supplement)
- `clinical_eda.Rmd`: This script performs exploratory data analysis on the clinical cohort, which is included as a supplemental figure.

#### coherence
This folder holds the coherence analyses. (Figure 3 analyses)
- `create_sig_theta_coherence_csv.Rmd`: This script creates a CSV file with the significant theta coherence values.
- `coherence_region_models.Rmd`: This script runs the coherence models for the different regions.
- `coherence_region_models_ppc_plv.Rmd`: This script runs the coherence models for the PPC and PLV.
- `fig3_simplified_differential_conn_plots.Rmd`: This script creates the simplified differential connectivity plots for Figure 3.
- `supp_fig5_differential_conn_plots.Rmd`: This script creates the differential connectivity plots for Supplementary Figure 5.
- `supp_fig6_differential_conn_plots_ppc_plv.Rmd`: This script creates the differential connectivity plots for the PPC and PLV for Supplementary Figure 6.
- `supp_table_coherence_region.Rmd`: This script creates the supplementary table for the coherence region models.
- `fig_3_rising_falling_plots.Rmd`: This script creates the plots for the rising and falling coherence.
- `fig_3_rising_falling_regional_plots.Rmd`: This script creates the regional plots for the rising and falling coherence.
- `fig3_example_coherence.Rmd`: This script creates the example coherence plots for Figure 3.
- `fig3_rising_falling_example_sub.Rmd`: This script creates the example rising and falling coherence plots for a single subject.
- `rising_falling_threshold_model_comparison.Rmd`: This script compares the rising and falling threshold models.
- `supp_table_rising_falling.Rmd`: This script creates the supplementary table for the rising and falling coherence models.

#### cross_correlations
This folder holds the computation and statistical analysis of cross-correlations for the directionality analysis. (Figure 4 analyses)
- `compute_regional_ccfs_theta.Rmd`: This script computes the regional cross-correlations for theta.
- `theta_ccf_stats.Rmd`: This script runs the statistics on the theta cross-correlations.

#### freq_power_analyses
This folder holds the analyses of theta and HFA power profiles. (Figure 2 analyses)
- `compile_ieeg_files_iti_logged_trialonset.Rmd`: This script compiles the iEEG files for the ITI and trial onset.
- `theta_and_hfa_power_profiles.Rmd`: This script creates the theta and HFA power profiles.
- `all_roi_theta_app_av.Rmd`: This script runs the models for the theta power in approach vs avoidance windows in all ROIs. 

#### granger
This folder holds the Granger causality analyses. (Figure 4 analyses)
- `granger_lmes.Rmd`: This script runs the linear mixed effects models on the Granger causality results to determine directionality.
- `granger_plots.Rmd`: This script creates the plots for the directionality results.
- `granger_thresholds.Rmd`: This script tests the Granger causality results at different theta coherence thresholds.

#### turnaround_time_correlations
This folder holds the analyses of the correlation between turnaround time and theta/HFA syncrhony. (Figure 4 analyses)
- `brms_all_roi_model.Rmd`: This script runs the Bayesian models theta syncrhony across threshold.
- `brms_hfa_all_roi_model.Rmd`: This script runs the Bayesian models for HFA in all ROIs.
- `calculate_trial_correlations.Rmd`: This script calculates the trial-by-trial correlations.
- `Figure4_combinedhfa_theta_plots.Rmd`: This script creates the combined HFA and theta plots for Figure 4.
- `supp_table_turn_times.Rmd`: This script creates the supplementary table for the turnaround times.
- `turntime_threshold_model_comparison.Rmd`: This script compares the syncrhony results across different thresholds.

## Installation

### Requirements
This code was created using R v4.1.2. All required packages are loaded at the beginning of each script. 

### Key Dependencies
- **tidyverse**: For data manipulation and visualization.
- **brms**: For Bayesian modeling.
- **ggplot2**: For plotting.