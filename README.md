# Deploy to AWS CodeDeploy using Bitbucket Pipes

This repo contains a basic example for deploying applications with AWS CodeDeploy using aws-coded-deploy pipe. It this example we build and deploy a simple JavaScript application to AWS.

#Medium Blog Link:
 https://medium.com/codelogicx/cicd-deploy-to-aws-codedeploy-with-bitbucket-pipeline-b5da79b55477

## How To Use this example
* Clone this Repo on your Local machine and upload it to your Bitbucket account repo
* Create an AMI 2023 EC2 Instance & Attach `AmazonEC2CodeDeploy` Role with `AmazonEC2RoleforAWSCodeDeploy` Policy attached to it
* Install NodeJS on it (https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/setting-up-node-on-ec2-instance.html) & Change node version in `app/scripts/start.sh` file.
* Install CodeDeployAgent on it (https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-linux.html)
* Create a S3 Bucket
* Create a IAM Role user with `AWSCodeDeployFullAccess` and `AmazonS3FullAccess` permissions.

## Enable Bitbucket Pipelines in your repo
Go to the repository settings and navigate to the Pipelines section. Toggle the `Enable Pipelines` button. After that Pipelines should start executing and after a successful build your application should be up and running.


## Set up a repository variables in Bitbucket settings for your repo
* `AWS_SECRET_ACCESS_KEY`: Secret key for a user with the required permissions.
* `AWS_ACCESS_KEY_ID`: Access key for a user with the required permissions.
* `AWS_DEFAULT_REGION`: Region where the target AWS CodeDeploy application is.
* `APPLICATION_NAME`: Name of AWS CodeDeploy application.
* `DEPLOYMENT_GROUP`: Name of the AWS CodeDeploy deployment group.
* `S3_BUCKET`: Name of the S3 Bucket.


## For any queries, You can connect with me on LinkedIn: https://www.linkedin.com/in/dcgmechanics/
# Thank You So Much!!!
