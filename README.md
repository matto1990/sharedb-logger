# sharedb-logger
Logger for pretty-printing [ShareDB](https://github.com/share/sharedb) events.

## Usage
You can instal the logging middleware by passing in your ShareDB instance.

```javascript
var ShareDB = require("sharedb");
var shareDBLogger = require("sharedb-logger");

var share = ShareDB();
shareDBLogger(share);
```

You can also include options as the second parameter:

```javascript
var ShareDB = require("sharedb");
var shareDBLogger = require("sharedb-logger");

var share = ShareDB();
var options = {
  getId: function(agent, message) {
    return "An ID";
  }
};
shareDBLogger(share, options);
```

## Options
* `options.getId` - An optional function which allows you to generate an addition ID which will be logged in addition to the agents client ID.
