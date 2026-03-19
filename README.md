# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Monika K________________________________
* **Register Number**: 212223090016_____________________
* **Date of Submission**: 19/03/26__________________

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

(Write the steps you followed in your own words)

1.First, I created a VPC in Amazon Web Services. I gave it a CIDR block of 10.0.0.0/16. This VPC acts as my private network where all my resources will be created.

Next, I created a public subnet inside the VPC with CIDR 10.0.1.0/24. I enabled auto-assign public IP so that any instance launched in this subnet will automatically get a public IP address.

After that, I created an Internet Gateway and attached it to my VPC. This allows my VPC to communicate with the internet.

Then, I created a route table and added a default route (0.0.0.0/0) pointing to the Internet Gateway. I associated this route table with my public subnet. This step ensures that traffic from my subnet can reach the internet.

Next, I created a security group which acts as a virtual firewall. I allowed inbound traffic for SSH on port 22 and HTTP on port 80.

After completing the network setup, I launched an EC2 instance using Amazon Linux 2 AMI with instance type t2.micro. I selected my VPC, public subnet, created security group, and key pair.

Finally, I connected to the EC2 instance using SSH and installed the Apache web server. I started the service and created a simple HTML page. Then I copied the public IP address of the instance and opened it in a web browser. The webpage was displayed successfully.

So, this is how I created a VPC, launched an EC2 instance, and hosted a simple web server in AWS. ---


---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1918" height="983" alt="image" src="https://github.com/user-attachments/assets/564c4bcf-e4c0-4f1c-9407-3657b7797100" />


---

### Screenshot 2: EC2 Instance Running

<img width="1918" height="987" alt="image" src="https://github.com/user-attachments/assets/0c91eafa-1010-45f1-bb31-9c0997137176" />


---

### Screenshot 3: Web Server Output in Browser

<img width="1907" height="1007" alt="image" src="https://github.com/user-attachments/assets/0bcf9e5a-b9b1-4512-8f96-0a61316a88ee" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
# Lab 1 - Introduction to AWS Identity and Access Management (IAM)

## Title
Introduction to AWS Identity and Access Management (IAM)


## Objective
The objective of this lab is to understand how AWS Identity and Access Management (IAM) controls authentication and authorization in AWS. The lab focuses on exploring IAM users and groups, analyzing attached policies, assigning users to appropriate groups based on organizational roles, and validating permissions by testing service access.


## Prerequisites
- Basic understanding of cloud computing concepts  
- AWS Academy Lab access  
- Web browser with internet connectivity  


## Tools Used
- AWS Management Console  
- AWS Identity and Access Management (IAM)  
- Amazon EC2  
- Amazon S3  


## Tasks Performed

### Task 1: Explore IAM Users and Groups
- Reviewed pre-created IAM users: user-1, user-2, user-3  
- Explored IAM groups: EC2-Admin, EC2-Support, S3-Support  
- Inspected managed and inline policies attached to groups  
**Screenshot:**  
<img width="1522" height="722" alt="image" src="https://github.com/user-attachments/assets/e7d2952a-6c28-4873-98ee-85d5d1f9b6d6" />


### Task 2: Add Users to Groups
- Added user-1 to the S3-Support group  
- Added user-2 to the EC2-Support group  
- Added user-3 to the EC2-Admin group  
**Screenshot:**  
<img width="1919" height="929" alt="image" src="https://github.com/user-attachments/assets/ac9e775e-3082-4eae-842e-00982538d78f" />


### Task 3: Test IAM User Permissions
- Logged in using IAM sign-in URL  
- Verified S3 access for user-1  
- Verified EC2 read-only access for user-2  
- Verified EC2 administrative access for user-3  
**Screenshot:**  
<img width="1600" height="762" alt="image" src="https://github.com/user-attachments/assets/91b9cca7-978f-4339-a983-853f3fb031d9" />



## Workflow
1. Accessed IAM console and reviewed users and groups.  
2. Inspected policy permissions attached to groups.  
3. Assigned users to groups based on their roles.  
4. Logged in as each IAM user using the sign-in URL.  
5. Validated permissions by accessing AWS services.  


## Learning Outcomes
- Understood the role of IAM in AWS security.  
- Learned how IAM users, groups, and policies interact.  
- Gained practical experience implementing role-based access control.  
- Verified permission enforcement through real-time service testing.  


## Conclusion
This lab provided hands-on experience with AWS IAM by demonstrating how organizations manage secure access to cloud resources. Assigning users to groups with predefined policies simplified permission management and ensured role-based access control across AWS services.


## Author
**Name:**Monika K and 212223090029
**Course:** Introduction to Cloud Computing  

