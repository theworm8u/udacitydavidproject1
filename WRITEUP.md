# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

App Services
- PaaS - Allows us to focus on the application and lets Azure take care of the infrastructure
- High availability and autoscaling (supports both Linux and Windows)
- CD model, allows me to use GitHub
- Not heavy RAM needed as this is a blog with some pictures.
- Continuously paying for the service

VM
- Full control / access of vm
- Lower upfront costs
- Also supports both Linux and Windows
- High availability, scalability, and redundancy

I chose to use App Services because VM is more time consuming for the developer. I also found
App Services to be enough power to handle the needs of a blog with images.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

If the application began to work with highly secure information like health records, I would want to switch to 
a VM. It would give me more control.