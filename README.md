## Package Distribution
Package distriution is an high level system allow the organizations to share the packages at organization level.

### High level system design:
![High level](/img/highlevel_design.png)
```architecture
  service ec2(ec2)[EC2 Server]
  service gateway(api_gateway)[API Gateway]
  service lambda(lambda)[Lambda]
  service serv1(ec2)[Public Server]
  service serv2(ec2)[Private Server]
  service s3(s3)[S3 Bucket]
  service rds(rds)[RDS DB]
  service ddb(dynamodb)[DynamoDB]
  service docdb(documentdb)[DocumentDB]
  
  group vpc[Private VPC]
    ec2
    gateway
    lambda

  group vpc2[Public VPC]
    serv1
    serv2

  group aws[AWS]
    vpc %% group in group
    vpc2 %% group in group
    s3
```
