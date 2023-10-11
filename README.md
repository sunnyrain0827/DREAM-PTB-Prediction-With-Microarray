# Prediction of Preterm Birth by Maternal Blood Omics


## Background:
Current approaches to establish gestational age rely on patient’s recollection of her last menstrual period and/or ultrasound, with the latter being not only costly but also less accurate if not performed during the first trimester of pregnancy. 
Therefore development of an inexpensive and accurate molecular clock of pregnancy would be of benefit to patients.
> Preterm birth (PTB), defined as giving birth prior to completion of 37 weeks of gestation, is the leading cause of newborn deaths and long-term complications including motor, cognitive, and behavioral impairment. Approximately one third of preterm births are medically indicated due to maternal or fetal conditions; the other two-thirds are categorized as spontaneous preterm births that include spontaneous preterm labor and delivery with intact membranes (sPTD) and preterm premature rupture of the membranes (PPROM).

## Dataset:
The original dataset could be found at https://www.synapse.org/#!Synapse:syn22127152/files/ 


## Method:
We predicted Control vs. sTPD and Control vs. PPROM using microarray data.
Combined differential expression, co-expression, survival analysis and classification.
Conducted model evaluation with logistic regression, SVM, and RF classifiers utilizing 5-fold cross-validation.

In the folder `data`,
- The two top tables store top 1000 differentially expression genes (sorted by P value) in Control vs. sPTD and Control vs. PPROM respectively, created in R using the package `limma`. They can be reproduced in `DREAM_Differential expression analysis.Rmd`.
- The concordance results store top survival-related genes (sorted by absolute difference between the concordance indices and 0.5, higher indicates more influential), created in Python using the library `lifelines`. They can be reproduced in `DREAM_Survival analysis.ipynb`.

## Result:
SVM demonstrated superior performance, achieving an AUC of 0.76 specifically for the 27-33 weeks gestation period.

## Future Direction:
Compare autoencoder and SVM-RFE for dimensionality reduction.




