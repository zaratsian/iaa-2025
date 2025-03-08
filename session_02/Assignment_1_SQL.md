# Assignment: Predicting NYC Trip Duration with BigQuery Sandbox

**Objective:** Gain hands-on experience with BigQuery Sandbox for data exploration, feature engineering, and model prediction (using BigQuery ML). 

**Dataset:** You'll be using this BigQuery publically available dataset: `bigquery-public-data.new_york_taxi_trips.tlc_yellow_trips_2017` 

**Tools:** Google Cloud Platform's BigQuery Sandbox (free tier). The Sandbox is a free version of BigQuery that you can use without signing up for Google Cloud and doesn't require any payment.

Helpful Links:
* [BigQuery Quickstart](https://cloud.google.com/bigquery/docs/quickstarts/query-public-dataset-console)
* [Get Started with BigQuery ML](https://cloud.google.com/bigquery/docs/create-machine-learning-model)
* [BigQuery ML Linear Regression Example](https://cloud.google.com/bigquery/docs/linear-regression-tutorial)

## Part 1: Data Exploration and Feature Engineering

1.  **Access the Dataset:**
    * Within the BigQuery Sandbox editor, you can run this SQL to access and see the structure of the dataset: 
    ```
    SELECT
      *
    FROM
      `bigquery-public-data.new_york_taxi_trips.tlc_yellow_trips_2017`
    LIMIT 10
    ```
2.  **Explore the Data:** 
    Write SQL to answer the following questions:
    * What is the average trip duration?
    * What is the passenger count distribution?
3.  **Feature Engineering:**
    Write SQL to perform the following (basic) feature engineering task: 
    * **Time-Based Features:** Extract `day_of_week` (e.g., Monday, Tuesday) from `pickup_datetime`.

## Part 2: Model Prediction

1.  **Create a Training and Evaluation Dataset:**
    * Write SQL to split your engineered data into training and evaluation sets based on `pickup_datetime` (e.g., 80% for training and 20% for evaluation).
2.  **Train a Regression Model:** ([Example/Reference Docs](https://cloud.google.com/bigquery/docs/linear-regression-tutorial#create_the_model))
    * Use BigQuery ML to train a regression model that predicts `trip_duration`.
    * Write SQL to evaluate the model's performance using metrics like mean squared error (MSE) and R-squared.
3.  **Make Predictions:** ([Example/Reference Docs](https://cloud.google.com/bigquery/docs/linear-regression-tutorial#use_the_model_to_predict_outcomes))
    * Write SQL that uses the trained model to make predictions on the evaluation dataset. ([Evaluation Examples](https://cloud.google.com/bigquery/docs/reference/standard-sql/bigqueryml-syntax-evaluate#examples))

## Deliverables:

Once you complete the assignment, then do the following: 

1. Save your SQL code in a .txt or .sql file.
2. Go to this url (https://h-scoring-116629923513.us-central1.run.app/sql) and upload your file along with your email and the code that I provide within class. It'll be autograded and recorded on my end. If anything that is exception or needs additional feedback, then I'll provide it. Also please email me or find me after class if you'd like to chat through any part of the assignment
