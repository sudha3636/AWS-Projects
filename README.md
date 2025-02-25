**AWS multi-tier architecture**

Objectives of the Project:-

1.Deployed a virtual network spread across multiple Availability Zones in a Region using a CloudFormation template.

2.Deployed a highly available and fully managed relational database across those Availability Zones using Amazon RDS.

3.Used Amazon EFS to provision a shared storage layer across multiple Availability Zones for the application tier, powered by NFS.

4.Created a group of web servers that automatically scales in response to load variations to complete your application tier.

![image](https://github.com/user-attachments/assets/2c9e3a0e-ede9-4961-9ef2-b96a9cf999de)

**Tasks followed up in the project:-**

1.Logged into the AWS Console.

2.Navigated to CloudFormation and created the stack, which required to create the related resources like VPC, Region, DBSubnets,EFS Mountarget SecurityGroup, AppInstance SecurityGroup.

![image](https://github.com/user-attachments/assets/f29aa2e0-1c7b-4072-a806-1d5d0df416de)

3.After creating the stack verified whether all the required resources are created or not and checked the output section also.

![image](https://github.com/user-attachments/assets/40f42824-e566-4b56-a6b1-0d2ae6d4e907)

4.To create databse navigated to RDS in AWS Console, Created DB SubnetGroup. 

![image](https://github.com/user-attachments/assets/c6e021e0-f52a-42b5-8662-eb2cbe8c928c)

5.created Amazon Aurora DB,chosen Aurora(MySQL Compatible) as a engine.

![image](https://github.com/user-attachments/assets/c7f82d32-3ba7-4828-8f62-449d31096068)

6.To create Amazon EFS file system Navigate to EFS in AWS Console.

7.Created a new file system and Configured network with VPC created before while creating the stack in first step, selected subnets & security group.

![image](https://github.com/user-attachments/assets/a2958060-cb85-4e3c-b01f-e29dd5e01914)

8.To Set up Application Load Balancer, navigated to EC2 in AWS Console. Created the Target group to send the traffics to the destionation instances.

![image](https://github.com/user-attachments/assets/cf469e22-2dd7-4219-acba-09b11f34d0d9)

9. Created the Load Balancer and attached public subnets and securiyu group, linked to the target group creted in the previous step.

![image](https://github.com/user-attachments/assets/3a7c118d-df74-47db-9d19-8e2fd6e370fb)

10.Created the another stack to connect the DB subnets and EFS mount target security groups to Webtier security group instances.

![image](https://github.com/user-attachments/assets/a0ec311e-acb8-45ed-9e7c-7e5a403d8ee8)

11.Navigated to EC2 to create Auto scaling group and set the desired capacity instances according to the requirement, attached the target group and enabled ELB health checks.

12. Verfied that EC2 instances are InService and checked the health of the instances and confirmed the instance is healthy.

![image](https://github.com/user-attachments/assets/77970d06-3a1d-4dc0-9a3a-843587e38191)

13.Checked the connectivity of the application in the browser and successfully logged into web application by giving the credentials. 

![image](https://github.com/user-attachments/assets/83a3540e-1701-4513-bb48-d67c4a3f32d2)
















