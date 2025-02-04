# SleepDisorderClassification
This is mainly the reimplementation of a research paper:  Applying Machine Learning Algorithms for the
 Classification of Sleep Disorders
Reference:
T. S. Alshammari, "Applying Machine Learning Algorithms for the Classification of Sleep Disorders," 
in IEEE Access, vol. 12, pp. 36110-36121, 2024, doi: 10.1109/ACCESS.2024.3374408. 
# Optimized Classification of Sleep Disorders Using Machine  Learning and Data Augmentation 
## Abstract 
The classification of sleep disorders has been critical in enhancing the quality of human health. This paper 
evaluates and fine-tunes several machine learning algorithms to improve the sleep disorder classification 
accuracy. With the publicly available Sleep Health and Lifestyle Dataset, k-Nearest Neighbors (KNN), 
Support Vector Machines (SVM), Decision Trees (DT), Random Forests (RF), and Artificial Neural 
Networks (ANN) were implemented. To overcome the limitation of the dataset, the data augmentation was 
performed by using Conditional Tabular Generative Adversarial Network (CTGAN), and thus the size of 
the dataset increased from 400 to 2000 samples. In addition, Genetic Algorithms (GA) were applied for 
hyperparameter tuning, and results were compared with Grid Search and Random Search techniques. 
Experimental results show that RF achieved the highest accuracy of 91.17% after GA optimization. This 
study presents an important contribution in optimizing MLA performance for sleep disorder classification 
using optimization techniques and data augmentation. 
## I. Introduction 
Sleep is an important physiological process that is very crucial for maintaining mental and physical health. 
Disruptions in sleep patterns, often labeled as sleep disorders, are very critical to cognitive and 
physiological well-being. Such disorders include insomnia, sleep apnea, and shift-work sleep disorder, and 
are common and require proper diagnosis to be managed accordingly. Traditional methods of diagnosing 
sleep disorders rely on expert analysis of polysomnography (PSG) data, which is often labor-intensive, 
time-consuming, and prone to human error. 

The development of MLAs has revolutionized the way sleep disorders are classified through automation. 
MLAs can be used to efficiently analyze complex datasets, identify patterns, and provide reliable 
predictions. However, the performance of such algorithms is greatly dependent on the availability of high
quality datasets and optimized hyperparameters. Small datasets with limited diversity often resulted in 
overfitting and reduced generalization. Also, default hyperparameters in MLAs may not necessarily yield 
the best performance. 

This study addresses these challenges by introducing two key contributions: 
### 1. Data Augmentation:
   The Conditional Tabular Generative Adversarial Network (CTGAN) was 
employed to expand the dataset size from 400 to 2000 samples, improving the representativeness 
and diversity of the data. 
### 2. Optimization Techniques: 
Genetic Algorithms (GA) were applied for hyperparameter tuning 
across five MLAs: k-Nearest Neighbors (KNN), Support Vector Machines (SVM), Decision Trees 
(DT), Random Forests (RF), and Artificial Neural Networks (ANN). The performance of GA was 
further compared with Grid Search and Random Search methods. 
The primary objective of this study is to evaluate the impact of these interventions on the classification 
accuracy of MLAs for sleep disorders. Through extensive experimentation, this research aims to highlight 
the effectiveness of combining optimization techniques and data augmentation to overcome dataset and 
parameter limitations.
The rest of the paper is organized as follows: Section II describes the methodology, Section III presents 
experimental results, Section IV discusses the findings, and Section V concludes the study with future 
research directions. 
## II. Methodology 
This section describes the dataset, the implemented machine learning models, data augmentation 
techniques, optimization approaches, and the evaluation metrics used in this study. Moreover, it highlights 
the unique contributions of this research. 
### A. Dataset 
The Sleep Health and Lifestyle Dataset, available on Kaggle [2], was used in this study. The original dataset 
contains 400 records and 13 features, including demographic attributes (e.g., age, gender, occupation), 
health indicators (e.g., body mass index, blood pressure), and sleep-related metrics (e.g., sleep duration, 
sleep quality). The target variable categorizes individuals into three classes: None (no sleep disorder), Sleep 
Apnea, and Insomnia. 
### B. Data Augmentation Using CTGAN 
To overcome the limitations of a small dataset, the Conditional Tabular Generative Adversarial Network 
(CTGAN) was used to generate synthetic data. The dataset was expanded from 400 to 2000 records, 
maintaining the distribution and feature relationships of the original data. This augmentation improved the 
generalizability of the machine learning models. 
### C. Machine Learning Models 
Five machine learning models were implemented: 
#### 1. k-Nearest Neighbors (KNN): 
A non-parametric algorithm that classifies data points based on their 
proximity to k-nearest neighbors. 
#### 2. Support Vector Machines (SVM):
A supervised learning model that constructs hyperplanes to 
separate classes with maximum margin. 
#### 3. Decision Tree (DT):
A tree-based algorithm that splits data into branches based on feature 
thresholds for classification. 
#### 4. Random Forest (RF): 
An ensemble learning method that aggregates predictions from multiple 
decision trees to improve accuracy and reduce overfitting. 
#### 5. Artificial Neural Networks (ANN): 
A deep learning model consisting of interconnected neurons 
organized in layers, capable of learning complex patterns. 
### D. Optimization Techniques 
#### 1) Genetic Algorithms (GA) 
Genetic Algorithms (GA) were applied to optimize hyperparameters for all models. The process involved: 
1. Initialization: Random generation of parameter sets. 
2. Fitness Evaluation: Performance of each parameter set was assessed using classification accuracy. 
3. Selection: High-performing parameter sets were selected for reproduction. 
4. Crossover and Mutation: New parameter sets were generated by combining and mutating the 
selected ones. 
5. Iteration: Steps 2–4 were repeated until convergence.
#### 2) Comparison with Grid Search and Random Search 
In addition to GA, this study employed Grid Search and Random Search methods for hyperparameter 
tuning: 
• Grid Search: Exhaustively evaluates all parameter combinations within predefined ranges. 
• Random Search: Randomly selects parameter combinations for evaluation, balancing 
performance and computational efficiency. 
### E. Contributions 
This study introduces the following novel contributions to the field of sleep disorder classification: 
  #### 1. Hybrid Optimization:
  A comparative analysis of three hyperparameter tuning 
  methods, namely Genetic Algorithms, Grid Search, and Random Search, was conducted. The study 
  evaluates their efficiency, accuracy, and computational cost in optimizing parameters for each 
  machine learning model. 
  #### 2. Data Augmentation via CTGAN: 
  The Conditional Tabular Generative Adversarial Network was 
  implemented to expand the dataset size to 2000 rows, improving model generalization and 
  mitigating the risk of overfitting. 
  #### 3. Performance Evaluation Framework: 
  A detailed analysis of training, cross-validation, and 
  testing performance metrics (Accuracy, Precision, Recall, F1-Score) across augmented and non
  augmented datasets was conducted to assess the impact of augmentation and optimization. 
  #### 4. Practical Insights: 
  Results show the 
  relative 
  strengths 
  of 
  each 
  optimization 
  method and how GA can be very effective in achieving robust model performance compared to 
  traditional methods like Grid Search. 
#### F. Evaluation Metrics 
The models were evaluated using the following metrics: 
  1. Accuracy: The ratio of correctly predicted instances to total instances. 
  2. Precision: The ratio of true positives to the total predicted positives. 
  3. Recall: The ratio of true positives to the total actual positives. 
  4. F1-Score: The harmonic mean of Precision and Recall, providing a balanced measure. 
These metrics were computed during the training, cross-validation, and testing phases to assess the 
performance of each model. 
