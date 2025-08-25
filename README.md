<h1>CloudFormation IaC Project</h1>



<h2>Project Description</h2>

For this project, I am using CloudFormation to deploy a solution to a simple scenario.

<img width="846" height="328" alt="image" src="https://github.com/user-attachments/assets/f9f133a1-a112-4424-8f95-9cd2e3b56cde" />

I will create 3 EC2 Instances: one Bastion EC2 in the public subnet, and one EC2 in each application private subnet. 

The goal is to ping the EC2 in the application subnet in AZ 2, from the EC2 in the application subnet from AZ 1. To do this, I need to SSH to the Bastion EC2 as a jumpbox, from there I can SSH to the EC2 in the application subnet of AZ 1, and ping the EC2 in the application subnet of AZ 2.
We cannot SSH into the EC2s in the application subnets directly, because they are in a private subnet, with no direct internet access.




