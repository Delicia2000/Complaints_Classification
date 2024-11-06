# Real-Time Complaint Monitoring System

## Objective
The goal of this project is to build a real-time complaint monitoring system that automatically categorizes incoming customer complaints, tracks their frequency by category, and helps service-based institutions—such as banks—address recurring issues more quickly. This system aims to enhance customer satisfaction and retention by identifying and resolving systemic issues in a timely manner.

## Problem Statement
Customer complaints are a crucial indicator of service quality. Service-oriented institutions like banks often struggle to manage large volumes of complaints efficiently. Without an automated system to categorize and monitor complaints, banks may fail to identify recurring issues that need urgent attention. This can lead to delayed resolutions, frustrated customers, and a negative impact on customer retention.

## Hypothesis
It is hypothesized that specific financial products (e.g., credit cards, credit reporting) generate more complaints than others. Additionally, specific complaint types may indicate systemic issues within these products, which can be targeted for improvement.

---

## Snapshot of the Data

### Data Source
The dataset used for this project is sourced from Kaggle, containing customer complaints related to financial products and services.

#### Data Distribution by Category

The following barplot and Pie chart visualizes the distribution of complaints across various categories:

![Barplot - Distribution of Complaints by Category](https://github.com/user-attachments/assets/98b20590-9d5b-4ba9-9c05-a5c76959146e)
<img width="294" alt="image" src="https://github.com/user-attachments/assets/3932248a-828e-47f1-9902-ae397e64794e">


These plots provides an overview of which complaint categories are most frequent, offering insights into areas of potential concern.

---

## Data Preprocessing

### Data Cleaning
The dataset undergoes an extensive cleaning process to remove noise, handle missing values, and standardize text. The following image illustrates the steps involved:

![Data Cleaning Process](https://github.com/user-attachments/assets/0e738006-0e3e-49a3-b3a0-3b80dc94a9a2)

### Common Words in Complaints (After Data Cleaning)
After data cleaning, a word cloud was generated to highlight the most frequently occurring words in the complaints. The image below displays the common words after removing stop words and non-relevant terms:

![Word Cloud - Most Common Words in Complaints](https://github.com/user-attachments/assets/270189d2-97cc-49a4-98cd-33994e37c8de)

---

## Complaint Length Analysis

### Heatmap of Complaint Length by Category
The heatmap below shows the distribution of complaint lengths across various categories, helping us to analyze whether certain categories tend to generate longer or more detailed complaints:

![Heatmap - Length of Complaints by Category](https://github.com/user-attachments/assets/29774533-3155-43ba-aab3-e18da636cf65)

This analysis provides insights into the complexity of complaints in each category, which could guide prioritization efforts.

---

## Creating a Numerical Model
After performing tokenization and lemmatization, I'll perform vectorization 
### Vectorization using TF-IDF
For vectorizing the textual data, we used TF-IDF (Term Frequency-Inverse Document Frequency). This technique helps highlight the most significant terms in the complaints that can differentiate between categories. The following image shows the process of applying TF-IDF to the dataset:

![TF-IDF Vectorization](https://github.com/user-attachments/assets/9f6c58e7-526d-4526-9ba8-d76ca7773706)

### Classification using Naive Bayes
We selected Naive Bayes as the classification algorithm due to its simplicity, speed, and effectiveness in text classification tasks. Below is an illustration of the Naive Bayes classifier:

![Naive Bayes Classification](https://github.com/user-attachments/assets/93170142-4dbf-4e53-b1c0-0ba510a148e7)

---

## Model Evaluation

### Metrics using the Naive Bayes Model
The model was initially evaluated using standard metrics. The following table summarizes the performance:

![Model Metrics](https://github.com/user-attachments/assets/91933342-261c-4c61-a915-a88a5b78c3b0)

---

## Fine-Tuning the Model

### Hyperparameter Tuning with GridSearch
To improve the model’s performance, we applied GridSearch for hyperparameter tuning.
Grid search is  method that tries every possible combination of specified hyperparameters for a machine learning model to find the best combination that optimizes model performance.
The following image demonstrates the process of fine-tuning the model:

![GridSearch Fine-Tuning](https://github.com/user-attachments/assets/dc15058e-dfbd-4ae7-a606-738fe87f7abb)

### Metrics After Fine-Tuning
After fine-tuning, the model’s performance improved, as seen in the following metrics:

![Metrics After Fine-Tuning](https://github.com/user-attachments/assets/a1c09e61-bd07-4771-9aea-92baa169e223)

---

## Final Model Performance

### Confusion Matrix and Results
The confusion matrix provides a detailed look at the model’s performance across different categories. The following image highlights the classification performance:

![Confusion Matrix](https://github.com/user-attachments/assets/c94a012e-3e83-4073-8263-9dc9de1abcc6)
##### Interpretation
****2430 successfully predicted as Cedit Reporting complaints** 
**16757 successfully predicted as debt collection complaints** 
 **3334 successfully predicted as Mortgages and loans complaints** 
 **3356 successfully predicted as Cedit card complaints** 
 **2334 successfully predicted as Retail banking complaints** **
   
---

## Future Improvements

- **Advanced Text Classification Models:** Explore deep learning models like BERT to improve classification accuracy.
- **Deploy my model using Flask:** Incorporate real-time data for continuous improvement and faster issue resolution.
- **Dashboard:** Using Power BI, make a dashboard that showcases in real-time the complaints distribution















