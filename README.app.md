# Instantly Generate React Components 🔥


## Install

```sh
npm i -g sugar-generate
```

## Prereqs

- have mongodb [installed and running](https://treehouse.github.io/installation-guides/mac/mongo-mac.html)!
- have nodejs installed

if you're running mongodb locally and using the docker container, make sure to start mongo using

```sh
sudo mongod --bind_ip_all
```
otherwise you wont be able to connect to mongo from docker.

## Getting Started

```sh
cd /my-monkeys
npm i
npm start
# Or build the docker container!
docker build -t myMonkeys:0.1.0 .
```



## Features 
- Generates simple Nodejs code
- Graphql and Rest out of the box
- Uses Mongodb with Mongoose ORM
- Easy to build / deploy
- Dockerfile included
- supports multiple schemas
- Generates CRUD APIs
  - create
  - get (many, with pagination; supports search, sort, filter, pagination out of the box)
  - getOne
  - update
  - delete
- Generates GraphQL apis for both query and mutation

## What it's good at 

- Generating an initial API
- Microservice oriented
- Ready to deploy (build with docker => deploy)

## What it's not good at (yet) 

- idempotent changes (i.e. it doesn't know if you wrote code in there or changed things around)
- working with modified code
- populating table joins
- custom actions inside controller functions


## TODO


### API

- graphql tests
- other databases?
- **your ideas?**
- middleware for auth, token validation, etc.


## Graphql support



graphql is supported and gets created by default so you can choose between rest and graphql

Graphql is on [http://localhost:3000/graphql](http://localhost:3000/graphql)



## Generated project structure

    .
    ├── configs                 # Config File
    ├── connection              # DB Connections (mongo, redis)
    ├── controller              # Controllers
    │   ├── <model name>        # Functions (one file, one function) create, delete, update, get, getOne
    ├── models                  # DB Models
    ├── router                  # Endpoint Routes
    ├── tests                   # Single Test File

## Generated tests

** WARNING ** running the tests will pull the config file from **configs/config.json** and clear the DB

```sh
npm run test
```
