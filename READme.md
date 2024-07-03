# README for Student Dropout Prediction Challenge Group Project
#### HUDK 4054 Individual Assignment #2
## Project Information
##### **Title:** Predicting Student Dropout with Machine Learning 
##### **Creators:** Yanfei Chen, Viola Tan, Maggie Zhao, Bryan Wu, Summer Wu, Theresa Zhao
##### **Principal Investigators:** Yanfei Chen, Viola Tan, Maggie Zhao, Bryan Wu, Summer Wu, Theresa Zhao
##### **Data Manager:** Yanfei Chen
##### **ORCID iD:** 0009-0006-7790-6961
##### **Affiliation:** Teacher College, Columbia University
##### **Research Date:** 10-30-2023

## Project Abstract
The objective of this project was to develop a predictive model capable of identifying students at risk of dropping out from educational institutions. Recognizing the multifaceted nature of student retention, our approach involved a comprehensive analysis of various factors that could potentially influence dropout rates. These factors included demographic information, academic performance, financial aid data, and student engagement metrics. To address this challenge, we embarked on a rigorous data preparation phase, which involved merging, cleaning, and feature engineering processes applied to three distinct datasets: Financial Aid data, Student Static Data, and Student Progress data. This meticulous preparation enabled us to construct a unified dataset that encapsulates a holistic view of the student experience, spanning from 2011 to 2017. Leveraging this rich dataset, we explored seven different predictive models to evaluate their effectiveness in forecasting student dropouts. The models ranged from traditional machine learning algorithms to more advanced ensemble methods, with a particular focus on optimizing the F2 score to balance the precision-recall trade-off effectively. Among the models trained, the LightGBM model distinguished itself as the most effective, demonstrating superior performance in predicting dropout risks.This project not only sheds light on the predictive power of machine learning in educational settings but also sets the stage for the development of targeted intervention strategies. By identifying at-risk students with greater accuracy, educational institutions can allocate resources more effectively and implement support mechanisms designed to improve student retention rates. The implications of our findings extend beyond the academic domain, offering valuable insights for policymakers and educators committed to fostering educational success and reducing dropout rates.


## Dataset Overview

The cornerstone of our dropout prediction model is a robust and comprehensive dataset, meticulously compiled to encapsulate the multifaceted aspects of student life that influence their academic journey. This dataset is an amalgamation of three distinct but interrelated datasets, covering a broad spectrum of variables from financial aid details to demographic information and academic progress. Spanning the academic years from 2011 to 2017, it offers unparalleled insights into the dynamics of student retention and dropout rates across a significant temporal span.

1. Financial Aid Data- The Financial Aid dataset provides a detailed account of the financial support extended to students, encompassing various types of aid such as grants, scholarships, loans, and work-study arrangements. This component is crucial for understanding the financial landscape of the student body, revealing the critical role that economic support plays in facilitating or hindering academic success. Through careful preprocessing, we have standardized the dataset to ensure seamless integration with other data sources, enabling a comprehensive analysis of financial aid's impact on dropout rates.

2. Student Static Data- This dataset delves into the demographic fabric of the student population, offering static, unchanging information about students at the time of their entry into the institution. It includes critical demographic markers such as age, gender, ethnicity, and socioeconomic status, alongside academic indicators like entrance exam scores and initial major selection. The Student Static Data is instrumental in identifying demographic and initial academic standing correlations with student persistence, providing a snapshot of the diversity within the educational institution.

3. Student Progress Data- The Student Progress Data tracks the academic trajectory of students, cataloging course enrollments, grades, academic standing changes, and progress toward degree requirements. This dynamic dataset is pivotal for examining how academic engagement, performance, and milestones correlate with retention and dropout rates. It allows for a longitudinal analysis of student progress, identifying at-risk patterns and the efficacy of academic support services.

4. Integration and Preparation Process- Integrating these datasets into a singular analytical framework posed substantial challenges, requiring meticulous attention to data cleaning, merging, and feature engineering. Our approach began with the harmonization of identifiers and key variables across datasets, ensuring accuracy and consistency in student records. We then engaged in a rigorous process of data cleaning to address missing values, outliers, and inconsistencies, laying a clean foundation for feature engineering and model training.


## Models

In our quest to develop a predictive model with high accuracy and reliability for student dropout prediction, we embarked on an exhaustive exploration of various machine learning algorithms. This journey encompassed a wide range of models, from simple linear classifiers to complex ensemble methods, each offering unique strengths and challenges. Below, we delve into the specifics of the models evaluated, the rationale behind their selection, and the intricacies of their implementation and optimization.

#### 1. Initial Model Selection

Our initial foray into modeling began with baseline models, including Logistic Regression and Decision Trees. These models served as benchmarks, providing a foundational understanding of the predictive capability of our dataset. Despite their simplicity, these models are highly interpretable, making them invaluable for gaining initial insights and identifying key predictive features.

#### 2. Advanced Ensemble Techniques

Recognizing the potential for improved accuracy and robustness, we progressed to more sophisticated ensemble methods:

- **Random Forest:** This model combines multiple decision trees to reduce overfitting and improve prediction accuracy. It was particularly valuable for handling the high dimensionality of our dataset without extensive parameter tuning.
  
- **Gradient Boosting Machines (GBM):** GBM models, including XGBoost and LightGBM, were chosen for their effectiveness in handling diverse data types and their capacity for high performance. These models sequentially build weak learners to form a strong predictive model, adept at capturing complex patterns in the data.

- **LightGBM:** Among the GBM variants, LightGBM stood out for its efficiency and scalability, crucial for managing our extensive dataset. Its innovative handling of categorical features and gradient-based one-side sampling (GOSS) for faster training without compromising accuracy made it a top contender.

#### 3. Deep Learning Approaches

With the advancements in computational power and the increasing availability of large datasets, deep learning models have emerged as powerful tools for predictive analytics. We experimented with:

- **Convolutional Neural Networks (CNNs):** Although traditionally used for image processing, CNNs were adapted to our tabular dataset to capture complex patterns and interactions between features.
  
- **Recurrent Neural Networks (RNNs):** Given the temporal nature of some of our features, such as academic progress over time, RNNs were explored for their ability to process sequences and temporal data.

#### 4. Model Optimization and Evaluation

Each model underwent a rigorous process of hyperparameter tuning and cross-validation to ensure optimal performance. We utilized grid search and random search techniques to explore the hyperparameter space efficiently. The models were evaluated based on a range of metrics, with a particular focus on the F2 score to prioritize the balance between precision and recall, especially given the high cost of false negatives in dropout prediction.

#### 5. Final Model Selection

The LightGBM model emerged as the final selection due to its superior performance across multiple metrics, including accuracy, F2 score, and AUC-ROC. Its ability to handle large datasets with categorical features efficiently, coupled with its lower computational demand and faster training times, made it ideally suited for our project's requirements.

#### 6. Insights and Implications

The exploration of these models provided deep insights into the predictive dynamics of student dropout. The LightGBM model's feature importance analysis revealed that factors such as academic performance, engagement metrics, and financial aid were critical predictors of dropout. These findings underscore the potential of targeted interventions to mitigate dropout risks.

#### 7. Future Directions

Building on the success of the LightGBM model, future research could explore hybrid models that combine the strengths of machine learning and deep learning approaches. Additionally, incorporating more granular temporal data and exploring unsupervised learning techniques for feature extraction could further enhance the model's predictive accuracy.

.

## Python Libraries Used

##### The development and implementation of our predictive models relied heavily on a suite of Python libraries, each chosen for its specific functionality and contribution to the data science workflow. Below is an overview of the key libraries used in this project, along with a brief description of how they were employed:

##### 1. Data Manipulation and Analysis

- Pandas
  
- NumPy
  
- Os

##### 2. Data Visualization

- Matplotlib

- Seaborn

##### 3. Machine Learning and Model Building

- Scikit-learn

- XGBoost

- LightGBM

  
##### 4. Deep Learning

- TensorFlow

- Keras


## Results and Conclusion
The comparative analysis of the F2 scores across our model suite highlighted the LightGBM model's superior capability, recording an impressive F2 score of 0.9428. This model's prowess was further validated on the Kaggle dataset, where it achieved a commendable score of 0.9269, underscoring its robust predictive performance.

##### 1. Limitations and Challenges
Our journey into data analytics, while rewarding, illuminated the paramount importance and inherent challenges of data preprocessing. Recognizing our novice status, we encountered several hurdles:

- Data Wrangling: Our decision to focus on the most recent semester's data may have inadvertently led to the omission of valuable historical insights. The potential for a more nuanced data integration approach exists, which could preserve a richer dataset for analysis.
  
- Exploratory Data Analysis (EDA): Our initial foray into EDA, particularly in interpreting heatmaps, revealed our limitations in extracting actionable insights, which in turn affected our data cleaning effectiveness.

- Data Imputation: The approach to address missing values and entries marked as -2, especially within race-related columns, was somewhat elementary. A more sophisticated strategy in feature engineering and imputation could significantly improve data quality.

##### 2. Learning and Development
Hyperparameter tuning emerged as a particularly daunting task, with the exhaustive search mechanisms proving both complex and time-intensive. This experience has been a profound learning curve, highlighting areas for growth in feature engineering and EDA proficiency. We are motivated by the understanding that enhanced skill in these areas will directly translate to improved data preparation and model performance.

##### 3. Reflective Insights
This project marked our inaugural dive into the realm of machine learning, blending theoretical learning with invaluable practical experience. It has been a revelation, teaching us about the intricate balance between algorithmic precision and the subjective nuances of dataset preparation.

We have learned that algorithms, much like their creators, can harbor biases—each decision in the data preprocessing phase can pivotally influence the final model's performance. This realization underpins the critical need for data analysts to approach their work with a keen awareness of the potential for bias, ensuring that the models developed serve their intended purpose without unintended consequences.



## Data Storage/Access

Effective data management played a crucial role in the success of our dropout prediction project. Recognizing the sensitivity and the value of the data involved, we implemented robust storage and access protocols to ensure data integrity, security, and accessibility throughout the project's lifecycle.

##### 1. Storage Solutions

Our project utilized a combination of cloud-based and local storage solutions to maintain the dataset's availability and security:

- **Cloud Storage:** For collaborative and scalable access, critical datasets were stored on secure cloud platforms. This approach facilitated remote access by team members, allowed for real-time data updates, and provided a layer of data loss prevention through redundancy features.

- **Local Storage:** Sensitive data elements and intermediate processing stages were securely stored on encrypted local servers. This dual-storage approach balanced the need for accessibility with the imperative of data protection, adhering to privacy standards and compliance requirements.

##### 2. Access Control

Access to the dataset was strictly regulated through a comprehensive access control system, ensuring that only authorized personnel could view or manipulate the data:

- **Authentication:** Team members were required to authenticate through multi-factor authentication mechanisms, ensuring that access was limited to verified individuals.

- **Role-Based Access Control (RBAC):** Access permissions were assigned based on roles within the project team, with different levels of access for data analysts, project managers, and other stakeholders. This granularity in access control helped prevent unauthorized data exposure and manipulation.

##### 3. Data Privacy and Compliance

Our project was committed to upholding the highest standards of data privacy and compliance with relevant data protection regulations, such as GDPR and HIPAA, where applicable:

- **Anonymization and Pseudonymization:** Personal identifiers within the dataset were anonymized or pseudonymized to protect individual privacy, ensuring that data analysis could proceed without compromising the subjects' confidentiality.

- **Data Use Agreements:** All project members were required to sign data use agreements, acknowledging their understanding of and commitment to ethical data handling practices.

##### 4. Data Backup and Recovery

To safeguard against data loss or corruption, comprehensive backup and recovery procedures were established:

- **Regular Backups:** The dataset and all associated analysis files were backed up regularly to multiple secure locations, ensuring that recent work could be recovered in the event of data loss.

- **Recovery Testing:** Recovery procedures were periodically tested to confirm that data could be effectively restored from backups, ensuring the project's resilience against data loss incidents.

##### 5. Addition

Our meticulous approach to data storage and access underscores the project's commitment to data integrity, security, and ethical handling. By implementing these rigorous data management practices, we were able to maintain a secure and efficient workflow, enabling our team to focus on the critical task of developing predictive models for student dropout with confidence in the underlying data's quality and reliability.


## Final Observations

### Which metadata standard did you choose and why?
In the development of our dropout prediction project, I selected the Dublin Core metadata standard due to its flexibility, widespread acceptance, and ease of integration across various digital platforms and repositories. This decision was underpinned by Dublin Core's ability to facilitate the discovery of digital resources, enhance interoperability, and ensure consistency in metadata usage. Its simplicity, combined with the capacity to describe digital resources comprehensively, made it the ideal choice for cataloging our project's datasets, methodologies, and findings, thereby enhancing the accessibility and reusability of our research outputs.

### Which template/software did you use?
For the creation of our README file, I utilized the Markdown language with the support of Jupyter Notebook's repository interface. Markdown was chosen for its straightforward syntax and compatibility with various version control systems, making it suitable for documenting and sharing project details in a clear, structured manner. And more importantly, it is a more familiar interface for me. 

### What was the most challenging part of creating a ReadME file? How did you overcome these obstacles?
The most challenging aspect of creating the README file was ensuring clarity and completeness while maintaining brevity. Balancing the need to provide comprehensive information about the project, including its objectives, methodologies, results, and conclusions, against the imperative to keep the document concise and readable presented a significant challenge. To overcome these obstacles, I adopted a structured approach to content organization, employing headings, bullet points, and tables to enhance readability. I also engaged in iterative reviews and revisions, soliciting feedback from peers to refine the document's content and presentation. This collaborative, iterative process was instrumental in producing a README file that is both informative and accessible to a broad audience.



### Acknowledgments
We extend our gratitude to Kaggle.com for providing the dataset and to Teacher College for supporting this research.


```python

```


```python

```


```python

```


```python

```
