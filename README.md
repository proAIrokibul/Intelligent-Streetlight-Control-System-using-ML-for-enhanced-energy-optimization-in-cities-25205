# **Streetlight Control System Using Machine Learning for Enhanced Energy Efficiency in Smart Cities**

## **Project Overview**
In the era of smart cities, energy efficiency is paramount. This project presents an intelligent streetlight control system that leverages machine learning to optimize energy consumption while ensuring adequate illumination for public safety. The system analyzes real-time data—such as traffic density, ambient light, and weather conditions—to dynamically adjust streetlight power states and dimming levels. This solution not only reduces energy consumption but also aligns with sustainability and cost-saving goals for urban development.

---

## **Dataset Summary**
The project utilizes a dataset containing 1,000 observations with the following key attributes:

| **Feature Name**            | **Description**                                                                 |
|------------------------------|---------------------------------------------------------------------------------|
| **Timestamp**               | Date and time of the observation.                                               |
| **Street ID**               | Unique identifier for each streetlight.                                         |
| **Day/Night**               | Indicator for whether it is daytime or nighttime.                               |
| **Traffic Count**           | Number of vehicles during the observation period.                               |
| **Traffic Density**         | Proportion of the road occupied by vehicles.                                    |
| **Traffic Speed**           | Average speed of vehicles during the observation.                               |
| **Ambient Light (lux)**     | Natural light intensity measured in lux.                                        |
| **Weather**                 | Current weather conditions (e.g., clear, cloudy, rainy).                        |
| **Energy Consumption (kWh)**| Power consumption of the streetlight during the period.                         |
| **Power State**             | Binary state of the streetlight (ON=1, OFF=0).                                  |
| **Dim Level**               | Percentage of dimming applied to the streetlight.                               |
| **Latitude & Longitude**    | Geographical coordinates of the streetlight.                                    |
| **Special Event**           | Indicator for public events affecting traffic or lighting needs.                |
| **Holiday/Weekend**         | Indicator for weekends or public holidays.                                      |

---

## **Key Features of the Project**

### **1. Exploratory Data Analysis (EDA):**
- Comprehensive visualization of traffic patterns, weather conditions, and energy consumption trends.
- Insights into feature correlations, such as the impact of traffic density on dimming levels and energy usage.

### **2. Data Preprocessing:**
- Removal of duplicates and handling of missing values.
- Normalization of numerical features for model compatibility.
- Encoding of categorical variables (e.g., `Day/Night` and `Weather`) for machine learning compatibility.
- Detection and treatment of outliers to improve model robustness.

### **3. Machine Learning Models:**
Three classification models were applied to predict the **Power State** (ON/OFF) of streetlights:

#### **Random Forest Classifier**:
- A baseline model leveraging ensemble learning for high accuracy.
- Achieved **100% accuracy**, indicating its effectiveness in this context.

#### **Support Vector Machine (SVM)**:
- Known for handling complex relationships, SVM delivered robust performance.
- Achieved an accuracy of **98.99%**, with the following evaluation metrics:
  - **Precision**: 0.98 (class 0), 1.00 (class 1)
  - **Recall**: 1.00 (class 0), 0.98 (class 1)
  - **F1-Score**: 0.99 for both classes.

#### **XGBoost with PCA**:
- Principal Component Analysis (PCA) was applied for dimensionality reduction to improve computational efficiency.
- XGBoost achieved an accuracy of **68.34%**, demonstrating that dimensionality reduction can sometimes lead to reduced performance when applied inappropriately for the dataset.

---

## **Model Comparison**

| **Model**              | **Accuracy** | **Key Insights**                                                                                     |
|-------------------------|--------------|-----------------------------------------------------------------------------------------------------|
| **Random Forest**       | 100%         | Perfect accuracy due to ensemble learning's robustness and ability to handle feature interactions.   |
| **SVM**                 | 98.99%       | Delivered near-perfect accuracy, effectively capturing complex decision boundaries.                  |
| **XGBoost + PCA**       | 68.34%       | Moderate accuracy; PCA reduced dimensionality but may have led to loss of critical feature information. |

---

## **Business Impact**
This project has significant implications for urban energy management and sustainability:

1. **Energy Cost Savings**: 
   - By intelligently dimming streetlights during periods of low traffic or sufficient ambient light, municipalities can achieve substantial reductions in electricity costs.

2. **Environmental Sustainability**:
   - Reduced energy consumption leads to lower greenhouse gas emissions, contributing to climate change mitigation and environmental preservation.

3. **Enhanced Public Safety**:
   - Maintains adequate lighting during high-traffic periods and adverse weather conditions, ensuring safety for drivers and pedestrians.

4. **Operational Efficiency**:
   - Extends the operational life of streetlights through optimized usage, minimizing maintenance and replacement costs.

5. **Scalable Smart City Solutions**:
   - The system can be integrated into IoT frameworks, enabling real-time updates and scalability for large-scale deployment in urban areas.
