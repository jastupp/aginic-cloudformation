#Cloud Formation

The script allows the application to be deployed as a
stack in AWS. There are two versions of the script. 
One allowing ssh to each of the instances. One which 
blocks ssh. The allow SSH script is to be used only for 
dev / debug purposes.

##Usage

- SSH stack - The ssh deployment script has five parameters, two of 
which are mandatory.
- The non SSH stack does not have the key pair name parameter.

#### Parameters
 - VPCIdParameter: (required) The VPC id for the deployment.
 - KeyNameParameter: (required) The Key pair name for the EC2 instances
 - DBUsername: The DB username to use.
 - DBPassword: The DB password to use.
 - DataBaseName: The database to create / use".

example...
```bash 
aws cloudformation deploy \
    --template-file ./Aginic.CF.json \
    --stack-name Aginic \
    --parameter-overrides \
        VPCIdParameter=vpcID \
        KeyNameParameter=KeyName # (only needed in ssh delployment)

```

