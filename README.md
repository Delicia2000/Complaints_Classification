# Real-Time Complaint Monitoring System
## Objective
To build a real-time complaint monitoring system that will allow service-based institutions, such as banks, to categorize incoming customer complaints automatically and track the frequency of complaints by category. This system aims to help institutions address recurring issues faster, thereby improving customer satisfaction and retention.

## Problem Statement
Customer complaints are a critical indicator of service quality. However, organizations such as banks that directly serve clients often struggle to manage large volumes of complaints effectively. This can lead to delayed resolutions and frustrated customers. Without proper categorization and monitoring, companies cannot identify the most frequent or urgent issues that require immediate action, causing dissatisfaction and potential customer loss.

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
###vectorization using TF-IDF
I chose to use TF-IDF for this project (Term Frequency-Inverse Document Frequency) for vectorization in this project because it helps focus the model on words that are particularly significant for distinguishing between different types of complaints, rather than just frequent terms. 
<img width="579" alt="image" src="https://github.com/user-attachments/assets/9f6c58e7-526d-4526-9ba8-d76ca7773706">






