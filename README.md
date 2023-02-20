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


Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:
* Setup Cloudshell 
Login to Azure Portal and Click on the Cloudsheell on the right top as shown in the screenshot
<img width="1108" alt="Screenshot 2023-02-19 at 2 37 16 PM" src="https://user-images.githubusercontent.com/84101851/219971148-d711b4db-4ef0-4373-af32-b1dc6c43e73d.png">

* Project cloned into Azure Cloud Shell
 Clone the project in this repository to the CloudShell
  <img width="877" alt="Git-Clone-From-Cloudshell" src="https://user-images.githubusercontent.com/84101851/219971221-77bb083f-bfd2-4a8c-a5d6-11276e2370f4.png">

* Passing tests that are displayed after running the `make all` command from the `Makefile`
<img width="1413" alt="Screenshot_testcase_passed" src="https://user-images.githubusercontent.com/84101851/219971919-fe69551c-fc9d-4dd4-ac79-2d5434b46c06.png">

* On the Cloud shell run the following command
az webapp up -n <your-appservice> , where your-appservice is a unique name for your service.
 
* Check the app running, go to URL https://<your-appservice>.azurewebsites.net/, you will see a screenshot as below
 <img width="482" alt="Screenshot 2023-02-19 at 3 04 08 PM" src="https://user-images.githubusercontent.com/84101851/219972360-b6134765-9f31-4582-a451-ee4e1c56078b.png">

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).
 Setup Azure pipeline and deploying the app automaticall from azure pipeline is shown in the demo video.
 On the Demo video 
  * first 9 minutes is the set up
  * finanal 5 min will be the demo of CI/CD

* Running Azure App Service from Azure Pipelines automatic deployment
 Clieck on deployments on the azure portal and you will see the webapp deployed and it shows the Git Repo.
 
<img width="1393" alt="Screenshot 2023-02-19 at 3 06 02 PM" src="https://user-images.githubusercontent.com/84101851/219972578-6dc0852b-bb07-4268-b869-26a3f07ceb77.png">

* Successful prediction from deployed flask app in Azure Cloud Shell. 
 Change the line in make_predict_azure_app.sh to match the deployed prediction -X POST https://<yourappname>.azurewebsites.net:$PORT/predict
 
The output should look similar to this:

<img width="873" alt="Screenshot 2023-02-19 at 3 26 30 PM" src="https://user-images.githubusercontent.com/84101851/219973428-01ba3c0d-22c0-434c-a2d9-e01ebc3c3526.png">

udacity@Azure:~$ ./make_predict_azure_app.sh

* Output of streamed log files from deployed application
Run the following command 
 ```
 az webapp log tail --resource-group HousingPrice_ML_RG --name housing02052023
 ````
> 
Output will be like as shown here
 <img width="1362" alt="Screenshot 2023-02-19 at 3 11 39 PM" src="https://user-images.githubusercontent.com/84101851/219972744-6cb60312-e7e9-4c23-b826-1a213b12995f.png">


## Demo 

https://www.youtube.com/watch?v=lw3pzBM9VWU


