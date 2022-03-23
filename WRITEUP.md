# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

App Services
- Costs: The costs will be continuous as the service is always running. 
- Scalability: There is vertical scaling without the app having to be redeployed. There is a limit of 14GB of memory and 4 vCPUs per instance.
- Availability: No control over the web server. One cannot change any server configurations. Azure handles this area for you as well as managing OS upgrades. Both Linux and Windows machines are available.
- Workflow: There is the capability to connect to GitHub and have CI/CD.

VM
- Costs: The costs scale with power. It is important to note that the upfront costs are lower. This means this could be a good option for creating Proof of Concepts and quickly testing.
- Scalability: VMs can scale vertically (more power) and horizontally (more machines). 
- Availability: There is much higher control of your server using VMs. One also as more security controls with VMs. One can have both Linux and Windows machines.
- Workflow: VMs require a lot more management support. This requires knowledge of image configurations to ensure best practices are applied. It would also require one to be responsible for patches and OS upgrades when needed. (However, these processes can be automated with a little extra effort.)


I chose to use App Services because it requires less management support by me. App Services is managed by Azure as a PaaS. App Services can autoscale based on site traffic / usage needs without having to redeploy to a larger server. I also chose App Services because of the CI/CD and being able to connect to GitHub. This makes it easier to sync code changes quickly.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

If the application began to work with highly secure information like health records, I would want to switch to 
a VM. It would give me more control.