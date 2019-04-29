# AWS Lambda Layers

A collection of [AWS Lambda layers](https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-now-supports-custom-runtimes-and-layers/)
that allow your functions to use layered binaries during execution.

<br/>

## Setup

Once a layer is added to your lambda execution environment you will be able to use the binaries packaged in that layer directly in your function code.

To add a new layer:
1. Open up AWS Lambda Console 
2. Click Layers -> Create Layer
3. Upload layer zip file from this repo
4. Create

AWS Lambda mounts layers in the `/opt` directory from where they can be invoked if needed. See specific instructions for each layer below:

<br/>

### Hugo

To invoke the Hugo static site builder: `/opt/hugo`

#### Versions

| Hugo version | 
| --- | 
| 0.48 | 

<br/>

### AWS CLI

To invoke an AWS CLI command: `/opt/aws`

#### Versions

| AWS CLI version | Botocore version | 
| --- | --- | 
| 1.16.117 | 1.12.107 | 

<br/>

### Git-Svn-SSH

To invoke the Git, Svn & SSH binaries `<git | svn | ssh>`

*Note:* The binaries in this layer are mounted directly to `/opt/bin` which is included in your PATH, hence the ommitance of `/opt`

## Versions

| Svn version | Git version | openssh version | ARN |
| --- | --- | --- | --- |
| 1.9.7 | 2.20.0 | OpenSSH_6.6.1p1, OpenSSL 1.0.1k-fips | `arn:aws:lambda:us-east-1:666142237544:layer:svn-git-ssh:1` |
