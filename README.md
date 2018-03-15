# APIs-Problems-With-DialogFlow-

That example works like a charm on firebase CLI
``` javascript
        const request = require("request");
        const urls = 'http://maps.googleapis.com/maps/api/geocode/json?address=london';
        request.get(urls, (error, response, body) => {
            body = JSON.parse(body);
            sendResponse(
              `Location: ${body.results[0].formatted_address} -`+`Latitude: ${body.results[0].geometry.location.lat} -`+`Longitude: ${body.results[0].geometry.location.lng} Link: https://www.google.com.eg/maps/place/`+rz+`/@${body.results[0].geometry.location.lat},${body.results[0].geometry.location.lng},14z` 
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

