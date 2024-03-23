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

 ![image (3)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/0022fb89-156d-4707-bd44-59c96838ee2e)

3. Scroll down and Click "Create subscription" <br>
4. After this , you will receive some mail for Subscription Confirmation and you have to confirm that.<br>
5. You can use any other protocols also like SQS, HTTP, SMS etc .,<br>

![22 03 2024_13 02 26_REC](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/72330bf8-b58b-41de-b29a-0e83a6dfb778)
![22 03 2024_13 02 53_REC](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/79ee6ac6-32d6-4283-a878-b86518b19307)

### Step 3 :
### Creating the Lambda :

1. Navigate to the Lambda Console.
2. Follow the Outlined steps below.
![image (2)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/efe6fc7b-8d85-4c01-afae-a4cb707cdc65)

3. Now create a Function by selecting Author from scratch.Give a function name and choose python 3.9.
   
![create function_2](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/5595fd85-b593-47a7-836c-ec1f80a0efdb)

3. Now replace the default code with the risizing-image.py and deploy the changes , Don't test the code now we have to do some more actions before testing.
4. After that , We have to give some permission for our Lambda Function to do our process (resizing) , For that navigate to the IAM Console and follow the below steps.

![image (4)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/a138f8ba-df38-42b5-90c0-d9bbdd7bb21a)

![image (5)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/23f9187c-adb9-449e-802c-95daabe079d4)

![image (6)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/870dff4e-bf65-41bd-a5ed-814b8d2e2271)

![image (7)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/068a4a5d-ec0b-49f7-8b4c-471805af2194)

![image (8)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/488e9cc8-aaa1-40f7-9577-dae199e26910)

![image (10)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/3c5a5e29-9ffa-4c08-983f-1a2c10a346b8)

![image (9)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/14d3377a-c2fc-4be9-b084-5aa2fc3842ac)

5. Now navigate to the Lambda Console and follow the steps below.
   
![image (11)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/d45e63b7-b441-4060-b3b3-a16b0a5f98f3)

![image (12)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/8366abb4-1c2f-4212-ab0f-1868a4629752)

![image (13)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/a485018a-2837-4fd1-ac8a-e7b0019b2613)

6. Now we have to trigger the function.

![image (14)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/b4f8a26a-632f-4663-8400-66f923df7775)

![image (15)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/0d9946fc-e8f8-420c-9beb-1b3364e17f67)
![image (16)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/92f26cc6-d117-44fe-81e9-4219e8532563)

7. Now we have to go to code section , and scroll down to  layers.<br>
8. We have to add layer .<br>
9. May be you can think , why ?<br>
10. It's because for resize the image we upload in our source S3 bucket , We need a python library called pillow in our code to resize the image . We can manually add Pillow library also, But it's very time consuming and you have to do lot more , Instead of manually adding pillow library we are going to use layers for Some easy action.<br>
11. Follow the outlined Steps below.

![image (17)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/44dc83ec-3d36-4a60-8a40-925bcf6cc17a)

![image (18)](https://github.com/Pravnk57/Resizing-ImaGe-Using-s3-lambda/assets/117705143/85334f7f-8dd2-4caf-8a48-974f17d4a825)
12.You can copy the arn from below.

```
arn:aws:lambda:ap-south-1:770693421928:layer:Klayers-p39-pillow:1
```
























