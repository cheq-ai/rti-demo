<h5>Cheq's Real Time Interception Demo</h1>

The following repoistory demonstare a simple demo which utilize Cheq's RTI solution.

In order to run the demo a `config.js` file will need to be created under root directory.

```javascript
//config.js
module.exports = {
    tagHash : '00000000000000000000000000000000', 
    decryptionKey : '123456789012345678901234'
}
``` 

**tagHash** - a 32 chars hash which can be found under Cheq's invocation code url.

```
https://ob.cheqzone.com/i/[TAG_HASH].js
```

**decryptionKey** - a 24 chars decryption key given by Cheq.


Once config file have been setup properly, simply run the demo by
 
```
node server.js
```

And visit  `localhost:8080`

**Notes:**
* The `views/block.ejs` represnt a page where an invalid request will reach.
* The `views/pass.ejs` represnt a page where a valid request will reach.