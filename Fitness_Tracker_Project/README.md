# Fitness Tracker Data Analysis

## Overview
Introduction
This project is being undertaken as a capstone to the Google Data Analytics Course on Coursera. It aims to exhibit a holistic application of the data analysis methodologies, tools, and techniques learned throughout the course. The core objective of this exercise is to glean actionable insights from consumer data to steer the marketing strategy of Bellabeat, a high-tech manufacturer of health-focused products for women, thereby unlocking potential growth opportunities.

Case Study Background
Bellabeat, a high-tech company specializing in health-focused products for women, aims to broaden its market presence in the global smart device sector. Under the vision of Urška Sršen, the co-founder and Chief Creative Officer, analyzing smart device fitness data is seen as a catalyst for unveiling new growth opportunities. The product lineup includes the Bellabeat App, Leaf, Time, and Spring.

Sršen has tasked the marketing analytics team to delve into smart device usage data to uncover insights into consumer behaviors. The insights derived are anticipated to shape Bellabeat’s marketing strategy, with an end goal of presenting an analysis and strategic recommendations to the executive team.

## Structure
- `Data`: Contains raw data files, including daily activity, sleep patterns, and weight logs.
- `Scripts`: R Markdown document (`fitness_tracker_project.Rmd`) detailing the analysis process, from data loading to final recommendations.
- `Outputs`: Includes an HTML version of the R Markdown analysis and any generated figures or tables.

## Methodology
In this project, I embarked on an in-depth analysis of fitness tracker data to uncover insights into user behaviors and activity patterns. My approach encompassed several stages, from initial data cleaning to advanced statistical analysis, employing a variety of R packages to facilitate each step. Here's an overview of my methodology:

Data Preparation:
- Utilized `janitor` for initial data cleaning, including removing empty columns and rows, and cleaning column names for ease of use.
- Employed `lubridate` for handling and manipulating DateTime data, converting strings to DateTime objects where necessary.
- Removed unnecessary columns to streamline the dataset, ensuring focus on relevant variables.
- Converted data types to ensure consistency across datasets, enhancing the accuracy of subsequent analyses.
- Addressed duplicate and missing information, employing strategies to impute or exclude data as appropriate.
- Merged datasets using `dplyr` to create a comprehensive data frame for analysis, carefully handling keys to ensure accurate joins.

Exploratory Data Analysis (EDA):
- Defined a custom `hist_box` function to standardize the visualization of variables across datasets, facilitating a consistent approach to examining distributions and outliers.
- Utilized the `purrr` package for efficient variable mapping, enabling sophisticated data manipulation and transformation techniques.
- Conducted outlier analysis to identify and control for extreme values, ensuring they did not unduly influence the results.

Advanced Statistical Analysis:
- Performed cluster analysis using the `cluster` package, scaling data to normalize distributions before applying clustering algorithms.
- Generated an elbow plot and a silhouette plot using the `factoextra` package to determine the optimal number of clusters, ensuring meaningful segmentation of user groups.
- Transitioned to hierarchical clustering methods with the `stats` library, analyzing the resulting dendrogram to identify distinct user profiles based on their activity patterns.
- Examined correlations between variables using the `corrplot` library, creating matrices and heatmaps to visualize relationships and identify potential areas of interest.

Modeling and Insights:
- Employed linear modeling to explore the effects of sleep on various activity variables, identifying statistically significant variations albeit with small effect sizes. This nuanced understanding allowed for a deeper interpretation of how sleep quality and duration influence daily activity metrics.

Throughout this process, I prioritized reproducibility and transparency, documenting each step of my analysis to ensure that others could follow my methodology and arrive at similar conclusions. My use of a wide range of R packages, from `dplyr` and `ggplot2` for data manipulation and visualization to `cluster` and `factoextra` for advanced statistical analysis, was instrumental in uncovering actionable insights from the fitness tracker data.

## How to Run
1. Clone this repository to your local machine.
2. Open `fitness_tracker_project.Rmd` in RStudio.
3. Install the required R packages using `install.packages()`.
4. Knit the document to produce the HTML output, which includes all analysis steps and findings &#8203;``【oaicite:0】``&#8203;
