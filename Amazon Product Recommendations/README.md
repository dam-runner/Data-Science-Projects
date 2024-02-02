# Project: Amazon Product Recommendation System


### Introduction
This project is part of the MIT Data Science and Machine Learning course, focusing on developing a recommendation system for Amazon's electronic products. It utilizes various machine learning models to recommend products to customers based on their previous ratings.

### Context
In the era of information overload, Recommender Systems play a crucial role in filtering through vast choices and providing personalized recommendations. Companies like Amazon invest heavily in algorithmic techniques to enhance customer experience through personalized suggestions.

### Objective
The objective is to build a recommendation system that recommends products to customers based on their past interactions. The system aims to derive meaningful insights from Amazon reviews and leverage them for product recommendations.

### Dataset
The dataset `ratings_Electronics.csv` (304 Mb) contains the following attributes:
- **userId:** Unique identifier for users.
- **productId:** Unique identifier for products.
- **Rating:** User-provided rating for the product.
- **timestamp:** Timestamp of the rating (not used in this project).

### Installation and Setup
To run this project, you will need to install the following libraries:
```python
# Basic python libraries
import numpy as np
import pandas as pd

# Data visualization libraries
import matplotlib.pyplot as plt
import seaborn as sns

# Surprise library for recommendation systems
from surprise import Reader, Dataset, accuracy
from surprise.prediction_algorithms import SVD, KNNBasic, KNNWithMeans
from surprise.model_selection import KFold
from surprise.prediction_algorithms.matrix_factorization import SVD
from collections import defaultdict

# Model evaluation libraries
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.metrics import mean_squared_error, mean_absolute_error

# Data management and utility libraries
import pickle
import os
import sys
import gc
import warnings
warnings.filterwarnings('ignore')

# Install the Surprise library
!pip install scikit-surprise

Download the dataset `ratings_Electronics.csv` and place it in the root directory of the project.

### Execution Steps
1. Clone the repository to your local machine.
2. Install all required libraries mentioned in the 'Installation and Setup' section.
3. Place the `ratings_Electronics.csv` file in the project root directory.
4. Run the Jupyter notebook to execute the project.

### Conclusions and Business Recommendations
- **Conclusions**: The project successfully implemented various models like user-user/item-item collaborative filtering and SVM. The optimized item-based collaborative filtering model showed superior performance.
- **Business Recommendations**: Include deploying the optimized item-based model, utilizing diverse datasets, allocating resources for computation, investigating result instabilities, and continuous model evaluation.

### Technical Challenges

The development of the Amazon Product Recommendation System was not without its challenges, particularly in managing computational resources and handling large datasets in the Google Colab environment. Below are the key technical hurdles encountered and the strategies employed to overcome them:

#### 1. Managing RAM in Google Colab:
- **Issue**: The project frequently encountered RAM limitations in Google Colab, causing the environment to crash. This was a significant challenge given the size of the dataset and the computational intensity of the machine learning models being used.
- **Solutions**:
  - **Efficient Data Management**: Implementing strategies to minimize memory usage, such as careful selection of data types and deleting unnecessary variables.
  - **Monitoring and Optimization**: Actively monitoring RAM usage during the execution of the code and optimizing code blocks to be less memory-intensive.

#### 2. Data Handling and Filtering:
- **Issue**: Handling the large `ratings_Electronics.csv` dataset required careful consideration, particularly when filtering the data to balance the inclusivity of users and products with computational feasibility.
- **Solutions**:
  - **Strategic Filtering**: Experimenting with different filtering criteria, such as varying the threshold for the number of ratings per user and product, to find a balance between a comprehensive dataset and manageable computational load.
  - **Iterative Testing**: Testing the impact of different filtering strategies on model performance to identify the optimal dataset structure.

#### 3. Model Development and Optimization:
- **Issue**: Building and tuning various machine learning models, including collaborative filtering and SVM, demanded significant computational resources and posed challenges in model optimization.
- **Solutions**:
  - **Model Pickling**: Utilizing the Python `pickle` module to save and load trained models. This allowed for efficient reuse of models without the need to retrain them, saving both time and computational resources.
  - **Parameter Tuning**: Employing grid search for hyperparameter tuning, which, while resource-intensive, was crucial for optimizing model performance.

#### 4. Runtime Management:
- **Issue**: Frequent crashes and the need to restart the runtime in Google Colab disrupted the workflow and posed a risk of losing progress.
- **Solutions**:
  - **Code Modularization**: Structuring the code in a modular way to allow for easy re-execution of specific segments without needing to rerun the entire notebook.
  - **Efficient Runtime Restart**: Implementing setup blocks that facilitate quick reloading of datasets and libraries upon restarting the runtime, minimizing downtime and enhancing workflow continuity.

### Model Accuracy Scores
- `model2`: RMSE: 0.8887, Precision: 0.878, Recall: 0.892, F_1 score: 0.885
- `model2_opt`: RMSE: 1.0258, Precision: 0.839, Recall: 0.898, F_1 score: 0.867
- `model_item_item`: RMSE: 0.8048, Precision: 0.886, Recall: 0.912, F_1 score: 0.899
- `model_item_item_opt`: RMSE: 0.7798, Precision: 0.891, Recall: 0.915, F_1 score: 0.903
- `svd`: RMSE: 1.0051, Precision: 0.827, Recall: 0.866, F_1 score: 0.846
- `svd_optimized`: RMSE: 1.0002, Precision: 0.83, Recall: 0.877, F_1 score: 0.853

### Acknowledgments
This project was completed as part of the MIT Data Science and Machine Learning course. Special thanks to the course instructors and coordinators for providing the guidance and resources necessary for this project.
