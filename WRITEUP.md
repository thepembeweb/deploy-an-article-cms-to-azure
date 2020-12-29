# Write-up

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

#### VM
Deploying the app to a VM would have been a great choice if the primary requirement was to have full access and control of the VM. If high availability, scalability, and redundancy were a priority, then we could group multiple VMs to efficiently achieve this. However, going the VM route comes at a cost. With the pricing for a standard tier D2 VM with a Linux OS being about $80 a month, horizontal scaling could get quite costly very quickly. Another drawback is that VMs can be more time consuming for the developers than other compute options. Deployment workflows for VMs can also get complicated and require more expertise because the developers also need to manage the end to end process especially if the app is not built in a language that is fully supported in Azure. 


#### App Service
Using App Service would be ideal for this app if the main criteria was cost. With the basic tier being $13.14 per instance for 730 hours, this means we can have multiple instances to get high availability and scalability for less than the price of the single VM (standard tier). CI/CD through GitHub workflows on the Azure portal also makes updating the CMS app very easy as it is fully supported out of the box. 

#### Selected Deployment Option
I went with App Service because the CMS app is very simple one, and is not expected to handle a vast increase in the number of users, with separate, dedicated servers which would have been suitable for a VM. Also, because the CMS app is built with Python, using App Services is a great choice since Python is fully supported. 


### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.*

#### VM
I would have used a VM if the app the requirements changed, for example; if the app needed more compute power, needed to use an unsupported language feature; or OS customization. A VM is better suited to handle any of the needs stated above.

#### App Service
I would have changed my previous decision if the CMS app required more compute power, an unsupported language feature or had been expected to handle a vast increase in the number of users, with separate, dedicated servers. A VM would be the ideal choice in terms of costs, scalability, availability, and workflow.
