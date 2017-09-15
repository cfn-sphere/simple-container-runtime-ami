# Choice of build tools

## Context:
This projects goal is to create an AWS EC2 AMI which can be done in several ways.

## Decision:
Use Hashicorp Packer and Ansible

## Consequences:
- Configuration of the AMI is clearly defined in separate and testable roles. 
- Implementing additional features is really easy. 
- The build process with all the edge cases that can occur is handled by a well developed specialized tool.
- A lot of logic can be handled with Ansible modules without a lot of effort.
- Developers need to understand packer and ansible and how they interact with each other.