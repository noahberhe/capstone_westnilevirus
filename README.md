# Capstone: West Nile Virus
<img src="http://imgur.com/1ZcRyrc.png" width="60">

## Competition Description:

West Nile virus is most commonly spread to humans through infected mosquitos. Around 20% of people who become infected with the virus develop symptoms ranging from a persistent fever, to serious neurological illnesses that can result in death.

In 2002, the first human cases of West Nile virus were reported in Chicago. By 2004 the City of Chicago and the Chicago Department of Public Health (CDPH) had established a comprehensive surveillance and control program that is still in effect today.

Every week from late spring through the fall, mosquitos in traps across the city are tested for the virus. The results of these tests influence when and where the city will spray airborne pesticides to control adult mosquito populations.

Given weather, location, testing, and spraying data, this competition asks you to predict when and where different species of mosquitos will test positive for West Nile virus. A more accurate method of predicting outbreaks of West Nile virus in mosquitos will help the City of Chicago and CPHD more efficiently and effectively allocate resources towards preventing transmission of this potentially deadly virus.

Submissions are evaluated on area under the ROC curve between the predicted probability that West Nile Virus is present and the observed outcomes.

## Approach Summary:
Data Analysis:
- 
- Matplotlib, Seaborn to visualise key features.

Data Pre-Processing:
- 
- PCA used to compress weather features
- RandomOversampling to deal with 5% representation from the minority class

Modelling:
- 
- Imblearn pipeline to allow correct re-sampling during GridSearchCV cross-validation
- Classification models compared: Logistic Regression, Decision Tree, Random Forest, Bagging, Gradient Boosting.
- Cross-validation scoring method = roc-auc

Prediction:
- 
- Tableau used to map quality of predictions geographically and temporally.

Outcome:
-
- Gradient Boosting was the selected classifier, however despite achieving a cross-validated auc of 82%, the test score was 66%. This overfitting problem is something I looked into after the course was over, as documented in the Python Notebook.
