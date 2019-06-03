veild-rpc.js
===============
A client library to connect to veild using RPC in JavaScript.

## Get Started

veild-rpc.js runs on [node](http://nodejs.org/), and can be installed via [npm](https://npmjs.org/):

```bash
npm install veild-rpc
```

## Examples

```javascript
var run = function() {
    var RpcClient = require('veild-rpc');
  
    var config = {
      protocol: 'http',
      user: 'user',
      pass: 'pass',
      host: '127.0.0.1',
      port: '58812',
    };

    var rpc = new RpcClient(config);
    
    rpc.getinfo(function (err, ret) {
        if (err) {
            console.error(err);
        }
        console.log(ret);
    });
}

run();
```


