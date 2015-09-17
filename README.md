# init-contract-json

A node module to get your node module started.

## Usage

```javascript
var init = require('init-contract-json')
var path = require('path')

// a path to a promzard module.  In the event that this file is
// not found, one will be provided for you.

// the dir where we're doin stuff.
var dir = process.cwd()

// Any existing stuff from the package.json file is also exposed in the
// PromZard module as the `package` object.  There will also be free
// vars for:
// * `filename` path to the package.json file
// * `basename` the tip of the package dir
// * `dirname` the parent of the package dir

init(dir, 'No init needed', function (er, data) {
  // the data's already been written to {dir}/contract.json
  // now you can do stuff with it
})
```

Or from the command line:

```
$ npm-init
```

See [PromZard](https://github.com/isaacs/promzard) for details about
what can go in the config file.
