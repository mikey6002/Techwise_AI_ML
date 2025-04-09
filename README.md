
# ML for Public Safety: Predictive Crime Modeling and Decision Support in the LA region 

# Introduction
This project focuses on predicting insights for crime prevention and resource allocation in the Los Angeles area. Crime remains a persistent issue in urban communities, and we were motivated to explore the factors that influence criminal behavior in order to identify key elements contributing to criminal activity. By leveraging machine learning, our goal is to uncover patterns in crime data that can support proactive interventions and informed decision-making by public safety organizations.

# Bias and Ethical Considerations
Through our research of similar projects, we found that including demographic and socio-economic data—such as race, income level, or indicators like graffiti—can unintentionally introduce racial and socio-economic bias into predictive models. As a result, we made a conscious decision to avoid using such features in order to reduce the risk of reinforcing existing disparities and ensure a more equitable approach to crime prediction.

# Methodology
**Data Collection**: The dataset used for this project was obtained from Kaggle and closely mirrors the crime report data published by the Los Angeles Police Department (LAPD). While not sourced directly from the LAPD, the dataset includes similar fields such as crime type, location, date, and time of incident. This allowed us to analyze realistic trends and patterns in crime within the LA area while working with a publicly accessible dataset suitable for machine learning applications.

**Data Cleaning:**
To prepare the dataset for analysis, we performed several data cleaning steps. We began by removing duplicate records to ensure the integrity of the data. Null or missing values were handled through imputation or removal, depending on the context and frequency of the missing data. Additionally, we dropped certain columns and specific crime types that had the potential to introduce socio-economic or demographic bias. This included features such as demographic indicators and proxies like graffiti, Vandalism, Bike Theft..etc , which could disproportionately reflect over-policed areas rather than objective crime patterns. These steps were taken to promote fairness and reduce bias in our predictive modeling process.

**Model Selection and Design:**
We experimented with several machine learning models to evaluate their effectiveness in predicting crime patterns. These included K-Nearest Neighbors (KNN), Random Forest combined with SMOTE (Synthetic Minority Over-sampling Technique) to handle class imbalance and and Polynomial Regression.

**Results:** To model and predict hourly crime frequency, we applied a polynomial regression model using temporal features, including hour of the day, season, and weekday. The results reveal that crime frequency is lowest during the early morning hours (3 AM to 6 AM) and begins to rise steadily throughout the day, peaking significantly around 12 PM and again between 5 PM and 9 PM. This suggests a correlation between daily routines, human activity levels, and crime incidence. 

To predict crime hotspots across the Los Angeles area, we implemented a Random Forest Classifier enhanced with SMOTE to address class imbalance. The model performs very well at detecting actual hotspots, but struggles more with identifying non-hotspot areas
