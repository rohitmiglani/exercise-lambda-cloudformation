<div align="center">
  <h3>Exercise-Lambda-Cloudformation</h3>  
</div>
<br />


###Pre-requisites:
Use your AWS Account

# Initial Setup
1) Open AWS System Manager Parameter Store from the AWS Console, and create the following parameter using Standard Tier of type String:
   ####Name: UserName
   ####Value: JohnDoe
2) From the AWS Console, create an S3 bucket .This S3 bucket will be passed as a Parameter in Cloudformation template 
3) Open AWS Cloudformation service and create a Cloud formation Stack by uploading CFT_Lambda.yaml template in your aws Account
4) Give a name to your stack and pass the S3 bucket name as an parameter in your Cloudformation which was created in step2
5) Click on Create Stack

# Functionality

As soon as stack is created it creates three resources 
* exercise-lambda-role - An IAM role gets created with minimum permissions which is required to execute lambda function 
* exercise-lambda - Python lambda function which reads a parameter from AWS SSM Paramstore and stores the value in a file which is uploaded to s3 bucket 
* PrimerInvoke - Custom cloudformation function to invoke lambda (exercise-lambda) 





