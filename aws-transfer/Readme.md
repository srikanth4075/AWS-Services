# AWS TRANSFER

## Helpful links:
[Enabling user self-service key management with AWS Transfer Family and AWS Lambda](https://aws.amazon.com/blogs/storage/enabling-user-self-service-key-management-with-aws-transfer-family-and-aws-lambda/)

## Highlights:

Serves as sftp service to companies to share data with business partners or vendors.

## Authentication:
  - Generate the public key using (ssh-keygen -b 4096 -t rsa)
  - When requested passpharse just press enter twice
  - This will create two files in default .ssh directory
    - Public key file: ~/.ssh/id_rsa.pub 
    - Private key file: ~/.ssh/id_rsa

## Creating a user in aws transfer console:
  - create a user in aws transfer console and select role that grants permissions to s3 buckets
  - For ssh key section input the above public key file i.e. ~/.ssh/id_rsa.pub 

## Making the connection using aws transfer:
  - Get the endpoint from aws transfer console
  - For the username,input the username that was created above 
  - password should left blank as aws transfer only supports public key authentication
  - ssh private key select the above private key file i.e. ~/.ssh/id_rsa


    <img width="507" alt="Screen Shot 2022-11-30 at 22 12 15" src="https://user-images.githubusercontent.com/46095027/204979217-9cc997f5-b5ac-42d0-ae50-0560fde32ab7.png">







