# Amazon ElastiCache for the AWS Service Broker
Provision, manage and connect to [Amazon ElastiCache](https://aws.amazon.com/elasticache/).

## Prerequisites

**IAM resources** - see the [AWS Service Broker Requirements](https://github.com/awslabs/aws-servicebroker-documentation/blob/master/Overview.md#requirements) for details  
**VPC** - A VPC ID will be requested during launch, A VPC with unused CIDR space is required as the plan will create the required subnets.

## Plans

### memcached-custom
Exposes all available parameters for the memcached ElastiCache engine.

### memcached-prod
Best practice memcached plan for production by setting the following parameters:

    ClusterType: multi-node
    AllowVersionUpgrade: false
    PortNumber: 6379
    AZMode: cross-az
    NumberOfAvailabilityZones: 2
    AvailabilityZones: automatic
    CidrBlocks: automatic
    CidrSize: 26

## Retained resources

No resources are retained. The ElastiCache cluster, data and all associated resources will be fully removed if the Service Instance is deleted.


## Resources

[Getting Started With OCP and the AWS Service Broker](https://github.com/awslabs/aws-servicebroker-documentation/blob/master/getting-started.md)  
[AWS Service Broker Overview](https://github.com/awslabs/aws-servicebroker-documentation/blob/master/Overview.md)  
[FAQ](https://github.com/awslabs/aws-servicebroker-documentation/blob/master/FAQ.md)  
[Troubleshooting](https://github.com/awslabs/aws-servicebroker-documentation/blob/master/Troubleshooting.md)  

## License

This library is licensed under the Apache 2.0 License.