# MSCS 634 Lab 2: KNN and Radius Neighbors Classification

## Purpose

The purpose of this lab is to evaluate and compare the performance of K-Nearest Neighbors (KNN) and Radius Neighbors classifiers using the Wine dataset from scikit-learn. The lab examines how different values of k and radius affect classification accuracy and uses visualizations to compare the performance trends of both models.

## Dataset

The Wine dataset contains 178 observations, 13 numerical features, and 3 wine classes. The features represent different chemical properties of wine. The dataset was split into 80% training data and 20% testing data using stratified sampling.

## KNN Results

The KNN classifier was evaluated using k values of 1, 5, 11, 15, and 21.

- k = 1: Accuracy = 0.7778
- k = 5: Accuracy = 0.8056
- k = 11: Accuracy = 0.8056
- k = 15: Accuracy = 0.8056
- k = 21: Accuracy = 0.8056

The results show that accuracy improved when k increased from 1 to 5. The accuracy then remained stable for the larger k values that were tested.

## Radius Neighbors Results

The Radius Neighbors classifier was evaluated using radius values of 350, 400, 450, 500, 550, and 600.

- Radius = 350: Accuracy = 0.7222
- Radius = 400: Accuracy = 0.6944
- Radius = 450: Accuracy = 0.6944
- Radius = 500: Accuracy = 0.6944
- Radius = 550: Accuracy = 0.6667
- Radius = 600: Accuracy = 0.6667

The highest Radius Neighbors accuracy occurred at radius 350. Increasing the radius generally reduced classification accuracy because more distant observations were included in the neighborhood.

## Key Insights

KNN performed better than Radius Neighbors for the tested parameter values. The best KNN accuracy was 0.8056, while the best Radius Neighbors accuracy was 0.7222.

The results demonstrate that parameter selection has an important effect on classification performance. KNN provided more stable performance after k reached 5, while Radius Neighbors was more sensitive to changes in the radius value.

## Challenges and Decisions

One challenge was selecting appropriate parameters for each classifier. The required values from the lab instructions were used so that the performance of both models could be compared consistently.

The Wine dataset was used without feature scaling because the required Radius Neighbors values were relatively large and were intended to work with the dataset's original feature scales. Stratified sampling was used during the train-test split to preserve the class distribution in both datasets.

## Files

- `Lab2_KNN_RNN_Wine_Classification.ipynb` - Jupyter Notebook containing the complete analysis, model implementation, results, plots, and discussion.
- `README.md` - Summary of the lab purpose, results, observations, challenges, and decisions.

## Conclusion

This lab demonstrated how KNN and Radius Neighbors classifiers respond to changes in their main parameters. KNN produced the stronger results for this dataset, while Radius Neighbors accuracy decreased as the radius increased. The experiment highlights the importance of choosing suitable neighborhood parameters when using distance-based classification models.