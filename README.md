**Configure an Amazon CloudFront Distribution with an Amazon S3 Origin**

Amazon Web Services (AWS) solutions architects must frequently design and build secure, high-performing, resilient, efficient architectures for applications and workloads to deliver content. Amazon CloudFront is a web service that provides a cost-effective way to distribute content with low latency and high data transfer speeds. You can use CloudFront to accelerate static website content delivery, serve video on demand or live streaming video, and even run serverless code at the edge location. In this lab, you configure a CloudFront distribution in front of an Amazon Simple Storage Service (Amazon S3) bucket and secure it using origin access control (OAC) provided by CloudFront.

**Objectives of the project:-**

Created an S3 bucket with default security settings.

Configured an S3 bucket for public access.

Added an S3 bucket as a new origin to an existing CloudFront distribution.

Secured an S3 bucket to allow access only through the CloudFront distribution.

Configured OAC to lock down security to an S3 bucket.

Configured Amazon S3 resource policies for public or OAC access.

![image](https://github.com/user-attachments/assets/db162536-9548-4994-b7c1-eabf9fdd0204)

**Tasks followed in the Project**

1.Logged into the AWS Management Console.

2.Observed the already created CloudFront origin, Explored different tabs like General,Security,Origins(Chosen ELB as origin),Behaviors,Error pages,INvalidations, Tags.

3.Created S3 bucket and changed the configuration of the bucket to allow public access.

![image](https://github.com/user-attachments/assets/a7b0839e-c76c-49d2-b588-2f179d85be89)

4. Changed the Public read policy by adding the Bucket ARN which applies to each objects in the bucket.

5. Created the new folder in the object and uploaded the image in the object and tested that the objcet can be accessible by opening in a new tab by clicking the object URL.
      ![image](https://github.com/user-attachments/assets/b03b7837-7638-46b6-8887-05821e389485)

6. Edited the Public read ploicy adding the cloudfront ARN to get origin access to the cloudfront.

7. Created the new origin and added S3 bucket as origin which created earlier.

8. Created the new behavior and added the object folder in path pattern and chosen the origin which created in the above step.

9. Tested the access to the object through the cloudfront distribution DNS by pasting it in the new tab and appended the object name.

   ![image](https://github.com/user-attachments/assets/1b267f92-43f5-49dc-b253-f10ecd83ed1b)
 



