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
const RpcClient = require('veild-rpc');

var run = function(){

    // Veild Configuration Object
    var RpcConfig = {
        protocol: 'http',
        user: 'veild',
        pass: 'somerandompassword',
        host: '127.0.0.1',
        port: '58812'
    };

    var rpc = new RpcClient(RpcConfig);

    // Get the total spendable balance of all coin derivitives.
    rpc.getspendablebalance(function(err, ret){
        if(err){
            console.log(err);
        }
        console.log(ret);
    });
}

run();
```


