## Shinkansen Travel Experience Hackathon Project

### Introduction
This project was my submission for the Shinkansen Travel Experience Hackathon, concluding the MIT Data Science and Machine Learning Course. The objective was to predict passenger satisfaction on the Shinkansen Bullet Train, based on their overall travel experience.

- Date: Jan 11, 10:00 PM - Jan 14, 9:59 PM
- Team Size Allowed: 1 - 3 members
- Overall Rank: 9th Place out of 31 teams
- My Highest Accuracy: 94.80%
- 1st Place Team's Accuracy: 95.54%
- Number of Models Built: 6 + 2 ensemble models
- Number of Submissions: 13

Unfortunately, the datasets are proprietary to Great Learning and cannot be shared here, but the Data Dictionary is still included for review.

### Models Used

Throughout the hackathon, I experimented with various machine learning models to analyze and predict passenger satisfaction:

- Logistic Regression: A foundational model for binary classification tasks.
- Decision Tree: Useful for its interpretability and simplicity.
- Random Forest: An ensemble method that improves on the decision tree's performance by reducing overfitting.
- XGBoost: An efficient and powerful boosting model known for its speed and performance.
- Neural Network: A deep learning approach to capture complex nonlinear relationships in the data.
- SVM (Support Vector Machine): Effective for high-dimensional spaces and various types of data.
- Ensemble Models: Combined predictions from multiple models to improve overall accuracy.

### Technologies Used
Python, Google Colab
Libraries: NumPy, Pandas, Matplotlib, Seaborn, Scikit-Learn, TensorFlow, XGBoost, tqdm

### Features and Highlights
- Implementation and comparison of a wide range of machine learning models.
- Rigorous data analysis and visualization to understand passenger satisfaction factors.
- Exploration of both traditional machine learning and deep learning techniques.
- Created 6 different types of models plus 2 ensemble models

### Data Sources and Preprocessing
The dataset for this project was centered on the passenger experience with the Shinkansen Bullet Train. The preprocessing included cleaning, normalization, and feature engineering to prepare the data for modeling.  The datasets included training and testing sets for both information about the trip and survey results.  They are proprietary to Great Learning and so are not included here, but the data dictionary in the "Data" folder describes its structure.  

### Methodology
The project's methodology was methodically structured to systematically explore various machine learning models. The process began with the essential steps of data processing, which included cleaning, imputation, and exploratory data analysis (EDA) to understand underlying patterns and relationships.

For categorical variables like 'Gender', 'Customer_Type', and 'Type_Travel', I dealt with missing values by imputing the mode or creating an 'Unknown' category and then applied one-hot encoding to transform these features into a format suitable for modeling. Continuous variables like 'Age' were imputed with the median value, and variables with skewed distributions like 'Departure_Delay_in_Mins' and 'Arrival_Delay_in_Mins' were log-transformed to normalize their distribution.

An extensive hyperparameter tuning exercise was conducted for most models using GridSearchCV, optimizing their performance. Special attention was given to feature importance analysis, particularly for the Decision Tree model, leading to tailored adjustments to enhance its predictive capability.

For the Neural Network, I experimented with various architectures, varying the number and types of layers and activation functions. The best-performing model used a mix of relu and tanh activations with dropout to mitigate overfitting. Adam optimizer was chosen for its efficiency, and early stopping with model checkpointing was employed to save the best iteration during training.

The models were trained on a rich dataset that combined survey and trip information, encompassing over 90,000 records and 27 features. Predictions were made on a test set of more than 30,000 records, aiming to classify passenger satisfaction as '1' (satisfied) or '0' (unsatisfied).  

### Results and Discussion
The project culminated in a successful outcome, with my submission securing the 9th place out of 31 participating teams. The highest model accuracy achieved was 94.80% with XGBoost, closely followed by a fine-tuned Decision Tree model at 94.4%, and a Simple Majority Vote ensemble model at 94%. All models performed with an accuracy above 90%, except for the Logistic Regression model, which lagged at 64% accuracy.

The XGBoost model stood out for its performance, benefiting significantly from the systematic hyperparameter tuning. The Decision Tree model's performance was bolstered through an informed feature importance analysis, which guided adjustments yielding a near-top accuracy. The ensemble models, particularly the Simple Majority Vote approach, demonstrated the strength of combining predictions, although they did not surpass the XGBoost model's accuracy.

The Neural Network models' development highlighted the importance of architectural choices, where the incorporation of relu and tanh activations in conjunction with dropout layers resulted in the most effective iteration. However, due to constraints on time and computational resources, comprehensive hyperparameter tuning on the Neural Networks and SVM was not feasible, indicating a potential area for future exploration.

The extensive data set provided a robust foundation for the model training, and the predictions on the test set were indicative of the models' generalizability. The consistent performance across multiple models underscores the thoroughness of the data preparation and the effectiveness of the modeling approach.

These results not only validate the methodologies employed but also open avenues for further refinement, particularly in optimizing the most promising models and exploring more complex ensemble techniques. The experience gained through this hackathon has been invaluable, providing deep insights into practical machine learning applications and setting the stage for ongoing learning and development in the field of data science.

### Conclusion
Participating in the Shinkansen Travel Experience Hackathon and achieving 9th place out of 31 teams was a significant accomplishment. This project allowed me to apply a variety of machine learning models, achieving a highest accuracy of 94.80% with the XGBoost model, and gaining practical insights into model selection, data preprocessing, and hyperparameter tuning.

The experience highlighted the strengths and limitations of different models, including the challenges of computational constraints, which limited the extent of hyperparameter tuning for some models. Despite these constraints, the project results were promising, demonstrating the potential of machine learning to analyze and predict complex patterns in data effectively.

This hackathon has sharpened my data science skills and provided a clear direction for future projects, especially in exploring more advanced models and techniques. It reinforced the importance of continuous learning and experimentation in the field of data science.

Moving forward, I plan to delve deeper into optimizing the performance of machine learning models and exploring new approaches to improve accuracy and efficiency. The insights gained from this hackathon will be invaluable in guiding my future work in data science.

### Contribution and Acknowledgments
This project was an individual effort for the MIT DSML Hackathon. Special thanks to the instructors and organizers for providing the resources and guidance.

