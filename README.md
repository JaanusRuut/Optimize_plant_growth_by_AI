<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Using AI to optimize plant growth

Final project for the Building AI course

## Summary

The project focuses on the application of artificial intelligence to analyze and predict how different environmental conditions will affect plant growth. The goal is to develop a system that will help determine the best conditions for different plants, improving yields and gardening efficiency.


## Background

The idea addresses the challenge of optimizing plant growth conditions to enhance yield and efficiency in gardening and agriculture. This problem is widespread, as environmental factors significantly impact plant health and productivity. My personal motivation stems from a desire to integrate technology with nature, improving sustainable farming practices. This topic is important because it offers a solution to global food security challenges by maximizing crop yield with minimal resources. It's interesting due to its potential to revolutionize traditional farming methods through AI, making it relevant for farmers, hobbyists, and researchers alike.

This is how you make a list, if you need one:
* problem 1
* problem 2
* etc.


## How is it used?

The solution involves collecting environmental data, analyzing it with AI to determine optimal plant growth conditions, and then applying these insights to improve gardening or agricultural practices. It's particularly useful in environments where maximizing resource efficiency is crucial, such as in controlled agriculture settings, urban farming, or areas with limited water. Users range from commercial farmers seeking to increase yield and reduce waste, to home gardeners aiming for healthier plants. Needs include accurate data collection (climate, soil, light), reliable predictions, and user-friendly interfaces for implementing recommendations.

Plant growth for increased yield and efficiency, highlighting the dependency of plant growth on various environmental factors. To use of artificial intelligence to analyze and understand the impact of these factors, with applications in gardening, agriculture, and home gardens. Key data sources include weather data, soil moisture sensors, and light measurements. Challenges involve collecting sufficient and accurate data, and improving machine learning model precision. Future plans focus on enhancing the system for real-time data analysis and prediction accuracy, merging technology with horticulture to achieve better gardening outcomes.



import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor

# We assume that we have a DataFrame 'df' that contains data on soil moisture
('soil_moisture')
# ('light_intensity'), ('temperature') ('growth_rate')

example
data = {
    'soil_moisture': [20, 45, 65, 70, 80],
    'light_intensity': [200, 800, 500, 300, 900],
    'temperature': [15, 20, 25, 22, 18],
    'growth_rate': [1.2, 3.5, 2.8, 2.5, 4.0]
}
df = pd.DataFrame(data)

 # Dividing data into training and test kits
 X = df[['soil_moisture', 'light_intensity', 'temperature']]
y = df['growth_rate']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Model creation and training
model = RandomForestRegressor(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# Estimating model accuracy
score = model.score(X_test, y_test)
print(f'Mudeli täpsus: {score}')

# Predicting growth rates based on new data
new_data = np.array([[50, 700, 21]])  #New data: soil moisture, lighting, 
temperature
predicted_growth_rate = model.predict(new_data)
print(f'Predicted plant growth rate:{predicted_growth_rate[0]}')
This script collects data, divides it into training and test kits, creates and trains a machine learning model (RandomForestRegressor is used here), evaluates the accuracy of the model, and predicts plant growth rates based on new data. When working with data from actual sensors, the data set should be replaced with real-world measurement results.

import numpy as np
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor

data = {
    'soil_moisture': [20, 45, 65, 70, 80],
    'light_intensity': [200, 800, 500, 300, 900],
    'temperature': [15, 20, 25, 22, 18],
    'growth_rate': [1.2, 3.5, 2.8, 2.5, 4.0]
}
df = pd.DataFrame(data)

X = df[['soil_moisture', 'light_intensity', 'temperature']]
y = df['growth_rate']
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

model = RandomForestRegressor(n_estimators=100, random_state=42)
model.fit(X_train, y_train)
score = model.score(X_test, y_test)
print(f'Model accuracy: {score}')

new_data = np.array([[50, 700, 21]])  # Uued andmed: mulla niiskus, valgustus, temperatuur
predicted_growth_rate = model.predict(new_data)
print(f'Predicted plant growth rate: {predicted_growth_rate[0]}')





## Data sources and AI methods

The data for optimizing plant growth using AI can come from various sources. It can be collected directly through environmental sensors measuring soil moisture, light intensity, temperature, and other relevant conditions. Alternatively, data can be sourced from existing datasets provided by research institutions, agricultural organizations, or open data platforms. The choice between collecting data oneself or using data collected by others depends on the project's scope, resources available, and specific requirements for data accuracy and granularity.

Smart farming technologies, including IoT (Internet of Things) applications, provide a wide array of solutions for the agriculture sector, aiming to enhance efficiency, productivity, and sustainability. These technologies leverage data collected from various sources, such as environmental sensors and machine metrics, to inform decision-making and improve agricultural practices.

## Challenges

The project of using AI for optimizing plant growth, while innovative and beneficial, does not address several issues and comes with certain limitations and ethical considerations: Biodiversity and Genetic Variation:, Data Privacy and Security, Economic Disparity, 
Environmental Impact, Ethical Use of AI, Dependence on Technology and Labor Displacement.

## What next?

To expand the project of using AI for optimizing plant growth into something even larger and more impactful, several avenues can be explored, along with necessary skills and assistance: Integration with Global Data Networks, Advanced AI and Machine Learning Models,
Automation and Robotics, Sustainability and Environmental Impact Analysis, Ethical and Societal Impact Studies, Policy and Regulation Engagement, Community and Educational Outreach and Funding and Investment.

## Acknowledgments

For the project on using AI to optimize plant growth, acknowledgments would include:

Sources of Inspiration: This project draws inspiration from pioneering research and development in the fields of smart farming and precision agriculture. Innovations by companies like CropX, Arable, and Semios, which have developed advanced soil and crop monitoring technologies, as well as livestock management solutions by SCR by Allflex and Cowlar, have been instrumental. The integration of IoT in agriculture, as detailed by Smarter Technologies and Eastern Peak, has also shaped the vision for this project.

Usage of Materials: It's crucial to adhere to the principles of fair use and copyright laws. For any external code, images, data, or other materials used, ensure you have permission from the original creators. For instance, if using datasets from agricultural research institutions, verify their terms of use to ensure compliance with open source or Creative Commons licenses.

Attribution: When permission is granted to use materials, always credit the original creator and specify the license under which their work is shared. For example, if using open weather data from platforms like allMETEO or Smart Elements, mention the source and note the license, such as "Data provided by [Source Name] under the [Specific License] license." This practice respects the contributions of others and fosters a culture of sharing and collaboration in the scientific community.

By recognizing the contributions of these sources and adhering to ethical use guidelines, the project not only ensures legal and moral integrity but also promotes a collaborative ecosystem that benefits all stakeholders in the agricultural and technological fields.
