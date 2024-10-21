![image](https://github.com/user-attachments/assets/7c6575db-82ff-4c0d-bddb-404a1a5cf12b)



## **Leveraging Terraform for User Management in Azure Entra ID and AWS IAM**

#Intro
In today’s cloud-centric world, managing user identities and permissions efficiently is crucial for maintaining security and operational integrity. I recently undertook a project that involved using Terraform to automate the creation of users in both Azure Entra ID and AWS IAM. This experience not only enhanced my technical skills but also deepened my understanding of infrastructure as code (IaC) principles.
What is Terraform?

Terraform, an open-source tool developed by HashiCorp, allows users to define and provision infrastructure using a declarative configuration language. Its ability to manage resources across multiple cloud providers makes it a versatile choice for cloud infrastructure management.
Setting Up Azure Entra ID Users

## Setup Azure

Step 1: Preparing the Environment
Before diving into Terraform scripts, I set up my Azure environment. I ensured I had the necessary permissions to create users in Azure Entra ID and configured my Azure CLI to interact with my Azure subscription.

Step 2: Writing the Terraform Configuration
Using Terraform, I created a configuration file to define the desired state of my Azure Entra ID users. Here’s a simplified example of what my configuration looked like:
<img width="506" alt="image" src="https://github.com/user-attachments/assets/c555ca46-5e8c-4a1f-84fc-490bef6275c0">

This configuration defined a single user with a unique principal name, display name, and password.

Step 3: Applying the Configuration
After validating my configuration using the terraform plan command, I applied it with terraform apply. Terraform communicated with Azure's API to create the user seamlessly, demonstrating the power of IaC.
<img width="910" alt="Screenshot 2024-10-17 144630" src="https://github.com/user-attachments/assets/27e9a3db-4536-4fb2-b8a1-1860c787a29c">

## Creating a Virtual Machine with Networking (Azure)

Next, I focused on provisioning a Virtual Machine (VM) along with the necessary networking resources in Azure. Using Terraform’s resource blocks, I defined a Virtual Network (VNet) and a VM and put them into a new Resource Group (rg):

<img width="632" alt="image" src="https://github.com/user-attachments/assets/2c2901f1-3f5d-43b4-b20c-eb0ae4fc935d">


<img width="631" alt="image" src="https://github.com/user-attachments/assets/ceca8dac-ae9e-4944-be01-a0ba03455723">

![Screenshot 2024-10-17 144537](https://github.com/user-attachments/assets/1e73f860-a2a4-499b-b853-dbe9808e6b74)


By structuring my Terraform configurations this way, I could create a robust Azure environment that included networking capabilities, ensuring my VM was ready for deployment.

## Creating IAM Users in AWS

Step 1: Preparing the AWS Environment
Similar to the Azure setup, I ensured that my AWS CLI was configured correctly and that I had the necessary IAM permissions to create users.

Step 2: Writing the Terraform Configuration
Next, I crafted another configuration file for AWS IAM user creation and group creation and moved those user into a specfric group that i created. I did this for another set of users which would be part of the IT Support Team. Here’s a snippet of the configuration:


<img width="710" alt="Screenshot 2024-10-15 124308 AWS (5)" src="https://github.com/user-attachments/assets/792bddf3-17a2-4d04-a51e-357335e66955">

![Screenshot 2024-10-15 124308 AWS (4)](https://github.com/user-attachments/assets/dac6950d-9589-48b4-914c-35188712efe8)




 Step 3: Applying the Configuration
As with Azure, I ran terraform plan to preview the changes, followed by terraform apply to execute the creation of the user in AWS.
<img width="1310" alt="Screenshot 2024-10-15 124308 AWS (2)" src="https://github.com/user-attachments/assets/5fab4c94-a7fe-4fcb-9c1d-ab3206748178">

<img width="1337" alt="Screenshot 2024-10-15 124308 AWS (3)" src="https://github.com/user-attachments/assets/6ca00786-61e8-4e77-9dce-c7c34680ad4e">


## Creating an EC2 Instance Environment

To complete the setup, I provisioned an EC2 instance within the AWS environment:

<img width="365" alt="Screenshot 2024-10-15 124308 AWS (1)2" src="https://github.com/user-attachments/assets/8c1a54ce-f928-4575-b289-19e3926f4185">

This configuration allowed me to quickly spin up an EC2 instance, ready to run applications or services as needed.

## Skills Gained from This Experience

Working with Terraform to manage users in both Azure Entra ID and AWS IAM significantly enhanced my skill set:
1.	Infrastructure as Code (IaC): I gained a deep understanding of defining infrastructure using code, which allows for version control and collaboration.
2.	Cloud Resource Management: I learned to efficiently manage and provision resources across both Azure and AWS platforms, improving my adaptability.
3.	Automation and Efficiency: By automating repetitive tasks, I significantly reduced the time spent on manual configurations, allowing me to focus on more strategic initiatives.
4.	Networking Concepts: Working with VNet, subnets, and network interfaces in Azure enhanced my networking knowledge, vital for building secure cloud environments.
5.	Security Best Practices: Understanding IAM users and group management in AWS helped me grasp the importance of security and access control in cloud environments

## Conclusion

Using Terraform to create users in Azure Entra ID and AWS IAM and manage cloud infrastucture was a rewarding experience that not only simplified my resource management but also  broadened my technical abilities and understanding of cloud identity management. The skills I gained are not only applicable to user management but also extend to broader cloud infrastructure automation tasks. As cloud environments continue to evolve, proficiency in tools like Terraform will be invaluable for any IT professional looking to stay ahead in the field .Whether you’re new to cloud computing or an experienced engineer, leveraging Terraform can transform your approach to infrastructure management, making it more efficient and scalable.
