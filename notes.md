https://github.com/madebygps/projects/blob/main/az-204/readme.md

### Steps:

- Create an Azure App Service Web App.
- Develop a basic web application that uses weather APIs.
- Containerize the application.
- Publish the container image to Azure Container Registry.
- Test the application using Azure Container Instance.
- Implement an Azure Function to send alerts when a specified weather threshold is met.
- Integrate Azure Function with your web application.
- Deploy the web application to Azure Container Apps.
- Setup a CI/CD pipeline for your application and Function.
- Setup Application insights and Azure monitor
- Push to GitHub
- Document

### oci artificats

OCI artifacts, in simple terms, refer to a range of different file formats and types that conform to the standards set by the Open Container Initiative (OCI). It aims to develop open standards for container formats and runtimes to ensure interoperability and consistency across different environments and platforms.

### Helm charts

are essentially packages for Kubernetes applications. Think of them like a folder of instructions and settings that tell Kubernetes how to install, configure, and run an application on a cluster. These charts are created according to a standard format and include all the necessary information to run an application, service, or tool inside Kubernetes.

### Functions

Function parameter like Ilogger and HttpRequest are provided by the Azure Function runtime, not the caller.

### Steps for docker and azure container registry

docker build -t yourblazorapp .
az acr login --name containerregistryweathertracker.azurecr.io
docker run -p 8080:8080 --name myblazorapp yourblazorapp (run container locally to test functionality)
docker tag yourblazorapp containerregistryweathertracker.azurecr.io/yourblazorapp:v1
docker push containerregistryweathertracker.azurecr.io/yourblazorapp:v1
