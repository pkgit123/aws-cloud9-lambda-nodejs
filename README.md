# aws-cloud9-lambda-nodejs
Notes from AWS Tutorial Debug Serverless App with IDE in Cloud9

* This came from the AWS Hands-On Tutorials, search for "Cloud9".
* Also review the long list of Cloud9 tutorials, see link below.

### Files in repo:
1. `index.js` - this is NodeJS code to parse datetime event data within Lambda, from tutorial step 3.  
    * This function takes an incoming payload with an option value of date or time. If date is specified, you must also specify a period value of yesterday, today, or tomorrow. The function then returns the corresponding month, day, and year. If, however, an option value of time is specified, the function returns the current hour, minute, and second. 
1. `payload.js` - this is payload to supply to lambd function when running globally.  
1. See `more-payloads` folder for more versions of the payload to compare results running in Lambda.

### AWS Infrastructure: 
* Cloud9
* API Gateway
* Lambda

### Steps in Tutorial:
1. Create AWS Cloud9 environment
   * Amazon Linux 2
   * EC2 direct access
1. Create AWS Lambda Function
   * Lambda pane: AWS Resources -> Create Lambda function
      * Node.js 12.x
      * Blueprint is empty nodejs
      * Function trigger is API Gateway
      * Resource path is /
1. Add code to Lambda function
   * See the file in repo `index.js`
1. Run or debug the function locally
   * Lambda pane: AWS Resources -> Right click on lambda function name -> Run -> Run local
   * Add payload, see file in repo `payload1.js`
   * Review results from Lambda execution
   * Run Lambda again in debug mode 
   * Add `Watch Expressions` 
      * `event.option`
      * `event.period`
      * `sc`
      * `response.body`
   * Add breakpoint to line 62 `callback` -> use other payloads
   * Review results in debug window and code window
   
### Continue from here:
* https://docs.aws.amazon.com/cloud9/latest/user-guide/tutorial-lambda-run-or-debug-local-api.html
   

### References:
* AWS Hand-On Tutorials.  Locally Debug a Serverless Application from an IDE.  https://aws.amazon.com/getting-started/hands-on/locally-debug-serverless-app-ide-cloud9/
* AWS Cloud9 Tutorials.  https://docs.aws.amazon.com/cloud9/latest/user-guide/tutorials.html
