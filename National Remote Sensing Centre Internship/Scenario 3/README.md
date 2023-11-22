# Crop Recommendation for Forest Conservation

## Scenario
The Forest Department of Karnataka is working to protect endangered species in a tropical rainforest. They have access to a dataset of deforestation events and a shapefile of the rainforest boundaries. The goal is to identify areas of the rainforest that are most at risk of deforestation and focus conservation efforts on those areas. This project develops a model using Python to address the problem.

## Dataset
The dataset used for this project is sourced from Kaggle and includes information about soil attributes, weather conditions, and other environmental factors. The data is relatively straightforward and features attributes such as Nitrogen, Phosphorous, Potassium content in soil, temperature, humidity, pH value of the soil, and rainfall.

### Data Fields
- N: Ratio of Nitrogen content in soil
- P: Ratio of Phosphorous content in soil
- K: Ratio of Potassium content in soil
- Temperature: Temperature in degree Celsius
- Humidity: Relative humidity in %
- pH: pH value of the soil
- Rainfall: Rainfall in mm

## Context
Precision agriculture is in trend nowadays, helping farmers make informed decisions about farming strategy. This dataset allows users to build a predictive model to recommend the most suitable crops to grow in a particular farm based on various parameters.

## Visualizations
- Bar Graph
- ![bargraph](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/ae2ec4ad-a9ca-4572-bb1b-70949b918b00)
- Box Plot
- ![boxplot](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/8b3583e9-0a33-4ebb-94d0-6e43019e7fd2)

- Heatmap
- ![heatmap](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/9f108f88-6b8d-464d-9ee1-791245c03510)

- Pie chart
- ![piechart](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/aeafd7dc-2266-40af-9679-407bd6ad6673)

- Sub Plot
- ![subplot](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/fca11920-4a70-42cf-a211-f314eb1a892d)


## Data Preprocessing

### Converting Categories to Integer
crop_dict = {
    'rice': 1,
    'maize': 2,
    'jute': 3,
    'cotton': 4,
    'coconut': 5,
    'papaya': 6,
    'orange': 7,
    'apple': 8,
    'muskmelon': 9,
    'watermelon': 10,
    'grapes': 11,
    'mango': 12,
    'banana': 13,
    'pomegranate': 14,
    'lentil': 15,
    'blackgram': 16,
    'mungbean': 17,
    'mothbeans': 18,
    'pigeonpeas': 19,
    'kidneybeans': 20,
    'chickpea': 21,
    'coffee': 22
}
dataset['crop_num']=dataset['label'].map(crop_dict)
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/f9756682-37b7-4bcd-bfde-e72bc7cbe0b1)


### Train-Test Split

![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/ff76e0ae-78a7-45ba-8d89-379a714048bd)
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/72a6b275-b4a5-4c33-94ab-14666d49d3a4)


## Models Used
- Decision Tree

- ![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/a8483285-73f5-4d9c-81a6-ea476e50447c)
-![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/7825836c-a2eb-4b2d-9704-ac63dc433740)

- Gaussian Naive Bayes
  
- ![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/6809cc44-4abe-4519-aeea-3c2a955216e9)
-![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/dee9f335-880b-4a78-9516-f153edd4cae0)

- Support Vector Machine (SVM)
  
- ![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/bd7952a6-8132-4672-81ce-a94c45af91f8)

- Logistic Regression
  
- ![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/9e67ab18-c231-43e8-b8f4-22c701d911d6)
-![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/6d7e7a20-6ab4-41b9-8689-88d3a541ea90)
-![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/9b77a395-40ba-46cd-be6e-985fb4f0c14c)

- Random Forest

-![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/f4deb2cb-7e48-4731-9fe4-e15c27279e59)
-![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/26e4380d-0b51-484b-a74c-b19b2d1f0bb9)

### Model Performance
Decision Tree = 0.9
Naive Bayes = 0.990909090909091
SVM = 0.10681818181818181
Logistic Regression = 0.9522727272727273
RF = 0.990909090909091
Random Forest achieved the highest accuracy with 99.09%.
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/238ece90-9037-4495-b80e-3309c6659aab)

## Predictions

![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/f990cc25-74af-46fa-84cf-f1573a493cfc)
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/2baf5ec1-b659-4fda-a587-ce1af5573f20)

## Making Pickle File
![image](https://github.com/AbhishekGit23/National-Remote-Sensing-Centre-Internship/assets/123490715/64066c94-6b08-484d-a010-5dc48ac692b9)

## Getting Started
1. Clone the repository.
2. Install the required dependencies.
3. Run the main Python script.

## Conclusion
In conclusion, this project aims to address the conservation needs of the rainforest by predicting areas at risk of deforestation. The crop recommendation model provides valuable insights for informed decision-making in agriculture.

Feel free to explore the code, visualizations, and documentation!

**GitHub Link:** [Your GitHub Repository Link]


