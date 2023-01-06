# Postman-newman-circleci


### How to Testing API using Postman (newman) in local

## Install newman on Windows
```
npm install -g newman
```

## Run Testing API
```
newman run API_Testing.postman_collection.json -e Test_Environment.postman_environment.json
```
