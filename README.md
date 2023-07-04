# Cardiovascular-Risk-Prediction

The data comes from an ongoing cardiovascular study of people living in the Massachusetts town of Framingham. Determine whether the patient has a 10-year risk of developing coronary heart disease (CHD) is the classification goal. Information about the patients is provided by the dataset. It has 15 qualities and nearly 4,000 recordings. Each quality has the potential to be risky. Risk factors can be medical, behavioural, or demographic.


**Approaches:-**

**Step 1:-**
We began by loading the required libraries, mounting the drive, and saving the data in variables in order to derive relevant insights. Viewing and cleaning the data was our first step.


 ![1](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/fc0cc8ac-1f3d-496d-a8a8-0953c2e284f4)


 We next analysed our data distribution using univariate, bivariate, and multivariate plots as the next step in the data analysis and visualisation process. There was a multicollinearity check.


 ![2](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/a6cb492e-e9a1-4e63-b1d0-7bbe774e6d0b)


 ![3](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/cf6c17cd-3af7-477a-827b-ded847047e36)


 ![4](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/d1714fc0-7468-40fc-8ebd-0ed8321fdb09)


 ![5](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/450153a8-2191-4fd4-b80a-038e092000ec)


 ![6](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/5cf4ed0c-a6aa-41aa-bffb-c6be44bf0ba3)


**Step 2:-**
 We tested three hypotheses: first, whether outliers were present using boxplots; second, whether age and cardiovascular risk were related; and third, whether the mean value of total cholesterol was significant using the z test.


**Step 3:-**
Because the median is unaffected by outliers and categorical null values are replaced by the mode, the presence of null values would have produced potential mistakes in the subsequent phases. We also eliminated outliers that had no relevance because all outliers are important for risk prediction and cannot be replaced.

**Step 4:-**
Systolic and diastolic blood pressure were discovered to be closely associated, thus as part of feature engineering, we created a new column called BP. Additionally, the daily column was changed to a categorised column. Our data was severely unbalanced, therefore we utilised SMOTE to construct a balanced set of data. Next, we used hot encoding to create dummy variables for categorical data.


![210253845-e9516403-5ca5-4725-b958-78702ebac7ef](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/40c3dd37-caf3-4a96-8988-9c00a8ae08e6)


**Step 5:-**
The final phase was training the model using various methods; we tried logistic regression, KNN, Naive-Bayes, XGBclassifier, and Random Forest. F1 score and recall were the evaluation criteria utilised to compare the models.


### BEST MODEL

**KNN**

![7](https://github.com/KamalRawalCS/Cardiovascular-Risk-Prediction/assets/138231554/515cf14e-1c6f-4b53-bcc4-db1ebf35640f)


# CONCLUSION:

### EDA :-
1.	Our data set has 17 features & 3390 rows. We studied all these features and have drawn following comclusions:
2.	The very first graphs gives us the distribution of dependent variable and whch shows that very less no of peoples are prone to cardiovascular risk.
3.	Any value outiside the given normal range determines higher risk of cardiovascular risk. Thus, various companies like insurance, healthcare, fitness-nutrition and medical can target this population for better revenue generation.
4.	We have observed that people wether or not smoking are at equal risk of cardio vascular diseases, which suggests companies to target them equally.
5.	Our data shows that people having hypertension are more prone to cardio vascular diseases, very less no. of paitents are on BpMeds, but 50 % of then are at cardiovascular risk, which is significant. Thus, this information can be leveraged by various companies.
6.	Distribution of cardiovascular Risk and Age shows that with increase in age chances of having cardiovascular diseases increases.
7.	Diabetic patients are high risk of getting cardio vascular disease as our data shows; ~ 61% of the diabetic population is at high risk.
8.	Gender distribution shows that males are more prone to cardio vascular risk as compared to females because the frequency of males having smoking habits is more.
9.	Another bivariate plot between Systolic and diastolic BP shows that they are positivly correalted and with increase in any of this values increses the ridk of cardiovascular diseases.
10.	Orderwise correlation shows that age and systolic pressure highly affect our dependent variable.

### Model Training :-
1.	Our dependent variable is "TenyearCHD" which determines, people having cardiovascular issue in ten years of span.
2.	We tried 5 different algorithms for model training namely, logistic regression, KNN, Naive-Bayes, XGBclassifier, RandomForestClassifier.
3.	Evalution metrics for this project were f1 score and recall, as our data was highly imbalance it would have given us false accuracy, f1 which is the averge of presicion and recall might give us better predictions than accuracy. In our case no of False negatives can have a huge bussiness cost, therefore, instead of precision recall is the more appropiate metrics for evalution.
4.	Out of all the five algorithms KNN was found to be more efficient for model training as it has 0.98 F1 score
5.	So we tried setting an optimum hyperparameter to prevent overfitting of the model.




