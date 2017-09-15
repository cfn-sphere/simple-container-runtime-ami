# EC2 UserData Configuration

## Context:
SCR is designed to accept yaml or json based configuration from any file, S3 or http(s) location. Easy configuration is key for simplicity and usability. 

## Decision:
Automatically use AWS EC2 Instance UserData to configure SCR. 

## Consequences:
SCR can be run by choosing the latest AMI and passing json or yml as user-data to an instance. This is a really flexible and common solution to configure EC2 instances.