# Svn, Git & SSH binaries for AWS Lambda

An AWS Lambda [layer](https://aws.amazon.com/about-aws/whats-new/2018/11/aws-lambda-now-supports-custom-runtimes-and-layers/)
that allows your functions to use `svn`, `git` & `ssh` binaries.

## Setup

This layer once added to your Lambda function will allow you to use svn, git & ssh 
commands in your function regardless of runtime.

AWS Lambda mounts layers at `/opt/bin` and includes that in your `PATH` so they will
be 'ready to use' in your function once invoked.

Click on Layers -> Add a layer -> Provide a layer version ARN -> and enter the following ARN:

```
arn:aws:lambda:us-east-1:666142237544:layer:svn-git-ssh:1
```

### Note

This ARN is only published in region `us-east-1`. If your function is deployed in a different region,
download the `svn-git-ssh.zip` file in the repository and publish the zip file layer in your desired region.

## Versions

| Svn version | Git version | openssh version | ARN |
| --- | --- | --- | --- |
| 1.9.7 | 2.20.0 | OpenSSH_6.6.1p1, OpenSSL 1.0.1k-fips | `arn:aws:lambda:us-east-1:666142237544:layer:svn-git-ssh:1` |
