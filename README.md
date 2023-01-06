# Postman-newman-circleci

(postman/newman) for running Postman collections and Environment with Newman - https://github.com/postmanlabs/newman


## Usage

To use the `postman/newman` , reference it in your CircleCI config and then use the `newman-run` command.

```yaml
version: 2.1
orbs:
  newman: postman/newman@1.0.0
jobs:
  build:
    executor: newman/postman-newman-docker
    steps:
      - checkout
      - newman/newman-run:
          collection: ./API_Testing.postman_collection.json
          environment: ./Test_Environment.postman_environment.json
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
