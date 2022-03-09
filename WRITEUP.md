# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
|         | VM           | App Service  |
| ------------- |:-------------:| :--------:|
| Cost      | For 1 tier A1 (1 vCPU, 1.75 GB RAM, 70 GB Storage) x 1 Days (Pay as you go) with Linux OS, it costs $1.44 | For 1 Tier B1 (1 Core(s), 1.75 GB RAM, 10 GB Storage) x 1 Days, it costs $0.43 |
| Scalability      | Virtual machine scale sets for autoscaling, Azure Load Balancer, limitations are platform image with 1000 nodes per scale set and custom image with 600 nodes per scale set     |   Autoscaling is built-in service, integrated load balancer, limitations are 30 instances, 100 with App Service Environment |
| Availability |  Depends on availability zones, azure region, Dedicated Host Group, type of OS disk and Data disk, the availability is atleast 95% to 99.99%      |    Depends on the tier deployments, single region or across regions, or across availability zone, the availability is atleast 99.95% to 99.99%, except developer tier of the API Management Service and any self-hosted API Management components |
| Workflow |  Create or utilize a resource group -> create VM -> connect to VM -> install any app dependencies -> run application     |  Create or utilize a resource group -> create App Service -> Deploy code to the app service       |

- VM are usually better when we need control of the underlying operating system or are using custom software to support our needs, App Service is better for lightweight applications and services. 
- App Services cost less than VMs do as table above. 
- Both VM and App Service support High availability and scalability. 
- The workflow to deploy an application in App Service is easier than VM.

- Because this is lightweight application, it doesn't require a huge power process or a huge number of users using it, so I choose App Service.

### Assess app changes that would change your decision.

- If this application need to handle a vast increase in the numbers of users or dedicate servers for security reasons, I have to change my decision to use the VM. 
