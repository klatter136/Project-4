<h1>CloudFormation IaC Project</h1>



<h2>Project Description</h2>

This project uses AWS CloudFormation to automate the deployment of two simple but practical scenarios. Working through it helped me gain hands-on experience with Infrastructure as Code (IaC) and understand how to build secure, scalable architectures programmatically.

<img width="1185" height="543" alt="image" src="https://github.com/user-attachments/assets/69b14b54-b578-4ac5-a930-d586e0945af7" />


Scenario 1: Bastion Host and Private EC2 Instances

In the first iteration, I created three EC2 instances:

- A Bastion EC2 instance in the public subnet
- One EC2 instance in each application private subnet across two Availability Zones

The goal was to enable secure communication between the EC2 instances in separate private subnets. To achieve this, I SSH into the Bastion EC2 (acting as a jumpbox) from my local machine. From there, I SSH into the private EC2 instance in AZ 1 and then ping the private EC2 instance in AZ 2. Because the application EC2s are in private subnets with no direct Internet access, the Bastion host provides a secure entry point.

<img width="754" height="576" alt="image" src="https://github.com/user-attachments/assets/0084ab9b-ac92-43f5-b53c-2c0f13b32d75" />

Scenario 2: Auto Scaling Group with CloudWatch Alarms


For the next scenario, I used CloudFormation to create a Launch Configuration for an Auto Scaling Group spanning two Availability Zones. I then configured a CloudWatch alarm to monitor CPU utilization and trigger scaling events automatically. This setup allows the environment to respond to workload changes, improving availability and performance while keeping costs under control.



