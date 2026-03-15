ConnectaTel Customer Usage Analysis
Project Objective

The objective of this project is to analyze customer behavior for ConnectaTel, a telecommunications company.
Using historical usage data, the analysis focuses on understanding customer usage patterns, segmentation, and potential business opportunities.

The project includes data cleaning, exploratory analysis, customer segmentation, and actionable business insights that can support decision-making for service plans and marketing strategies.

Datasets Used

The analysis uses two main datasets:

users dataset

Contains demographic and account information for each customer.

Key columns:

user_id – Unique identifier of each user

first_name, last_name

age

city

reg_date – Registration date

plan – Type of plan (Basic or Premium)

churn_date – Date when the customer left the service (if applicable)

2️usage dataset

Contains historical records of user activity.

Key columns:

user_id

date

type – Event type (call or text)

duration – Call duration in minutes

length – Message length

Analysis Process

The project was developed in several stages:

1. Data Cleaning

Replacement of sentinel values (-999 in age).

Standardization of invalid categorical values (? in city).

Conversion of date columns to datetime format.

Detection of impossible or out-of-range dates.

2. Missing Values Analysis

Analysis of missing values in duration and length.

Identification of MAR (Missing At Random) patterns depending on event type (call or text).

3. Feature Engineering

Creation of usage metrics per user:

total number of messages

total number of calls

total call minutes

These metrics were merged with the user dataset to build a complete user profile.

4. Exploratory Data Analysis

Visual exploration of distributions:

Age

Number of messages

Number of calls

Total call minutes

5. Outlier Detection

Outliers were identified using:

Boxplots

IQR method

Extreme values were kept because they represent high-usage customers, not data errors.

6. Customer Segmentation

Customers were segmented by:

Usage level

Low usage

Medium usage

High usage

Based on number of messages and calls.

Age group

Young (<30)

Adult (30-59)

Senior (60+)

Key Findings

Most users belong to the Adult segment, suggesting that ConnectaTel’s primary audience is working-age customers.

The majority of customers fall into the medium usage category.

A smaller group of high-usage customers generates a disproportionate amount of activity.

Outliers in calls and minutes correspond to power users, representing valuable customers.

Business Recommendations

Based on the analysis:

Develop premium plans tailored for high-usage customers.

Offer simpler, low-cost plans for low-usage users.

Focus marketing efforts on the adult demographic segment.

Consider targeted offers for high-activity users to increase retention and revenue.

How to Run This Project

Clone the repository

Open the notebook in Google Colab or Jupyter Notebook

Run all cells sequentially.

Example:

git clone https://github.com/your-username/connectatel-analysis.git
📁 Repository Structure
connectatel-analysis
│
├── notebook/
│   └── connectatel_analysis.ipynb
│
├── data/
│   ├── users.csv
│   └── usage.csv
│
└── README.md
👩‍💻 Author

Project developed as part of a Data Analysis training program focused on practical data cleaning, exploration, and business insights.


