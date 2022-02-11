 <h1 align="center">Udacity Udagram project</h1>

  <h3 align="center">
    Deploying a highly available web app using AWS Cloudfront</h3>




### About the project

Deploying a highly available web app - Udagram  - an Instagram like web app
Udacity project demonstrating deploying a webapp using infrastructure as code on AWS Cloudformation.

#### Scenario
Your company is creating an Instagram clone called Udagram.

Developers want to deploy a new application to the AWS infrastructure.

You have been tasked with provisioning the required infrastructure and deploying a dummy application, along with the necessary supporting software.

This needs to be automated so that the infrastructure can be discarded as soon as the testing team finishes their tests and gathers their results.

### Solution diagram
![AWS Cloudformation network and servers](UdagramAWSArchitecture2.png?raw=true "Architecture Diagram")


### Cloudformation Stacks
* UdagramNetwork
* UdagramServers

### Rubric

>#### Basics
|Criteria|Meets Specifications|
|---|---|
|Parameters|Parameter files should contain 1 or more params
|Resources|Must include a LoadBalancer, LaunchConfig, AutoscalingGroup health check, security groups, Listener and Target Group
|Outputs|Application URL i.e. Load Balancer DNS with 'http'
|Working Test| Display Apache2 Ubuntu Server Default Page 


>#### Load Balancer
|Criteria|Meets Specifications|
|---|---|
|Target Group|The auto-scaling group needs to have a property that associates it with a target group. The Load Balancer will have a Listener rule associated with the same target group
|Health Check and Listener|Port 80 should be used in Security groups, health checks and listeners associated with the load balancer

>#### Auto-Scaling
|Criteria|Meets Specifications|
|---|---|
|Subnets|Use PRIV-NET ( private subnets ) for auto-scaling instances
|Machine Specs| The machine should have 10 GB or more of disk and should be a t3.small or better
|SSH Key|There shouldn’t be a ‘keyname’ property in the launch config

>#### Bonus
|Criteria|Meets Specifications|
|---|---|
|Output| Any values in the output section are a bonus

