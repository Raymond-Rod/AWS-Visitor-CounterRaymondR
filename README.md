# AWS Visitor Counter Raymond Rodriguez
Website Counter, a simple serverless webpage that counts page visits using Amazon S3, API Gateway, AWS Lambda, and DynamoDB

Project Overview
For this project, I created a simple visitor counter using AWS services. Whenever someone loads the webpage, a request is sent to an API that updates a visitor count stored in DynamoDB. The updated count is then displayed on the page.
The counter tracks page loads, not unique visits, so refreshing the page increases the count.

Why I Chose These Services
Lambda: I chose Lambda because I didn't want to manage an EC2 server.
S3: My website is just a simple HTML page, so S3 was an easy way to host it.
DynamoDB: I only needed to store a page name and visitor count, so DynamoDB was a good fit.
API Gateway: It gave me an easy way for my website to communicate with Lambda.

Testing
To test the project, I opened the website and refreshed the page several times. Each refresh increased the visitor count, and I verified that the updated value was being stored correctly in DynamoDB. Screenshots of the results are included in the evidence folder.

Challenge
One issue I ran into was deleting an old S3 bucket. CloudFormation couldn't delete it because the bucket still had files inside it. After some troubleshooting, I learned that S3 buckets have to be empty before they can be deleted. To move forward, I created a new stack and updated my website with the new API URL.

AI Use
I used ChatGPT and Gemini to help me come up with ideas for the project and understand some of the AWS errors I ran into. Explained why I couldn't delete an old S3 bucket as I had files inside of it. 
