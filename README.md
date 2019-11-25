# AWS Security Toolbox :lock:

This toolbox will bring to you all necessary apps as a Docker container for SecOps on AWS, especially for auditing purpose.

## Requirements

- docker

## Tools

### Optional tools (host machine)

- [aws-vault](https://github.com/99designs/aws-vault)

### Tools (guest container)

- [awscli](https://aws.amazon.com/cli/)
- [CloudMapper](https://github.com/duo-labs/cloudmapper)
- [CloudTracker](https://github.com/duo-labs/cloudtracker)
- [prowler](https://github.com/toniblyx/prowler)
- [ScoutSuite](https://github.com/nccgroup/ScoutSuite)
- [PMapper](https://github.com/nccgroup/PMapper)
- [Enumerate-IAM](https://github.com/andresriancho/enumerate-iam)

## Usage

Clone the repository:

        $ git clone https://github.com/z0ph/aws-security-toolbox.git

Run the magic:

        $ make run

Working directory: `/opt/secops`

### Optional

if you want to build your own container

        $ make build

```bash
docker exec -it -v $HOME/.aws:/root/.aws:ro z0ph/aws-sec-toolbox:latest bash
docker run -it z0ph/aws-sec-toolbox:latest /bin/bash
```

#### Ref
- https://hub.docker.com/r/toniblyx/prowler/dockerfile
- https://ryanparman.com/posts/2019/running-aws-vault-with-local-docker-containers/