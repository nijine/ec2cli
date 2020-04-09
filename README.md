# ec2cli
A friendlier alternative to awscli ec2 module.

## What's it for?
It makes looking up simple EC2 instance details quick and easy, versus digging through AWS' console or structuing kludgey command strings in awscli.

## Requirements
* python3.7+
* python boto3 module (pip install boto3)

## Usage
```
# First time use (with optional addition to /usr/local/bin for easy usage anywhere)
chmod +x ec2_cli [&& cp ec2_cli /usr/local/bin]

# General usage
ec2_cli [filter(s)]

# Examples
ec2_cli --pip=10.10.50.12
ec2_cli --az=us-east-1b --name=my-instance  # this will match my-instance1, my-instance2, and so on in Availability Zone us-east-1b
```

Note: Filters can be on virtually any field used in the `values` array, and support wildcards without requiring an asterisk (\*).
