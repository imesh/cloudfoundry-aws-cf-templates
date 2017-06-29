# CloudFoundry AWS CloudFormation Templates

This repository contains AWS CloudFormation Templates for deploying Pivotal CloudFoundry on AWS. These
templates have been taken from https://network.pivotal.io/ and updated ```DBInstanceClass``` in the 
```ops-manager.json``` to be able to work in a VPC:

```json
 ...
 "PcfRds": {
       "Type": "AWS::RDS::DBInstance",
       "Condition": "CreateRDS",
         "Properties": {
         "AllocatedStorage": "100",
         "DBInstanceClass": "db.t2.large"
         ...
       }
 }
 ...
```

