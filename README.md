# Uber Dynamic Pricing Prediction Model

## Project Overview
This project is focused on predicting the optimal ride price for Uber using a machine learning model based on various factors such as pickup location, drop-off location, time of day, and traffic conditions. The model is designed to dynamically adjust pricing in real-time, enabling Uber to optimize revenue and manage demand fluctuations.

## Model Used
### 1. **Gradient Boosting Regressor (UberPricingModel)**
The chosen model for this project is a **Gradient Boosting Regressor**, a powerful ensemble learning algorithm that builds multiple decision trees and combines them to improve prediction accuracy. This model was selected because it balances bias and variance well, making it highly suitable for predicting dynamic pricing, which involves multiple interacting factors.

- **Test Loss**: 0.5576 (Mean Squared Error)
- **Test Accuracy**: 85.9%
- **Training Time**: 135.67 seconds

## Key Features and Approach
The data for this project includes a variety of features that are relevant to predicting Uber's dynamic pricing:

1. **Time-based features**: The hour of the day, day of the week, and whether the ride is happening on a weekend or a holiday.
2. **Location-based features**: Distance between pickup and drop-off points, urban versus rural locations.
3. **Demand indicators**: Variables related to surge pricing and demand fluctuations at different times.
4. **External factors**: Traffic and weather conditions that could affect travel time and ride prices.

### Feature Engineering
The following key steps were undertaken for feature engineering:
- **Distance Calculation**: Computed as the Haversine distance between pickup and drop-off locations.
- **Time Binning**: Hours of the day were categorized to capture rush hours versus off-peak times.
- **Weather Data Integration**: If available, weather conditions were added to enhance model predictions for potential delays.

## Dependencies
To run the code, the following Python libraries are required:
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
