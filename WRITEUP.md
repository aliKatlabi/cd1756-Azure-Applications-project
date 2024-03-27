# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.


We need to carefully evaluate and justify the best resource option for deploying our application.

* When it comes to cost analysis, creating a VM with a Standard B1s - basic size would cost us $4.09/month. However, we have the option to create an App service on a free tier to deploy our application, which could be more cost-effective.

* In terms of scalability, a VM allows us to easily scale resources such as CPU, RAM, and storage as the application grows. On the other hand, while an App service can scale up/out with an App Service plan, it only supports a maximum of 14GB of memory and 4 vCPU cores per instance.

* Both VM and App Service ensure high availability. VM provides two options for scaling—Virtual Machine Scale Sets and Load Balancers. App service supports both Linux and Windows environments but is limited to a specific set of programming languages.

* For the workflow, deploying applications on a VM requires us to prepare and configure everything like runtime, environment, open port, SSL, firewall, domain connection, IIS, etc. With App service, we can focus on deployment and configuration. Azure supports automated deployment directly from several resources like Azure Repos, GitHub, Bitbucket, and Local git.

* Considering all these factors, App service seems to be a good choice for this project. This is a small application and we can quickly configure and deploy it to App service from Github. It also allows us to easily authenticate users with Active Directory and monitor with Alert, Logs, which provides easy log filtering with many example queries.
### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* https://cmsapplication.azurewebsites.net/