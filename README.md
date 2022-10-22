

# Azure Cosmos DB for Multitenant Applications Workshop

## Cosmos DB Introduction
Multi Tenancy Value

## Business Scenario

List of companies and its business locations
Sample of of the data

## Architecture Solution Diagram
<img src="./images/cosmos-lab-architecture.jpg" alt="Architecture for Azure Cosmos DB Lab" Width="600"> 

## Descprtion of the other services:
1. Azure Storage Service (Azure Data Lake Service Gen2)
2. Azure Data Factory (ADF)


## Challenge-1: Deploy Azure Services  

1.1 Click the "Deploy to Azure" button

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsalavala%2FCosmosDBForMultitenantApplications%2Fmain%2Fazuredeploy.json)

1.2. It display a custom deployment screen as shown below.

<img src="./images/Deploy_CosmosDBMultTenant_Lab_Services.jpg" alt="Azure Custom Depolyment Screen" Width="600">
	
1.3 Select your region from the dropdown list for example "East US 2".

1.4 Click on "Review+create" button.

1.5 It completes the validation as the next step and click on 'create' button.

It will create the following services in your subscription:
* Azure Cosmos DB with 4 containers
* Azure Data Lake Storage Gen2 with 2 containers
* Azure Data Factory
* Configures Linked Services in ADF for both the Cosmos DB and ADLS Gen2
* Configures Datasets for the 4 Cosmos Db containers and the 2 ADLS containers

It may take 2 to 5 minutes to create the services.

1.6 Click on "Go to resource group" when the deployment is complete.

<img src="./images/Deploy_CosmosDBMultTenant_Lab_Services_Complete.jpg" alt="Deployment complete" Width="600">

It will take you to your resource group showing the installed services.

<img src="./images/MulittenantCosmosDB_ResourceGroup.jpg" alt="Resource Group with Services list" Width="600">

You have successfully deployed the services to Azure. Congratulations for completing your first challenge.

## Challenge-2: Load data in Azure Storage Account

2.1 Download the sample test data from the repo data folder to your laptop folder
<img src="./images/MulittenantCosmosDB_Storage_SampleDataSource.jpg" alt="Source Sample Data location" Width="600">

2.2 Select the Storage Account Service from the Resource group Overview screen (above screen)
<img src="./images/MulittenantCosmosDB_storage_container_selection.jpg" alt="select hotel storage container" Width="600">

2.3 Upload Hotel booking data into hotel storage container.

Click-1: Select Upload button on the hotel data container overview screen.

Click-2: It will open up ""Upload blob"" window and Select the File Folder icon.

Click-3: Browse through your laptop and select the downloaded 'multi_tenent_hotel_reservations.csv' file

<img src="./images/MulittenantCosmosDB_storage_upload_hotel_data.jpg" alt="select sample data from laptop" Width="600">

You would see csv file in the container after successful upload operation.
<img src="./images/MulittenantCosmosDB_storage_hotel_data_loaded.jpg" alt="Uploaded hotel data file" Width="600">

2.4 Select Containers bread crumb and then select 'rentdata' container from the list to upload the sample data.
Repeat the above steps and upload data from 'mult_tenent_car_reservations.csv' file.

You have successfully loaded the sample booking data into a storage account. 

Congratulation, You have completed the second challenge and now you know how to store data in Azure Storage accounts!!


## Challenge-3: Design Cosmos DB Account to serve small, medium and large customers


## Challenge-4: Build ADF Pipelines to load data into Cosmos DB

4.1 Select Azure Data Factory service from the above picture.

It will show you the overview page of the ADF Service.

4.2 Click on the "Launch Studio" button to launch the designer studio for building the pipelines.

<img src="./images/MulittenantCosmosDB_LaunchADFStudio.jpg" alt="Launch ADF Studio" Width="600">

It will open up "Azure DataFactory Studio"" in a new window tab. 

4.3 Select "Admin" box as shown in the picture to validate the Data Source Connection(Linked) services

<img src="./images/MulittenantCosmosDB_ADFLandingPage.jpg" alt="ADF Studio Landing Page" Width="600">

It will take you to the admin page. Select the "linked services"" if it is not selected already. 

It will list the data source linked services to Cosmos DB and Storage account.

<img src="./images/MulittenantCosmosDB_ADF_Verify_linked_Services.jpg" alt="list ADF Linked Services" Width="600">

4.4 Select Cosmos DB linked Service to test the connectivity.

It will show the edit screen with the connection configuration. You can explore the options to authenticate 
such as "Account Key", "Service Principal", "System Assigned Managed Identity", "User Assigned Managed Identity" 
and access options such as "Cosmos DB Access Key" or ""Azure Key Vault".
<img src="./images/" alt="Test Cosmos DB connectivity" Width="600">

4.5 Click on "Test connection" to verify the connectivity.

4.6 Follow the same way to test the connectivity to the storage account.

## Challenge-3: Validate Partitioning Strategies
1. Partitioning Strategy for many Small size customers
2. Partitioning Strategy for many mid size customers
3. Partitioning Strategy for large customers
4. Partitioning Additional options

## Challeng-4: Build ADF pipelines to load data into Cosmos DB

## Challeng-5: Validate the partitioning strategies




