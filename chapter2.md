# Chapter 2 - Upload Image and run the process to save Information to Database

## Objective
Upload a Medicine bottle image to Azure Storage Account and have a record created in Azure CosmosDB Database with location of the image on the storage account

## Azure Concepts/Terms 

No AI capabilities will be added in this chapter, the work on this chapter lays out a framework which will be enhanced in the subsequent chapters. This chapter introduce you to a few critical Azure related concepts.

* Resource Group - is a container that holds related resources for an Azure solution. The resource group includes those resources that you want to manage as a group. As part of this starter kit you will be creating a single resource group for all the resources.
* Azure Storage - is Microsoft's cloud storage solution for modern data storage scenarios, a storage account offers multiple ways to storage files and we will be uses Azure Blobs for the purpose of our purpose. 
* CosmosDb  - is a fully managed NoSQL database service which allows saving documents without the need to design table in rigid formats and provides superior querying capabilities where saved information can be looked up easily in a performant manner.
* Logic App Service - is a cloud service that helps you automate tasks and workflows, for our purpose we will be using the Logic App to develop the background process which runs once the image is uploaded to Azure Storage. The solutions are developed using drag drop without coding effort,


## Learn More
* Resource Group - <https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview#resource-groups>
* Azure Storage - <https://docs.microsoft.com/en-us/azure/storage/>
* CosmosDb - <https://docs.microsoft.com/en-us/azure/cosmos-db/>
* Logic App Service - <https://docs.microsoft.com/en-us/azure/logic-apps/>


## Architecture Diagram
> TODO: Architecture Diagram


## Exercise

> TODO: This section is not completed, on the Logic App step it will get bigger with details on how to implement with screenshots 

* Task 1 - Sign in to the Azure Portal
* Task 2 - Follow the instruction [here](https://docs.microsoft.com/en-us/azure/storage/common/storage-quickstart-create-account?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json%23create-a-storage-account&tabs=azure-portal#create-a-storage-account-1) to create a new Storage Account keeping the following two points in mind:
	* Specify Create new Resource Group for the resources (e.g. ai-staterkit-mymeds), this only needs to be unique within your Azure Subscription
	* Storage Account Name needs to be globally unique (one trick is to use your initials with a number suffix to make it unique)
* Task 3 - Create CosmosDb Account, create database and collection
* Task 4 - Create Logic App
	* Configure EventGrid Trigger to run when file loaded to Blob Storagev
	* Configure CosmosDb Connect to create record with path to medicine image file on Blob storage