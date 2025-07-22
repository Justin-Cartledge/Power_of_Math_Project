![Justin](Justin Black.jpeg)

![Banner](github-header-image (4).png)

# To The Power of Math! Application - AWS Project

[Click - AWS-Based Exponential Calculation Application](https://dev.dcszzvgx7dd82.amplifyapp.com/)

<br><ins>Project Summary</ins><br>

This application is built on Amazon Web Services (AWS) to perform mathematical calculations, specifically raising a base number to a given exponent. It utilizes a serverless architecture for scalability and efficiency, leveraging services such as AWS Lambda for backend computation, Amazon API Gateway for secure access, and AWS Amplify or S3 for front-end hosting.


<br><ins>**Part 1. AWS Amplify** </ins><br>


<br>Create and host a simple webpage using AWS Amplify for a simple index.html ![Amplify from AWS Console](Amplify from AWS Console.png)<br>

<br>![Amplify Click Deploy App](Amplify Click Deploy App.png)

<br>Choose a create method.

<br>![Amplify Deploy App part 2](Amplify Deploy App part 2.png)

<br>Choose the App Name, Branch Name, and choose the Drag and Drop method to add the simple index.html.zip file.

<br>![Amplify Name App](Amplify Name App.png)

<br>Save and Deploy.

<br>![Amplify drag index zip](Amplify drag index zip.png)<br>

<br><br><ins>**Part 2. AWS Lambda**</ins><br>

<br>Use AWS Lambda to add the mathematical function to be triggered with Python code.<br>
Choose the "Author from Scratch" option to create the function, add the Function Name, and choose the Runtime (language for the function).<br>



<br>![Lambda python function](Lambda Python function.png)<br>


<br>![Lambda python function 2](Lambda python function 2.png)<br>

<br>Test the Lambda function.<br>

<br>![Lambda python function test](Lambda python function test.png)

<br>![Lambda python function test successful](Lambda python function test successful.png)<br>

<br>Configure the Role Name and Permissions.<br>

<br>![lambda config role name execution](lambda config role name execution.png)<br>
<br>![lambda config role name execution 2](lambda config role name execution 2.png)<br>
<br>![lambda config role name execution 3](lambda config role name execution 3.png)<br>





<br><br><ins>**Part 3. AWS API Gateway**</ins><br>

<br>Use AWS API Gateway to invoke the AWS Lambda function and enable CORS to allow objects in different domains to speak to each other.<br>

<br>![API Gateway](API Gateway.png)<br>
<br>![API Gateway 2](API Gateway 2.png)<br>
<br>![API Gateway 3](API Gateway 3.png)<br>
<br>![API Gateway 4](API Gateway 4.png)<br>
<br>![API Gateway 5](API Gateway 5.png)<br>
<br>![API Gateway 6](API Gateway 6.png)<br>


<br><br><ins>**Part 4. AWS DynamoDB**</ins><br>

<br>Use AWS DynamoDB to store results. Since AWS DynamoDB is noSQL, its lighter and easier to use.<br>

<br>![dynamo db 1](dynamo db 1.png)<br>
<br>![dynamo db 2](dynamo db 2.png)<br>

<br>Use AWS IAM (Identity and Access Management) to grant the AWS Lambda function the permission to add results to the AWS DynamoDB with the ARN URL.<br>
<br>Finally, Update the AWS Amplify code with the API Gateway URL to fully connect all the components for the application.

