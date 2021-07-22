Overview
Cloud platform automation assets is a centralized repository which manages automation templates and community contributed templates for creating azure resources. The repository is consumable for M&S Engineers. Using these templates project teams can include their IaC scripts as part of their CI/CD pipeline.

Features
The repository will be managed by cloud platform team with all fixes and updates required for templates
The automation templates are developed based on M&S Governance and Policy
Infrastructure as code will be part of your CI/CD pipeline
Contribute reusable automation templates for building infrastructure
How To Consume
Pre-Requisites
User needs to have a Service Principal with below permission to consume the automaton templates.
Network Read write (Subscription Level)
To read the Vnet / Subnet details
APPS Admins (Resource Group Level)
To create azure resources – VM , Load balancer, Storage account.
Reader
Reader access to shared image gallery (Windows VM OS , Linux OS)
Automation Account (DSC windows) - To install Extensions
Service principal - API permission
AD Reader Scope for Service Principal
How to use the templates
The template consist of two files,
Wrapper Scripts - It is used to execute the ARM templates with required inputs.It can be used within a CI/CD pipeline.
ARM Templates - It used for provisioning a resource.
User has to create a separate stage called "Build Infra" in their CI/CD pipeline stage.
Prepare the inputs required for the automation templates.
Clone the cloud-platform-automation-assets repo in "Build Infra" Stage.
Pass the input file location as an argument to the wrapper script which is available in the powershell folder.
Copy the required templates and update in your CI/CD Pipeline.
