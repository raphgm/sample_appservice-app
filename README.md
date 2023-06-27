# Deploy code to sample_appservice-app in Azure portal  
## Create a resource group  
- az group create --name techdirectg --location eastus
## Create an App Service Plan  
- az appservice plan create --name techdAppServicePlan --resource-group techdirectg
## Create a Web Application
- az webapp create --name techdirectappserviceapplication  --resource-group techdirectg --plan techdAppServicePlan

## Move code into the web application  
- az webapp deployment source config –name techdirectappserviceapplication –resource-group techdirectg –repo-url https://github.com/raphgm/sample_appservice-app.git –branch master –manual-integration  

  
