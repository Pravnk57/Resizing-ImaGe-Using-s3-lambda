# Automated-Image-Resizing using aws services


# Project Description: 
This project focuses on building an automated system for image processing and management within the AWS ecosystem. The goal is to streamline the handling of images by automatically resizing them and transferring them to a designated storage location while keeping stakeholders informed through notifications. Key AWS services, such as Lambda, S3, and SNS, are used to orchestrate this workflow.

# Key Features:
1.Image processing automation: Automatically resize and optimize images upon upload.

2.Secure storage: Store processed images in a secure and reliable S3 bucket.

3.Real-time notifications: Receive immediate updates about image processing via SNS.

4.Scalable architecture: Design for scalability to handle image processing demands.

5.Cost-efficient solution: Leverage AWS serverless technologies to minimize operational costs.


# Overview :
![image](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/71ce82d5-2297-4830-a5bb-fe0cb612e506)


## Steps :
### Step 1 :
### Creating Source and Designation s3 Buckets :

1. Navigate to the S3 Console.
2. Follow the Outlined Steps below.
![1st_step-s3](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/7a02a061-751b-4df0-ade1-7bff7498151c)

![2nd_step](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/4da8b875-df01-4ff9-9e89-7d7d8916de11)

![step3](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/39bd624b-d906-4474-bc49-d7f56d6af461)
3. Create the destination bucket using the same steps and name it with a unique name.
![4thstep](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/d2b7cac3-937d-4d93-88d1-5980a00b99a2)


4. As you can see above , I created two buckets one is Source bucket and another one is Destination bucket.

5. ### Step 2 :
### Creating the SNS Notification :

1. Navigate to the SNS console.
2. Follow the Outlined Steps below.
 ![topic_step5](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/5946d74c-2084-461d-ad22-a207653fceb0)

  ![resize_t0pic_6step](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/76d08162-6ec5-4581-8259-e3de9936509f)
![step07](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/77614e9f-8c37-4895-9b9a-7855a3d724f1)

  

































