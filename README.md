# The `AMBITION` study
# `A`ssessing `M`itochondrial `BI`oenergetics in chronic coronary artery disease: A `T`ranslational study `I`ntegrating multi`O`mic analysis of human left ventricular tissue and qua`N`titative stress perfusion cardiovascular magnetic resonance

The notebook contains:
Metabolomics data of patients myocardial biopsies that were analysed by liquid chromatography-mass spectrometry (LC-MS).

## Reproducibility
Code for the R analysis can be reproduced by following the script in `AMBITION_Metabolomics.Rmd`. This includes the data normalisation, differential metabolite analysis and all subsequent plots (PCA plot, Correlation plot, Volcano plot).

Metabolic signatures used for pathway analysis where manually assigned based on our a priori knowledge.

## Data
The Metabolomics data of the patients myocardial biopsies will be deposited with the manuscript (under revision). LC-MS data aquistion has been performed by the Frezza Laboratory, CECAD Research Center, Faculty of Medicine, University Hospital Cologne, Germany. Input data will be available upon publication in the folder `"InputData_AMBITION-Metabolomics"`:

- `AMBITION_RawData.csv` (Metabolomics results)
- `Template_MetabolicPathways.csv` (Metabolite names and associated pathways)

After performing data filtering and normalisation (80%-filtering rule, missing value imputation, total/ion count normalisation) and outlier detection based on quality control (muma analysis, for details see html and folder `"Muma"`), the results will be saved in the folder `"OutputData_AMBITION-Metabolomics"`upon publication:

- `Sheet2_MVI-TIC-normalised_OutliersMarked.csv`

Using the normalised data `Sheet2_MVI-TIC-normalised_OutliersMarked.csv`, we removed the outliers and 
1. calculated the mean of the analytical replicates. The results will be saved in the folder `"OutputData_AMBITION-Metabolomics"`upon publication:

- `Sheet3_MVI-TIC-normalised_Means.csv`

2. Performed differential metabolite analysis comparing `Ischemia versus Remote` using the analytical replicates for the statistics. Here we performed the t-Test and p-value adjustment using Benjamini Hochberg. The results will be saved in the folder `"OutputData_AMBITION-Metabolomics"`upon publication:

- `Sheet4_DMA_ISCHEMIAvREMOTE.csv`

Lastly, using the normalised data means `Sheet3_MVI-TIC-normalised_Means.csv`, we performed differential metabolite analysis comparing `impaired LVEF versus preserved LVEF`. Here we performed the Mann-Whitney-Wilcoxon Test and p-value adjustment using Benjamini Hochberg. The results will be saved in the folder `"OutputData_AMBITION-Metabolomics"`upon publication:

- `Sheet5_DMA_Impairedvspreserved_LVEF.csv`

## Figures
Generated figures can be found in the html files or in the folder `"Figures_AMBITION-Metabolomics"` upon publication.
