# Postman-newman-circleci

CircleCI Orb (postman/newman) for running Postman collections with Newman - https://github.com/postmanlabs/newman

This Orb is available on CircleCI registry as `postman/newman`

## Usage

To use the `postman/newman` Orb, reference it in your CircleCI config and then use the `newman-run` command.

```yaml
version: 2.1
orbs:
  newman: postman/newman@0.0.2
jobs:
  newman-collection-run:
    # use the official newman docker image via newman/postman-newman-docker executor
    executor: newman/postman-newman-docker

    steps:
      # checkout step is optional if you are not referencing any files from the project
      - checkout

      # use newman-run command
      - newman/newman-run:
          collection: ./collection.json
```


### How to Testing API using Postman (newman) in local

## Install newman on Windows
```
npm install -g newman
```

## Run Testing API
```
newman run API_Testing.postman_collection.json -e Test_Environment.postman_environment.json
```
