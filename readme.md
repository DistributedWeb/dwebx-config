# DWebX Swarm Defaults

[![npm][npm-image]][npm-url]
[![travis][travis-image]][travis-url]
[![standard][standard-image]][standard-url]

Use DWebX defaults for `dns` and `dht` servers in [dwebdiscovery](https://github.com/karissa/dwebdiscovery) or [discovery-swarm](https://github.com/distributedweb/discovery-swarm). The *dns* and *dht* servers are used to discover other peers.

### Using Other Discovery Servers

Run discovery servers with [dns-discovery](https://github.com/distributedweb/dns-discovery#cli) or a [bittorrent-dht](https://github.com/webtorrent/bittorrent-dht) server (such as https://github.com/dwebswarm/dht).

## Usage 

Create a config object and pass it to discovery swarm. 

Any options you specify will overwrite the defaults. See discovery swarm for options.

```javascript
var Swarm = require('discovery-swarm')
var defaults = require('dwebx-config')

var config = defaults({
  stream: function () {
    return drive.createPeerStream()
  }
})
var swarm = Swarm(config)
```

## License

[MIT](LICENSE.md)

[npm-image]: https://img.shields.io/npm/v/dwebx-config.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/dwebx-config
[travis-image]: https://img.shields.io/travis/datproject/dwebx-config.svg?style=flat-square
[travis-url]: https://travis-ci.org/datproject/dwebx-config
[standard-image]: https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square
[standard-url]: http://npm.im/standard

