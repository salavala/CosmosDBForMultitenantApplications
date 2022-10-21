

# Azure Cosmos DB for Multitenant Applications Workshop

# Cosmos DB Introduction
Multi Tenancy Value

# Business Scenario

List of companies and its business locations
Sample of of the data

# Architecture Solution Diagram
<img src="./images/cosmos-lab-architecture.jpg" alt="Architecture for Azure Cosmos DB Lab" Width="600"> 

# Descprtion of the other services:
1. Azure Storage Service (Azure Data Lake Service Gen2)
2. Azure Data Factory (ADF)


# Challenge-1: Deploy Azure Services  

You will be deploying the following when you click the button:
1. Azure Cosmos DB with 4 containers
2. Azure Data Lake Storage Gen2 with 2 containers
3. Azure Data Factory
4. Configures Linked Services in ADF for both the Cosmos DB and ADLS Gen2
5. Configures Datasets for the 4 Cosmos Db containers and the 2 ADLS containers

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsalavala%2FCosmosDBForMultitenantApplications%2Fmain%2Fazuredeploy.json)

# Challenge-2: Load data into Azure Storage Account

# Challenge-3: Validate Partitioning Strategies
1. Partitioning Strategy for many Small size customers
2. Partitioning Strategy for many mid size customers
3. Partitioning Strategy for large customers
4. Partitioning Additional options

# Challeng-4: Build ADF pipelines to load data into Cosmos DB

# Challeng-5: Query the data in Cosmos DB to validate the partitioning strategies

# 


