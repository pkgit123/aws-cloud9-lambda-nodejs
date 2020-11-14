# aws-cloud9-lambda-nodejs
Notes from AWS Tutorial Debug Serverless App with IDE in Cloud9

* This came from the AWS Hands-On Tutorials, search for "Cloud9".
* Also review the long list of Cloud9 tutorials, see link below.

### Files in repo:
* index.js - this is NodeJS code to parse datetime event data within Lambda, from tutorial step 3.  
    * This function takes an incoming payload with an option value of date or time. If date is specified, you must also specify a period value of yesterday, today, or tomorrow. The function then returns the corresponding month, day, and year. If, however, an option value of time is specified, the function returns the current hour, minute, and second. 

### AWS Infrastructure: 
* Cloud9
* API Gateway
* Lambda

### References:
* AWS Hand-On Tutorials.  Locally Debug a Serverless Application from an IDE.  https://aws.amazon.com/getting-started/hands-on/locally-debug-serverless-app-ide-cloud9/
* AWS Cloud9 Tutorials.  https://docs.aws.amazon.com/cloud9/latest/user-guide/tutorials.html
