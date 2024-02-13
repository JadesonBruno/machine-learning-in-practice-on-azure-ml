# Machine Learning in practice on Azule ML

This repository has the purpose of storing the project developed within the scope of the "Introduction to Machine Learning" module of the "Microsoft Azure AI Fundamentals" Bootcamp by [DIO](https://www.dio.me/), under the instruction of the teacher [Valéria Baptista](https://www.linkedin.com/in/valeriabaptista/).

The project is an essential requirement for passing the "Introduction to Machine Learning" module, consolidating participants practical learning and preparing them for subsequent challenges.

The development of this project aims to demonstrate what it is like to create a Machine Learning model in Microsoft Azure ML in practice. For a better understanding, i divided the entire process into steps, from creating the resource group to the final regression result.

## Step 1: Creating a Resource

First, let's create an Azure Machine Learning workspace. To do this, create a Resource and search for Azure Machine Learning.

<p align="center">
  <img src="./assets/create_recurses_groups.gif" alt="Creating Resourse Groups">
</p>

## Step 2: Configurating a Azure Machine Learning Workspace 

In the basics tab, we will add our workspace information. Since we are in a learning lab, we will not configure other tabs. 

To create we click on "Review + Create" and then "Create".

<p align="center">
  <img src="./assets/configurating_basics_workspace.png" alt="Configurating Workspace">
</p>

After finishing the creation of the Workspace, we click "Go to the Resource".

<p align="center">
  <img src="./assets/go_to_resource.png" alt="Go to Resource">
</p>

Next, we'll launch Azure ML Studio.

<p align="center">
  <img src="./assets/launch_studio.png" alt="Launch Studio">
</p>

## Step 3: Creating a new Machine Learning Job

On the Studio page we will start a new Machine Learning Job.

<p align="center">
  <img src="./assets/create_ml_automated_job.gif" alt="Create ML Automated Job">
</p>

## Step 4: Configurating a Machine Learning Job

We select the automatic training method.

<p align="center">
  <img src="./assets/selecting_training_method.png" alt="Selecting Trainning Method">
</p>

In basics settings we will fill in the name of the job and the name of the experiment.

<p align="center">
  <img src="./assets/basic_settings.png" alt="Basic Settings">
</p>

In task type and data we select the Regression task type and select the data set.

<p align="center">
  <img src="./assets/create_select_data.png" alt="Task Type Data">
</p>

We will inform the name and type of data.

<p align="center">
  <img src="./assets/data_type.png" alt="Data Type">
</p>

Now, we will select the data source.

<p align="center">
  <img src="./assets/source_data.png" alt="Source Data">
</p>

We enter the web url of the data source.

<p align="center">
  <img src="./assets/web_url_source_data.png" alt="Web Url Source Data">
</p>

We need to configure our data. Under "Columm Headers", we will select "Only First File has headers". After that, we wait for the data to be validated and move on to the next step.

<p align="center">
  <img src="./assets/configurating_data.png" alt="Configurating Data">
</p>

In Schema, we don't need to change any information.

<p align="center">
  <img src="./assets/schema.png" alt="Schema">
</p>

Now, we review our data and create it. Once created, we select them and move on to the next configuration.

In task settings we select the "Rentals" column as the variable of interest. And in additional settings we will select "NormalizeRootMeanSquaredError" as a metric, uncheck all flags and the allowed models will be "RadomForest" and "LightGBM".

In "Validate and Test" we will select "Train-Validation Split" as Validation Type and the Percentual validation of data will be 10%. 

<p align="center">
  <img src="./assets/target_columm_and_additional_configuration.png" alt="Target Columm and Additional Configuration">
</p>

In "Limits" we will fill in the information as shown in the image.

<p align="center">
  <img src="./assets/limits.png" alt="Limits">
</p>

When moving forward, in "Compute", i kept the values shown in the image below.

<p align="center">
  <img src="./assets/compute.png" alt="Compute">
</p>
Then, we review the job and click next to train the Machine Learning model.

Next, we need to create the model.

<p align="center">
  <img src="./assets/creating_model.gif" alt="Creating Model">
</p>

## Step 5: Model Metrics

To access the metrics of the trained model, on the model page, click the link indicated under “Created by job.” Once on the task page, navigate to the metrics tab to view the results.

<p align="center">
  <img src="./assets/acessing_metrics.gif" alt="Acessing Metrics">
</p>

## Step 6: Model Test

Now we will configure the endpoints so that we can deploy our model.

<p align="center">
  <img src="./assets/configurating_endpoints.gif" alt="Configurating Endpoints">
</p>

After the deployment process is complete, we will test the model.

For testing, i used the file:

[test.json](test.json)

<p align="center">
  <img src="./assets/model_test.gif" alt="Model Test">
</p>

The forecast generated for our model was 361.80 bicycle rentals.

## Useful Links:

[Explore Azure AI Services](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/02-content-safety.html)

[Explore Automated Machine Learning in Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)

[Data Source](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/ml/daily-bike-share.csv)

## Tecnologias Utilizadas

- Microsoft Azure Machine Learning

## Contributions

Contributions are welcome. Feel free to suggest improvements and possible corrections to the code.

## Author

Jadeson Bruno Albuquerque da Silva

[![Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jadeson-silva/)
