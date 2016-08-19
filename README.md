## Supported tags and respective `Dockerfile` links

 - `v0.10.2-go-1.6.3` ([0.10.2/go-1.6.3/Dockerfile](https://github.com/polds/apex-docker/blob/a029e5af5f4d6f666d08dd6b15a69fa05081307d/0.10.2/go-1.6.3/Dockerfile))
 - `v0.10.2`, `v0.10.2-go-1.7`, `latest` ([0.10.2/Dockerfile](https://github.com/polds/apex-docker/blob/a99fc3cf14a2ce2a576b6833d29156548d21d299/0.10.2/Dockerfile))

### What is [Apex](https://github.com/apex/apex)?

Apex lets you build, deploy, and manage AWS Lambda functions with ease. With Apex you can use languages that are not natively supported by AWS Lambda, such as Golang, through the use of a Node.js shim injected into the build. A variety of workflow related tooling is provided for testing functions, rolling back deploys, viewing metrics, tailing logs, hooking into the build system and more. ([Source](https://github.com/apex/apex/blob/master/Readme.md))

### How to use this image

 - Determine which version of Apex you want to use. If you don't care about the Go version just target the Apex version tag. (ie `polds/apex-docker:v0.10.2`)
 - `docker pull polds/apex-docker:v0.10.2`
 - `docker run -it polds/apex-docker:v0.10.2 apex`

##### Mounting a volume

The workdir for this image is `/opt/`, all volumes should be mounted to this directory:

```
docker run -it -v .:/opt/ polds/apex-docker:v0.10.2 apex deploy myfunc
```

#### AWS Credentials

You will need to mount your `~/.aws` folder into `/root/.aws/` to properly get your AWS Credentials in place.
