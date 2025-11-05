# Securing-Application-by-using-Amazon-Cognito

## Project Overview
This project demonstrates how to secure a web application using AWS Cognito for user authentication and authorization. It includes a NodeJS backend and a static website hosted on AWS S3 and CloudFront. Users can sign up, sign in, and access role-based protected pages.

## Features
- Amazon Cognito user pool for authentication
- Cognito identity pool for authorization and AWS credentials
- Role-based access control for students and admins
- Integration with DynamoDB for data storage
- Deployment using AWS Cloud9, S3, and CloudFront

## Technologies Used
- AWS Cognito (User Pools & Identity Pools)
- AWS DynamoDB
- AWS S3 & CloudFront
- NodeJS
- HTML, CSS, JavaScript

![alt text](image.png)

## Project Working
-	The user requests access to the administrator page from the browser.
-	The request is routed to the NodeJs application server that is hosting the Birds application.
-	The application redirects the request to the Amazon Cognito managed UI.
-	The user is authenticated by the Amazon Cognito user pool, and the access token is returned to the application.
-	The Amazon Cognito SDK also stores the access token in browser's local storage for subsequent use, with the default 
   expiration of 3,600 seconds.
-	The application validates the token and returns the administrator page as requested.
-	The page is returned to the user's browser through the Cloudfront distribution.
-	The user initiates a query to a DynamoDb table.
-	The application sends the token to the Amazon Cognito identity pool and receives temporary AWS credentials upon 
    validation.
-	The application uses the received credentials to query the DynamoDB table and return data to the protected page. The page 
    is returned to the user's browser through the Cloudfront distribution.
