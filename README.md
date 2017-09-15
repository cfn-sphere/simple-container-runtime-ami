# Simple Container Runtime AMI

This project creates an AWS EC2 Image containing simple-container-runtime ready to run something configured by instance user-data.

## Build

#### Requirements

This project uses Hashicorps Packer (https://www.packer.io) to create the AMI. You can install it on your machine:

##### OSX (homebrew)

    brew install packer

#### Run

get AWS credentials and run:

    packer build -var 'vpc_id=<fillme>' -var 'subnet_id=<fillme>' -var 'base_ami_id=<fillme>' packer.json

of if you want to provide a json file containing the variables required to run the build:

    packer build -var-file=my-config.json packer.json
