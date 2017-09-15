# Simple Container Runtime AMI (SCR-AMI)

This project creates an AWS EC2 Image containing simple-container-runtime ready to run something configured by instance user-data.
See https://github.com/cfn-sphere/simple-container-runtime for details about SCR itself!

## Introduction

Architectural decisions are documented in **doc/adr**

- The AMI is designed to use Amazon Linux as a base system
- Hashicorps Packer (https://www.packer.io) is used to build the AMI
- Ansible (https://www.ansible.com) is used for everything done to manipulate the base AMI

## Build

#### Requirements

This project uses Hashicorps Packer (https://www.packer.io) to create the AMI. You can install it on your machine:

##### OSX (homebrew)

    brew install packer

#### Build

get AWS credentials and run:

    packer build -var 'vpc_id=<fillme>' -var 'subnet_id=<fillme>' -var 'base_ami_id=<fillme>' packer.json

of if you want to provide a json file containing the variables required to run the build:

    packer build -var-file=my-config.json packer.json
