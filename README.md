# Country Schools Dataset Analysis

## 1. Project Overview

This project was carried out as part of Lab 2 to practice data preprocessing, anomaly detection, and cluster analysis using Python. The main purpose was to analyze school installation data, identify unusual records, and group counties with similar installation characteristics.

The analysis was performed using Kaggle Notebook with Python libraries such as Pandas, NumPy, Matplotlib, and Scikit-learn.

## 2. Dataset Description

The Country Schools dataset contains information about schools in 47 counties in Kenya. It includes the total number of schools, installed schools, pending schools, installation percentages, and the number of installed LDD and TDD devices.

The original dataset contained 50 rows and 8 columns. During preprocessing, two empty records and one TOTAL summary row were removed, leaving 47 records for analysis.

## 3. Data Preprocessing

Before starting the analysis, the dataset was checked for missing values, data types, and duplicate records.

The following activities were performed:

- Removed records with missing county names.
- Removed the TOTAL row because it represented a summary of all counties.
- Converted installation percentages from text into numerical values.
- Used descriptive statistics to understand the distribution of the data.
- Standardized six numerical features before applying K-Means clustering.

After cleaning, the dataset was ready for analysis.

## 4. Anomaly Detection

Two methods were used to identify unusual records: the Interquartile Range (IQR) method and Isolation Forest.

### IQR Method

The IQR method was used to identify values outside the normal statistical range of each numerical feature.

The method identified two counties, Kitui and Makueni, as potential anomalies because of their unusually high school installation counts.

### Isolation Forest

Isolation Forest was applied to identify unusual patterns across multiple numerical features.

The model identified three anomalous counties: Turkana, Kitui, and Kakamega.

Turkana had a low installation percentage of 10.34%, Kitui had a high number of installed schools, and Kakamega had the highest number of installed LDD devices.

The two methods produced different results, but both identified Kitui as an anomaly.

## 5. Cluster Analysis

K-Means clustering was used to group counties according to similarities in their school installation characteristics.

Before clustering, the numerical features were standardized using StandardScaler.

The Elbow Method and Silhouette Score were used to evaluate the appropriate number of clusters. The highest Silhouette Score was approximately 0.425 at K=8, so eight clusters were selected for the analysis.

The results showed that counties have different installation patterns.

Cluster 3, containing Kitui and Makueni, had the highest average installation percentage of 95.42%.

Cluster 5, containing Mandera, Marsabit, Wajir, Garissa, Turkana, and Samburu, had the lowest average installation percentage of 13.08%.

Other clusters contained counties with moderate or high installation percentages and different numbers of installed and pending schools.

## 6. Data Visualization

Several graphs were created to help understand and interpret the results.

These included a histogram, boxplot, anomaly detection scatter plot, Elbow Method graph, Silhouette Score graph, K-Means scatter plot, and bar chart showing average installation percentages by cluster.

The graphs helped show differences between counties, identify unusual observations, and compare installation progress across clusters.

## 7. How to Run the Project

The project was developed using Kaggle Notebook.

To run the analysis:

1. Open Kaggle and create a new notebook.
2. Upload the Country Schools CSV dataset.
3. Import the required Python libraries.
4. Load the dataset using Pandas.
5. Run the notebook cells from beginning to end.
6. Examine the generated tables, graphs, and interpretations.

The main libraries used are Pandas, NumPy, Matplotlib, and Scikit-learn.

## 8. Conclusion

Through this lab, I gained practical experience in preparing datasets and applying machine learning techniques to real data.

The anomaly detection methods helped identify counties with unusual school installation figures, while K-Means clustering grouped counties with similar characteristics.

The results showed that installation progress differs across counties, with some having high installation coverage and others still having many pending schools.

Overall, this lab helped me understand how Python can be used for data cleaning, visualization, anomaly detection, and clustering to support data analysis and decision-making.# country_school-lab
