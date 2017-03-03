# Provision a web app with a SQL Database

This sample creates a free Azure Web App and SQL Database at the "Basic" service level.  The template can support other tiers of service, details for each service can be found here:

[App Service Pricing](https://azure.microsoft.com/en-us/pricing/details/app-service/)    
[SQL Database Pricing](https://azure.microsoft.com/en-us/pricing/details/sql-database/)

For more information about using this template, see [Provision a web app with a SQL Database](https://azure.microsoft.com/en-us/documentation/articles/app-service-web-arm-with-sql-database-provision/).

**IMPORTANT: on line 356 updated the cost for the region that matches your CAM deployment policy location.**
```
"location": "eastus",
```
