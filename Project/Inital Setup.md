# Create an EC2

## Login Key

Select .pem file

## Network Setting

Create a security group. Allow SSH traffic from, HTTPS and HTTP.

## User Data

```shell
#!/bin/bash
yum update -y
yum install git -y
yum install python3 -y
# Development Tools have c++
yum groupinstall "Development Tools" -y
```



# SSH Config

1. Open ssh config file, add the following content

```txt
Host <Any Text>
  HostName <public ip>
  User ec2-user
  IdentityFile <path of .pem file>
```

2. Update permission to owner only

```shell
chmod 0400 <path of .pem file>
```

When instances restart, need to change public ip.

# Git Config

```shell
git config user.name "Your Name"
git config user.email "youremail@example.com"
```

