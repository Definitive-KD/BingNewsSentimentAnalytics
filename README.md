# BingNewsSentimentAnalytics
Bing News live Data Stream Ingestion and Sentiment Analysis via Microsoft Fabric

## Problem Statement

The objective of this project is to develop an automated and comprehensive news analytics dashboard that leverages Microsoft Azure's robust ecosystem. Using the Bing Search API, the project fetches the latest news articles. The data is then stored in Azure Data Lake Storage (ADLS), transformed and processed using Synapse Data Engineering, and subjected to sentiment analysis with Synapse Data Science. Finally, Power BI is utilized to visualize the data, and Data Factory pipelines automate the entire workflow, ensuring timely updates and alert configurations with Data Activator.

## Prerequisites:

####  1. Power BI Pro License: You'll need a Power BI Pro license to publish reports to the web. Free Power BI licenses don't allow this functionality.
####  2. Admin Permissions: Publishing to web might require permission from your Power BI administrator.




## Project Objective, Plan and Approach

- Objective

        1. reate an automated system to fetch the latest news articles.
        2. Perform sentiment analysis on the fetched news articles.
        3. Visualize the analyzed data using interactive dashboards.


- Project Plan

        1. Setup Environment: Create necessary resources and configurations in Microsoft Fabric and Power BI.
        2. Data Ingestion: Use Bing Search API to retrieve the latest news data.
        3. Data Transformation: Clean and structure the ingested data.
        4. Sentiment Analysis: Apply a pre-trained machine learning model for sentiment analysis.
        5. Data Visualization: Create interactive reports and dashboards in Power BI.
        6. Scheduling and Alerts: Automate the data pipeline and configure alerts for specific conditions.


- Approach

        1. Utilize Microsoft Fabric for data ingestion, transformation, and analysis.
        2. Store raw and processed data in Azure Data Lake Storage.
        3. Use Synapse Data Engineering for data transformation.
        4. Use Synapse Data Science for sentiment analysis.
        5. Visualize the final data using Power BI.




- Tools and Services Used

        1. Microsoft Fabric: For data ingestion, transformation, and analysis.
        2. Bing Search API: To fetch news data.
        3. Azure Data Lake Storage (ADLS): For storing raw and processed data.
        4. Synapse Data Engineering: For data processing.
        5. Synapse Data Science: For sentiment analysis.
        6. Power BI: For data visualization and reporting.



## Project Steps

### Step 1: Setup Environment
In this step, we will set up the foundational infrastructure required for the project. This involves creating an Azure resource group to manage related resources, configuring the Bing Search API to fetch news data, and establishing a Power BI workspace and database to store and visualize the data.

        1. Create a resource group in Azure.
        2. Set up a Bing Search API instance.
        3. Create a Power BI workspace and select the appropriate licensing.
        4. Create a database in Power BI for storing ingested data.




###  Step 2: Data Ingestion

We will connect to the Bing Search API to retrieve the latest news articles. This data will be ingested using Data Factory and stored in Azure Data Lake Storage in a structured JSON format

        1. Connect to Bing Search API: Use Data Factory to connect to the Bing Search API and fetch news data.
        2. Ingest Data: Configure the API to retrieve news data and store it in Azure Data Lake Storage in JSON format.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/a63feae6-82ab-48ac-ae31-e6d714c228cf)


### Step 3: Data Transformation

This step focuses on cleaning and structuring the ingested data. Using Synapse Data Engineering, we will process the raw JSON data into a Delta table format, making it suitable for analysis and visualization.

        1. Read JSON Data: Use Synapse Data Engineering to read raw JSON data.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/d30fa21f-5c93-433f-86e6-d10bad337713)

        2. Process Data: Transform the JSON data into a structured Delta table format.
![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/2e02463f-b44f-47d5-a0e5-74fe932d8640)

        3. Store Processed Data: Save the transformed data back to Azure Data Lake Storage.


![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/5e2fe41d-1689-431e-b1dd-2cf0d19cc967)




### Step 4: Sentiment Analysis

We will load the processed data into Synapse Data Science and apply a pre-trained machine learning model to perform sentiment analysis on the news articles. The results will be stored in a new Delta table.

        1. Load Data: Use Synapse Data Science to load the processed data.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/31d3af5c-c6a1-4f57-a45c-5c82c73ba699) 

        2. Apply Machine Learning Model: Perform sentiment analysis using a pre-trained model.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/372d35f3-3840-4633-9812-57c5aba97a09)

        3. Store Analyzed Data: Save the sentiment-analyzed data as a new Delta table.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/80249198-622f-4cc0-b1a7-b2023c44e186)



### Step 5: Data Visualization

In this step, we will create interactive reports and dashboards in Power BI. These visualizations will display the latest news articles and their sentiment scores, providing valuable insights.

        1. Create Reports: Use Power BI to create reports and visualizations based on the analyzed data.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/f3ab6cb0-42d3-41d9-9a71-77b6afbd17b8)

        2. Configure Reports: Display the latest news articles and their sentiment scores.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/a2d12761-9ff4-42e8-b2af-637c0747b061)




### Step 6: Scheduling and Alerts

We will automate the entire data pipeline using Data Factory, scheduling it to run at specified intervals. Additionally, alerts will be configured in Data Activator to notify us when certain conditions are met, ensuring proactive monitoring

        1. Automate Pipeline: Create a Data Factory pipeline to automate data ingestion, transformation, and analysis.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/88c4d5ca-ad65-44cc-8bf3-6b20f2b1d9c9)

        2. Schedule Pipeline: Set the pipeline to run daily at a specified time.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/13164d6e-c01d-4e41-900d-81372d98ac57)

        3. Set Alerts: Configure alerts in Data Activator to notify when specific conditions are met.

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/ed338fa2-7b8f-405a-9c5c-7c58dc805177)


### Step 7: End to End Testing

This step involves testing the entire workflow to ensure each component functions correctly. We will verify the setup, data ingestion, transformation, sentiment analysis, visualization, and scheduling processes, ensuring data flows seamlessly and alerts trigger as expected

#### Purpose
Ensure the entire data pipeline works seamlessly from data ingestion to visualization and alerts.

#### Steps
- Initial Setup Testing:

        Verify the Azure resource group and Bing Search API instance are correctly configured.
        Check the Power BI workspace and database creation.

- Data Ingestion Testing:

        Run the Data Factory pipeline to fetch news data.
        Confirm that the JSON data is correctly stored in Azure Data Lake Storage.

- Data Transformation Testing:

        Execute the Synapse Data Engineering notebook to process the raw JSON data.
        Validate the transformation and storage of structured data in Delta format.

- Sentiment Analysis Testing:

        Run the Synapse Data Science notebook for sentiment analysis.
        Verify the sentiment scores and ensure they are correctly stored.

- Visualization Testing:

        Create and publish reports in Power BI.
        Check the accuracy and interactivity of the dashboards.

- Scheduling and Alerts Testing:

        Schedule the Data Factory pipeline and ensure it runs at the specified time.
        Test alerts in Data Activator to ensure they trigger under specified conditions.


### Outcome
By conducting end-to-end testing, we ensure the reliability, accuracy, and efficiency of the entire data pipeline. This process verifies that data flows seamlessly from ingestion to visualization, providing timely and accurate insights. Moreover, the alerts configuration helps in proactive monitoring and quick response to specific data conditions, enhancing the overall effectiveness of the system.



#### Power BI report Page 1


![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/8e670c6b-b59d-47b9-b9ca-de5428602680)

#### Power BI report Page 2

![image](https://github.com/Definitive-KD/BingNewsSentimentAnalytics/assets/54216704/0b4bb8af-2fcd-454f-9d1f-37e89cb82edf)


### Conclusion
The Bing News Data Analytics project demonstrates the power and flexibility of Microsoft Azure's data engineering and analytics tools. From data ingestion using Bing Search API to sentiment analysis and interactive visualization with Power BI, this project covers a comprehensive workflow. By following the detailed steps and performing rigorous end-to-end testing, the project ensures a robust and reliable solution for news analytics. This project not only highlights the technical capabilities but also provides a practical implementation framework for similar data engineering projects.
