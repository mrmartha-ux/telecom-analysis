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

Hallazgos Clave

La mayoría de los usuarios son del segmento adulto (edad laboral).

La mayoría tiene uso medio, mientras que unos pocos usuarios de alto uso generan gran parte de la actividad.

Los outliers en llamadas y minutos representan clientes valiosos.

Recomendaciones

Crear planes premium para clientes de alto uso.

Ofrecer planes simples y económicos para usuarios de bajo uso.

Enfocar marketing en el segmento adulto.

Realizar ofertas dirigidas a usuarios de alta actividad para aumentar retención e ingresos.

Cómo Ejecutar

Clonar el repositorio:

git clone https://github.com/your-mrmartha-ux/connectatel-analysis.git

Abrir el notebook en Google Colab o Jupyter Notebook.

Ejecutar todas las celdas secuencialmente.

Estructura del Repositorio
connectatel-analysis
│
├── notebook/
│   └── connectatel_analysis.ipynb
├── data/
│   ├── users.csv
│   └── usage.csv
└── README.md
Autor

Proyecto desarrollado como parte de un bootcamp de Análisis de Datos en Triple Ten, enfocado en limpieza de datos, exploración y generación de insights de negocio.

