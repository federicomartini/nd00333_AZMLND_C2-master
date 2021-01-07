*NOTE:* This file is a template that you can use to create the README for your project. The *TODO* comments below will highlight the information you should be sure to include.


# Operationalizing Machine Learning with Microsoft Machine Learning Studio

*TODO:* Write an overview to your project.
## Overview

In a typical Machine Learning application, like it happens for any software product, it's critical to bring the application into production, monitor it, and update it when needed. The process of automating the process of getting software into production is named **DevOps**. Thanks to the Microsoft Azure environment, we can **automate** the process of productionizing any **Machine Learning Application** by using the **MLOps (Machine Learning Operations)** features provided by the environment, that is the application of the **DevOps** best-practices and principles to the **Machine Learning Operations**.

Below is the list of steps to operationalize a **Machine Learning Application**:

1. Create a **Dataset** with the data of the problem we want to study
2. Create a **Model** leveraging the **Automated ML** feature
3. Deploy the **Model** and create an **Endpoint** to interact with the model
4. Consume the **Endpoint**
5. Create a **Pipeline** in Python SDK using **Jupyter Notebook** on a **Python 3 Environment**

The **Dataset** contains data about a **Bank Marketing** campaign, and the **goal** of the **model** is to predict if a **client** is going to subscribe (the target variable is indicated as **y** which can be "yes" or "no"). The finite number of states of the target variable is a good fit for using a **Classification** algorithm.


## Architectural Diagram
For this project, I went through two methods to create and deploy a **Machine Learning** model:

* Using the **Azure Machine Learning AutoML UI**
* Using a **Jupyter Notebook** to create a **Pipeline** with **AutoMLStep**, and then deploy and consume it

![](./Media/XItC0J2oMS.png)

The first thing I did was to create a **Dataset** in **Azure** to hold the data to train the **Models**. The first path started with training a **Model** with **AutoML UI**. Once the **AutoML** completed, I've deployed the **Best Model** in an **ACI (Azure Container Instance)** enabling the **Application Insights** for logging. Next, I've checked that the **Swagger** service worked as intended by providing the **documentation** to interact with the **endpoint**. Lastly, I've consumed the **Endpoint** to check the answer. As for the **Pipeline**, I've taken advantage of a **Python 3** environment to run the code in a **Jupyter Notebook** to create a pipeline with **AutoMLStep**. After creating the **Pipeline**, I've deployed it and consumed it to verify it replied as intended.

## Key Steps - Automated ML
*TODO*: Write a short discription of the key steps. Remeber to include all the screencasts required to demonstrate key steps. 
*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

Below are the steps involved in the process:

* Select and upload the Dataset
* Create a New Automated ML run
* Configure a new compute cluster using a **Standard_DS12_V2** with 1 as the minimum number of nodes
* Run the experiment using **Classification**, ensuring the **Explain Best Model** is checked
* Deploy the **Best Model** found by the **Automated ML** experiment using an **ACI (Azure Container Instance)**
* Enable the **Application Insights** to enable logging
* Interact with the **Swagger** instance runnin the documentation for the **HTTP API** of the model
* Consume the model

### Description

#### Select and upload the Dataset
Register the dataset with data from the URL: [https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv](https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv)
![](./Media/Registered_Datasets.png)

## Key Steps - Pipeline
*TODO*: Write a short discription of the key steps. Remeber to include all the screencasts required to demonstrate key steps. 
*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

Below are the steps involved in the process:

* Create a pipeline in Python SDK
* Publish the pipeline in Python SDK
* Consume the pipeline in Python SDK



## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
