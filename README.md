# lambda-sam
This is a demo for AWS Lambda Serverless Application Model(SAM) for automation of build and deployment of lambda. 
Detail instructions can be found here http://docs.aws.amazon.com/lambda/latest/dg/automating-deployment.html 

The high-level flow is - 

1) Create the lambda code and SAM deployment spec (e.g. node.js index handler for lambda implementation and samTemplate.yaml file)

2) Create the build spec for CodeBuild. CodeBuild will install dependancy package ("npm install" commmands specified in CodeBuild spec) and packing the lambda function code basd off the SAM spec (aws cloudformation package). Cloudformation is used as a template for SAM packaging functions.

3) Use Code Pipeline to automate the build and deployment w/ code on github. It can also be integrated with AWS CodeCommit.
