# Real-Time AWS Account Activity Monitoring & Alerting System

## Introduction
This project focuses on monitoring AWS account activity by securely storing and analyzing security logs using Amazon S3, CloudTrail, and CloudWatch.

## Pre-requisites

- Basic understanding of cloud computing
- An AWS account (free tier available)
- Basic knowledge of command-line interface (CLI)

## Lab Set-up and Tools

1. *AWS Account*: Sign up for a free AWS account if you don't have one.
2. *AWS Management Console*: Access to the AWS Management Console.

## Implementation Steps
1. Created a secure S3 bucket with public access blocked.
2. Enabled encryption and versioning for data protection.
3. Configured AWS CloudTrail to send logs to S3.
4. Enabled S3 server access logging.
5. Integrated CloudTrail with CloudWatch Logs.
6. Created a CloudWatch alarm to detect root user activity


# Exercise 
    ##Step 1: Create an Amazon S3 Bucket

  Open the AWS Management Console.
    Go to Amazon S3.
    Click Create bucket.
    
  Choose the bucket type:
   • General Purpose (recommended)
   • Directory (only for S3 One Zone storage class)
  Enter a unique bucket name.
You can also use an existing bucket if already created.

Enable default encryption:
     Default: SSE-S3
     Optional: SSE-KMS or DSSE-KMS for higher security

    ##Step 2: Enable AWS CloudTrail for S3

  1. Open AWS CloudTrail from the console.
  2. Click Create trail.
  3. Enter a Trail name.
  4. Choose where to store logs:
             Create a new S3 bucket, or
             Use an existing S3 bucket
  5. (Optional) Enable CloudWatch Logs:
            Attach the required IAM role
  6. (Optional) Add tags.
  7. Select the event type to log (management or data events).

    ##Step 3: Set Up Amazon CloudWatch Alarms

 1. Open Amazon CloudWatch.
 2. Go to Alarms.
 3. Click Create alarm.
 4. Select the required metrics (for S3 or CloudTrail).
 5. Set the threshold value for the alarm.
 6. Add your email ID to receive notifications.
 7.  Review and create the alarm.
  
![CloudWatch Dashboard](images/cloudwatch.png)

 ✅  PutRequest has occurred
 ✅  S3 activity is now created
 ✅  CloudWatch metrics will appear soon

## Key Topics: S3 Bucket Policies, Encryption, Access Logs

## Tools: AWS Management Console

## Conclusion

By completing these exercises, successfully created an S3 bucket, enabled versioning and server-side encryption, set bucket policies, and configured access logs. 
These steps are essential for securing data stored in AWS S3.
