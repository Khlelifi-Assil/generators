# Rest/GraphQL APIs + React Components Generator 🔥



# Quick Start


1. Install the npm module

```sh
# install
npm i -g sugar-generate
```

2. Create a json schema save, this to **monkey.json**


```json
{
  "name": "monkey",
  "schema": {
    "name": {
      "type": "String",
      "default": ""
    },
    "alive": {
      "type": "Boolean",
      "default": false
    },
    "age": {
      "type": "Number",
      "default": false
    }
  }
}
```

3. Generate your api and app

```sh
sugar-generate \
--schema monkey.json \
--destination ./my-monkeys
```

Boom, you now have:

API:
- GraphQL API
- REST API
- Working Tests

APP:
- React create item form
- React table that supports
  - search
  - sort
  - filter
  - pagination
  - edit item
  - create item


### Start the API

```sh
cd ./my-monkeys/api
npm i
npm run start

# http://localhost:7777
```

### Start the APP

```sh
cd ./my-monkeys/app
npm i
npm run dev

# http://localhost:3000
```

# Links

[GraphQL is on localhost:7777/graphql](http://localhost:7777/graphql)

[Swagger is on localhost:7777](http://localhost:7777)

[APP is on localhost:3000](http://localhost:3000)

[API is on localhost:7777](http://localhost:3000)


