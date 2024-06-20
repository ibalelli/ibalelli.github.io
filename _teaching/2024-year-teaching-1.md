---
title: "Modélisation statistique pour les données complexes et le Big Data"
collection: teaching
type: "3rd year Bachelors degree course"
permalink: /teaching/2024-year-teaching-1
venue: "IUT Nice Côte d’Azur, BUT Science des Donne, S6"
date: 2024-04-01
location: "Sophia Antipolis, France"
---

Project on statistical modeling for complex data and big data, for 3rd year BUT students.

Cours description
======
**Objective:** Statistical modeling based on a given dataset, following all the steps required to understand its variables, process them and model them for a given objective. 

**Method:** 
* Individual work, in groups of 2 or 3 students (chosen at random), using Python.
* Objectives will be progressively set, every 2 sessions each group will have to provide the progress of their work (in the form of a notebook).

**Evaluation:**
* *Continuous assessment (1/5):* Work progress.
* *Written report (2/5):* A written report (clean) in which all the results obtained are brought together, commented on and put into perspective. Due on 13/06 (at the end of the session).
* *Oral exam (2/5):* 17/06 from 8am. Each group will present its work in the form of a talk (with support). 15-minute presentation + 15-minute Q&A.

Groups (Randomly defined)
======
* *G1* CROMBET, NIASSY
* *G2* FALAIS, EZ-ZEROUALI
* *G3* VIAUD, CARTON
* *G4* VIGLIETTI, HIRSINGER
* *G5* GOURAR, DIALLO
* *G6* JOUNDI, LOFTI, NOUIRA

Data (training and test sets)
======
[Data G1 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G1.zip) <br/>
[Data G2 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G2.zip) <br/>
[Data G3 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G3.zip) <br/>
[Data G4 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G4.zip) <br/>
[Data G5 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G5.zip) <br/>
[Data G6 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G6.zip) <br/>

1st Step: data analysis and preparation
======

* Dataset size and type. Are there any missing data? If so, we will eliminate them (for now).

* How many classes and elements/class?

* Selection of the most significant variables: explore and suggest several methods. Are there any collinearities? Which variables will you retain? How are the selected variables distributed?

* Pay particular attention to the graphic visualization of your results.


2nd Step: choice of classification model, hyperparameters tuning
======

* Preparation of training dataset for cross-validation (choice of number of folds, split).

* Several models can be adapted to the task at hand: logistic regression, SVM, random forests, xgboost,...
    * Initialize the models
    * Test them separately (k-fold cross-validation)
    * Tune their hyperparameters

* Compare the performance of the different models tested (each with its final choice of hyperparameters).

* Which model/parameters did you choose?

* Could a voting strategy improve predictions?

* With the final model chosen, predict the labels of the test dataset (to be saved on a .csv and sent with the notebook).

* Pay particular attention to the graphical visualization of your results.

3rd Step: handling missing data
======

* Here below, you can download the complete training and testing data (the ground truth for evaluating the imputation methods). Note that this time the datasets include all features' names. 

[Data G1 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G1_complete.zip) <br/>
[Data G2 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G2_complete.zip) <br/>
[Data G3 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G3_complete.zip) <br/>
[Data G4 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G4_complete.zip) <br/>
[Data G5 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G5_complete.zip) <br/>
[Data G6 (.zip)](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Data_G6_complete.zip) <br/>

* Check missing data patterns in data and data_test.

* Several methods can be used to impute these data (take a look at the [sklearn.impute](https://scikit-learn.org/stable/api/sklearn.impute.html) package; a method based on random forests is implented [here](https://pypi.org/project/MissForest/)): test them and evaluate their ability to impute your missing data (using cross-validation).

* Apply the classification models tested in the previous step to the full (imputed) dataset: do you observe any performance improvement?

* Could *multiple imputation* methods provide better classification results?

* Pay particular attention to the graphical visualization of your results.

Interpretation and written report
======

[Template](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Report_template.docx) <br/>

* The data you've handled so far has been extracted from the [Breast Cancer Wisconsin dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#breast-cancer-dataset), which contains 30 features calculated from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe the characteristics of the cell nuclei present in the image and are used to predict whether the tumor mass is benign (0) or malignant (1).

* We have artificially introduced missing data, which is frequent in the clinic, where errors can occur at various points in the data acquisition or transcription phases.

* The analysis you have carried out could answer a very simple but relevant clinical question: could you propose a tool to help classify a new patient's tumor mass from measurements (possibly partly missing) extracted from a FNA?

* Use this information to guide the writing of your report and work out your presentation. 

* Of note, this dataset has been widely explored, and you can find articles and several projects on Kaggle that use it.

Final grades
======

[Notes](http://ibalelli.github.io/files/course_material/mod_stat_BUT/Notes_BD.pdf) <br/>

<!---
Notes
======
-->