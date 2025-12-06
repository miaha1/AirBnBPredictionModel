# AirBnB Prediction Model

[Project Proposal.pdf](https://github.com/user-attachments/files/23979900/Project.Proposal.pdf)
# 1. Introduction
# Background:
Airbnb has ignited a revolution in hospitality, transforming into a global marketplace operating in over
220 countries and fundamentally changing how people travel and find accommodation. Since its founding in
2008, Airbnb has evolved from a simple room-sharing service into a complete ecosystem.
Accurate pricing is crucial for this sharing economic system. Hosts need data-driven guidance to set
competitive prices that maximize profit. Guests benefit from the fair market to make informed booking
decisions. Furthermore, the Airbnb platform needs a robust prediction model to forecast market trends in
advance and make rational business decisions.
Boston is a major tourism and education hub in the United States. The city has distinct seasonal
demand patterns and diverse neighborhoods, which makes Boston a compelling case to explore how geographic
and property-specific factors impact rental- price.
# Problem Explanation:
This project develops machine learning models to predict nightly rental prices for Boston Airbnb
listings. W e use the dataset published by the
“Inside Airbnb” project. The goal of this project is to solve a
supervised regression problem, where we utilize property attributes, host information, location data, and reviews
to predict continuous price values. Previous research shows that Random Forest performs well for this task.
Based on this finding, we will implement Linear Regression as a baseline and Random Forest as our main model.
This comparison will identify the most effective pattern for the Boston market.
# Dataset
Our dataset contains 4419 Boston listings as of September 23, 2025. The dataset includes 79 features
covering a wide range of data of host information: rental property characteristics, location, guest reviews, and
listing prices. After initial quality assessment, 75 out of 79 features have sufficient data (percentage of missing
values < 50%). This dataset provides a solid foundation for building our models.
The preliminary analysis shows rational price patterns. Prices range from $26 to $805 per night. The
mean price is $234.85 and the median is $201. Since the mean exceeds the median, the distribution is
right-skewed, indicating that some high-quality listings pull the average price upward. The standard deviation is
$160.76, which suggests a large price variation across listings.This variation motivates us to do further
normalization to improve model performance.
Room type distribution shows entire homes contribute 67.66% of listings, followed by private rooms at
30.91%. The 25 neighborhoods provide geographic diversity. Key numeric features include accommodates
(mean 3.38, max 16), bedrooms (mean 1.53), bathrooms (mean 1.28), and number of reviews (mean 52.75, max
989). These property size metrics typically show strong positive correlations with price and will serve as primary
predictors.
# Evaluation method
We will assess model performance using two key matrics. Mean Absolute Error (MAE) measures the
average prediction error in dollars. It shows the difference between our prediction and actual price. R^2
coefficient of determination measures explained variance. It reflects the proportion of price variance in prices
explained by model.
Data will be split by the ratio of 8 : 1 : 1 for training, validation and test sets, with cross-validation
during training to reduce overfitting.
# Reference
[1] Dataset available at: https://insideairbnb.com/boston/
[2] A. Lektorov, E. Abdelfattah and S. Joshi,
"Airbnb Rental Price Prediction Using Machine Learning Models,
"
2023 IEEE 13th Annual Computing and Communication W orkshop and Conference (CCWC), Las V egas,
NV , USA, 2023, pp. 0339-0344, doi: 10.1109/CCWC57344.2023.10099266.
[3] Zhang, A. X., Noulas, A., Scellato, S., & Mascolo, C. (2013, September). Hoodsquare: Modeling and
recommending neighborhoods in location-based social networks. In Social Computing (SocialCom), 2013
International Conference on (pp. 69-74). IEEE. http://arxiv.org/pdf/1308.3657.pdf
[4] Hill, D. (2015). How much is your spare room worth?. Spectrum, IEEE, 52(9), 32-58.
