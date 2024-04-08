---
section: Containers
title: Pushing to the cloud
nav_order: 3
---

In this unit, we will learn how to tag and push a Docker container image to Azure Container Registry (ACR). Azure Container Registry is a managed, private Docker registry service that stores and manages your container images. Tagging and pushing images to ACR allows you to deploy your containerized applications to Azure services such as Azure Kubernetes Service (AKS) or Azure App Service.

### Instructions

1. Install Azure CLI - If you haven't already, install the Azure CLI on your machine. The Azure CLI provides a command-line interface for interacting with Azure services.

2. Log in to Azure - Use the following command to log in to your Azure account:
   
    | ℹ️ Note                                   | 
    |------------------------------------------|
    | _Follow the on-screen instructions to complete the login process._ | 

    ```bash
    az login
    ```

3. Tag Your Docker Image - Tag your Docker image with the Azure Container Registry login server and the desired image name. Replace  **\<image-name>** with your username  name, and use **latest** as the **\<tag>**

    ```bash
    docker tag my-python-app embeddedworld24.azurecr.io/<image-name>:<tag>
    ```

    For example:

    ```bash
    docker tag my-python-app embeddedworld24.azurecr.io/fcabrera:latest
    ```

4. Log in to Azure Container Registry - Use the following command to log in to your Azure Container Registry. 
    ```bash
    az acr login --name embeddedworld24
    ```

5. Push Your Docker Image - Push your Docker image to Azure Container Registry using the following command. Replace <acr-name> with your Azure Container Registry name and <image-name> with the image name you tagged in Step 3:

    ```bash
    docker push embeddedworld24.azurecr.io/<image-name>:<tag>
    ```

    For exmaple:

     ```bash
    docker push embeddedworld24.azurecr.io/fcabrera:latest
    ```

6. Verify the image in the Azure Container Registry

    ```bash
    az acr repository list --name embeddedworld24
    ```

    | ℹ️ Note                                   | 
    |------------------------------------------|
    | _You can verify that your Docker image has been pushed to Azure Container Registry by logging in to the Azure portal, navigating to your Azure Container Registry, and checking the Repositories section._ | 



