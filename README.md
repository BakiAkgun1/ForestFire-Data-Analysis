# Forest Fires Dataset Analysis

This project involves an in-depth analysis of the Forest Fires dataset. The dataset includes various features related to forest fire occurrences, such as temperature, wind, rain, and area burned. The analysis includes statistical tests to determine the relationships between these features and visualizations to illustrate these relationships.

## Dataset

The Forest Fires dataset is available from the UCI Machine Learning Repository. It includes attributes like temperature, wind, rain, and the area affected by fires.

## Libraries Used
Pandas: For data manipulation and analysis.

Matplotlib: For creating static, animated, and interactive visualizations.

Seaborn: For statistical data visualization.

Scipy: For scientific and technical computing, including statistical tests.

## Visualizations

### Pairplot
A pairplot was generated to visualize the relationships between `temp`, `wind`, `rain`, and `area`.
![image](https://github.com/user-attachments/assets/88caba93-e219-4dc2-85ff-ff404c65e5ee)


### Boxplot
A boxplot was created to show the distribution of the `area` affected by fires with respect to the `wind` variable.
![image](https://github.com/user-attachments/assets/7a949355-5c9b-45e1-a905-73f7fdb11d74)

### Lineplot
A lineplot was created to visualize the relationship between `rain` and `temp`.
![image](https://github.com/user-attachments/assets/311cf3eb-0b07-41b2-bebb-f8963273c51e)

### Correlation Matrix
A correlation matrix was generated to explore the relationships between the numerical features, excluding `month` and `day`.

![image](https://github.com/user-attachments/assets/2027dd30-b0a3-4aac-af8b-70deb0ab2c4d)


### Histogram
A histogram was created to visualize the distribution of the `temp` variable.
![image](https://github.com/user-attachments/assets/ec3941ab-c9ad-4b54-92a7-ef5c68eb5688)


## Statistical Tests

### Shapiro-Wilk Test (Temperature and Wind)
The Shapiro-Wilk test was used to assess the normality of the temperature and wind data.

- **Temperature**
  - Statistic: 0.9868
  - p-value: 0.0001256
  - **Interpretation**: The data does not follow a normal distribution.

- **Wind**
  - Statistic: 0.9673
  - p-value: 2.493e-09
  - **Interpretation**: The data does not follow a normal distribution.

### D'Agostino's K^2 Test (Temperature and Wind)
The D'Agostino's K^2 test was used to check for normality.

- **Temperature**
  - Statistic: 9.6946
  - p-value: 0.007849
  - **Interpretation**: The data does not follow a normal distribution.

- **Wind**
  - Statistic: 25.2421
  - p-value: 3.301e-06
  - **Interpretation**: The data does not follow a normal distribution.

### Anderson-Darling Test
The Anderson-Darling test was used to check if the data follows a specific distribution.

- **Temperature**
  - Statistic: 1.8121
  - Critical Values: [0.572, 0.651, 0.781, 0.911, 1.084]
  - **Interpretation**: The data does not follow a normal distribution.

- **Wind**
  - Statistic: 4.3432
  - Critical Values: [0.572, 0.651, 0.781, 0.911, 1.084]
  - **Interpretation**: The data does not follow a normal distribution.

### t-Test
A t-Test was conducted to compare the means of two independent groups.

- **Statistic**: 0.0974
- **p-value**: 0.9224
- **Interpretation**: There is no significant difference between the two groups.

### Chi-Square Test
A Chi-Square test was used to examine the association between categorical variables.

- **Statistic**: 64.2383
- **p-value**: 0.5384
- **Interpretation**: There is no significant association between the variables.

### Pearson Correlation Coefficient (Temperature-Area)
This test measures the strength and direction of the linear relationship between two continuous variables.

- **Correlation**: 0.0978
- **p-value**: 0.0261
- **Interpretation**: There is a weak but statistically significant positive correlation.

### Spearman Rank Correlation Coefficient (RH-Area)
This non-parametric test assesses the strength and direction of the association between two ranked variables.

- **Correlation**: -0.0242
- **p-value**: 0.5827
- **Interpretation**: There is no significant correlation.

### Kolmogorov-Smirnov Test (Month-Area)
This test compares the distributions of two samples.

- **Statistic**: 0.1124
- **p-value**: 0.1917
- **Interpretation**: There is no significant difference in the distributions.

## Conclusion
The analysis of the Forest Fires dataset revealed that many of the variables do not follow a normal distribution, as indicated by the Shapiro-Wilk, D'Agostino's K^2, and Anderson-Darling tests. The t-Test and Chi-Square tests showed no significant differences or associations between the tested groups and variables. However, the Pearson correlation test found a weak but statistically significant positive correlation between temperature and area burned. This information can guide further data preprocessing and modeling efforts.

