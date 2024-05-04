# Logistic_Regression_Analysis
The dataset is from the Kaggle website (https://www.kaggle.com/datasets/iamsouravbanerjee/house-rent-prediction-dataset/data), uploaded by SOURAV BANERJEE. This data is collected from a housing website (https://www.magicbricks.com/). This dataset has data about housing information of more than 4700 available residential propertie in India, providing insights into housing features and price prediction. This dataset includes 12 variables, such as BHK, Rent, Floor, Area.Type, etc, and 4746 observations. In this case, it provides insights into the correlation between variables like Size, Floor and the house's price.
# Research Question
This project aims to investigate if there's a linear relationship between Rent and Size. The independent variables are Size, and the dependent variable is Rent. My hypothesis is that there is a positive linear relationship between Size and Rent. Ideally, I think the data like location index, furnished status can help to make the research more comprehensive. My motivation for this research is to better know about housing properties and have more accurate predictions toward the rent of the housing properties. 

- Size (independent variable): Size of the Houses/Apartments/Flats. It's a numerical data. Unit of variable is Square Feet. According to the summary, the Size variable has a minimum at 10.0, a median at 850.0, a max at 8000.0, and a mean at 967.5.
- Rent (dependent variable):Rent of the Houses/Apartments/Flats. It's a numerical data. According to the summary, the Rent variable has a minimum at 1200, a median at 16000, a max at 3500000, and a mean at 34993.

# Interpretations of the results

According to the summary table, there seems to be a positive linear relationship between Size and Rent:$Rent=0.001*Size+9.010$ (after rescaling Rent to normal distribution). This indicates that for 1 unit of increase in Size, there'll be 0.001 unit of increase in Rent. According to the scatter plot and the regression line in the plot, we can also see a linear positive relationship between Size and Rent, which aligns with the statistical findings. At the same time, the p-value is less than 2.2e-16, which is close to 0, indicating a statistically significant relationship between Size and Rent (p<0.01). However, the multiple R-squared is 0.2128, and the adjusted R-squared value is 0.2179, indicating a weak positive linear correlation (r-squared > 0.2) between the Size and Rent. 

In conclusion, from the surface, the data suggests that there may be a weak positive linear relationship between Size and Rent. However, I think the current statistical evidence supports my hypothesis that there's a linear relationship between Size and Rent, but it does not necessarily prove it. To be specific, the linear regression model has assumptions of linearity, normally distributed residuals, and homoskedasticity, which need to be met in order to be a linear relationship. 

In addition, the weak correlation also implies that although Size and Rent are positively correlated, making predictions based only on Size is insufficient. Due to this limitations, I think predicting Rent only based on Size may be insufficient. For further analysis, as the rent depends on several variables including size, location, etc., I will conduct multivariate regression model to make more accurate, precise predictions about the housing rent.

# Diagnostics

To further look at this linear relationship, I explored the distribution of the residuals. According to the Residuals vs. Fitted plot, the residuals do roughly form a “horizontal band” around the 0 line, indicating that the variances of the error terms are equal, showing that the assumption of homoscedasticity (constant variance of errors) is true. There's only one independent variable, so the assumption of multicollinearity is true. For the linearity, I looked at the scatterplot and I think the linearity is shown in the graph. For the Q-Q plot, I observe that the points do roughly fit the straight line. This indicates that the residuals may be normally distributed. However, the Shapiro-Wilk normality test shows that the residues do not have a normal distribution (p<0.05). 

In conclusion, the assumption of homoscedasticity is met, and the assumption of the linearity is met. Furthermore, although the QQ-plot suggests that the residuals are normally distributed, the Shapiro-Wilk normality test shows that they are not normally distributed. Therefore, although the statistics table suggests that it seems to be a linear positive relationship, using the linear model for this dataset is not appropriate, and there are concerns about the accuracy of the linear regression model.

<img width="563" alt="image" src="https://github.com/SophieJiaBo/Logistic_Regression_Analysis/assets/168926944/b0ce93a9-420c-4f81-91d0-2b56b6beb7a3">
<img width="563" alt="image" src="https://github.com/SophieJiaBo/Logistic_Regression_Analysis/assets/168926944/a14036ee-e679-42a2-b503-ee5de3415e1d">
<img width="529" alt="image" src="https://github.com/SophieJiaBo/Logistic_Regression_Analysis/assets/168926944/5072a36e-9090-45ff-8deb-97741f1ad414">




