# Simple Container Runtime AMI

This project creates an AWS EC2 Image containing simple-container-runtime ready to run something configured by instance user-data.

## Build

#### Requirements

This project uses Hashicorps Packer (https://www.packer.io) to create the AMI. You can install it on your machine:

##### OSX (homebrew)

    brew install packer

#### Run

- get AWS credentials to run this!
- fill packer.json with vpc and subnet id
- run the build


    packer build packer.json

