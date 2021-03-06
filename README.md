# PDACsurv
Meta-analysis of prognostic models for PDAC

Introduction

A unique set of 89 pancreatic cancer samples profiled using both sequencing and microarray platform was used for training the PCOSP (Pancreatic cancer overall survival predictor) to predict patients with early death (within >1 yr) after surgery. Further, to validate the model we used genomic profiles of 823 samples curated from public domain. The simplistic k-top scoring pair approach was used to build the model, where we looked at relative expression of gene pairs within the patient. 

Scripts

1. PCOSP_model_building.R : The script is used for building Pancreatic cancer overall survival predictor using unique 89 samples profiled using microarray and sequencing platform.

2. Meta_estimate_Calculation_Validation_Cohorts.R : The script calculates D-index and Concordance index for independent cohorts and calculate the meta-estimae of C-index and D-index. The forestplot of C-index and D-index was plotted for all the cohorts.

3. PCOSP_score_estimation.R: It is used for calculating the PCOSP score for independent datasets.

4. Validation cohorts formatting.R: Used for formatting independent datasets for input to PCOSP.

5. HyperGSA_Pathway_analysis.R: Used for identifying pathways overrepsentrated in PCOSP genes, the 12,430 common across all the cohorts were used as reference.

6. Clinical_model_comparison.R: This script is used for building linear regression  model using clinicopathological features and integrated clinicopathological and PCOSP model. 

7. Clinical_model_dindex_Cindex.R : The meta-estimate of C-index and D-index was compared between clinicopathological model, PCOSP model and integrated clinicopathological and PCOSP model.

8. Existing_Classifiers_Score_Calculation.R : The signature score for each validation cohort Birnbaum et al, 2017 and Chen et al, 2015 classifier was calculated using sig.score function in this script using the classifier genes for each classifier.

9. Existing_classifier_Forestplot: The forestplot of existing classifiers for C-index and D-index is plotted using this script.

10. predict_meta_estimates_function.R: Function to estimate meta-estimates.



