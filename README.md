# Azure Web App Service - Platform as a Service

## Azure App Service

**`Azure Web App Service`** is a fully managed platform for building, deploying, and scaling web apps. It is a part of Microsoft Azure, a cloud computing platform provided by Microsoft. Azure Web App Service allows developers to focus on their application code while Azure takes care of the infrastructure, making it easier to build and host web applications.

Key features of Azure Web App Service include:

1. **`Programming Language Support`**: It supports multiple programming languages such as .NET, Java, Node.js, Python, and more. This flexibility allows developers to use the language and framework of their choice.

2. **`Deployment Options`**: You can deploy your web applications using various methods, including Git, GitHub, Azure DevOps, Docker containers, or FTP. This makes it easy to integrate with popular development and deployment tools.

3. **`Scalability`**: Azure Web App Service provides automatic scaling and load balancing to handle varying levels of traffic. You can scale your application vertically by adjusting the size of the virtual machine or horizontally by adding more instances.

4. **`Managed Infrastructure`**: Azure takes care of the underlying infrastructure, such as patching, monitoring, and maintenance, allowing developers to focus on building and improving their applications.

5. **`Integrated Development Environment (IDE) Integration`**: Azure Web App Service integrates with popular IDEs such as Visual Studio, Visual Studio Code, and Eclipse, making it easier for developers to build, debug, and deploy their applications.

6. **`App Service Plans`**: Azure Web App Service offers different pricing tiers and plans, allowing you to choose the resources that fit your application's needs. This includes free and shared plans for small-scale applications and dedicated plans for larger, production-grade applications.

7. **`Security`**: Azure provides built-in security features such as authentication and authorization, SSL/TLS support, and integration with Azure Active Directory for identity management.

8. **`Monitoring and Diagnostics`**: Azure Web App Service includes tools for monitoring and diagnostics, such as Application Insights, which helps you gain insights into the performance and usage of your application.

9. **`Custom Domains and SSL Certificates`**: You can easily configure custom domains for your web applications, and Azure Web App Service supports the use of SSL certificates for secure communication.

By using Azure Web App Service, developers can streamline the deployment and management of web applications, reducing the operational overhead associated with infrastructure management. It is suitable for a wide range of web applications, from small projects to large-scale enterprise applications.

## Azure App Service Plan

Azure App Service Plans, on the other hand, **`are the underlying infrastructure that supports your web apps, mobile apps, API apps, or function apps`**. When you create an Azure App Service, you need to choose an App Service Plan, which determines the region, scale, and pricing tier for your application.

Key aspects of an App Service Plan include:

1. **`Region`**: The geographical location where your App Service Plan is hosted.

2. **`Scale`**: The number of VM instances that host your application. This can be a single instance for development and testing or multiple instances for production to provide high availability and scalability.

3. **`Size/Tier`**: The pricing tier determines the resources available for your application, including CPU, memory, and features. It ranges from basic to premium, with different performance levels.

4. **`Isolation`**: The App Service Plan provides isolation for your applications from other applications running on the same infrastructure.

By choosing the appropriate App Service Plan, you can scale your application vertically or horizontally based on your performance and availability requirements. Azure App Service takes care of the underlying infrastructure, allowing you to focus on building and deploying your applications.

**Notes**:
* Basic
  * Manual Scalling up to 3 instances
* Standard
  * Auto scalling up to 10 instances
    * Dynamic
    * Static

https://azure.microsoft.com/en-us/pricing/details/app-service/windows/

![Screenshot 2023-11-28 092803](https://github.com/codewithelmor/azure-web-app-service/assets/44918452/f45953be-2c75-4bd5-8f01-1b6de9ff9397)

![Screenshot 2023-11-28 092824](https://github.com/codewithelmor/azure-web-app-service/assets/44918452/3950b152-7a0b-42ca-a3d6-f94c8578817b)
