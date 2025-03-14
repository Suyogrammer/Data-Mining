# Predictive Analytics and Career Trends in Software Development: A Data Mining Approach

## Overview
This project explores the impact of technological advancements on software developers' career trajectories by analyzing Stack Overflow's developer survey data. The primary objectives are to derive meaningful insights, predict developer salaries, and anticipate future job roles. The project employs advanced machine learning techniques, including CatBoost Regressor, K-Means Clustering, and a Retrieval-Augmented Generation (RAG) framework, to provide data-driven insights for developers, employers, and policymakers.

## Key Objectives
1. **Salary Prediction**: Predict developer salaries based on factors like programming skills, location, and experience using the CatBoost Regressor.
2. **Career Trend Prediction**: Anticipate future job roles using synthetic data and a RAG framework with GPT-2 fine-tuning.
3. **Clustering Analysis**: Group developers based on age and compensation using K-Means Clustering to identify patterns in the data.

## Dataset
The dataset used in this project is derived from Stack Overflow's annual developer surveys (2022–2024). It includes information on demographics, skills, employment details, salaries, and more. The data was preprocessed to handle missing values, standardize column names, and merge datasets for consistent analysis.

## Methodology
### 1. **CatBoost Regressor**
- **Purpose**: Predict developer salaries based on features like programming languages, experience, and country.
- **Steps**:
  1. **Feature Selection**: Identify key features such as country, years of coding, and programming languages.
  2. **Model Training**: Train the CatBoost model using hyperparameters like learning rate, depth, and iterations.
  3. **Prediction**: Use the trained model to predict salaries for new data.
- **Results**: Achieved a test RMSE of 43.544 with 1000 iterations, depth 8, and a learning rate of 0.05.

### 2. **K-Means Clustering**
- **Purpose**: Group developers based on age and yearly compensation.
- **Steps**:
  1. **Initialization**: Select the optimal number of clusters using the Elbow Method.
  2. **Clustering**: Assign data points to clusters and update centroids iteratively.
  3. **Evaluation**: Measure clustering quality using the Silhouette Score.
- **Results**: Identified 4 clusters with a Silhouette Score of 0.64, indicating moderate clustering quality.

### 3. **RAG Framework with GPT-2 Fine-Tuning**
- **Purpose**: Predict future job roles using synthetic data and a RAG framework.
- **Steps**:
  1. **Data Preparation**: Combine text and numerical features into embeddings and create a FAISS index for similarity search.
  2. **Synthetic Data Generation**: Generate synthetic job roles using ChatGPT to fill gaps in the dataset.
  3. **Fine-Tuning**: Fine-tune the GPT-2 model on the synthetic dataset.
  4. **Inference**: Use the fine-tuned model to predict job roles for new queries.
- **Results**: Achieved a cosine similarity score of 0.39, indicating moderate alignment between generated and ground truth responses.

## Key Insights
- **Salary Trends**: Salaries are influenced by factors like country, years of coding experience, and programming languages.
- **Future Job Roles**: Emerging fields like AI, cloud computing, and quantum technologies are shaping future job roles.
- **Developer Demographics**: Developers aged 25–34 dominate the workforce, and JavaScript is the most widely used programming language.

## Challenges and Limitations
- **Synthetic Data**: Generating realistic synthetic data for future job roles was challenging and introduced some limitations.
- **Computational Resources**: Training large models like CatBoost and GPT-2 required significant computational power.
- **Generative Model Constraints**: GPT-2 sometimes produced repetitive or less original responses.

## Future Improvements
- **Enhanced Synthetic Data**: Use advanced generative models to create more diverse and realistic synthetic data.
- **Optimized Computational Resources**: Leverage cloud-based GPUs for faster training and experimentation.
- **Advanced Generative Models**: Explore GPT-3 or GPT-4 for more accurate and contextually relevant predictions.

## References
1. [CatBoost Regression](https://www.geeksforgeeks.org/regression-using-catboost/)
2. [K-Means Clustering](https://www.geeksforgeeks.org/k-means-clustering-introduction/)
3. [Stack Overflow Developer Survey](https://survey.stackoverflow.co/)
4. [Retrieval-Augmented Generation (RAG)](https://aws.amazon.com/what-is/retrieval-augmented-generation/)
5. [Fine-Tuning GPT-2](https://platform.openai.com/docs/guides/fine-tuning)
6. [FAISS Library](https://faiss.ai/index.html)
7. [RAG Use Case](https://cloud.google.com/use-cases/retrieval-augmented-generation)
8. [K-Means Clustering](https://en.wikipedia.org/wiki/K-means_clustering)
