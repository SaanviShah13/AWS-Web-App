# AWS-WEB-APPLICATION
Architected and built an end-end aws web application

# AWS Deployment Project: Power Calculation Web Application

## Overview
This project demonstrates a web application hosted on AWS Amplify that calculates the power of two numbers. This project, while simple in concept, serves as a practical exercise in leveraging key AWS services like Amplify, API Gateway, Lambda functions, and DynamoDB, providing valuable insights into their integration and functionality. 

## Architecture
The architecture involves the following components:
- **AWS Amplify**: Hosts the frontend web application.
- **API Gateway**: Receives HTTP requests from the frontend and triggers Lambda functions.
- **Lambda Function**: Computes the power of two numbers passed via API Gateway.
- **DynamoDB**: Stores the computed results.
  ![architecture](https://github.com/user-attachments/assets/21ee1256-a876-4798-a120-17806c900e13)

## Output
  ![Screenshot 2024-07-12 225119](https://github.com/user-attachments/assets/daa52ed0-6d66-40fc-9dd7-cd270bc5c45a)
  ![image](https://github.com/user-attachments/assets/9e8759e9-1888-47b8-855c-d5282cc2e872)


## Deployment Steps
To deploy this project on your AWS environment, follow these steps:
1. **Create an Amplify Application**
   - Set up an application using the Amplify Application deployment service on AWS. Keep this application handy for later steps.
     ![Screenshot 2024-07-12 214853](https://github.com/user-attachments/assets/6e310c7a-6c6b-4cde-b144-c10c0846a033)


2. **Create and Configure Lambda Function**
   - Create a Lambda function to handle the computation of the inputs from the web page.
   - Apply the provided JSON code to the Lambda function. This code will take the input from the web page, perform the mathematical operation, and return the result.
     ![Screenshot 2024-07-12 230630](https://github.com/user-attachments/assets/eb495898-bc32-49e8-b0cf-f8354371bb7f)


3. **Set Up DynamoDB for Result Storage**
   - Create a DynamoDB table to store the computed results.
   - Configure IAM roles and policies for the Lambda function to allow it to put/store data in the DynamoDB table. Ensure the Lambda function has the correct permissions.
     ![Screenshot 2024-07-12 230639](https://github.com/user-attachments/assets/a6a91dbb-80a5-47ae-96b6-e63af7c3a0f2) 
    

4. **Create API Gateway to Invoke Lambda**
   - Set up a RESTful API using AWS API Gateway.
   - Configure the API Gateway to invoke the Lambda function with the input values from the web application.
     ![Screenshot 2024-07-12 220146](https://github.com/user-attachments/assets/9275123a-167a-4e65-ac23-2d9e26c30108)

  
5. **Test Connectivity Between Services**
   - Test the connections between Amplify, Lambda, DynamoDB, and API Gateway.
   - If any issues arise, ensure the correct Amazon Resource Names (ARNs) are used and permissions are properly configured.

6. **Connect Web App to Backend**
   - Obtain the URL link of the API Gateway, which is generated during the deployment.
   - Insert this URL link into the script section of your HTML code in the web application. This will allow the web app to access the API Gateway and invoke the Lambda function.

## Future Improvements
- **Custom Domain**: Purchase a domain and use Amazon Route 53 to configure a custom domain for the web application.
- **Enhanced User Interface**: Improve the web application's UI/UX for a better user experience.
- **Additional Features**: Add more mathematical operations or other functionalities to make the application more versatile.
- **Scalability**: Implement auto-scaling for Lambda functions and DynamoDB to handle increased traffic and data volume.

# AWS-Web-App
