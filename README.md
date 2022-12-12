
# Heart Disease Classification

An analysis of the vitals of 1050 patients with and without heart disease. The dataset has been taken from
[Kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset).

The data analysis and modelling can be found in `classification.ipynb`.

## Objectives
- See the distribution of male and females with heart disease.
- See the distribution of people with heart disease with respect to their age.
- Binary classification of dataset into patients with and without heart disease based on the vitals using various models.

## Attribute Information
The dataset has 14 attributes, the 'target' column is the dependent variable.

1. **age**: age in years
2. **sex**: sex (1 = male; 0 = female)
3. **cp**: chest pain type -- Value 1: typical angina -- Value 2: atypical angina -- Value 3: non-anginal pain -- Value 4: asymptomatic
4. **trestbps**: resting blood pressure (in mm Hg on admission to the hospital) trestbps
5. **chol**: serum cholestoral in mg/dl
6. **fbs**: (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
7. **restecg**: resting electrocardiographic results -- Value 0: normal -- Value 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV) -- Value 2: showing probable or definite left ventricular hypertrophy by Estes' criteria
8. **thalach**: maximum heart rate achieved
9. **exang**: exercise induced angina (1 = yes; 0 = no)
10. **oldpeak** = ST depression induced by exercise relative to rest
11. **slope**: the slope of the peak exercise ST segment -- Value 1: upsloping -- Value 2: flat -- Value 3: downsloping
12. **ca**: number of major vessels (0-3) colored by fluoroscopy
13. **thal**: 3 = normal; 6 = fixed defect
14. **target** - diagnosis of heart disease (angiographic disease status) -- Value 0: < 50% diameter narrowing -- Value 1: > 50% diameter narrowing

## Data Cleaning
There are incorrect entries in the dataset that must be deleted. \
https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset/discussion/307455

1. 'thal' should have values 1, 2, or 3 and not 0.
2. 'ca' should have values 0, 1, 2, or 3 and not 4.

According to the definitions of 'thal' and 'ca' in attribute information at the top of the notebook there are certain false entries. These can be deleted using the drop function in pandas.
A total of 25 entries are deleted.

## Data Modelling
The data is preprocessed and split into a train and test set before modelling. Six models are used to classify the data into patients with and without heart disease.
1. Logistic regression
2. KNN
3. Naive Bayes
4. SVC
5. Decision treee classification
6. Random forest classification

## Results and Conclusion
1. More males have heart disease then females
2. Patients in the age group of 40-60 have more heart disease than patients of any other age group.
3. All the above mentioned classification models perform with 100% accuracy except K-nearest neighbors.

| Model                        | Accuracy |
|------------------------------|----------|
| Logistic Regression          | 100%     |
| K-NN                         | 90.73%   |
| Support Vector Machine       | 100%     |
| Naive Bayes                  | 100%     |
| Decision Tree Classification | 100%     |
| Random Forest Classification | 100%     |