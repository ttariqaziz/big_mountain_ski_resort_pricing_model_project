# big_mountain_ski_resort_pricing_model_project

This data science project's primary purpose is to develop a pricing model for Montana ski resort tickets. The business team understands that the returns are getting low, relative to its position in the market. This model will guide them for future investment plans. 

<img src = "https://github.com/ttariqaziz/big_mountain_ski_resort_project/blob/main/Plots/Region_state.png">
<img src = "https://github.com/ttariqaziz/big_mountain_ski_resort_project/blob/main/Plots/Average_ticket_price.png">
<img src = "https://github.com/ttariqaziz/big_mountain_ski_resort_project/blob/main/Plots/Price_weekend_weekdays.png">
<img src = "https://github.com/ttariqaziz/big_mountain_ski_resort_project/blob/main/Plots/Features_heatmap.png">
<img src = "https://github.com/ttariqaziz/big_mountain_ski_resort_project/blob/main/Plots/Random_forest_feature_importance.png">

# Key Takeaways
Based on the provided exploratory data analysis, here are the key points:

1. Features in the Data:
The dataset includes both numerical and categorical features. Numerical features include attributes like "AdultWeekend," "LongestRun_mi," "NightSkiing_ac," "Runs," "SkiableTerrain_ac," and so on. Categorical features include "Name," "Region," and "State," which represent the name of the resort, its region, and the state it's located in, respectively.


2. Relationship Between State and Ticket Price:
There is a suggested pattern of a relationship between the "State" feature and the "AdultWeekend" ticket price. Different states have different average ticket prices for skiing resorts. For instance, resorts in Alaska generally have lower ticket prices compared to resorts in Arizona.

3. Feature Selection for Subsequent Modeling:
Given the potential relationship between state and ticket price, the "State" feature should be considered for inclusion in subsequent modeling, as it appears to be a relevant predictor of the target variable, "AdultWeekend." Other features like "SkiableTerrain_ac," "Snow Making_ac," "averageSnowfall," "daysOpenLastYear," "resort_days_open_state_ratio," and "resorts_per_100kcapita" might also be valuable for modeling.

4. Aspects to be Wary of in Feature Selection:
While performing feature selection, it's important to be cautious of potential multicollinearity between features. For example, "total_chairs" and "total_chairs_runs_ratio" might be highly correlated. Additionally, the ratio-based features like "fastQuads_runs_ratio" and "fastQuads_skiable_ratio" could have a high correlation with their respective base features ("fastQuads" and "SkiableTerrain_ac"), which might lead to redundancy in the model.

5. Handling State Labels:
The "State" labels are categorical and need to be properly encoded before using them in a predictive model. This could be achieved using techniques like one-hot encoding or label encoding. However, considering that there might be some inherent relationship between states (e.g., geolocation, climate), a straightforward one-hot encoding might not be the best choice. Alternatively, you could explore creating additional features that capture regional or geographical information.

6. Choice of Target Feature:
The chosen target feature for modeling is "AdultWeekend," which represents the price of an adult weekend ticket. This is likely to be influenced by a combination of factors, including resort characteristics, location, and other amenities.


In conclusion, the data shows a potential relationship between state and ticket price, which suggests that "State" should be considered as a feature in subsequent modeling. Careful consideration of feature selection, addressing potential multicollinearity, and handling categorical features like "State" are important steps to ensure an effective predictive model.


