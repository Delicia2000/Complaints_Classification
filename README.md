# Real-Time Complaint Monitoring System
## Objective
To build a real-time complaint monitoring system that will allow service-based institutions, such as banks, to categorize incoming customer complaints automatically and track the frequency of complaints by category. This system aims to help institutions address recurring issues faster, thereby improving customer satisfaction and retention.

## Problem Statement
Customer complaints are a critical indicator of service quality. However, organizations such as banks that directly serve clients often struggle to manage large volumes of complaints effectively. This can lead to delayed resolutions and frustrated customers. Without proper categorization and monitoring, companies cannot identify the most frequent or urgent issues that require immediate action, causing dissatisfaction and potential customer loss.

## Hypothesis: 
Certain categories of financial products (like credit cards or credit reporting) generate more complaints than others, and specific complaint types may reveal systemic issues within these products

## Snapshot of my data and data source
The data is downloaded from Kaggle.
<img width="419" alt="image" src="https://github.com/user-attachments/assets/9d07fcc0-51e4-4bd8-afc8-c4275757414e">

Data Distribution by Category
Below is the distribution of complaints across different categories, visualized in a barplot:

![Barplot - Distribution of Complaints by Category](https://github.com/user-attachments/assets/98b20590-9d5b-4ba9-9c05-a5c76959146e)

## Data preprocessing
This barplot helps identify which categories receive the most complaints
### Data cleaning
<img width="467" alt="image" src="https://github.com/user-attachments/assets/0e738006-0e3e-49a3-b3a0-3b80dc94a9a2">

### Common Words in Complaints (After Data Cleaning)
The most frequently occurring words in this dataset after data cleaning are shown below in a word cloud:

![Word Cloud - Most Common Words in Complaints](https://github.com/user-attachments/assets/270189d2-97cc-49a4-98cd-33994e37c8de)

### Heatmap of Complaint Length by Category
The heatmap below shows the distribution of complaint lengths across different categories:

![Heatmap - Length of Complaints by Category](https://github.com/user-attachments/assets/29774533-3155-43ba-aab3-e18da636cf65)

This heatmap provides insights into the complexity of complaints in each category, allowing institutions to understand and manage lengthy or detailed complaints more effectively.

## Creating a numerical model
### vectorization using TF-IDF
I chose to use TF-IDF for this project (Term Frequency-Inverse Document Frequency) for vectorization in this project because it helps focus the model on words that are particularly significant for distinguishing between different types of complaints, rather than just frequent terms. 
<img width="579" alt="image" src="https://github.com/user-attachments/assets/9f6c58e7-526d-4526-9ba8-d76ca7773706">

### classification using Naive bays
Naive bays is used for this project because of its Simplicity, speed and effectiveness with text.
<img width="403" alt="image" src="https://github.com/user-attachments/assets/93170142-4dbf-4e53-b1c0-0ba510a148e7">

##### Metrics using the Naive Bayes Model:
<img width="243" alt="image" src="https://github.com/user-attachments/assets/91933342-261c-4c61-a915-a88a5b78c3b0">

#### FineTuning using GridSearch
<img width="387" alt="image" src="https://github.com/user-attachments/assets/dc15058e-dfbd-4ae7-a606-738fe87f7abb">

##### metrics after fine-tuning:
<img width="232" alt="image" src="https://github.com/user-attachments/assets/a1c09e61-bd07-4771-9aea-92baa169e223">

 Heatmap
<img width="481" alt="image" src="https://github.com/user-attachments/assets/c94a012e-3e83-4073-8263-9dc9de1abcc6">

Interpretation of results:

## Future Improvements:
 Future Improvements
- **Real-Time Feedback Loop:** Incorporate real-time data for continuous improvement and faster issue resolution.
- **Advanced Text Classification Models:** Explore deep learning models like BERT or GPT to improve classification accuracy.
- **Sentiment Analysis:** Analyze customer sentiment to gauge the emotional tone of complaints and prioritize urgent issues.

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

The following barplot visualizes the distribution of complaints across various categories:

![Barplot - Distribution of Complaints by Category](https://github.com/user-attachments/assets/98b20590-9d5b-4ba9-9c05-a5c76959146e)

This plot provides an overview of which complaint categories are most frequent, offering insights into areas of potential concern.

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

### Vectorization using TF-IDF
For vectorizing the textual data, we used TF-IDF (Term Frequency-Inverse Document Frequency). This technique helps highlight the most significant terms in the complaints that can differentiate between categories. The following image shows the process of applying TF-IDF to the dataset:

![TF-IDF Vectorization](https://github.com/user-attachments/assets/9f6c58e7-526d-4526-9ba8-d76ca7773706)

### Classification using Naive Bayes
We selected Naive Bayes as the classification algorithm due to its simplicity, speed, and effectiveness in text classification tasks. Below is an illustration of the Naive Bayes classifier:

![Naive Bayes Classification](https://github.com/user-attachments/assets/93170142-4dbf-4e53-b1c0-0ba510a148e7)

---

## Model Evaluation

### Metrics using Naive Bayes Model
The model was initially evaluated using standard metrics. The following table summarizes the performance:

![Model Metrics](https://github.com/user-attachments/assets/91933342-261c-4c61-a915-a88a5b78c3b0)

---

## Fine-Tuning the Model

### Hyperparameter Tuning with GridSearch
To improve the model’s performance, we applied GridSearch for hyperparameter tuning. The following image demonstrates the process of fine-tuning the model:

![GridSearch Fine-Tuning](https://github.com/user-attachments/assets/dc15058e-dfbd-4ae7-a606-738fe87f7abb)

### Metrics After Fine-Tuning
After fine-tuning, the model’s performance improved, as seen in the following metrics:

![Metrics After Fine-Tuning](https://github.com/user-attachments/assets/a1c09e61-bd07-4771-9aea-92baa169e223)

---

## Final Model Performance

### Confusion Matrix and Results
The confusion matrix provides a detailed look at the model’s performance across different categories. The following image highlights the classification performance:

![Confusion Matrix](https://github.com/user-attachments/assets/c94a012e-3e83-4073-8263-9dc9de1abcc6)

---

## Conclusion
By implementing this real-time complaint monitoring system, we can help institutions like banks effectively categorize and track customer complaints. This will not only streamline the complaint resolution process but also provide actionable insights to address recurring issues, improving customer satisfaction and retention.

---

## Future Improvements
- **Real-Time Feedback Loop:** Incorporate real-time data for continuous improvement and faster issue resolution.
- **Advanced Text Classification Models:** Explore deep learning models like BERT or GPT to improve classification accuracy.
- **Sentiment Analysis:** Analyze customer sentiment to gauge the emotional tone of complaints and prioritize urgent issues.














