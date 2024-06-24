Blood Donation Forecast:
Blood transfusions are critical in healthcare, saving lives in emergencies and treating various medical conditions. Ensuring a steady supply of blood is a constant challenge. This project aims to address this issue using machine learning to predict future blood donations. Our dataset comes from a mobile blood donation vehicle in Taiwan, collected during blood drives at various universities. We aim to predict if a donor will donate blood the next time the vehicle visits.

Project Overview:
Dataset Description:
The dataset follows the RFMTC marketing model:

R (Recency): Months since the last donation
F (Frequency): Total number of donations
M (Monetary): Total blood donated (in c.c.)
T (Time): Months since the first donation
Target: Binary variable indicating donation in March 2007 (1: donated, 0: not donated)

Data Inspection and Preprocessing:
We began by loading and inspecting the dataset to understand its structure and characteristics. All columns are numerical, making them suitable for building a machine learning model. We renamed the target column for convenience and checked the target incidence, revealing a 76% non-donation rate.

Data Splitting and Model Selection:
We split the data into training and testing sets, maintaining the same target incidence using stratification. We employed TPOT, an Automated Machine Learning tool, to explore various pipelines and identified Logistic Regression as the best model with an AUC score of 0.7850.

Feature Normalization and Model Training:
High variance in the Monetary column prompted us to apply log normalization. This preprocessing step improved the model's performance slightly, achieving a new AUC score of 0.7900 with Logistic Regression.

Conclusion:
The final model provides a valuable tool for forecasting blood donations, aiding in the efficient planning of blood collection drives. Small improvements in model accuracy can significantly impact real-world applications, potentially saving more lives by ensuring a stable blood supply. This project demonstrates the practical application of machine learning in addressing critical healthcare challenges.

Feel free to explore the code and insights provided in this repository to understand the process and methodology in more detail. Contributions and feedback are welcome to enhance this project further.
