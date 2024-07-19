# Optimizing-pricing-strategies-for-used-phones-and-tablets-A-comprehensive-analysis

OPTIMIZING PRICING STRATEGIES FOR USED PHONES AND TABLETS: A COMPREHENSIVE ANALYSIS
BACKGROUND:
In the light of growing market for refurbished and used electronic devices, the issue at hand mainly revolves around developing a model that accurately predicts the normalized price of the electronic devices. However, there is absence of precise model which takes into consideration crucial factors like brand, usage history, and device specifications acts a crucial challenge. Developing such models can aid in making informed decisions and promote effective circulation of electronic devices.

PROBLEM STATEMENT:
The main aim is to build model that predicts normalized used price of the refurbished electronic devices. However, the main challenge is to harness data that encompasses device attributes to effectively gauge the value of such devices. The overarching goal is to furnish both the businesses with a reliable model for effective pricing of the devices. It fosters financial prudence, waste minimization in the electronics industry. The project aims to answer the following questions:
1.	How do device attributes and usage history influence the pricing of used and refurbished electronic devices?
2.	What factors influence customer purchase decisions and what pricing strategies can businesses employ to optimize customer retention and competitiveness in the used electronics market?

DATA DESCRIPTION:
The dataset was obtained from Kaggle. Dataset has a record size of 3454 rows and 15 columns. The key variables are - device_brand, os, screen_sizr, 4g, 5g, front_camera_mp, back_camera_mp, internal_memory, ram, battery, weight, release_year, days_used, normalized_new_price, normalized_used_price. The dataset obtained provides insights into customer behavior and demographics. Furthermore, the dataset enables exploratory data analysis to develop a precise model.
METHODOLOGY:
•	Data cleaning is the most important preprocessing step for ensuring reliable data being utilized for modeling. The missing values have been addressed through imputation via mean, median, or mode. 
•	The outliers have not been removed as it is eliminating all the 5G compatible devices, which will affect the analysis of the data.
•	Exploratory Data Analysis (EDA) is vital for understanding the distribution of variables and identify potential patterns. 
•	The mean, standard deviation, minimum, maximum, and correlation were identified to uncover trends or patterns in the dataset.
•	Through visualizations like box plots, bar graphs, scatter plots, and heat maps variable distributions were examined, and potential outliers were identified. These visualizations will aid in the detection of patterns influencing the pricing modeling strategy.
•	Linear regression, multiple regression, and KNN model will be used and evaluated. For selecting the final model, complexity, interpretability, and predictive performance will be taken into consideration while choosing the best model. 
•	The performance of the models will be evaluated through MSE, MSME coefficient. 

FINDINGS (through exploratory data analysis):
•	The dataset comprises mobile phones with varying screen sizes (mean: 13.62 inches) and camera resolutions (rear: 9.48 MP, front: 6.09 MP), alongside diverse internal memory capacities (52.10), RAM (3.96), and battery capacities (mean: 3074.93 mAh). Phones weigh an average of 182.49 grams and were predominantly released between 2013 and 2020.
•	It is observed that “other” brands manufacture a maximum number of phones, at 15.4% of the total share. The second highest share is owned by Samsung with 10.5%, followed by Huawei with 7.72%. 
•	Further, it is observed that Android phones have a significant market share of 92.96%. The total number of devices compatible with 4G and 5G are 66.03% and 97.39% respectively.
•	The relationship between normalized prices for each OS has been plotted which displays the difference between new price and used price. New iOS devices have the highest price, and then followed by Android, Windows, and others. Further, phones compatible with 4G & 5G are priced higher.
•	Through exploration of relationship between normalized prices for release year, it is understood that each year the prices of the new and used phones have been gradually increasing each year. 
•	The scatter plot of screen size vs. normalized price compares the screen size of devices to their normalized new and used prices. It indicates that there is no clear trend suggesting screen size has a strong linear correlation with either new or used device prices. Both new and used prices vary widely across different screen sizes without a distinct pattern. It implies that factors other than screen size may play a more significant role in pricing.
•	The scatter plot between the number of days a device was used and its normalized used price, indicates a negative correlation. The points are densely packed at lower 'days_used' values and spread out as 'days_used' increases. This indicates that there is more variability in the used price of devices that have been used for a longer period.
•	In the heat map, dark red represents a high positive correlation, and dark blue represents a high negative correlation. Lighter colors indicate weaker correlations. It can be understood that larger screen sizes, battery capacity, and device weight are strongly correlated. There is a strong negative correlation between a device’s release year and days used. Additionally, camera quality shows a moderate positive impact on both new and used device prices.
Results:

Linear regression:
•	Statistical Significance: The linear regression for Days Used Vs. Normalized Used price shows that the number of days a device is used has a statistically significant negative impact on its normalized used price (coefficient = -0.0008, p < 0.001), indicating that as devices are used longer, their value decreases, in line with depreciation expectations.
•	Intercept Interpretation: The intercept value of 4.9055 suggests that a device not used at all (0 days) would have a normalized used price of approximately 4.9055 units, representing its initial value before any depreciation.
•	The Adjusted R-squared value of 0.108 implies that the model explains about 10.8% of the variability in the normalized used price, indicating that other unaccounted factors also play significant roles in determining a device's used price.

Multiple regression:
•	Identifying that device valuation is influenced by several factors beyond just usage duration, multiple regression was considered by modeling the target variable as a function of several predictors, offering a more nuanced understanding of how various features impact the normalized used price.
•	The RMSE of 0.2426 and the MAE of 0.1905 both reflect the model’s prediction accuracy, with lower values indicating better performance. 
•	The MPE of -0.6999 and the MAPE of 4.6280% illustrate the model’s average percentage error. 
•	Brands like Realme and BlackBerry, and technology features like 4G capability, significantly increase a device’s resale value, demonstrating the importance of brand reputation and network technology in determining used device prices. 
•	Higher RAM, better camera specifications, and the iOS operating system are associated with higher resale values, underscoring the value consumers place on device performance, photographic capabilities, and premium operating systems.
•	Multiple regression analysis reveals a complex interplay of factors that influence the normalized used price of devices, highlighting the multifaceted nature of device valuation in the used market. Based on this, the businesses can manage inventory with the devices and features that are in demand. For e.g., they can maintain more stock of Realme devices.

KNN:
•	The range of accuracy scores from 85.6% to 89.7% indicates that the KNN model is highly effective at predicting the normalized used price. This high level of accuracy suggests that the model can reliably identify the resale value of devices based on their nearest neighbors in the feature space, making it a valuable tool for stakeholders in the used device market.
•	K = 21 yields the highest accuracy signifies that considering the 21 nearest neighbors provides the best balance for making accurate predictions. These 21 neighbours are alike profiles to the newly introduced data. The businesses can decide the price of given used phone by comparing its profile to the 21 neighbour’s profile. This not only streamlines the valuation process but also ensures consistency and reliability in the pricing strategy, fostering customer trust and potentially increasing the efficiency of the sales process.
•	The choice of K = 7, and the observation that it is odd helps to avoid ties. KNN’s performance suggests a well-tuned model that neither overfits nor underfits the data. A larger K value helps to reduce variance by considering more neighbors, thereby smoothing out predictions. At the same time, choosing an odd number for K helps mitigate potential decision-making ambiguities, further enhancing model reliability.

CONCLUSION:
•	Knowing the attributes that contribute to high/low selling price of refurbished devices will keep the seller informed about the choice of models that will boom in the market of sales of refurbished devices.
•	Multiple regression model aids in determining the relationship between various attributes and the normalized new price. 
•	KNN model has identified 21 nearest neighbors, showcasing the effectiveness of KNN in handling the dataset's complexities. It has demonstrated a high degree of accuracy in predicting the normalized used prices of devices, making it a reliable method for valuation in the used device market. By using these models, the businesses can avoid overpricing and underpricing, thus potentially maximizing profits, improve competitiveness, and optimize inventory management.

