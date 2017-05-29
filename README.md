## Node-Github-GraphQL

A GitHub GraphQL HTTP wrapper

### Installation

```
npm install https://github.com/wilsonchingg/node-github-graphql.git
```

### Example

```javascript
var GithubGraphQLApi = require('github-graphql');
var github = new GithubGraphQLApi({
	Promise: require('bluebird'),
	token: process.env.GITHUB_API_TOKEN,
	userAgent: 'Hello', //Optional, if not specified, a default user agent will be used
	debug: true
});
github.query(`
  viewer {
    login
  }`
).then(function(res, err){
	console.log(res);
	console.log(err);
});
```

### LICENSE

MIT license. See the LICENSE file for details.
