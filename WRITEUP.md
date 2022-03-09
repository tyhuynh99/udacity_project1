# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- VM are usually better when we need control of the underlying operating system or are using custom software to support our needs, App Service is better for lightweight applications and services. 
- App Services cost less than VMs do. 
- Both VM and App Service support High availability and scalability. 
- The workflow to deploy an application in App Service is easier than VM.

- Because this is lightweight application, it doesn't require a huge power process or a huge number of users using it, so I choose App Service.

### Assess app changes that would change your decision.

- If this application need to handle a vast increase in the numbers of users or dedicate servers for security reasons, I have to change my decision to use the VM. 