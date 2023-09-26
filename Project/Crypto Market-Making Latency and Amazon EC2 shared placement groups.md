[Crypto market-making latency and Amazon EC2 shared placement groups](https://aws.amazon.com/blogs/industries/crypto-market-making-latency-and-amazon-ec2-shared-placement-groups/)



# Terminology Explanation

**EC2**

Amazon Elastic Compute Cloud

**AWS Region**

Each *AWS Region* is a separate geographic area. Each AWS Region has multiple, isolated locations known as *Availability Zones*.AWS often has multiple regions in a single country.

**Availability Zone**

An Availability Zone is one or more discrete data centers. When you create a DB instance, you can choose an AZ or have Amazon RDS choose randomly. Random selection by RDS doesn't guarantee an even distribution of DB instances among Availability Zones.

**Host Rack**

It actually contains physical servers. Every rack has its own power source and its own network infrastructure.

**Partition placement groups**

It's an EC2 feature. It allows you to get groups of two instances(partitions) and ensure that all of the EC2 instances in a given partition group do not share any physical racks with those instances of the other partition groups.

**Access Cell**

It's a container of network of routers that connect with host racks machines. Keep adding access cell is a way to scale.

## Levels of Building Blocks

- [Placement Group Network](https://www.youtube.com/watch?v=UObQZ3R9_4c&t=896s)
  - Spine cell
  - Access cell
    - Router 1
    - Router 2
    - ... (routers are connected)
  - Host Racks
    - Machine 1
    - Machine 2
    - ... (machine coulbe be placed in parition placement groups or separate groups)
  - Racks and access cells are connected (like a parse nn)