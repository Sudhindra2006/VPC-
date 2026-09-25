### DEPLOYMENT AND CONFIGURATION OF A PRIVATE CLOUD IN AWS

## NAME: SUDHINDRA R
## REGISTER NO: 212224240164

# AIM:

This repository provides a comprehensive overview of Identity and Access Management (IAM), focusing on its purpose, components, and implementation practices in cloud and enterprise environments. The aim is to educate developers, system admins, and security teams on IAM essentials and offer a hands-on guide for setting up and managing IAM policies.

# Introduction
Identity and Access Management (IAM) is a framework of policies, technologies, and practices designed to manage digital identities and control access to resources. IAM helps ensure the right individuals have the right access to resources at the right time. It is crucial for securing sensitive data and resources in any organization, especially those operating in a cloud environment.

# Objectives

•	To understand the purpose and benefits of IAM
•	To learn about the core components of IAM
•	To gain hands-on experience setting up and managing IAM policies
•	To explore best practices for enhancing security through IAM

# Prerequisites

Before diving into IAM, you should have a foundational understanding of:

•	Cloud Services (AWS, Azure, Google Cloud)
•	Basic Networking and Security Concepts
•	Programming (Python, Bash, or any language preferred for API interactions)
•	Version Control (Git for managing this project)

# Core Components of IAM

IAM encompasses several core components that work together to provide secure access management:

•	Identities: Represent users, roles, or services accessing resources. Identities can be internal users, external partners, or applications.
•	Policies: Define permissions for each identity, specifying what actions they can perform on which resources.
•	Roles: Enable resource-specific permissions that can be assumed by users or services, allowing temporary access as needed.
•	Authentication: The process of verifying an identity, typically through credentials such as passwords or tokens.
•	Authorization: Determines what an authenticated identity can access or modify, enforced through policies.

# IAM Best Practices

1.	Use the Principle of Least Privilege: Limit permissions to the minimum necessary.
2.	Enable Multi-Factor Authentication (MFA): Protect against unauthorized access.
3.	Implement Role-Based Access Control (RBAC): Group permissions by roles to simplify management.
4.	Regularly Audit and Monitor Access Logs: Stay aware of access patterns and detect suspicious activities.
5.	Rotate and Manage Access Keys Carefully: Reduce risks by rotating keys frequently.

# SETUP GUIDE:

1.	Configure IAM Roles and Policies

•	Step 1: Create an IAM role with specific permissions for your users or applications.
•	Step 2: Attach policies to roles, limiting permissions according to your needs.
•	Step 3: Test access by assuming roles and attempting various actions.

2.	Enable Multi-Factor Authentication (MFA)

•	Step 1: Go to your IAM console and select your user account.
•	Step 2: Choose "Security credentials" and follow instructions to enable MFA.

3.	Set Up Identity Federation

•	Step 1: Configure identity providers (IdP) like SAML or OpenID Connect for single sign-on.
•	Step 2: Map IdP roles to IAM roles for seamless access control.

4.	Monitor and Audit with CloudTrail

•	Step 1: Enable logging of all IAM activity using services like AWS CloudTrail.
•	Step 2: Regularly review logs to ensure compliance with security policies.

# EXAMPLES:

Here are a few basic examples of IAM commands and scripts:
•	Creating a User:
aws iam create-user --user-name NewUser
•	Attaching a Policy to a User:
aws iam attach-user-policy --user-name NewUser --policy-arn arn:aws:iam::aws:policy/ReadOnlyAccess
•	Creating an Access Key for a User:
aws iam create-access-key --user-name NewUser

#While IAM is essential for managing access control, it does have limitations:
•	Complex policies can lead to unintended access if not configured carefully.
•	Requires continuous auditing and updates as roles and permissions evolve.
•	Proper training and understanding of IAM policies are critical for avoiding misconfigurations.

# Procedure

## Task 1: Create a Virtual Private Cloud (VPC)

1. Log in to the AWS Management Console and open the **VPC** service.
2. Select **Create VPC** and choose **VPC and More**.
3. Configure the VPC with the required CIDR block, public subnet, private subnet, Internet Gateway, and NAT Gateway.
4. Create the VPC and verify that all resources are created successfully.

---

## Task 2: Create Additional Subnets

1. Create a second public subnet in another Availability Zone.
2. Create a second private subnet in the same Availability Zone.
3. Associate the private route table with the new private subnet.
4. Associate the public route table with the new public subnet.
5. Verify the subnet associations.
---

## Task 3: Create a Security Group

1. Navigate to **Security Groups** in the VPC console.
2. Create a new security group named **Web Security Group**.
3. Add an inbound rule allowing **HTTP (Port 80)** traffic from **Anywhere (IPv4)**.
4. Save the security group.
---

## Task 4: Launch an EC2 Web Server

1. Open the **EC2** service and launch a new instance.
2. Select **Amazon Linux 2023 AMI** and **t2.micro** instance type.
3. Configure the instance to use the newly created VPC, public subnet, and Web Security Group.
4. Add the provided user data script to install Apache, PHP, and the sample web application.
5. Launch the instance and wait until all status checks pass.
6. Access the web server using the Public IPv4 DNS.

---
# OUTPUT:
<img width="1040" height="455" alt="image" src="https://github.com/user-attachments/assets/6792d2d8-cedb-4e7d-8463-6b3bc07ff421" />
<img width="1898" height="847" alt="image" src="https://github.com/user-attachments/assets/33ac319f-28d5-4479-bd59-da006aefd575" />
<img width="1903" height="830" alt="image" src="https://github.com/user-attachments/assets/2059d6d5-acba-4b65-8dd2-273791e3a2a4" />
<img width="1892" height="841" alt="image" src="https://github.com/user-attachments/assets/cb28dea2-8f05-4140-af06-32470c319858" />
<img width="1900" height="842" alt="image" src="https://github.com/user-attachments/assets/59d46b7b-5dbd-4d01-9293-c772b10eb109" />
<img width="1902" height="857" alt="image" src="https://github.com/user-attachments/assets/6544e47d-800d-4856-9091-a33b0d66dc1d" />
<img width="1822" height="920" alt="image" src="https://github.com/user-attachments/assets/95c4cd06-20d2-46cf-8160-63068f4bf696" />






# RESULT:
IAM is a foundational aspect of security in cloud environments, helping control and monitor access to resources effectively. By following best practices and regularly auditing IAM configurations, organizations can maintain robust access control, protecting their digital assets from unauthorized access.






