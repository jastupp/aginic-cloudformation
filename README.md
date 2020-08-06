#Cloud Formation

The script allows the application to be deployed as a
stack in AWS. 

##Usage

The deployment script has five parameters, one of 
which is mandatory.

#### Parameters
 - VPCIdParameter: (required) The VPC id for the deployment.
 - KeyNameParameter: The Key pair name for the EC2 instances
 - DBUsername: The DB username to use.
 - DBPassword: The DB password to use.
 - DataBaseName: The database to create / use".

example...
```bash 
aws cloudformation deploy \
    --template-file ./Aginic.CF.json \
    --stack-name Aginic \
    --parameter-overrides \
        VPCIdParameter=vpcID
```

