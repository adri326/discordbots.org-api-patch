# discordbots.org-api-patch
#### A patch for the discordbots.org-api wrapper

## Get started

You'll first have to add the package to your `package.json`, adding this in the `dependencies` element:

```json
    "discordbots.org-api-patch": "https://github.com/adri326/discordbots.org-api-patch.git"
```

Then, you can start using it like this:

```js
var dbapi = require("discordbots.org-api-patch");

var db = new dbapi("<Your token here>")

db.getStats("<Your bot ID>").then((botData) => {
  console.log(botData)
}).catch(console.error)
```

## NPM Package
https://www.npmjs.com/package/discordbots.org-api-patch

## Documentation

**.getBots**

```js
db.getBots.then((botData) => { console.log(botData) })
```
Returns all the data added to the API.

<hr>

**.getInfo(botID)**

```js
db.getInfo(botID).then((botData) => { console.log(botData) })
```
Returns information about a bot on the API.

<hr>

**.getStats(botID)**

```js
db.getStats(botID).then((botData) => { console.log(botData) })
```
Returns stats about a bot on the API, returns `undefined` if a server count isnt `POST`'d to the API.

<hr>

**.getUser(userID)**

```js
db.getUser("133483105645232129").then((userData) => { console.log(userData) })
```
Returns the bots a user owns.

<hr>

**.postStats(botID, server_count)**

```js
db.postStats(botID, serverCount).then((botData) => { console.log(botData) })
````
Returns undefined. Bot stats were posted.

<hr>

**.postStatsShard(botID, shardID, shard_count, server_count)**

```js
db.postStatsShard(botID, shardID, shard_count, server_count).then((botData) => { console.log(botData) })
````
Returns undefined. Bot stats were posted via shard.

#### How do i get a token?

From [here](https://discordbots.org/api/docs)
