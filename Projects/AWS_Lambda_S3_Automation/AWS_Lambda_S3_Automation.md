# AWS Lambda S3 Automation

<p align="center"> <img src="./images/logo_lambda_s3.png" width="400"> </p>

## 🎯 Objectives

        Consolidate my practical knowledge of AWS resource automation using AWS Lambda and Amazon S3, exploring the creation of serverless functions to perform automated tasks, object management in S3 buckets, and integration between these services. Additionally, apply cloud computing, serverless architecture, and automation best practices to develop an efficient, scalable, and maintainable solution.

> Project developed based on the Code Girls AWS 2025 Bootcamp

## 🔁 Executing Automated Tasks with Lambda Functions and S3

        AWS Lambda is a serverless computing service provided by Amazon Web Services that allows code to run without the need to manage servers. It can be used to automate tasks and efficiently integrate different AWS services, with costs based on the execution time of the code.

        One of the most common uses of Lambda is task automation with Amazon S3, a highly scalable object storage service. When configured together, S3 can automatically trigger a Lambda function in response to events such as uploading, deleting, or modifying files (objects) in a bucket.

### ⚙️ How the Automation Works

* An event occurs in S3 — for example, a file is uploaded to a bucket.
* The event triggers a Lambda function configured to respond to that type of action.

The Lambda function then performs an automated task, such as:

* Processing or converting the file (e.g., resizing images, generating thumbnails, or extracting metadata).
* Moving or copying the file to another bucket.
* Updating a database (e.g., DynamoDB) with information about the new file.
* Sending notifications through SNS, SQS, or email.

## 🧩 Benefits of Lambda and S3 Automation

**Serverless:** no need to provision or manage infrastructure.
**Automatic scalability:** AWS adjusts capacity according to the volume of events.
**Cost efficiency:** you pay only for the time the code runs.
**Native integration:** easily integrates with other AWS services.
**High reliability:** executes tasks consistently and resiliently.

## 💡 Practical Example

When an image is uploaded to an S3 bucket named `imagens-entrada`, S3 triggers a Lambda function that resizes the image and saves the processed version to another bucket named `imagens-processadas`. Everything happens automatically, without manual intervention.

<p align="center"> <img src="./images/Diagrama_labda_s3_auto.drawio.png"> </p>

## 📌 Conclusion

        This project demonstrated how the integration between AWS Lambda and Amazon S3 enables the creation of efficient automation workflows using a serverless architecture. By using S3 events to trigger Lambda functions, I gained practical experience in automating tasks, reducing manual intervention, and developing scalable, cost-efficient, and maintainable solutions on AWS.

