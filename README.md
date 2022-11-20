# Overview

This project tries to bring the ever popular Machine Learning model "Boston House Price Calculator" to Azure Cloud CI/CD environment. It amkes use of Azure Pipelines for Continuos Delovery.

## Project Plan
#### The project plan here involves bringing the project to cloud native environment so that like minded people can collaborate and biuld on an already successful machine learning model.

* [Here](https://trello.com/b/E3Fk0Ir5/azure-cicd-pipeline-for-boston-hosing-prediction-ml-build-automation) is a link to Trello board, with details of current enhancements in progress and future enhancements planned.
* A project plan with estimated delivery dates can be found from the link [here](https://docs.google.com/spreadsheets/d/11sRM9VPb4arO48ChZtrHJdZn_FJhWFqeG1Onlnw36nE/edit?usp=sharing).

## Instructions

# Architectural Diagram (Shows how key parts of the system work)
![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/project_background.png)

Instructions for running the Python project. 

[Find the project code here](https://github.com/BhabaniPrasadKar/webapp1.git)
###Steps to be followed
1. Login to azure cloud shell, generate ssh key
2. Add the ssh key to your github
3. Clone the git hub repository to Azure Cloud shell![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/git_clone.png)
5. Navigate to repository folder by using `cd webapp1`,create a virtual environment in Azure cloud shell and run `make all` command
 ![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/makeall.png)
6. Run `az webapp up --name <your app name> --resource-group <your resource group> --runtime "PYTHON:3.7"` command to start a webapp
  ![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/creatingwebapp.png)
7. To verify your application is up, you can visit link https://<yourwebapp_name>.azuresites.net  
    ![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/webapp_up_and_running.png)
8.  At this point from cloud shell virtual environment submit command `./make_predict_azure_app.sh` .
    You will get a result like below,
     ![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/prediction_working.png)

##### Deploy Azure pipelines for continuous delivery
9. Login to Azure Devops and create a new devops project.
![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/create_project.png)
10. Create a service connection so that your Azure Devops account has acces to your Azure resources.
![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/create_project.png)
3. Create a  Pipeline for continuous delivery.
![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/pipeline_create.png)

To test you can make changes to the files in GITHub and find the pipeline run triggered.
![img](https://github.com/BhabaniPrasadKar/webapp1/blob/main/p6readme/successful_build_and_deploy.png)



## Enhancements

The Project can be enhanced to accept larger dataset to cater to more cities. It can also account for buyer sentiments while creating predictions.  


## Demo 

<TODO: Add link Screencast on YouTube>


