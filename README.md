### DEPLOYMENT AND CONFIGURATION OF A PRIVATE CLOUD IN AWS

## NAME: SUDHINDRA R
## REGISTER NO: 212224240164

## Aim
To create an Amazon Virtual Private Cloud (VPC) with public and private subnets, configure a security group, and launch an EC2 instance hosting a web server within the VPC. 

## Objectives
- Create an Amazon VPC.
- Create public and private subnets.
- Configure a security group for HTTP access.
- Launch an EC2 instance inside the VPC.
- Deploy and access a web server running on the EC2 instance.
## Procedure

### Task 1: Create a VPC
1. Open the **AWS VPC Console** and select **Create VPC → VPC and More**.
2. Configure the **CIDR block, public/private subnets, Internet Gateway, and NAT Gateway**, then create the VPC.
3. Verify that all VPC resources are created successfully.

### Task 2: Create Additional Subnets
4. Create a **second public subnet** in another Availability Zone.
5. Create a **second private subnet** and associate it with the appropriate private route table.
6. Associate the public subnet with the **public route table** and verify the associations.

### Task 3: Create a Security Group
7. Open **Security Groups** and create a group named **Web Security Group**.
8. Add an inbound rule allowing **HTTP (Port 80) from Anywhere (IPv4)**.

### Task 4: Launch an EC2 Web Server
9. Open the **EC2 Console** and launch an instance using **Amazon Linux 2023**.
10. Select the **t2.micro** instance type and configure it with the created VPC and public subnet.
11. Attach the **Web Security Group** to the instance.
12. Add the provided **User Data script** to install Apache, PHP, and the sample web application.
13. Launch the instance and wait until all **status checks pass**.
14. Access the web server using its **Public IPv4 DNS** and verify that the application is running.
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






