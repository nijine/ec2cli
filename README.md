# ec2cli
A friendlier alternative to awscli ec2 module.

## What's it for?
It makes looking up simple EC2 instance details quick and easy, versus digging through AWS' console or structuing kludgey command strings in awscli.

## Requirements
* python3.7+
* python boto3 module (pip install boto3)

## Usage
This will require a valid AWS API Key and AWS Region configured ( ~/.aws/credentials file, environment variables, etc ), along with the relevant IAM permissions in AWS.

```
# First time use (with optional addition to /usr/local/bin for easy usage anywhere)
chmod +x ec2cli [&& cp ec2cli /usr/local/bin]

# General usage
ec2cli [filter(s)]

# Examples
ec2cli --pip=10.10.50.12
ec2cli --az=us-east-1b --name=my-instance  # this will match my-instance1, my-instance2, and so on in Availability Zone us-east-1b
ec2cli  # this will print details for all instances in your target AWS region
```

Note: Filters can be on virtually any field used in the `values` array, and support wildcards without requiring an asterisk (\*).
