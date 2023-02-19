# HousingPrice_Microservice

![HousingPrice_Microservice workflow](https://github.com/pgpillai/HousingPrice_Microservice/actions/workflows/python-package-conda.yml/badge.svg)

# Overview

HousingPrice_Microservice is a ML project which predicts the housing price based on trained model, in this project we focused only on Continuous Integration and Continuous Delivery pipeline. We will be using the Azure DevOps pipeline Project for build and release/deployment using a Azure webapp for python flask based app and a pre trained model.

## Project Plan
The link for the Plan spreadsheet
https://docs.google.com/spreadsheets/d/12iEFXMM9TGLkD0P91e5AF7EikzzWjlo28430Mp0y56k/edit?usp=sharing

* A link to a Trello board for the project
 https://trello.com/b/6lpeh9z3/ml-predict-api


## Instructions

  
* Architectural Diagram (Shows how key parts of the system work)>
![image](https://user-images.githubusercontent.com/84101851/219969946-65bd1f8b-4e1f-45d2-a12f-3133562312e0.png)

Code resides in Git repository, Azure Devops-pipeline is configured to build and deploy the ML app to microsoft webapp.


<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


