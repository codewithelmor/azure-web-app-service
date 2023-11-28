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

## App Service Features

### App Service Always On Setting

In Azure App Service, the **`"Always On"`** feature is a setting that helps ensure that your web app or API is **`always running and responsive`**. By default, this feature is turned off for cost-saving reasons, especially in scenarios where applications don't need to be constantly active. However, for certain types of applications or scenarios, you might want to enable the "Always On" setting.

Here's what you need to know about the "Always On" feature in Azure App Service:

1. **`Purpose`**: The primary purpose of the "Always On" feature is to keep the application warm and responsive. In a standard web hosting environment, if your application is idle for some time, the platform might decide to unload it from memory to conserve resources. When a request comes in, the application might experience a delay as it needs to be loaded back into memory. Enabling "Always On" prevents the application from being unloaded, reducing the startup time for the first request.

2. **`Scenario`**: This feature is particularly useful for applications that rely on background processes, scheduled jobs, or need to be instantly responsive to incoming requests. If your application has periodic tasks or relies on background processing, "Always On" helps ensure that these processes continue to run without interruption.

3. **`Configuration`**: You can enable "Always On" through the Azure Portal or by configuring it in your application's settings. In the Azure Portal, navigate to your App Service, go to "Configuration" under the "Settings" section, and set the "Always On" option to "On."

4. **`Cost Implications`**: Enabling "Always On" may increase the cost of running your app since it keeps the app continuously running, consuming resources even during periods of low or no activity. Therefore, consider your application's requirements and usage patterns before deciding to enable this feature.

5. **`Performance Monitoring`**: While "Always On" helps with responsiveness, it's also essential to monitor your application's performance to ensure that it meets your expectations. Azure Application Insights or other monitoring tools can be valuable for tracking application health and performance.

### **Azure App Service Deployment Center**

The **`Azure App Service Deployment Center`** is a feature within Azure App Service that provides a **`centralized place for managing and configuring continuous deployment for your web applications`**. It supports various source code repositories and build systems.

Some key points about the Deployment Center include:

1. **`Source Integration`**: Deployment Center allows you to connect your web app to source control repositories like Azure Repos, GitHub, Bitbucket, and others.

2. **`Build Providers`**: It supports different build providers, such as Azure Pipelines, Bitbucket Pipelines, and GitHub Actions, to build and package your application.

3. **`Deployment Options`**: After the build process, Deployment Center assists in deploying your application to the Azure App Service. It supports both manual and continuous deployment options.

4. **`Integration with CI/CD`**: While Deployment Center can be used for manual deployments, it often works in conjunction with CI/CD tools to enable automated, continuous deployment processes.

### Azure App Service Deployment Slots

**`Azure App Service Deployment Slots`** are a feature provided by Microsoft Azure that allows you to **`host different versions of your web app or API in separate slots, or environments, within a single Azure App Service`**. Deployment slots enable you to deploy, test, and swap different versions of your application without affecting the production environment. This can be useful for scenarios such as testing new features, rolling out updates, or performing A/B testing.

Here are some key concepts related to Azure App Service Deployment Slots:

1. **`App Service Plan`**: An App Service Plan defines the region and the size (small, medium, large, etc.) of the virtual machines that host your web apps. Deployment slots share the same App Service Plan as the production slot.

2. **`Production Slot`**: This is the main slot where your live application runs. When users access your app, they are interacting with the production slot.

3. **`Deployment Slots`**: Each Azure App Service can have multiple deployment slots, including a production slot and additional slots for staging, testing, or other purposes. These slots are essentially separate instances of your web app.

4. **`Slot Settings`**: Deployment slots can have their own configuration settings, including connection strings, environment variables, and other app settings. This allows you to configure each slot independently.

5. **`Slot Swap`**: The slot swap feature allows you to swap the content of one slot with another without any downtime. This is particularly useful for rolling out updates or promoting a tested version to production.

6. **`Testing and Staging`**: Deployment slots are often used for testing and staging environments. You can deploy a new version of your app to a slot, test it thoroughly, and then swap it with the production slot if everything looks good.

6. **`Traffic Routing`**: You can control the percentage of traffic routed to each slot during a swap. This allows for gradual rollouts and A/B testing.

To create and manage deployment slots in the Azure portal, you can navigate to your App Service, select "Deployment slots" from the menu, and then add or configure slots as needed.

Deployment slots provide a powerful mechanism for managing and deploying web applications in a flexible and controlled manner, reducing the risk associated with updates and changes to your production environment.

### Azure App Configuration

**`Azure App Configuration`** is a service provided by Microsoft Azure that helps developers **`manage application settings and feature flags in a central location`**. It allows you to store and retrieve configuration settings for your applications in a secure and scalable manner.

Here are some key aspects of Azure App Configuration:

1. **`Centralized Configuration Store`**: Azure App Configuration provides a centralized location to store configuration settings for your applications. This makes it easier to manage and update settings across multiple environments.

2. **`Dynamic Configuration`**: One of the key features is the ability to update configurations dynamically, without requiring a restart of your application. This is particularly useful for scenarios where you want to make changes to your application's behavior without redeploying the entire application.

3. **`Feature Flags`**: Azure App Configuration supports feature flags, also known as feature toggles or feature switches. Feature flags allow you to control the availability of certain features in your application without redeploying it. This is useful for gradual feature rollouts, A/B testing, and other experimentation scenarios.

4. **`Secure Configuration Store`**: Azure App Configuration ensures that your configuration data is stored securely. It supports encryption of sensitive information, and you can control access using Azure Active Directory (Azure AD) authentication and authorization.

5. **`Integration with Azure Services`**: Azure App Configuration can be easily integrated with other Azure services. For example, it can be used in conjunction with Azure Key Vault for managing sensitive configuration settings.

6. **`Versioning and History`**: Azure App Configuration keeps track of configuration changes, allowing you to view the history of changes and roll back to a previous version if needed.

7. **`SDKs and Language Support`**: Azure App Configuration provides SDKs for various programming languages, making it easy to integrate with your applications regardless of the technology stack you are using.

To use Azure App Configuration, you typically create a configuration store in the Azure portal, configure your application to use the store, and then access configuration settings programmatically through the Azure App Configuration SDK.

## Azure App Service Plan

Azure App Service Plans, on the other hand, **`are the underlying infrastructure that supports your web apps, mobile apps, API apps, or function apps`**. When you create an Azure App Service, you need to choose an App Service Plan, which determines the region, scale, and pricing tier for your application.

Key aspects of an App Service Plan include:

1. **`Region`**: The geographical location where your App Service Plan is hosted.

2. **`Scale`**: The number of VM instances that host your application. This can be a single instance for development and testing or multiple instances for production to provide high availability and scalability.

3. **`Size/Tier`**: The pricing tier determines the resources available for your application, including CPU, memory, and features. It ranges from basic to premium, with different performance levels.

4. **`Isolation`**: The App Service Plan provides isolation for your applications from other applications running on the same infrastructure.

By choosing the appropriate App Service Plan, you can scale your application vertically or horizontally based on your performance and availability requirements. Azure App Service takes care of the underlying infrastructure, allowing you to focus on building and deploying your applications.

Here are some common pricing tiers for Azure App Service Plans:

1. **`Free Tier`**: This tier provides a basic level of service for small applications with minimal traffic. It is suitable for development and testing purposes.

2. **`Shared Tier`**: This tier is a low-cost option suitable for small-scale applications with low traffic. It shares resources with other apps on the same plan.

3. **`Basic Tier`**: This tier offers increased performance and additional features compared to the Free and Shared tiers. It is suitable for small to medium-sized applications.

4. **`Standard Tier`**: This tier is designed for applications that require additional scaling and performance capabilities. It includes more resources and features than the Basic tier.

5. **`Premium Tier`**: The Premium tier is suitable for applications that demand high performance, scalability, and additional features. It provides enhanced capabilities compared to the Standard tier.

6. **`Isolated Tier`**: This tier is designed for mission-critical applications that require high performance, scalability, and advanced networking features. It provides dedicated resources and isolation for increased reliability.

Each tier comes with different resource allocations, such as CPU, memory, and storage, as well as additional features like custom domains, automatic scaling, and deployment slots.

Keep in mind that the pricing may vary based on factors such as region, resource allocation, and whether the plan is on a Windows or Linux operating system.

**Notes**:
* Basic (non-production environment)
  * Manual scalling up to 3 instances
* Standard (production environments)
  * Auto scalling up to 10 instances
    
How to visually check the App Service current running instance count?
![image](https://github.com/codewithelmor/azure-web-app-service/assets/44918452/96f20bc6-fb11-47da-8289-530e03fb1954)

https://azure.microsoft.com/en-us/pricing/details/app-service/windows/

![Screenshot 2023-11-28 092803](https://github.com/codewithelmor/azure-web-app-service/assets/44918452/f45953be-2c75-4bd5-8f01-1b6de9ff9397)

![Screenshot 2023-11-28 092824](https://github.com/codewithelmor/azure-web-app-service/assets/44918452/3950b152-7a0b-42ca-a3d6-f94c8578817b)
