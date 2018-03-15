# APIs-Problems-With-DialogFlow-

That example works like a charm on firebase CLI
``` javascript
        const request = require("request");
        const urls = 'http://maps.googleapis.com/maps/api/geocode/json?address=london';
        request.get(urls, (error, response, body) => {
            body = JSON.parse(body);
            sendResponse(
              `Location: ${body.results[0].formatted_address}`
            );
```

While this same method on another APIs won't work
``` javascript
        const request = require("request");
        const urls = 'http://api.yomomma.info';
        request.get(urls, (error, response, body) => {
            body = JSON.parse(body);
            sendResponse(
              `Joke: ${body.joke}`
            );
```

