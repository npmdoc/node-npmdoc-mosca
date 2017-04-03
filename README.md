# api documentation for  [mosca (v2.3.0)](https://github.com/mcollina/mosca#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-mosca.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-mosca) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-mosca.svg)](https://travis-ci.org/npmdoc/node-npmdoc-mosca)
#### MQTT broker as a module

[![NPM](https://nodei.co/npm/mosca.png?downloads=true)](https://www.npmjs.com/package/mosca)

[![apidoc](https://npmdoc.github.io/node-npmdoc-mosca/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-mosca_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-mosca/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-mosca/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-mosca/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Matteo Collina",
        "email": "hello@matteocollina.com"
    },
    "bin": {
        "mosca": "./bin/mosca"
    },
    "bugs": {
        "url": "http://github.com/mcollina/mosca/issues"
    },
    "dependencies": {
        "amqp": "~0.2.4",
        "array-from": "^2.1.1",
        "ascoltatori": "^3.0.0",
        "brfs": "~1.4.2",
        "clone": "^1.0.2",
        "commander": "~2.9.0",
        "deepcopy": "^0.6.1",
        "extend": "^3.0.0",
        "ioredis": "^1.15.1",
        "json-buffer": "~2.0.11",
        "jsonschema": "^1.0.3",
        "level-sublevel": "^6.5.2",
        "leveldown": "~1.4.3",
        "levelup": "^1.3.1",
        "lru-cache": "~4.0.0",
        "memdown": "~1.1.1",
        "minimatch": "~3.0.0",
        "moment": "~2.13.0",
        "mongodb": "~2.1.4",
        "moving-average": "0.1.1",
        "mqtt": "^1.6.3",
        "mqtt-connection": "^2.1.1",
        "msgpack5": "^3.3.0",
        "pbkdf2-password": "^1.1.0",
        "pino": "^2.4.2",
        "qlobber": "~0.7.0",
        "retimer": "^1.0.1",
        "shortid": "^2.2.4",
        "st": "~1.1.0",
        "steed": "^1.0.0",
        "uuid": "^2.0.1",
        "websocket-stream": "~3.1.0"
    },
    "description": "MQTT broker as a module",
    "devDependencies": {
        "browserify": "~13.0.0",
        "chai": "^3.5.0",
        "coveralls": "~2.11.1",
        "dox-foundation": "~0.5.4",
        "istanbul": "~0.4.0",
        "jshint": "~2.9.1",
        "mocha": "^2.0.1",
        "mongo-clean": "^1.1.0",
        "osenv": "^0.1.0",
        "pre-commit": "1.1.2",
        "rimraf": "^2.2.8",
        "sinon": "~1.7.0",
        "sinon-chai": "~2.8.0",
        "supertest": "~1.2.0",
        "tmp": "0.0.24",
        "uglify-js": "^2.4.16",
        "underscore": "^1.7.0",
        "ws": "^1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "712fcbbcf52729dacb76faddee02e3b6dba5f578",
        "tarball": "https://registry.npmjs.org/mosca/-/mosca-2.3.0.tgz"
    },
    "engines": {
        "node": ">= 0.12"
    },
    "gitHead": "697dffd2024a11badeb866d57f76648a65b6f844",
    "homepage": "https://github.com/mcollina/mosca#readme",
    "keywords": [
        "mqtt",
        "mqtt server",
        "publish",
        "subscribe",
        "pubsub",
        "rabbitmq",
        "zeromq",
        "0mq",
        "amqp",
        "mosquitto",
        "websocket"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "matteo.collina",
            "email": "hello@matteocollina.com"
        }
    ],
    "name": "mosca",
    "optionalDependencies": {
        "amqp": "~0.2.4",
        "ioredis": "^1.15.1",
        "leveldown": "~1.4.3",
        "mongodb": "~2.1.4"
    },
    "pre-commit": [
        "jshint-lib",
        "jshint-test",
        "test"
    ],
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/mcollina/mosca.git"
    },
    "scripts": {
        "bundle": "browserify -r mqtt -s mqtt | uglifyjs --screw-ie8 > public/mqtt.js",
        "ci": "mocha --recursive --bail --watch test",
        "coverage": "rm -rf coverage; istanbul cover _mocha -- --recursive --reporter spec --bail",
        "jshint-lib": "jshint lib",
        "jshint-test": "jshint test",
        "prepublish": "npm run bundle",
        "publish-coverage": "(cat coverage/lcov.info | coveralls)",
        "start": "./bin/mosca -v | bunyan",
        "test": "mocha --recursive --bail --reporter spec test 2>&1"
    },
    "version": "2.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module mosca](#apidoc.module.mosca)
1.  [function <span class="apidocSignatureSpan">mosca.</span>Authorizer (users)](#apidoc.element.mosca.Authorizer)
1.  [function <span class="apidocSignatureSpan">mosca.</span>Server (opts, callback)](#apidoc.element.mosca.Server)
1.  [function <span class="apidocSignatureSpan">mosca.</span>Stats ()](#apidoc.element.mosca.Stats)
1.  [function <span class="apidocSignatureSpan">mosca.</span>client (conn, server)](#apidoc.element.mosca.client)
1.  [function <span class="apidocSignatureSpan">mosca.</span>persistence.LevelUp (options, callback)](#apidoc.element.mosca.persistence.LevelUp)
1.  [function <span class="apidocSignatureSpan">mosca.</span>persistence.Memory (options, callback)](#apidoc.element.mosca.persistence.Memory)
1.  [function <span class="apidocSignatureSpan">mosca.</span>persistence.Mongo (options, done)](#apidoc.element.mosca.persistence.Mongo)
1.  [function <span class="apidocSignatureSpan">mosca.</span>persistence.Redis (options, callback)](#apidoc.element.mosca.persistence.Redis)
1.  object <span class="apidocSignatureSpan">mosca.</span>Authorizer.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>Server.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>Stats.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>client.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>interfaces
1.  object <span class="apidocSignatureSpan">mosca.</span>options
1.  object <span class="apidocSignatureSpan">mosca.</span>persistence
1.  object <span class="apidocSignatureSpan">mosca.</span>persistence.LevelUp.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>persistence.LevelUp.super_.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>persistence.Memory.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>persistence.Mongo.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>persistence.Redis.prototype
1.  object <span class="apidocSignatureSpan">mosca.</span>serializers

#### [module mosca.Authorizer](#apidoc.module.mosca.Authorizer)
1.  [function <span class="apidocSignatureSpan">mosca.</span>Authorizer (users)](#apidoc.element.mosca.Authorizer.Authorizer)

#### [module mosca.Authorizer.prototype](#apidoc.module.mosca.Authorizer.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>_authenticate (client, user, pass, cb)](#apidoc.element.mosca.Authorizer.prototype._authenticate)
1.  [function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>addUser (user, pass, authorizePublish, authorizeSubscribe, cb)](#apidoc.element.mosca.Authorizer.prototype.addUser)
1.  [function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>authenticate (client, user, pass, cb)](#apidoc.element.mosca.Authorizer.prototype.authenticate)
1.  [function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>authorizePublish (client, topic, payload, cb)](#apidoc.element.mosca.Authorizer.prototype.authorizePublish)
1.  [function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>authorizeSubscribe (client, topic, cb)](#apidoc.element.mosca.Authorizer.prototype.authorizeSubscribe)
1.  [function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>rmUser (user, cb)](#apidoc.element.mosca.Authorizer.prototype.rmUser)

#### [module mosca.Server](#apidoc.module.mosca.Server)
1.  [function <span class="apidocSignatureSpan">mosca.</span>Server (opts, callback)](#apidoc.element.mosca.Server.Server)

#### [module mosca.Server.prototype](#apidoc.module.mosca.Server.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>attachHttpServer (server, path)](#apidoc.element.mosca.Server.prototype.attachHttpServer)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authenticate (client, username, password, callback)](#apidoc.element.mosca.Server.prototype.authenticate)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authorizeForward (client, packet, callback)](#apidoc.element.mosca.Server.prototype.authorizeForward)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authorizePublish (client, topic, payload, callback)](#apidoc.element.mosca.Server.prototype.authorizePublish)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authorizeSubscribe (client, topic, callback)](#apidoc.element.mosca.Server.prototype.authorizeSubscribe)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>close (callback)](#apidoc.element.mosca.Server.prototype.close)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>deleteOfflinePacket (client, messageId, callback)](#apidoc.element.mosca.Server.prototype.deleteOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>forwardOfflinePackets (client, callback)](#apidoc.element.mosca.Server.prototype.forwardOfflinePackets)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>forwardRetained (pattern, client, callback)](#apidoc.element.mosca.Server.prototype.forwardRetained)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>generateUniqueId ()](#apidoc.element.mosca.Server.prototype.generateUniqueId)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>nextDedupId ()](#apidoc.element.mosca.Server.prototype.nextDedupId)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>persistClient (client, callback)](#apidoc.element.mosca.Server.prototype.persistClient)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>publish (packet, client, callback)](#apidoc.element.mosca.Server.prototype.publish)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>published (packet, client, callback)](#apidoc.element.mosca.Server.prototype.published)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>restoreClientSubscriptions (client, callback)](#apidoc.element.mosca.Server.prototype.restoreClientSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>storePacket (packet, callback)](#apidoc.element.mosca.Server.prototype.storePacket)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>subscribe (topic, callback, done)](#apidoc.element.mosca.Server.prototype.subscribe)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>toString ()](#apidoc.element.mosca.Server.prototype.toString)
1.  [function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>updateOfflinePacket (client, originMessageId, packet, callback)](#apidoc.element.mosca.Server.prototype.updateOfflinePacket)

#### [module mosca.Stats](#apidoc.module.mosca.Stats)
1.  [function <span class="apidocSignatureSpan">mosca.</span>Stats ()](#apidoc.element.mosca.Stats.Stats)

#### [module mosca.Stats.prototype](#apidoc.module.mosca.Stats.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.Stats.prototype.</span>wire (server)](#apidoc.element.mosca.Stats.prototype.wire)

#### [module mosca.client](#apidoc.module.mosca.client)
1.  [function <span class="apidocSignatureSpan">mosca.</span>client (conn, server)](#apidoc.element.mosca.client.client)

#### [module mosca.client.prototype](#apidoc.module.mosca.client.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>_buildForward ()](#apidoc.element.mosca.client.prototype._buildForward)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>_setup ()](#apidoc.element.mosca.client.prototype._setup)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>close (callback, reason)](#apidoc.element.mosca.client.prototype.close)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleAuthorizePublish (err, success, packet)](#apidoc.element.mosca.client.prototype.handleAuthorizePublish)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleAuthorizeSubscribe (err, success, s, cb)](#apidoc.element.mosca.client.prototype.handleAuthorizeSubscribe)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleConnect (packet, completeConnection)](#apidoc.element.mosca.client.prototype.handleConnect)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handlePingreq ()](#apidoc.element.mosca.client.prototype.handlePingreq)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handlePuback (packet)](#apidoc.element.mosca.client.prototype.handlePuback)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleSubscribe (packet)](#apidoc.element.mosca.client.prototype.handleSubscribe)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>onNonDisconnectClose (reason)](#apidoc.element.mosca.client.prototype.onNonDisconnectClose)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>setUpTimer ()](#apidoc.element.mosca.client.prototype.setUpTimer)
1.  [function <span class="apidocSignatureSpan">mosca.client.prototype.</span>unsubscribeMapTo (topic, cb)](#apidoc.element.mosca.client.prototype.unsubscribeMapTo)

#### [module mosca.interfaces](#apidoc.module.mosca.interfaces)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>buildServe (iface, mosca)](#apidoc.element.mosca.interfaces.buildServe)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>buildWrap (mosca)](#apidoc.element.mosca.interfaces.buildWrap)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>httpFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.httpFactory)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>httpsFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.httpsFactory)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>mqttFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.mqttFactory)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>mqttsFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.mqttsFactory)
1.  [function <span class="apidocSignatureSpan">mosca.interfaces.</span>serverFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.serverFactory)

#### [module mosca.options](#apidoc.module.mosca.options)
1.  [function <span class="apidocSignatureSpan">mosca.options.</span>defaultsLegacy ()](#apidoc.element.mosca.options.defaultsLegacy)
1.  [function <span class="apidocSignatureSpan">mosca.options.</span>defaultsModern ()](#apidoc.element.mosca.options.defaultsModern)
1.  [function <span class="apidocSignatureSpan">mosca.options.</span>modernize (legacy)](#apidoc.element.mosca.options.modernize)
1.  [function <span class="apidocSignatureSpan">mosca.options.</span>populate (opts)](#apidoc.element.mosca.options.populate)
1.  [function <span class="apidocSignatureSpan">mosca.options.</span>validate (opts, validationOptions)](#apidoc.element.mosca.options.validate)

#### [module mosca.persistence](#apidoc.module.mosca.persistence)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>LevelUp (options, callback)](#apidoc.element.mosca.persistence.LevelUp)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>Memory (options, callback)](#apidoc.element.mosca.persistence.Memory)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>Mongo (options, done)](#apidoc.element.mosca.persistence.Mongo)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>Redis (options, callback)](#apidoc.element.mosca.persistence.Redis)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>getFactory (name)](#apidoc.element.mosca.persistence.getFactory)

#### [module mosca.persistence.LevelUp](#apidoc.module.mosca.persistence.LevelUp)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>LevelUp (options, callback)](#apidoc.element.mosca.persistence.LevelUp.LevelUp)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.</span>super_ ()](#apidoc.element.mosca.persistence.LevelUp.super_)

#### [module mosca.persistence.LevelUp.prototype](#apidoc.module.mosca.persistence.LevelUp.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>_cleanupStream (stream)](#apidoc.element.mosca.persistence.LevelUp.prototype._cleanupStream)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>_storePacket (client, packet, cb)](#apidoc.element.mosca.persistence.LevelUp.prototype._storePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>close (cb)](#apidoc.element.mosca.persistence.LevelUp.prototype.close)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>deleteOfflinePacket (client, messageId, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.deleteOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>lookupRetained (pattern, cb)](#apidoc.element.mosca.persistence.LevelUp.prototype.lookupRetained)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>lookupSubscriptions (client, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.lookupSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>storeOfflinePacket (packet, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.storeOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>storeRetained (packet, cb)](#apidoc.element.mosca.persistence.LevelUp.prototype.storeRetained)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>storeSubscriptions (client, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.storeSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>streamOfflinePackets (client, cb, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.streamOfflinePackets)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>updateOfflinePacket (client, messageId, packet, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.updateOfflinePacket)

#### [module mosca.persistence.LevelUp.super_.prototype](#apidoc.module.mosca.persistence.LevelUp.super_.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.super_.prototype.</span>close (done)](#apidoc.element.mosca.persistence.LevelUp.super_.prototype.close)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.super_.prototype.</span>wire (server)](#apidoc.element.mosca.persistence.LevelUp.super_.prototype.wire)

#### [module mosca.persistence.Memory](#apidoc.module.mosca.persistence.Memory)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>Memory (options, callback)](#apidoc.element.mosca.persistence.Memory.Memory)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Memory.</span>super_ (options, callback)](#apidoc.element.mosca.persistence.Memory.super_)

#### [module mosca.persistence.Memory.prototype](#apidoc.module.mosca.persistence.Memory.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Memory.prototype.</span>close (cb)](#apidoc.element.mosca.persistence.Memory.prototype.close)

#### [module mosca.persistence.Mongo](#apidoc.module.mosca.persistence.Mongo)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>Mongo (options, done)](#apidoc.element.mosca.persistence.Mongo.Mongo)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.</span>super_ ()](#apidoc.element.mosca.persistence.Mongo.super_)

#### [module mosca.persistence.Mongo.prototype](#apidoc.module.mosca.persistence.Mongo.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>_storePacket (client, packet, cb)](#apidoc.element.mosca.persistence.Mongo.prototype._storePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>close (cb)](#apidoc.element.mosca.persistence.Mongo.prototype.close)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>deleteOfflinePacket (client, messageId, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.deleteOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>lookupRetained (pattern, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.lookupRetained)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>lookupSubscriptions (client, done)](#apidoc.element.mosca.persistence.Mongo.prototype.lookupSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>storeOfflinePacket (packet, done)](#apidoc.element.mosca.persistence.Mongo.prototype.storeOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>storeRetained (packet, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.storeRetained)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>storeSubscriptions (client, done)](#apidoc.element.mosca.persistence.Mongo.prototype.storeSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>streamOfflinePackets (client, cb, done)](#apidoc.element.mosca.persistence.Mongo.prototype.streamOfflinePackets)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>updateOfflinePacket (client, messageId, packet, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.updateOfflinePacket)

#### [module mosca.persistence.Redis](#apidoc.module.mosca.persistence.Redis)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.</span>Redis (options, callback)](#apidoc.element.mosca.persistence.Redis.Redis)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.</span>super_ ()](#apidoc.element.mosca.persistence.Redis.super_)

#### [module mosca.persistence.Redis.prototype](#apidoc.module.mosca.persistence.Redis.prototype)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_buildClient ()](#apidoc.element.mosca.persistence.Redis.prototype._buildClient)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_cleanClient (client, done)](#apidoc.element.mosca.persistence.Redis.prototype._cleanClient)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_explicitlyClosed (done)](#apidoc.element.mosca.persistence.Redis.prototype._explicitlyClosed)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_storePacket (client, packet, pipeline, cb)](#apidoc.element.mosca.persistence.Redis.prototype._storePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>close (done)](#apidoc.element.mosca.persistence.Redis.prototype.close)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>deleteOfflinePacket (client, messageId, done)](#apidoc.element.mosca.persistence.Redis.prototype.deleteOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>lookupRetained (pattern, done)](#apidoc.element.mosca.persistence.Redis.prototype.lookupRetained)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>lookupSubscriptions (client, cb)](#apidoc.element.mosca.persistence.Redis.prototype.lookupSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>storeOfflinePacket (packet, done)](#apidoc.element.mosca.persistence.Redis.prototype.storeOfflinePacket)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>storeRetained (packet, cb)](#apidoc.element.mosca.persistence.Redis.prototype.storeRetained)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>storeSubscriptions (client, cb)](#apidoc.element.mosca.persistence.Redis.prototype.storeSubscriptions)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>streamOfflinePackets (client, cb, done)](#apidoc.element.mosca.persistence.Redis.prototype.streamOfflinePackets)
1.  [function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>updateOfflinePacket (client, messageId, packet, done)](#apidoc.element.mosca.persistence.Redis.prototype.updateOfflinePacket)

#### [module mosca.serializers](#apidoc.module.mosca.serializers)
1.  [function <span class="apidocSignatureSpan">mosca.serializers.</span>clientSerializer (client)](#apidoc.element.mosca.serializers.clientSerializer)
1.  [function <span class="apidocSignatureSpan">mosca.serializers.</span>packetSerializer (packet)](#apidoc.element.mosca.serializers.packetSerializer)



# <a name="apidoc.module.mosca"></a>[module mosca](#apidoc.module.mosca)

#### <a name="apidoc.element.mosca.Authorizer"></a>[function <span class="apidocSignatureSpan">mosca.</span>Authorizer (users)](#apidoc.element.mosca.Authorizer)
- description and source-code
```javascript
function Authorizer(users) {
  this.users = users || {};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Server"></a>[function <span class="apidocSignatureSpan">mosca.</span>Server (opts, callback)](#apidoc.element.mosca.Server)
- description and source-code
```javascript
function Server(opts, callback) {
  var modernOpts = options.modernize(opts);
  var validationResult = options.validate(modernOpts);

  if (validationResult.errors.length > 0) {
    var errMessage = validationResult.errors[0].message;
    if (callback) {
      callback(new Error(errMessage));
    } else {
      throw new Error(errMessage);
    }
  }

  modernOpts = options.populate(modernOpts);

  if (!(this instanceof Server)) {
    return new Server(opts, callback);
  }

  EventEmitter.call(this);

  if (true) { // REFACTOR: kludge for tests that rely on options structure
    this.opts = extend(true, {}, defaults, opts);
    this.modernOpts = modernOpts;

    if (this.opts.secure) {
      this.opts.secure.port = this.opts.secure.port || 8883;
    }
    if (this.opts.http) {
      this.opts.http.port = this.opts.http.port || 3000;
    }
    if (this.opts.https) {
      this.opts.https.port = this.opts.https.port || 3001;
    }
  } else { // REFACTOR: enable this once test are updated
    this.opts = modernOpts;
  }

  callback = callback || function() {};

  this._dedupId = 0;
  this.clients = {};
  this.closed = false;

  if (this.modernOpts.logger.childOf) {
    this.logger = this.modernOpts.logger.childOf;
    delete this.modernOpts.logger.childOf;
    delete this.modernOpts.logger.name;
    this.logger = this.logger.child(this.modernOpts.logger);
  } else {
    this.logger = pino(this.modernOpts.logger);
  }

  if(this.modernOpts.stats) {
    new Stats().wire(this);
  }

  var that = this;

  // each Server has a dummy id for logging purposes
  this.id = this.modernOpts.id || shortid.generate();

  // initialize servers list
  this.servers = [];


  steed.series([

    // steed.series: wait for ascoltatore
    function (done) {

      if(that.modernOpts.ascoltatore) {
        that.ascoltatore = that.modernOpts.ascoltatore;
        done();
      }
      else {
        that.ascoltatore = ascoltatori.build(that.modernOpts.backend, done);
        that.ascoltatore.on('error', that.emit.bind(that, 'error'));
      }
    },

    // steed.series: wait for persistence

    function (done) {
      // REFACTOR: partially move to options.validate and options.populate?
      var persistenceFactory = that.modernOpts.persistence && that.modernOpts.persistence.factory;
      if (persistenceFactory) {
        if (typeof persistenceFactory === 'string') {
          var factoryName = persistenceFactory;
          persistenceFactory = persistence.getFactory(factoryName);
          if (!persistenceFactory) {
            return callback(new Error('No persistence factory found for ' + factoryName ));
          }
        }

        that.persistence = persistenceFactory(that.modernOpts.persistence, done);
        that.persistence.wire(that);
      } else {
        that.persistence = null;
        done();
      }
    },

    // steed.series: iterate over defined interfaces, build servers and listen
    function (done) {

      steed.eachSeries(that.modernOpts.interfaces, function (iface, dn) {
        var fallback = that.modernOpts;
        var host = iface.host || that.modernOpts.host;
        var port = iface.port || that.modernOpts.port;

        var server = interfaces.serverFactory(iface, fallback, that);
        that.servers.push(server);
        server.maxConnections = iface.maxConnections || 10000000;
        server.listen(port, host, dn);
      }, done);
    },

    // steed.series: log startup information
    function (done) {
      var logInfo = {};

      that.modernOpts.interfaces.forEach(function (iface) {
        var name = iface.type;
        if (typeof name !== "string") {
          name = iface.type.name;
        }
        logInfo[name] = iface.port;
      });

      that.logger.info(logInfo, "server started");
      that.emit("ready");
      done(null);
    }
  ], function(err, results){
    if(err) {
      callback(err);
    }
  });

  that.on("clientConnected", function(client) {
    if(that.modernOpts.publishNewClient) {
      that.publish({
        topic: "$SYS/" + that.id + "/new/clients",
        payload: client.id ...
```
- example usage
```shell
...
};

var settings = {
  port: 1883,
  backend: ascoltatore
};

var server = new mosca.Server(settings);

server.on('clientConnected', function(client) {
    console.log('client connected', client.id);
});

// fired when a message is received
server.on('published', function(packet, client) {
...
```

#### <a name="apidoc.element.mosca.Stats"></a>[function <span class="apidocSignatureSpan">mosca.</span>Stats ()](#apidoc.element.mosca.Stats)
- description and source-code
```javascript
function Stats() {
  if (!(this instanceof Stats)) {
    return new Stats();
  }

  this.maxConnectedClients = 0;
  this.connectedClients = 0;
  this.lastIntervalConnectedClients = 0;
  this.publishedMessages = 0;
  this.lastIntervalPublishedMessages = 0;
  this.started = new Date();

  this.load = {
    m15: new Load(15),
    m5: new Load(5),
    m1: new Load(1)
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.client"></a>[function <span class="apidocSignatureSpan">mosca.</span>client (conn, server)](#apidoc.element.mosca.client)
- description and source-code
```javascript
function Client(conn, server) {
  this.connection = conn;
  this.server = server;
  this.logger = server.logger;
  this.subscriptions = {};

  this.nextId = 1;
  this.inflight = {};
  this.inflightCounter = 0;
  this._lastDedupId = -1;
  this._closed = false;
  this._closing = false;

  this._setup();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp"></a>[function <span class="apidocSignatureSpan">mosca.</span>persistence.LevelUp (options, callback)](#apidoc.element.mosca.persistence.LevelUp)
- description and source-code
```javascript
function LevelUpPersistence(options, callback) {
  if (!(this instanceof LevelUpPersistence)) {
    return new LevelUpPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);


  this.db = levelup(this.options.path, this.options);

  var db = sublevel(this.db);

  this._retained = db.sublevel("retained");
  this._clientSubscriptions = db.sublevel("clientSubscriptions");
  this._subscriptions = db.sublevel("subscriptions");
  this._offlinePackets = db.sublevel("offlinePackets");
  this._subMatcher = new Matcher();
  this._packetCounter = 0;
  this._lastStoredPacketTime = Date.now();
  this._streams = [];

  var that = this;
  var stream = this._subscriptions.createReadStream();
  this._streams.push(stream);
  stream.on("data", function(data) {
    that._subMatcher.add(data.value.topic, data.key);
  });
  stream.on("end", function() {
    that._cleanupStream(stream);
    if (callback) {
      callback(null, that);
    }
  });
  stream.on("close", function() {
    that._cleanupStream(stream);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Memory"></a>[function <span class="apidocSignatureSpan">mosca.</span>persistence.Memory (options, callback)](#apidoc.element.mosca.persistence.Memory)
- description and source-code
```javascript
function MemoryPersistence(options, callback) {
  if (!(this instanceof MemoryPersistence)) {
    return new MemoryPersistence(options, callback);
  }

  options = options || {};
  options.db = factory;
  options.path = "RAM";
  LevelUpPersistence.call(this, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo"></a>[function <span class="apidocSignatureSpan">mosca.</span>persistence.Mongo (options, done)](#apidoc.element.mosca.persistence.Mongo)
- description and source-code
```javascript
function MongoPersistence(options, done) {
  if (!(this instanceof MongoPersistence)) {
    return new MongoPersistence(options, done);
  }


  this.options = extend(true, {}, defaults, options);
  this.options.mongo.safe = true;

  // This offlineMessageTimeout(in milliseconds) can set the maximum life time for stored offline messages. This is a
  // Mongo-only feature which relies on TTL index. Since Mongo checks expired entries on a minute-based clock, the
  // actual lifetime is ceil(offlineMessageTimeout/60000) minutes. For this reason, we do not have an unit test
  // for this feature.
  if (options.offlineMessageTimeout) {
    this.options.ttl.packets = options.offlineMessageTimeout;
  }

  var that = this;

  var connected = function(err, db) {
    if (err) {
      if (done) {
        return done(err);
      }
      // we have no way of providing an error handler
      throw err;
    }

    that.db = db;
    steed.parallel([
      function(cb) {
        db.collection("subscriptions", function(err, coll) {
          that._subscriptions = coll;
          steed.parallel([
            that._subscriptions.ensureIndex.bind(that._subscriptions, "client"),
            that._subscriptions.ensureIndex.bind(that._subscriptions, { "added": 1 }, { expireAfterSeconds: Math.round(that.options
.ttl.subscriptions / 1000 )} )
          ], cb);
        });
      },
      function(cb) {
        db.collection("packets", function(err, coll) {
          if (err) {
            return cb(err);
          }

          that._packets = coll;
          steed.series([
            that._packets.ensureIndex.bind(that._packets, "client"),
            function(cb){
              // Check expiration indexes. If not exist, create; If exist but with different TTL, delete and recreate; Otherwise
, do nothing.
              that._packets.indexes(function(error, colIndexes){
                if (error) {
                  cb(error);
                } else {
                  var addedIndexKey = {"added": 1};
                  var addedIndexKeyString = 'added_1'; // If addedIndex changes, this value should also be changed accordingly.
                  var addedIndexObj = colIndexes.filter(function(obj){
                    return obj.name == addedIndexKeyString;
                  });
                  var packetTTLInSeconds = Math.round(that.options.ttl.packets / 1000);
                  if (addedIndexObj.length <= 0 || addedIndexObj[0].expireAfterSeconds != packetTTLInSeconds) {
                    if (addedIndexObj.length > 0) {
                      // Different index TTL, recreate index to make sure the TTL is set to the new number.
                      that._packets.dropIndex(addedIndexKeyString, function (error, result){
                        if (error) {
                          cb(error);
                        } else {
                          that._packets.createIndex(addedIndexKey, {expireAfterSeconds: packetTTLInSeconds}, cb);
                        }
                      });
                    } else {
                      // Create Index for the first time.
                      that._packets.createIndex(addedIndexKey, {expireAfterSeconds: packetTTLInSeconds}, cb);
                    }
                  } else {
                    cb(null);
                  }
                }
              });
            }
          ], cb);
        });
      },
      function(cb) {
        db.collection("retained", function(err, coll) {
          that._retained = coll;
          that._retained.ensureIndex("topic", { unique: true }, cb);
        });
      }
    ], function(err) {
      if (done) {
        done(err, that);
      }
    });
  };

  // Connect to the db
  if (options.connection) {
    connected(null, this.options.connection);
  } else {
    MongoClient.connect(this.options.url, this.options.mongo, connected);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis"></a>[function <span class="apidocSignatureSpan">mosca.</span>persistence.Redis (options, callback)](#apidoc.element.mosca.persistence.Redis)
- description and source-code
```javascript
function RedisPersistence(options, callback) {
  if (!(this instanceof RedisPersistence)) {
    return new RedisPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);

  this._subMatcher = new Matcher();

  this._client = this._buildClient();
  this._pubSubClient = this._buildClient();
  this._id = shortid.generate();

  this._packetKeyTTL = this.options.ttl.packets;
  this._listKeyTTL = this._packetKeyTTL * 2; // list key should live longer than packet key
  this._closing = false;
  this._closed = false;

  var fetchAndUpdateLocalSub = function(key, unsubs, retried, cb) {
    that._client.get(key, function(err, result) {
      if (err) {
        if (cb) {
          cb(err);
        } else {
          return;
        }
      }

      var subs = JSON.parse(result);
      if (!result || typeof subs !== 'object') {
        if (!retried) {
          setTimeout(fetchAndUpdateLocalSub.bind(null, key, unsubs, true, cb), 500);
        } else {
          cb && cb();
        }
        return;
      }

      updateLocalSub(key, subs, unsubs);

      if (cb) {
        cb();
      }
    });
  };

  var updateLocalSub = function(key, subs, unsubs) {
    var xs = key.split(":");
    var id = key.substr(xs[0].length + xs[1].length + 2);

    Object.keys(subs).forEach(function(sub) {
      that._subMatcher.add(sub, id);
    });

    if( unsubs ) {
      unsubs.forEach(function(unsub) {
        that._subMatcher.remove(unsub, id);
      });
    }
  };

  var that = this;

  this._pubSubClient.subscribe(this.options.channel, function(){
    if (that._explicitlyClosed()) {
      return;
    }
    var subsStream = that._client.scanStream({
      match: "client:sub:*",
      count: 25000
    });
    var pipeline = that._client.pipeline();
    var total = 0;
    var done = null;

    subsStream.on('data', function(moreKeys){
      total += moreKeys.length;
      moreKeys.map(function(k){
        pipeline.get(k, function(err, result) {
          if (err) {
            done && done(err);
            return;
          }
          var subs = JSON.parse(result);
          if (!result || typeof subs !== 'object') {
            done && done();
            return;
          }
          updateLocalSub(k, subs);
          done && done();
        });
      });
    });

    subsStream.on('end', function(){
      if (total === 0) {
        return callback(null, that);
      }
      done = function() {
        if (--total === 0 && callback) {
          callback(null, that);
          callback = null;
        }
      };
      pipeline.exec();
    });
  });

  this._pubSubClient.on("message", function(channel, message) {
    if (that._explicitlyClosed()) {
      return;
    }
    var parsed = JSON.parse(message);
    if (parsed.process !== that._id) {
      updateLocalSub(parsed.key, parsed.subs, parsed.unsubs);
    }
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.Authorizer"></a>[module mosca.Authorizer](#apidoc.module.mosca.Authorizer)

#### <a name="apidoc.element.mosca.Authorizer.Authorizer"></a>[function <span class="apidocSignatureSpan">mosca.</span>Authorizer (users)](#apidoc.element.mosca.Authorizer.Authorizer)
- description and source-code
```javascript
function Authorizer(users) {
  this.users = users || {};
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.Authorizer.prototype"></a>[module mosca.Authorizer.prototype](#apidoc.module.mosca.Authorizer.prototype)

#### <a name="apidoc.element.mosca.Authorizer.prototype._authenticate"></a>[function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>_authenticate (client, user, pass, cb)](#apidoc.element.mosca.Authorizer.prototype._authenticate)
- description and source-code
```javascript
_authenticate = function (client, user, pass, cb) {

  var missingUser = !user || !pass || !this.users[user];

  if (missingUser) {
    cb(null, false);
    return;
  }

  user = user.toString();

  client.user = user;
  user = this.users[user];

  hasher({
    password: pass.toString(),
    salt: user.salt
  }, function(err, pass, salt, hash) {
    if (err) {
      cb(err);
      return;
    }

    var success = (user.hash === hash);
    cb(null, success);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Authorizer.prototype.addUser"></a>[function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>addUser (user, pass, authorizePublish, authorizeSubscribe, cb)](#apidoc.element.mosca.Authorizer.prototype.addUser)
- description and source-code
```javascript
addUser = function (user, pass, authorizePublish, authorizeSubscribe, cb) {
  var that = this;

  if (typeof authorizePublish === "function") {
    cb = authorizePublish;
    authorizePublish = null;
    authorizeSubscribe = null;
  } else if (typeof authorizeSubscribe == "function") {
    cb = authorizeSubscribe;
    authorizeSubscribe = null;
  }

  if (!authorizePublish) {
    authorizePublish = defaultGlob;
  }

  if (!authorizeSubscribe) {
    authorizeSubscribe = defaultGlob;
  }

  hasher({
    password: pass.toString()
  }, function(err, pass, salt, hash) {
    if (!err) {
      that.users[user] = {
        salt: salt,
        hash: hash,
        authorizePublish: authorizePublish,
        authorizeSubscribe: authorizeSubscribe
      };
    }
    cb(err);
  });
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Authorizer.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>authenticate (client, user, pass, cb)](#apidoc.element.mosca.Authorizer.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (client, user, pass, cb) {
  that._authenticate(client, user, pass, cb);
}
```
- example usage
```shell
...
  });
  client.stream.end();
  return;
}
  }


  that.server.authenticate(this, packet.username, packet.password,
                       function(err, verdict) {

if (err) {
  logger.info({ username: packet.username }, "authentication error");
  client.connack({
    returnCode: 4
  });
...
```

#### <a name="apidoc.element.mosca.Authorizer.prototype.authorizePublish"></a>[function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>authorizePublish (client, topic, payload, cb)](#apidoc.element.mosca.Authorizer.prototype.authorizePublish)
- description and source-code
```javascript
authorizePublish = function (client, topic, payload, cb) {
  cb(null, minimatch(topic, that.users[client.user].authorizePublish || defaultGlob));
}
```
- example usage
```shell
...
client.on("subscribe", function(packet) {
  that.setUpTimer();
  that.handleSubscribe(packet);
});

client.on("publish", function(packet) {
  that.setUpTimer();
  that.server.authorizePublish(that, packet.topic, packet.payload, function(err, success) {
    that.handleAuthorizePublish(err, success, packet);
  });
});

client.on("unsubscribe", function(packet) {
  that.setUpTimer();
  that.logger.info({ packet: packet }, "unsubscribe received");
...
```

#### <a name="apidoc.element.mosca.Authorizer.prototype.authorizeSubscribe"></a>[function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>authorizeSubscribe (client, topic, cb)](#apidoc.element.mosca.Authorizer.prototype.authorizeSubscribe)
- description and source-code
```javascript
authorizeSubscribe = function (client, topic, cb) {
  cb(null, minimatch(topic, that.users[client.user].authorizeSubscribe || defaultGlob));
}
```
- example usage
```shell
...
  }
};

function handleEachSub (s, cb) {
  /*jshint validthis:true */
  var that = this;
  if (this.subscriptions[s.topic] === undefined) {
    this.server.authorizeSubscribe(that, s.topic, function(err, success) {
      that.handleAuthorizeSubscribe(err, success, s, cb);
    });
  } else {
    cb(null, true);
  }
}
...
```

#### <a name="apidoc.element.mosca.Authorizer.prototype.rmUser"></a>[function <span class="apidocSignatureSpan">mosca.Authorizer.prototype.</span>rmUser (user, cb)](#apidoc.element.mosca.Authorizer.prototype.rmUser)
- description and source-code
```javascript
rmUser = function (user, cb) {
  delete this.users[user];
  cb();
  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.Server"></a>[module mosca.Server](#apidoc.module.mosca.Server)

#### <a name="apidoc.element.mosca.Server.Server"></a>[function <span class="apidocSignatureSpan">mosca.</span>Server (opts, callback)](#apidoc.element.mosca.Server.Server)
- description and source-code
```javascript
function Server(opts, callback) {
  var modernOpts = options.modernize(opts);
  var validationResult = options.validate(modernOpts);

  if (validationResult.errors.length > 0) {
    var errMessage = validationResult.errors[0].message;
    if (callback) {
      callback(new Error(errMessage));
    } else {
      throw new Error(errMessage);
    }
  }

  modernOpts = options.populate(modernOpts);

  if (!(this instanceof Server)) {
    return new Server(opts, callback);
  }

  EventEmitter.call(this);

  if (true) { // REFACTOR: kludge for tests that rely on options structure
    this.opts = extend(true, {}, defaults, opts);
    this.modernOpts = modernOpts;

    if (this.opts.secure) {
      this.opts.secure.port = this.opts.secure.port || 8883;
    }
    if (this.opts.http) {
      this.opts.http.port = this.opts.http.port || 3000;
    }
    if (this.opts.https) {
      this.opts.https.port = this.opts.https.port || 3001;
    }
  } else { // REFACTOR: enable this once test are updated
    this.opts = modernOpts;
  }

  callback = callback || function() {};

  this._dedupId = 0;
  this.clients = {};
  this.closed = false;

  if (this.modernOpts.logger.childOf) {
    this.logger = this.modernOpts.logger.childOf;
    delete this.modernOpts.logger.childOf;
    delete this.modernOpts.logger.name;
    this.logger = this.logger.child(this.modernOpts.logger);
  } else {
    this.logger = pino(this.modernOpts.logger);
  }

  if(this.modernOpts.stats) {
    new Stats().wire(this);
  }

  var that = this;

  // each Server has a dummy id for logging purposes
  this.id = this.modernOpts.id || shortid.generate();

  // initialize servers list
  this.servers = [];


  steed.series([

    // steed.series: wait for ascoltatore
    function (done) {

      if(that.modernOpts.ascoltatore) {
        that.ascoltatore = that.modernOpts.ascoltatore;
        done();
      }
      else {
        that.ascoltatore = ascoltatori.build(that.modernOpts.backend, done);
        that.ascoltatore.on('error', that.emit.bind(that, 'error'));
      }
    },

    // steed.series: wait for persistence

    function (done) {
      // REFACTOR: partially move to options.validate and options.populate?
      var persistenceFactory = that.modernOpts.persistence && that.modernOpts.persistence.factory;
      if (persistenceFactory) {
        if (typeof persistenceFactory === 'string') {
          var factoryName = persistenceFactory;
          persistenceFactory = persistence.getFactory(factoryName);
          if (!persistenceFactory) {
            return callback(new Error('No persistence factory found for ' + factoryName ));
          }
        }

        that.persistence = persistenceFactory(that.modernOpts.persistence, done);
        that.persistence.wire(that);
      } else {
        that.persistence = null;
        done();
      }
    },

    // steed.series: iterate over defined interfaces, build servers and listen
    function (done) {

      steed.eachSeries(that.modernOpts.interfaces, function (iface, dn) {
        var fallback = that.modernOpts;
        var host = iface.host || that.modernOpts.host;
        var port = iface.port || that.modernOpts.port;

        var server = interfaces.serverFactory(iface, fallback, that);
        that.servers.push(server);
        server.maxConnections = iface.maxConnections || 10000000;
        server.listen(port, host, dn);
      }, done);
    },

    // steed.series: log startup information
    function (done) {
      var logInfo = {};

      that.modernOpts.interfaces.forEach(function (iface) {
        var name = iface.type;
        if (typeof name !== "string") {
          name = iface.type.name;
        }
        logInfo[name] = iface.port;
      });

      that.logger.info(logInfo, "server started");
      that.emit("ready");
      done(null);
    }
  ], function(err, results){
    if(err) {
      callback(err);
    }
  });

  that.on("clientConnected", function(client) {
    if(that.modernOpts.publishNewClient) {
      that.publish({
        topic: "$SYS/" + that.id + "/new/clients",
        payload: client.id ...
```
- example usage
```shell
...
};

var settings = {
  port: 1883,
  backend: ascoltatore
};

var server = new mosca.Server(settings);

server.on('clientConnected', function(client) {
    console.log('client connected', client.id);
});

// fired when a message is received
server.on('published', function(packet, client) {
...
```



# <a name="apidoc.module.mosca.Server.prototype"></a>[module mosca.Server.prototype](#apidoc.module.mosca.Server.prototype)

#### <a name="apidoc.element.mosca.Server.prototype.attachHttpServer"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>attachHttpServer (server, path)](#apidoc.element.mosca.Server.prototype.attachHttpServer)
- description and source-code
```javascript
attachHttpServer = function (server, path) {
  var that = this;

  var opt = { server: server };
  if (path) {
    opt.path = path;
  }

  ws.createServer(opt, function(stream) {
    var conn = new Connection(stream);
    new Client(conn, that);
  });
}
```
- example usage
```shell
...
return tls.createServer(credentials, buildWrap(mosca));
}

function httpFactory(iface, fallback, mosca) {
var serve = buildServe(iface, mosca);
var server = http.createServer(serve);

mosca.attachHttpServer(server);
return server;
}

function httpsFactory(iface, fallback, mosca) {
var credentials = iface.credentials || fallback.credentials;
if (credentials === undefined) {
  throw new Error("missing credentials for https server");
...
```

#### <a name="apidoc.element.mosca.Server.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authenticate (client, username, password, callback)](#apidoc.element.mosca.Server.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (client, username, password, callback) {
  callback(null, true);
}
```
- example usage
```shell
...
  });
  client.stream.end();
  return;
}
  }


  that.server.authenticate(this, packet.username, packet.password,
                       function(err, verdict) {

if (err) {
  logger.info({ username: packet.username }, "authentication error");
  client.connack({
    returnCode: 4
  });
...
```

#### <a name="apidoc.element.mosca.Server.prototype.authorizeForward"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authorizeForward (client, packet, callback)](#apidoc.element.mosca.Server.prototype.authorizeForward)
- description and source-code
```javascript
authorizeForward = function (client, packet, callback) {
  callback(null, true);
}
```
- example usage
```shell
...
  var that = this;

  function doForward(err, packet) {
    if (err) {
return that.client && that.client.emit('error', err);
    }

    that.server.authorizeForward(that, packet, function(err, authorized) {
if (err) {
  return that.client && that.client.emit('error', err);
}

if (!authorized) {
  that.logger.warn(packet, "Unauthorized Forward");
  return;
...
```

#### <a name="apidoc.element.mosca.Server.prototype.authorizePublish"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authorizePublish (client, topic, payload, callback)](#apidoc.element.mosca.Server.prototype.authorizePublish)
- description and source-code
```javascript
authorizePublish = function (client, topic, payload, callback) {
  callback(null, true);
}
```
- example usage
```shell
...
client.on("subscribe", function(packet) {
  that.setUpTimer();
  that.handleSubscribe(packet);
});

client.on("publish", function(packet) {
  that.setUpTimer();
  that.server.authorizePublish(that, packet.topic, packet.payload, function(err, success) {
    that.handleAuthorizePublish(err, success, packet);
  });
});

client.on("unsubscribe", function(packet) {
  that.setUpTimer();
  that.logger.info({ packet: packet }, "unsubscribe received");
...
```

#### <a name="apidoc.element.mosca.Server.prototype.authorizeSubscribe"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>authorizeSubscribe (client, topic, callback)](#apidoc.element.mosca.Server.prototype.authorizeSubscribe)
- description and source-code
```javascript
authorizeSubscribe = function (client, topic, callback) {
  callback(null, true);
}
```
- example usage
```shell
...
  }
};

function handleEachSub (s, cb) {
  /*jshint validthis:true */
  var that = this;
  if (this.subscriptions[s.topic] === undefined) {
    this.server.authorizeSubscribe(that, s.topic, function(err, success) {
      that.handleAuthorizeSubscribe(err, success, s, cb);
    });
  } else {
    cb(null, true);
  }
}
...
```

#### <a name="apidoc.element.mosca.Server.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>close (callback)](#apidoc.element.mosca.Server.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  var that = this;
  var stuffToClose = [];

  callback = callback || function nop() {};

  if (that.closed) {
    return callback();
  }

  that.closed = true;

  Object.keys(that.clients).forEach(function(i) {
    stuffToClose.push(that.clients[i]);
  });

  that.servers.forEach(function(server) {
    stuffToClose.push(server);
  });

  if (that.persistence) {
    stuffToClose.push(that.persistence);
  }

  steed.each(stuffToClose, function(toClose, cb) {
    toClose.close(cb, "server closed");
  }, function() {
    that.ascoltatore.close(function () {
      that.logger.info("server closed");
      that.emit("closed");
      callback();
    });
  });
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```

#### <a name="apidoc.element.mosca.Server.prototype.deleteOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>deleteOfflinePacket (client, messageId, callback)](#apidoc.element.mosca.Server.prototype.deleteOfflinePacket)
- description and source-code
```javascript
deleteOfflinePacket = function (client, messageId, callback) {
  if (callback) {
    callback();
  }
}
```
- example usage
```shell
...
var that = this;

logger.debug({ packet: packet }, "puback");
if (this.inflight[packet.messageId]) {
  this.server.emit("delivered", this.inflight[packet.messageId], that);
  this.inflightCounter--;
  delete this.inflight[packet.messageId];
  this.server.deleteOfflinePacket(this, packet.messageId, function(err) {
    if (err) {
      return that.client && that.client.emit("error", err);
    }
    logger.debug({ packet: packet }, "cleaned offline packet");
  });
} else {
  logger.info({ packet: packet }, "no matching packet");
...
```

#### <a name="apidoc.element.mosca.Server.prototype.forwardOfflinePackets"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>forwardOfflinePackets (client, callback)](#apidoc.element.mosca.Server.prototype.forwardOfflinePackets)
- description and source-code
```javascript
forwardOfflinePackets = function (client, callback) {
  if (callback) {
    callback();
  }
}
```
- example usage
```shell
...
    sessionPresent: session_present ? true : false
  });

  that.logger.info("client connected");
  that.server.emit("clientConnected", that);

  // packets will be forward only if client.clean is false
  that.server.forwardOfflinePackets(that);
});

client.on("puback", function(packet) {
  that.setUpTimer();
  that.handlePuback(packet);
});
...
```

#### <a name="apidoc.element.mosca.Server.prototype.forwardRetained"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>forwardRetained (pattern, client, callback)](#apidoc.element.mosca.Server.prototype.forwardRetained)
- description and source-code
```javascript
forwardRetained = function (pattern, client, callback) {
  if (callback) {
    callback();
  }
}
```
- example usage
```shell
...
  return;
}

that.server.persistClient(that);

packet.subscriptions.forEach(function(sub, index) {
  if (authorized[index]) {
    that.server.forwardRetained(sub.topic, that);
    that.server.emit("subscribed", sub.topic, that);
  } else {
    granted[index] = 0x80;
  }
});

if(!that._closed) {
...
```

#### <a name="apidoc.element.mosca.Server.prototype.generateUniqueId"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>generateUniqueId ()](#apidoc.element.mosca.Server.prototype.generateUniqueId)
- description and source-code
```javascript
generateUniqueId = function () {
  return shortid.generate();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Server.prototype.nextDedupId"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>nextDedupId ()](#apidoc.element.mosca.Server.prototype.nextDedupId)
- description and source-code
```javascript
nextDedupId = function () {
  return this._dedupId++;
}
```
- example usage
```shell
...
              indexPlus >= 0 &&
              indexPlus < 2
            )
          );

    if (forward) {
if (options._dedupId === undefined) {
  options._dedupId = that.server.nextDedupId();
  that._lastDedupId = options._dedupId;
}

if (qos && options.messageId) {
  that.server.updateOfflinePacket(that, options.messageId, packet, doForward);
} else {
  doForward(null, packet);
...
```

#### <a name="apidoc.element.mosca.Server.prototype.persistClient"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>persistClient (client, callback)](#apidoc.element.mosca.Server.prototype.persistClient)
- description and source-code
```javascript
persistClient = function (client, callback) {
  if (callback) {
    callback();
  }
}
```
- example usage
```shell
...
  that.logger.info({ packet: packet }, "unsubscribe received");
  steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
    if (err) {
      that.logger.warn(err);
      that.close(null, err.message);
      return;
    }
    that.server.persistClient(that);
    client.unsuback({
      messageId: packet.messageId
    });
  });
});

client.on("disconnect", function() {
...
```

#### <a name="apidoc.element.mosca.Server.prototype.publish"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>publish (packet, client, callback)](#apidoc.element.mosca.Server.prototype.publish)
- description and source-code
```javascript
function publish(packet, client, callback) {

  var that = this;
  var logger = this.logger;

  if (typeof client === 'function') {
    callback = client;
    client = null;
  } else if (client) {
    logger = client.logger;
  }

  if (!callback) {
    callback = nop;
  }

  var newPacket = {
    topic: packet.topic,
    payload: packet.payload,
    messageId: this.generateUniqueId(),
    qos: packet.qos,
    retain: packet.retain
  };

  var opts = {
    qos: packet.qos,
    messageId: newPacket.messageId
  };

  if (client) {
    opts.clientId = client.id;
  }

  that.storePacket(newPacket, function() {
    if (that.closed) {
      logger.debug({ packet: newPacket }, "not delivering because we are closed");
      return;
    }

    that.ascoltatore.publish(
      newPacket.topic,
      newPacket.payload,
      opts,
      function() {
        that.published(newPacket, client, function() {
          if( newPacket.topic.indexOf( '$SYS' ) >= 0 ) {
            logger.trace({ packet: newPacket }, "published packet");
          } else {
            logger.debug({ packet: newPacket }, "published packet");
          }
          that.emit("published", newPacket, client);
          callback(undefined, newPacket);
        });
      }
    );
  });
}
```
- example usage
```shell
...
    }

    if (!authorized) {
      that.logger.warn(packet, "Unauthorized Forward");
      return;
    }

    that.connection.publish(packet);

    if (packet.qos === 1) {
      that.inflight[packet.messageId] = packet;
    }
  });
}
...
```

#### <a name="apidoc.element.mosca.Server.prototype.published"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>published (packet, client, callback)](#apidoc.element.mosca.Server.prototype.published)
- description and source-code
```javascript
published = function (packet, client, callback) {
  callback(null);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Server.prototype.restoreClientSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>restoreClientSubscriptions (client, callback)](#apidoc.element.mosca.Server.prototype.restoreClientSubscriptions)
- description and source-code
```javascript
restoreClientSubscriptions = function (client, callback) {
  if (callback) {
    callback();
  }
}
```
- example usage
```shell
...
  this._buildForward();

  client.on("error", nop);

  function completeConnection() {
that.setUpTimer();

that.server.restoreClientSubscriptions(that, function(session_present) {
  client.connack({
    returnCode: 0,
    // maybe session_present is null, custom old persistence engine
    // or not persistence defined
    sessionPresent: session_present ? true : false
  });
...
```

#### <a name="apidoc.element.mosca.Server.prototype.storePacket"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>storePacket (packet, callback)](#apidoc.element.mosca.Server.prototype.storePacket)
- description and source-code
```javascript
storePacket = function (packet, callback) {
  if (callback) {
    callback();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Server.prototype.subscribe"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>subscribe (topic, callback, done)](#apidoc.element.mosca.Server.prototype.subscribe)
- description and source-code
```javascript
function subscribe(topic, callback, done) {
  this.ascoltatore.subscribe(topic, callback, done);
}
```
- example usage
```shell
...

var handler = function(topic, payload, options) {
  that.forward(topic, payload, options, s.topic, s.qos);
};

if (this.subscriptions[s.topic] === undefined) {
  this.subscriptions[s.topic] = { qos: s.qos, handler: handler };
  this.server.ascoltatore.subscribe(
    s.topic,
    handler,
    function(err) {
      if (err) {
        delete that.subscriptions[s.topic];
        cb(err);
        return;
...
```

#### <a name="apidoc.element.mosca.Server.prototype.toString"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>toString ()](#apidoc.element.mosca.Server.prototype.toString)
- description and source-code
```javascript
toString = function () {
  return 'mosca.Server';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.Server.prototype.updateOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.Server.prototype.</span>updateOfflinePacket (client, originMessageId, packet, callback)](#apidoc.element.mosca.Server.prototype.updateOfflinePacket)
- description and source-code
```javascript
updateOfflinePacket = function (client, originMessageId, packet, callback) {
  if (callback) {
    callback(null, packet);
  }
}
```
- example usage
```shell
...
    if (forward) {
      if (options._dedupId === undefined) {
        options._dedupId = that.server.nextDedupId();
        that._lastDedupId = options._dedupId;
      }

      if (qos && options.messageId) {
        that.server.updateOfflinePacket(that, options.messageId, packet, doForward);
      } else {
        doForward(null, packet);
      }
    }
  };
};
...
```



# <a name="apidoc.module.mosca.Stats"></a>[module mosca.Stats](#apidoc.module.mosca.Stats)

#### <a name="apidoc.element.mosca.Stats.Stats"></a>[function <span class="apidocSignatureSpan">mosca.</span>Stats ()](#apidoc.element.mosca.Stats.Stats)
- description and source-code
```javascript
function Stats() {
  if (!(this instanceof Stats)) {
    return new Stats();
  }

  this.maxConnectedClients = 0;
  this.connectedClients = 0;
  this.lastIntervalConnectedClients = 0;
  this.publishedMessages = 0;
  this.lastIntervalPublishedMessages = 0;
  this.started = new Date();

  this.load = {
    m15: new Load(15),
    m5: new Load(5),
    m1: new Load(1)
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.Stats.prototype"></a>[module mosca.Stats.prototype](#apidoc.module.mosca.Stats.prototype)

#### <a name="apidoc.element.mosca.Stats.prototype.wire"></a>[function <span class="apidocSignatureSpan">mosca.Stats.prototype.</span>wire (server)](#apidoc.element.mosca.Stats.prototype.wire)
- description and source-code
```javascript
function wire(server) {
  server.stats = this;

  var count = 0;

  function doPublish(topic, value) {
    server.publish({
      topic: "$SYS/" + server.id + "/" + topic,
      payload: "" + value
    });
  }

  var mom = moment(this.started);

  var timer = setInterval(function() {
    var stats = server.stats;
    var mem = process.memoryUsage();

    var date = new Date();

    stats.load.m1.maConnectedClients.push(date, stats.lastIntervalConnectedClients);
    stats.load.m5.maConnectedClients.push(date, stats.lastIntervalConnectedClients);
    stats.load.m15.maConnectedClients.push(date, stats.lastIntervalConnectedClients);
    stats.lastIntervalConnectedClients = 0;

    stats.load.m1.maPublishedMessages.push(date, stats.lastIntervalPublishedMessages);
    stats.load.m5.maPublishedMessages.push(date, stats.lastIntervalPublishedMessages);
    stats.load.m15.maPublishedMessages.push(date, stats.lastIntervalPublishedMessages);
    stats.lastIntervalPublishedMessages = 0;

    doPublish("version", version);
    doPublish("started_at", server.stats.started.toISOString());
    doPublish("uptime", mom.from(Date.now(), true));
    doPublish("clients/maximum", stats.maxConnectedClients);
    doPublish("clients/connected", stats.connectedClients);
    doPublish("publish/received", stats.publishedMessages);
    doPublish("load/connections/15min", stats.load.m15.connectedClients);
    doPublish("load/publish/received/15min", stats.load.m15.publishedMessages);
    doPublish("load/connections/5min", stats.load.m5.connectedClients);
    doPublish("load/publish/received/5min", stats.load.m5.publishedMessages);
    doPublish("load/connections/1min", stats.load.m1.connectedClients);
    doPublish("load/publish/received/1min", stats.load.m1.publishedMessages);
    doPublish("memory/rss", mem.rss);
    doPublish("memory/heap/current", mem.heapUsed);
    doPublish("memory/heap/maximum", mem.heapTotal);
  }, 10 * 1000);

  events.forEach(function(event) {
    server.on(event.name, event);
  });

  server.once("closed", function() {
    clearInterval(timer);

    events.forEach(function(event) {
      server.removeListener(event.name, event);
    });
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.client"></a>[module mosca.client](#apidoc.module.mosca.client)

#### <a name="apidoc.element.mosca.client.client"></a>[function <span class="apidocSignatureSpan">mosca.</span>client (conn, server)](#apidoc.element.mosca.client.client)
- description and source-code
```javascript
function Client(conn, server) {
  this.connection = conn;
  this.server = server;
  this.logger = server.logger;
  this.subscriptions = {};

  this.nextId = 1;
  this.inflight = {};
  this.inflightCounter = 0;
  this._lastDedupId = -1;
  this._closed = false;
  this._closing = false;

  this._setup();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.client.prototype"></a>[module mosca.client.prototype](#apidoc.module.mosca.client.prototype)

#### <a name="apidoc.element.mosca.client.prototype._buildForward"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>_buildForward ()](#apidoc.element.mosca.client.prototype._buildForward)
- description and source-code
```javascript
_buildForward = function () {
  var that = this;

  function doForward(err, packet) {
    if (err) {
      return that.client && that.client.emit('error', err);
    }

    that.server.authorizeForward(that, packet, function(err, authorized) {
      if (err) {
        return that.client && that.client.emit('error', err);
      }

      if (!authorized) {
        that.logger.warn(packet, "Unauthorized Forward");
        return;
      }

      that.connection.publish(packet);

      if (packet.qos === 1) {
        that.inflight[packet.messageId] = packet;
      }
    });
  }

  this.forward = function(topic, payload, options, subTopic, qos, cb) {
    if (options._dedupId <= that._lastDedupId) {
      return;
    }

    that.logger.trace({ topic: topic }, "delivering message");

    var sub = that.subscriptions[subTopic],
        indexWildcard = subTopic.indexOf("#"),
        indexPlus = subTopic.indexOf("+"),
        forward = true,
        newId = this.nextId++;

    // Make sure 'nextId' always fits in a uint8 (http://git.io/vmgKI).
    this.nextId %= 65536;

    var packet = {
      topic: topic,
      payload: payload,
      qos: qos,
      messageId: newId
    };

    if (qos) {
      that.inflightCounter++;
    }

    if (that._closed || that._closing) {
      that.logger.debug({ packet: packet }, "trying to send a packet to a disconnected client");
      forward = false;
    } else if (that.inflightCounter >= that.server.opts.maxInflightMessages) {
      that.logger.warn("too many inflight packets, closing");
      that.close(null, "too many inflight packets");
      forward = false;
    }

    if (cb) {
      cb();
    }

    // skip delivery of messages in $SYS for wildcards
    forward = forward &&
              ! ( topic.indexOf('$SYS') >= 0 &&
                  (
                    indexWildcard >= 0 &&
                    indexWildcard < 2 ||
                    indexPlus >= 0 &&
                    indexPlus < 2
                  )
                );

    if (forward) {
      if (options._dedupId === undefined) {
        options._dedupId = that.server.nextDedupId();
        that._lastDedupId = options._dedupId;
      }

      if (qos && options.messageId) {
        that.server.updateOfflinePacket(that, options.messageId, packet, doForward);
      } else {
        doForward(null, packet);
      }
    }
  };
}
```
- example usage
```shell
...
 * Sets up all the handlers, to not be called directly.
 *
 * @api private
 */
Client.prototype._setup = function() {
  var that = this, client = that.connection;

  this._buildForward();

  client.on("error", nop);

  function completeConnection() {
that.setUpTimer();

that.server.restoreClientSubscriptions(that, function(session_present) {
...
```

#### <a name="apidoc.element.mosca.client.prototype._setup"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>_setup ()](#apidoc.element.mosca.client.prototype._setup)
- description and source-code
```javascript
_setup = function () {
  var that = this, client = that.connection;

  this._buildForward();

  client.on("error", nop);

  function completeConnection() {
    that.setUpTimer();

    that.server.restoreClientSubscriptions(that, function(session_present) {
      client.connack({
        returnCode: 0,
        // maybe session_present is null, custom old persistence engine
        // or not persistence defined
        sessionPresent: session_present ? true : false
      });

      that.logger.info("client connected");
      that.server.emit("clientConnected", that);

      // packets will be forward only if client.clean is false
      that.server.forwardOfflinePackets(that);
    });

    client.on("puback", function(packet) {
      that.setUpTimer();
      that.handlePuback(packet);
    });

    client.on("pingreq", function() {
      that.logger.debug("pingreq");
      that.setUpTimer();
      that.handlePingreq();
      that.connection.pingresp();
    });

    client.on("subscribe", function(packet) {
      that.setUpTimer();
      that.handleSubscribe(packet);
    });

    client.on("publish", function(packet) {
      that.setUpTimer();
      that.server.authorizePublish(that, packet.topic, packet.payload, function(err, success) {
        that.handleAuthorizePublish(err, success, packet);
      });
    });

    client.on("unsubscribe", function(packet) {
      that.setUpTimer();
      that.logger.info({ packet: packet }, "unsubscribe received");
      steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
        if (err) {
          that.logger.warn(err);
          that.close(null, err.message);
          return;
        }
        that.server.persistClient(that);
        client.unsuback({
          messageId: packet.messageId
        });
      });
    });

    client.on("disconnect", function() {
      that.logger.debug("disconnect requested");
      that.close(null, "disconnect request");
    });

    function handleError(err) {
      that.logger.warn(err);
      that.onNonDisconnectClose(err.message);
    }

    client.on("error", handleError);
    client.removeListener("error", nop);

    client.on("close", function() {
      that.onNonDisconnectClose("close");
    });
  }

  client.once("connect", function(packet) {
    that.handleConnect(packet, completeConnection);
  });
}
```
- example usage
```shell
...
 this.nextId = 1;
 this.inflight = {};
 this.inflightCounter = 0;
 this._lastDedupId = -1;
 this._closed = false;
 this._closing = false;

 this._setup();
}

/**
* Sets up all the handlers, to not be called directly.
*
* @api private
*/
...
```

#### <a name="apidoc.element.mosca.client.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>close (callback, reason)](#apidoc.element.mosca.client.prototype.close)
- description and source-code
```javascript
close = function (callback, reason) {

  callback = callback || nop;

  if (this._closed || this._closing) {
    return callback();
  }

  var that = this;

  if (this.id) {
    that.logger.debug("closing client, reason: " + reason);

    if (this.timer) {
      this.timer.clear();
    }
  }

  var cleanup = function() {
    that._closed = true;

    that.logger.info("closed");
    that.connection.removeAllListeners();
    // ignore all errors after disconnection
    that.connection.on("error", function() {});
    that.server.emit("clientDisconnected", that, reason);

    callback();
  };

  that._closing = true;

  steed.map(that, Object.keys(that.subscriptions), that.unsubscribeMapTo, function(err) {
    if (err) {
      that.logger.info(err);
    }

    // needed in case of errors
    if (!that._closed) {
      cleanup();
      // prefer destroy[Soon]() to prevent FIN_WAIT zombie connections
      if (that.connection.stream.destroySoon) {
        that.connection.stream.destroySoon();
      } else if (that.connection.stream.destroy) {
        that.connection.stream.destroy();
      } else {
        that.connection.stream.end();
      }
    }
  });
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```

#### <a name="apidoc.element.mosca.client.prototype.handleAuthorizePublish"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleAuthorizePublish (err, success, packet)](#apidoc.element.mosca.client.prototype.handleAuthorizePublish)
- description and source-code
```javascript
handleAuthorizePublish = function (err, success, packet) {
  var that = this;

  if (err || !success) {
    if (!this._closed && !this._closing) {
      that.close(null, (err && err.message) || "publish not authorized");
    }
    return;
  }

  if (success instanceof Buffer) {
    packet.payload = success;
  }

  that.server.publish(packet, that, function() {
    if (packet.qos === 1 && !(that._closed || that._closing)) {
      that.connection.puback({
        messageId: packet.messageId
      });
    }
  });
}
```
- example usage
```shell
...
  that.setUpTimer();
  that.handleSubscribe(packet);
});

client.on("publish", function(packet) {
  that.setUpTimer();
  that.server.authorizePublish(that, packet.topic, packet.payload, function(err, success) {
    that.handleAuthorizePublish(err, success, packet);
  });
});

client.on("unsubscribe", function(packet) {
  that.setUpTimer();
  that.logger.info({ packet: packet }, "unsubscribe received");
  steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
...
```

#### <a name="apidoc.element.mosca.client.prototype.handleAuthorizeSubscribe"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleAuthorizeSubscribe (err, success, s, cb)](#apidoc.element.mosca.client.prototype.handleAuthorizeSubscribe)
- description and source-code
```javascript
handleAuthorizeSubscribe = function (err, success, s, cb) {
  if (err) {
    cb(err);
    return;
  }

  if (!success) {
    this.logger.info({ topic: s.topic }, "subscribe not authorized");
    cb(null, false);
    return;
  }

  var that = this;

  var handler = function(topic, payload, options) {
    that.forward(topic, payload, options, s.topic, s.qos);
  };

  if (this.subscriptions[s.topic] === undefined) {
    this.subscriptions[s.topic] = { qos: s.qos, handler: handler };
    this.server.ascoltatore.subscribe(
      s.topic,
      handler,
      function(err) {
        if (err) {
          delete that.subscriptions[s.topic];
          cb(err);
          return;
        }
        that.logger.info({ topic: s.topic, qos: s.qos }, "subscribed to topic");
        //that.subscriptions[s.topic] = { qos: s.qos, handler: handler };
        cb(null, true);
      }
    );
  } else {
    cb(null, true);
  }
}
```
- example usage
```shell
...
};

function handleEachSub (s, cb) {
  /*jshint validthis:true */
  var that = this;
  if (this.subscriptions[s.topic] === undefined) {
    this.server.authorizeSubscribe(that, s.topic, function(err, success) {
      that.handleAuthorizeSubscribe(err, success, s, cb);
    });
  } else {
    cb(null, true);
  }
}

/**
...
```

#### <a name="apidoc.element.mosca.client.prototype.handleConnect"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleConnect (packet, completeConnection)](#apidoc.element.mosca.client.prototype.handleConnect)
- description and source-code
```javascript
handleConnect = function (packet, completeConnection) {
  var that = this, logger, client = this.connection;

  this.id = packet.clientId;

  this.logger = logger = that.logger.child({ client: this });

  // for MQTT 3.1.1 (protocolVersion == 4) it is valid to receive an empty
  // clientId if cleanSession is set to 1. In this case, Mosca should generate
  // a random ID.
  // Otherwise, the connection should be rejected.
  if(!this.id) {

    if(packet.protocolVersion == 4 && packet.clean) {

      this.id = uuid.v4();
    }
    else {

      logger.info("identifier rejected");
      client.connack({
        returnCode: 2
      });
      client.stream.end();
      return;
    }
  }


  that.server.authenticate(this, packet.username, packet.password,
                           function(err, verdict) {

    if (err) {
      logger.info({ username: packet.username }, "authentication error");
      client.connack({
        returnCode: 4
      });
      client.stream.end();
      return;
    }

    if (!verdict) {
      logger.info({ username: packet.username }, "authentication denied");
      client.connack({
        returnCode: 5
      });
      client.stream.end();
      return;
    }

    that.keepalive = packet.keepalive;
    that.will = packet.will;

    that.clean = packet.clean;

    if (that.id in that.server.clients){
      that.server.clients[that.id].close(completeConnection, "new connection request");
    } else {
      completeConnection();
    }
  });
}
```
- example usage
```shell
...

   client.on("close", function() {
     that.onNonDisconnectClose("close");
   });
 }

 client.once("connect", function(packet) {
   that.handleConnect(packet, completeConnection);
 });
};

/**
* Sets up the keepalive timer.
* To not be called directly.
*
...
```

#### <a name="apidoc.element.mosca.client.prototype.handlePingreq"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handlePingreq ()](#apidoc.element.mosca.client.prototype.handlePingreq)
- description and source-code
```javascript
handlePingreq = function () {
  var that = this;
  that.server.emit("pingreq", that);
}
```
- example usage
```shell
...
  that.setUpTimer();
  that.handlePuback(packet);
});

client.on("pingreq", function() {
  that.logger.debug("pingreq");
  that.setUpTimer();
  that.handlePingreq();
  that.connection.pingresp();
});

client.on("subscribe", function(packet) {
  that.setUpTimer();
  that.handleSubscribe(packet);
});
...
```

#### <a name="apidoc.element.mosca.client.prototype.handlePuback"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handlePuback (packet)](#apidoc.element.mosca.client.prototype.handlePuback)
- description and source-code
```javascript
handlePuback = function (packet) {
  var logger = this.logger;
  var that = this;

  logger.debug({ packet: packet }, "puback");
  if (this.inflight[packet.messageId]) {
    this.server.emit("delivered", this.inflight[packet.messageId], that);
    this.inflightCounter--;
    delete this.inflight[packet.messageId];
    this.server.deleteOfflinePacket(this, packet.messageId, function(err) {
      if (err) {
        return that.client && that.client.emit("error", err);
      }
      logger.debug({ packet: packet }, "cleaned offline packet");
    });
  } else {
    logger.info({ packet: packet }, "no matching packet");
  }
}
```
- example usage
```shell
...

  // packets will be forward only if client.clean is false
  that.server.forwardOfflinePackets(that);
});

client.on("puback", function(packet) {
  that.setUpTimer();
  that.handlePuback(packet);
});

client.on("pingreq", function() {
  that.logger.debug("pingreq");
  that.setUpTimer();
  that.handlePingreq();
  that.connection.pingresp();
...
```

#### <a name="apidoc.element.mosca.client.prototype.handleSubscribe"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>handleSubscribe (packet)](#apidoc.element.mosca.client.prototype.handleSubscribe)
- description and source-code
```javascript
handleSubscribe = function (packet) {
  var that = this, server = this.server, logger = this.logger;

  logger.debug({ packet: packet }, "subscribe received");

  var granted = calculateGranted(this, packet);

  steed.map(this, packet.subscriptions, handleEachSub, function(err, authorized) {

    if (err) {
      that.close(null, err.message);
      return;
    }

    that.server.persistClient(that);

    packet.subscriptions.forEach(function(sub, index) {
      if (authorized[index]) {
        that.server.forwardRetained(sub.topic, that);
        that.server.emit("subscribed", sub.topic, that);
      } else {
        granted[index] = 0x80;
      }
    });

    if(!that._closed) {
      that.connection.suback({
        messageId: packet.messageId,
        granted: granted
      });
    }
  });
}
```
- example usage
```shell
...
  that.setUpTimer();
  that.handlePingreq();
  that.connection.pingresp();
});

client.on("subscribe", function(packet) {
  that.setUpTimer();
  that.handleSubscribe(packet);
});

client.on("publish", function(packet) {
  that.setUpTimer();
  that.server.authorizePublish(that, packet.topic, packet.payload, function(err, success) {
    that.handleAuthorizePublish(err, success, packet);
  });
...
```

#### <a name="apidoc.element.mosca.client.prototype.onNonDisconnectClose"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>onNonDisconnectClose (reason)](#apidoc.element.mosca.client.prototype.onNonDisconnectClose)
- description and source-code
```javascript
onNonDisconnectClose = function (reason) {
  var that = this, logger = that.logger, will = that.will;

  if (this._closed || this._closing) {
    return;
  }

  if (that.will) {
    logger.info({ packet: will }, "delivering last will");
    setImmediate(function() {
      that.server.authorizePublish(that, will.topic, will.payload, function(err, success) {
        that.handleAuthorizePublish(err, success, will);
      });
    });
  }

  this.close(null, reason);
}
```
- example usage
```shell
...
client.on("disconnect", function() {
  that.logger.debug("disconnect requested");
  that.close(null, "disconnect request");
});

function handleError(err) {
  that.logger.warn(err);
  that.onNonDisconnectClose(err.message);
}

client.on("error", handleError);
client.removeListener("error", nop);

client.on("close", function() {
  that.onNonDisconnectClose("close");
...
```

#### <a name="apidoc.element.mosca.client.prototype.setUpTimer"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>setUpTimer ()](#apidoc.element.mosca.client.prototype.setUpTimer)
- description and source-code
```javascript
setUpTimer = function () {
  if (this.keepalive <= 0) {
    return;
  }

  var timeout = this.keepalive * 1000 * 3 / 2;
  var that = this;

  this.logger.debug({ timeout: timeout }, "setting keepalive timeout");

  if (this.timer) {
    this.timer.reschedule(timeout);
  } else {
    this.timer = retimer(function keepaliveTimeout() {
      that.logger.info("keepalive timeout");
      that.onNonDisconnectClose("keepalive timeout");
    }, timeout);
  }
}
```
- example usage
```shell
...
  var that = this, client = that.connection;

  this._buildForward();

  client.on("error", nop);

  function completeConnection() {
that.setUpTimer();

that.server.restoreClientSubscriptions(that, function(session_present) {
  client.connack({
    returnCode: 0,
    // maybe session_present is null, custom old persistence engine
    // or not persistence defined
    sessionPresent: session_present ? true : false
...
```

#### <a name="apidoc.element.mosca.client.prototype.unsubscribeMapTo"></a>[function <span class="apidocSignatureSpan">mosca.client.prototype.</span>unsubscribeMapTo (topic, cb)](#apidoc.element.mosca.client.prototype.unsubscribeMapTo)
- description and source-code
```javascript
unsubscribeMapTo = function (topic, cb) {
  var that = this;
  var sub = that.subscriptions[topic];
  if (!sub || !sub.handler) {
    that.server.emit("unsubscribed", topic, that);
    return cb();
  }

  that.server.ascoltatore.unsubscribe(topic, sub.handler, function(err) {
    if (err) {
      cb(err);
      return;
    }

    if (!that._closing || that.clean) {
      delete that.subscriptions[topic];
      that.logger.info({ topic: topic }, "unsubscribed");
      that.server.emit("unsubscribed", topic, that);
    }

    cb();
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.interfaces"></a>[module mosca.interfaces](#apidoc.module.mosca.interfaces)

#### <a name="apidoc.element.mosca.interfaces.buildServe"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>buildServe (iface, mosca)](#apidoc.element.mosca.interfaces.buildServe)
- description and source-code
```javascript
function buildServe(iface, mosca) {
  var mounts = [];
  var logger = mosca.logger.child({ service: 'http bundle' });

  if (iface.bundle) {
    mounts.push(st({
      path: __dirname + "/../public",
      url: "/",
      dot: true,
      index: false,
      passthrough: true
    }));
  }

  if (iface.static) {
    mounts.push(st({
      path: iface.static,
      dot: true,
      url: "/",
      index: "index.html",
      passthrough: true
    }));
  }

  return function serve(req, res) {

    logger.info({ req: req });

    var cmounts = [].concat(mounts);

    res.on('finish', function() {
      logger.info({ res: res });
    });

    function handle() {
      var mount = cmounts.shift();

      if (mount) {
        mount(req, res, handle);
      } else {
        res.statusCode = 404;
        res.end("Not Found\n");
      }
    }

    handle();
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.interfaces.buildWrap"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>buildWrap (mosca)](#apidoc.element.mosca.interfaces.buildWrap)
- description and source-code
```javascript
function buildWrap(mosca) {
  return function wrap(stream) {
    var connection = new Connection(stream);
    stream.setNoDelay(true);
    new Client(connection, mosca); // REFACTOR?
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.interfaces.httpFactory"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>httpFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.httpFactory)
- description and source-code
```javascript
function httpFactory(iface, fallback, mosca) {
  var serve = buildServe(iface, mosca);
  var server = http.createServer(serve);

  mosca.attachHttpServer(server);
  return server;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.interfaces.httpsFactory"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>httpsFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.httpsFactory)
- description and source-code
```javascript
function httpsFactory(iface, fallback, mosca) {
  var credentials = iface.credentials || fallback.credentials;
  if (credentials === undefined) {
    throw new Error("missing credentials for https server");
  }

  if (credentials.keyPath) {
    credentials.key = fs.readFileSync(credentials.keyPath);
  }

  if (credentials.certPath) {
    credentials.cert = fs.readFileSync(credentials.certPath);
  }

  if (credentials.caPaths) {
    credentials.ca = [];
    credentials.caPaths.forEach(function (caPath) {
    	credentials.ca.push(fs.readFileSync(caPath));
    });
  }

  var serve = buildServe(iface, mosca);
  var server = https.createServer(credentials, serve);
  mosca.attachHttpServer(server);
  return server;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.interfaces.mqttFactory"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>mqttFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.mqttFactory)
- description and source-code
```javascript
function mqttFactory(iface, fallback, mosca) {
  return net.createServer(buildWrap(mosca));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.interfaces.mqttsFactory"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>mqttsFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.mqttsFactory)
- description and source-code
```javascript
function mqttsFactory(iface, fallback, mosca) {
  var credentials = iface.credentials || fallback.credentials;
  if (credentials === undefined) {
    throw new Error("missing credentials for mqtts server");
  }

  if (credentials.keyPath) {
    credentials.key = fs.readFileSync(credentials.keyPath);
  }

  if (credentials.certPath) {
    credentials.cert = fs.readFileSync(credentials.certPath);
  }

  if (credentials.caPaths) {
    credentials.ca = [];
    credentials.caPaths.forEach(function (caPath) {
    	credentials.ca.push(fs.readFileSync(caPath));
    });
  }

  return tls.createServer(credentials, buildWrap(mosca));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.interfaces.serverFactory"></a>[function <span class="apidocSignatureSpan">mosca.interfaces.</span>serverFactory (iface, fallback, mosca)](#apidoc.element.mosca.interfaces.serverFactory)
- description and source-code
```javascript
function serverFactory(iface, fallback, mosca) {
  var factories = {
    "mqtt":  mqttFactory,
    "mqtts": mqttsFactory,
    "http":  httpFactory,
    "https": httpsFactory,
  };

  var type = iface.type; // no fallback
  var factory = factories[type] || type;
  return factory(iface, fallback, mosca);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.options"></a>[module mosca.options](#apidoc.module.mosca.options)

#### <a name="apidoc.element.mosca.options.defaultsLegacy"></a>[function <span class="apidocSignatureSpan">mosca.options.</span>defaultsLegacy ()](#apidoc.element.mosca.options.defaultsLegacy)
- description and source-code
```javascript
function defaultsLegacy() {
  return {
    port: 1883,
    host: null,
    maxConnections: 10000000,
    backend: {
      json: false,
      wildcardOne: '+',
      wildcardSome: '#'
    },
    stats: false,
    publishNewClient: true,
    publishClientDisconnect: true,
    publishSubscriptions: true,
    maxInflightMessages: 1024,
    logger: {
      name: "mosca",
      level: "warn",
      serializers: {
        client: serializers.clientSerializer,
        packet: serializers.packetSerializer,
        req: pino.stdSerializers.req,
        res: pino.stdSerializers.res
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.options.defaultsModern"></a>[function <span class="apidocSignatureSpan">mosca.options.</span>defaultsModern ()](#apidoc.element.mosca.options.defaultsModern)
- description and source-code
```javascript
function defaultsModern() {
  return {
    host: null,
    interfaces: [
      { type: "mqtt", port: 1883, maxConnections: 10000000 }
    ],
    backend: {
      json: false,
      wildcardOne: '+',
      wildcardSome: '#'
    },
    stats: false,
    publishNewClient: true,
    publishClientDisconnect: true,
    publishSubscriptions: true,
    maxInflightMessages: 1024,
    logger: {
      name: "mosca",
      level: "warn",
      serializers: {
        client: serializers.clientSerializer,
        packet: serializers.packetSerializer,
        req: pino.stdSerializers.req,
        res: pino.stdSerializers.res
      }
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.options.modernize"></a>[function <span class="apidocSignatureSpan">mosca.options.</span>modernize (legacy)](#apidoc.element.mosca.options.modernize)
- description and source-code
```javascript
function modernize(legacy) {

  legacy = legacy || {};

  var modernized = {};

  // "plain copyable" conserved options
  var conserved = [
    "id",
    "host",
    "maxInflightMessages",
    "stats",
    "publishNewClient",
    "publishClientDisconnect",
    "publishSubscriptions"
  ];

  // copy all conserved options
  conserved.forEach(function (name) {
    if (legacy.hasOwnProperty(name)) {
      modernized[name] = legacy[name];
    }
  });

  // TODO: copy 'backend' carefully
  if (legacy.hasOwnProperty('backend')) {
    modernized.backend = legacy.backend;
  }

  // TODO: copy 'ascoltatore' carefully
  if (legacy.hasOwnProperty('ascoltatore')) {
    modernized.ascoltatore = legacy.ascoltatore;
  }

  // TODO: copy 'persistence' carefully
  if (legacy.hasOwnProperty('persistence')) {
    modernized.persistence = legacy.persistence;
  }

  // TODO: copy 'logger' carefully
  if (legacy.hasOwnProperty('logger')) {
    modernized.logger = legacy.logger;
  }

  // construct 'credentials'
  if (legacy.hasOwnProperty('credentials')) {
    // copy as is
    modernized.credentials = clone(legacy.credentials);
  } else if (legacy.hasOwnProperty('secure')) {
    // construct from 'secure'
    modernized.credentials = {};
    if (legacy.secure.hasOwnProperty('keyPath')) {
      modernized.credentials.keyPath = legacy.secure.keyPath;
    }
    if (legacy.secure.hasOwnProperty('certPath')) {
      modernized.credentials.certPath = legacy.secure.certPath;
    }
  } // else no credentials were provided

  // construct 'interfaces'
  if (legacy.hasOwnProperty('interfaces')) {
    // cloning
    modernized.interfaces = clone(legacy.interfaces);
  } else {
    // construct from legacy keys
    modernized.interfaces = [];

    // translate mqtt options
    var mqtt_enabled = !legacy.onlyHttp && (typeof legacy.secure === 'undefined' || legacy.allowNonSecure);
    if (mqtt_enabled) {
      var mqtt_interface = { type: 'mqtt' };

      if (legacy.hasOwnProperty('port')) {
        mqtt_interface.port = legacy.port;
      }

      if (legacy.hasOwnProperty('maxConnections')) {
        mqtt_interface.maxConnections = legacy.maxConnections;
      }

      modernized.interfaces.push(mqtt_interface);
    }

    // translate mqtts options
    var mqtts_enabled = !legacy.onlyHttp && legacy.secure;
    if (mqtts_enabled) {
      var mqtts_interface = { type: 'mqtts' };

      if (legacy.secure.hasOwnProperty('port')) {
        mqtts_interface.port = legacy.secure.port;
      }

      modernized.interfaces.push(mqtts_interface);
    }

    // translate http options
    var http_enabled = !!(legacy.http);
    if (http_enabled) {
      var http_interface = { type: 'http' };

      if (legacy.http.hasOwnProperty('port')) {
        http_interface.port = legacy.http.port;
      }

      if (legacy.http.hasOwnProperty('bundle')) {
        http_interface.bundle = legacy.http.bundle;
      }

      if (legacy.http.hasOwnProperty('static')) {
        http_interface.static = legacy.http.static;
      }

      modernized.interfaces.push(http_interface);
    }

    // translate https options
    var https_enabled = !!(legacy.https);
    if (https_enabled) {
      var https_interface = { type: 'https' };

      if (legacy.https.hasOwnProperty('port')) {
        https_interface.port = legacy.https.port;
      }

      if (legacy.https.hasOwnProperty('bundle')) {
        https_interface.bundle = legacy.https.bundle;
      }

      if (legacy.https.hasOwnProperty('static')) {
        https_interface.static = legacy.https.static;
      }

      modernized.interfaces.push(https_interface);
    }

    // NOTE: there are ways end up with no interfaces at all, for example
    // 'httpOnly: true' with undefined http and https
  }

  return modernized;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.options.populate"></a>[function <span class="apidocSignatureSpan">mosca.options.</span>populate (opts)](#apidoc.element.mosca.options.populate)
- description and source-code
```javascript
function populate(opts) {
  var defaults = defaultsModern();

  // do not extend 'interfaces'
  if (opts.hasOwnProperty('interfaces')) {
    delete defaults.interfaces;
  }
  var populated = extend(true, defaults, opts);

  populated.interfaces.forEach(function (iface) {
    if (typeof iface.port === "undefined") {
      switch (iface.type) {
        case "mqtt":   iface.port = 1883; break;
        case "mqtts":  iface.port = 8883; break;
        case "http":   iface.port = 3000; break;
        case "https":  iface.port = 3001; break;
      }
    }
  });

  return populated;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.options.validate"></a>[function <span class="apidocSignatureSpan">mosca.options.</span>validate (opts, validationOptions)](#apidoc.element.mosca.options.validate)
- description and source-code
```javascript
function validate(opts, validationOptions) {
  var validator = new jsonschema.Validator();

  // custom function type
  validator.types.function = function testFunction(instance) {
    return instance instanceof Function;
  };

  validator.addSchema({
    id: '/Credentials',
    type: 'object',
    additionalProperties: true,
    properties: {
      'keyPath': { type: 'string', required: true },
      'certPath': { type: 'string', required: true },
      'caPaths': { type: 'array', required: false },
      'requestCert': { type: 'boolean', required: false },
      'rejectUnauthorized': { type: 'boolean', required: false }
    }
  });

  validator.addSchema({
    id: '/Interface',
    type: 'object',
    properties: {
      'type': { type: ['string', 'function'], required: true },
      'host': { type: ['string', 'null'] },
      'port': { type: ['integer'] },
      'credentials': { $ref: '/Credentials' },
    }
  });

  validator.addSchema({
    id: '/Options',
    type: 'object',
    additionalProperties: false,
    properties: {
      'id': { type: 'string' },
      'host': { type: ['string', 'null'] },
      'interfaces': {
        type: 'array',
        items: { $ref: '/Interface' }
      },
      'credentials': { $ref: '/Credentials' },

      'backend': { type: 'object' },     // TODO
      'ascoltatore': { type: 'object' }, // TODO
      'persistence': { type: 'object' }, // TODO
      'logger': { type: 'object' },      // TODO

      'maxInflightMessages': { type: 'integer' },
      'stats': { type: 'boolean' },
      'publishNewClient': { type: 'boolean' },
      'publishClientDisconnect': { type: 'boolean' },
      'publishSubscriptions': { type: 'boolean' }
    }
  });

  var result = validator.validate(opts, '/Options', validationOptions);

  // check required credentials
  if (opts.hasOwnProperty('interfaces')) {
    var hasCredentials = opts.hasOwnProperty('credentials');
    var reqCredentials = opts.interfaces.some(function (iface) {
      var req = (iface.type === 'mqtts' || iface.type === 'https');
      var has = iface.hasOwnProperty('credentials');
      return req && !has;
    });

    if (reqCredentials && !hasCredentials) {
      result.addError('one of the defiend interfaces requires credentials');
    }
  }

  // TODO: check conflicting backend and ascoltatore

  return result;
}
```
- example usage
```shell
...
    'stats': { type: 'boolean' },
    'publishNewClient': { type: 'boolean' },
    'publishClientDisconnect': { type: 'boolean' },
    'publishSubscriptions': { type: 'boolean' }
  }
});

var result = validator.validate(opts, '/Options', validationOptions);

// check required credentials
if (opts.hasOwnProperty('interfaces')) {
  var hasCredentials = opts.hasOwnProperty('credentials');
  var reqCredentials = opts.interfaces.some(function (iface) {
    var req = (iface.type === 'mqtts' || iface.type === 'https');
    var has = iface.hasOwnProperty('credentials');
...
```



# <a name="apidoc.module.mosca.persistence"></a>[module mosca.persistence](#apidoc.module.mosca.persistence)

#### <a name="apidoc.element.mosca.persistence.LevelUp"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>LevelUp (options, callback)](#apidoc.element.mosca.persistence.LevelUp)
- description and source-code
```javascript
function LevelUpPersistence(options, callback) {
  if (!(this instanceof LevelUpPersistence)) {
    return new LevelUpPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);


  this.db = levelup(this.options.path, this.options);

  var db = sublevel(this.db);

  this._retained = db.sublevel("retained");
  this._clientSubscriptions = db.sublevel("clientSubscriptions");
  this._subscriptions = db.sublevel("subscriptions");
  this._offlinePackets = db.sublevel("offlinePackets");
  this._subMatcher = new Matcher();
  this._packetCounter = 0;
  this._lastStoredPacketTime = Date.now();
  this._streams = [];

  var that = this;
  var stream = this._subscriptions.createReadStream();
  this._streams.push(stream);
  stream.on("data", function(data) {
    that._subMatcher.add(data.value.topic, data.key);
  });
  stream.on("end", function() {
    that._cleanupStream(stream);
    if (callback) {
      callback(null, that);
    }
  });
  stream.on("close", function() {
    that._cleanupStream(stream);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Memory"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>Memory (options, callback)](#apidoc.element.mosca.persistence.Memory)
- description and source-code
```javascript
function MemoryPersistence(options, callback) {
  if (!(this instanceof MemoryPersistence)) {
    return new MemoryPersistence(options, callback);
  }

  options = options || {};
  options.db = factory;
  options.path = "RAM";
  LevelUpPersistence.call(this, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>Mongo (options, done)](#apidoc.element.mosca.persistence.Mongo)
- description and source-code
```javascript
function MongoPersistence(options, done) {
  if (!(this instanceof MongoPersistence)) {
    return new MongoPersistence(options, done);
  }


  this.options = extend(true, {}, defaults, options);
  this.options.mongo.safe = true;

  // This offlineMessageTimeout(in milliseconds) can set the maximum life time for stored offline messages. This is a
  // Mongo-only feature which relies on TTL index. Since Mongo checks expired entries on a minute-based clock, the
  // actual lifetime is ceil(offlineMessageTimeout/60000) minutes. For this reason, we do not have an unit test
  // for this feature.
  if (options.offlineMessageTimeout) {
    this.options.ttl.packets = options.offlineMessageTimeout;
  }

  var that = this;

  var connected = function(err, db) {
    if (err) {
      if (done) {
        return done(err);
      }
      // we have no way of providing an error handler
      throw err;
    }

    that.db = db;
    steed.parallel([
      function(cb) {
        db.collection("subscriptions", function(err, coll) {
          that._subscriptions = coll;
          steed.parallel([
            that._subscriptions.ensureIndex.bind(that._subscriptions, "client"),
            that._subscriptions.ensureIndex.bind(that._subscriptions, { "added": 1 }, { expireAfterSeconds: Math.round(that.options
.ttl.subscriptions / 1000 )} )
          ], cb);
        });
      },
      function(cb) {
        db.collection("packets", function(err, coll) {
          if (err) {
            return cb(err);
          }

          that._packets = coll;
          steed.series([
            that._packets.ensureIndex.bind(that._packets, "client"),
            function(cb){
              // Check expiration indexes. If not exist, create; If exist but with different TTL, delete and recreate; Otherwise
, do nothing.
              that._packets.indexes(function(error, colIndexes){
                if (error) {
                  cb(error);
                } else {
                  var addedIndexKey = {"added": 1};
                  var addedIndexKeyString = 'added_1'; // If addedIndex changes, this value should also be changed accordingly.
                  var addedIndexObj = colIndexes.filter(function(obj){
                    return obj.name == addedIndexKeyString;
                  });
                  var packetTTLInSeconds = Math.round(that.options.ttl.packets / 1000);
                  if (addedIndexObj.length <= 0 || addedIndexObj[0].expireAfterSeconds != packetTTLInSeconds) {
                    if (addedIndexObj.length > 0) {
                      // Different index TTL, recreate index to make sure the TTL is set to the new number.
                      that._packets.dropIndex(addedIndexKeyString, function (error, result){
                        if (error) {
                          cb(error);
                        } else {
                          that._packets.createIndex(addedIndexKey, {expireAfterSeconds: packetTTLInSeconds}, cb);
                        }
                      });
                    } else {
                      // Create Index for the first time.
                      that._packets.createIndex(addedIndexKey, {expireAfterSeconds: packetTTLInSeconds}, cb);
                    }
                  } else {
                    cb(null);
                  }
                }
              });
            }
          ], cb);
        });
      },
      function(cb) {
        db.collection("retained", function(err, coll) {
          that._retained = coll;
          that._retained.ensureIndex("topic", { unique: true }, cb);
        });
      }
    ], function(err) {
      if (done) {
        done(err, that);
      }
    });
  };

  // Connect to the db
  if (options.connection) {
    connected(null, this.options.connection);
  } else {
    MongoClient.connect(this.options.url, this.options.mongo, connected);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>Redis (options, callback)](#apidoc.element.mosca.persistence.Redis)
- description and source-code
```javascript
function RedisPersistence(options, callback) {
  if (!(this instanceof RedisPersistence)) {
    return new RedisPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);

  this._subMatcher = new Matcher();

  this._client = this._buildClient();
  this._pubSubClient = this._buildClient();
  this._id = shortid.generate();

  this._packetKeyTTL = this.options.ttl.packets;
  this._listKeyTTL = this._packetKeyTTL * 2; // list key should live longer than packet key
  this._closing = false;
  this._closed = false;

  var fetchAndUpdateLocalSub = function(key, unsubs, retried, cb) {
    that._client.get(key, function(err, result) {
      if (err) {
        if (cb) {
          cb(err);
        } else {
          return;
        }
      }

      var subs = JSON.parse(result);
      if (!result || typeof subs !== 'object') {
        if (!retried) {
          setTimeout(fetchAndUpdateLocalSub.bind(null, key, unsubs, true, cb), 500);
        } else {
          cb && cb();
        }
        return;
      }

      updateLocalSub(key, subs, unsubs);

      if (cb) {
        cb();
      }
    });
  };

  var updateLocalSub = function(key, subs, unsubs) {
    var xs = key.split(":");
    var id = key.substr(xs[0].length + xs[1].length + 2);

    Object.keys(subs).forEach(function(sub) {
      that._subMatcher.add(sub, id);
    });

    if( unsubs ) {
      unsubs.forEach(function(unsub) {
        that._subMatcher.remove(unsub, id);
      });
    }
  };

  var that = this;

  this._pubSubClient.subscribe(this.options.channel, function(){
    if (that._explicitlyClosed()) {
      return;
    }
    var subsStream = that._client.scanStream({
      match: "client:sub:*",
      count: 25000
    });
    var pipeline = that._client.pipeline();
    var total = 0;
    var done = null;

    subsStream.on('data', function(moreKeys){
      total += moreKeys.length;
      moreKeys.map(function(k){
        pipeline.get(k, function(err, result) {
          if (err) {
            done && done(err);
            return;
          }
          var subs = JSON.parse(result);
          if (!result || typeof subs !== 'object') {
            done && done();
            return;
          }
          updateLocalSub(k, subs);
          done && done();
        });
      });
    });

    subsStream.on('end', function(){
      if (total === 0) {
        return callback(null, that);
      }
      done = function() {
        if (--total === 0 && callback) {
          callback(null, that);
          callback = null;
        }
      };
      pipeline.exec();
    });
  });

  this._pubSubClient.on("message", function(channel, message) {
    if (that._explicitlyClosed()) {
      return;
    }
    var parsed = JSON.parse(message);
    if (parsed.process !== that._id) {
      updateLocalSub(parsed.key, parsed.subs, parsed.unsubs);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.getFactory"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>getFactory (name)](#apidoc.element.mosca.persistence.getFactory)
- description and source-code
```javascript
getFactory = function (name) {
  return factories[name.toLowerCase()];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.persistence.LevelUp"></a>[module mosca.persistence.LevelUp](#apidoc.module.mosca.persistence.LevelUp)

#### <a name="apidoc.element.mosca.persistence.LevelUp.LevelUp"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>LevelUp (options, callback)](#apidoc.element.mosca.persistence.LevelUp.LevelUp)
- description and source-code
```javascript
function LevelUpPersistence(options, callback) {
  if (!(this instanceof LevelUpPersistence)) {
    return new LevelUpPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);


  this.db = levelup(this.options.path, this.options);

  var db = sublevel(this.db);

  this._retained = db.sublevel("retained");
  this._clientSubscriptions = db.sublevel("clientSubscriptions");
  this._subscriptions = db.sublevel("subscriptions");
  this._offlinePackets = db.sublevel("offlinePackets");
  this._subMatcher = new Matcher();
  this._packetCounter = 0;
  this._lastStoredPacketTime = Date.now();
  this._streams = [];

  var that = this;
  var stream = this._subscriptions.createReadStream();
  this._streams.push(stream);
  stream.on("data", function(data) {
    that._subMatcher.add(data.value.topic, data.key);
  });
  stream.on("end", function() {
    that._cleanupStream(stream);
    if (callback) {
      callback(null, that);
    }
  });
  stream.on("close", function() {
    that._cleanupStream(stream);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.super_"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.</span>super_ ()](#apidoc.element.mosca.persistence.LevelUp.super_)
- description and source-code
```javascript
function AbstractPersistence() {

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.persistence.LevelUp.prototype"></a>[module mosca.persistence.LevelUp.prototype](#apidoc.module.mosca.persistence.LevelUp.prototype)

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype._cleanupStream"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>_cleanupStream (stream)](#apidoc.element.mosca.persistence.LevelUp.prototype._cleanupStream)
- description and source-code
```javascript
_cleanupStream = function (stream) {
  var index = this._streams.indexOf(stream);
  if (index !== -1) {
    this._streams.splice(index, 1);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype._storePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>_storePacket (client, packet, cb)](#apidoc.element.mosca.persistence.LevelUp.prototype._storePacket)
- description and source-code
```javascript
_storePacket = function (client, packet, cb) {
  var currentTime = Date.now();
  if (currentTime !== this._lastStoredPacketTime) {
    this._packetCounter = 0;
  }
  this._lastStoredPacketTime = currentTime;
  var key = util.format("%s:%d:%d", client, currentTime, ++this._packetCounter);
  packet.ttl = this.options.ttl.packets + currentTime;
  this._offlinePackets.put(key, packet, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>close (cb)](#apidoc.element.mosca.persistence.LevelUp.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  this._streams.forEach(function(stream) {
    stream.destroy();
  });
  this.db.close(cb);
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.deleteOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>deleteOfflinePacket (client, messageId, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.deleteOfflinePacket)
- description and source-code
```javascript
deleteOfflinePacket = function (client, messageId, done) {
  var that = this;
  var prefix = util.format('%s:', client.id);
  var found = false;
  var stream = that._offlinePackets.createReadStream({
    start : prefix,
    end : prefix + '~'
  });
  this._streams.push(stream);

  stream.on("data", function(data) {
    if (data.value.messageId !== messageId) {
      return;
    }

    found = true;

    that._offlinePackets.del(data.key, function() {
      if (done) {
        done();
      }
    });
  });

  stream.on("end", function() {
    that._cleanupStream(stream);
  });

  stream.on("close", function() {
    that._cleanupStream(stream);
  });

  if (done) {
    stream.on("error", done);
    stream.on("end", function() {
      if (!found) {
        done();
      }
    });
  }
}
```
- example usage
```shell
...
var that = this;

logger.debug({ packet: packet }, "puback");
if (this.inflight[packet.messageId]) {
  this.server.emit("delivered", this.inflight[packet.messageId], that);
  this.inflightCounter--;
  delete this.inflight[packet.messageId];
  this.server.deleteOfflinePacket(this, packet.messageId, function(err) {
    if (err) {
      return that.client && that.client.emit("error", err);
    }
    logger.debug({ packet: packet }, "cleaned offline packet");
  });
} else {
  logger.info({ packet: packet }, "no matching packet");
...
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.lookupRetained"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>lookupRetained (pattern, cb)](#apidoc.element.mosca.persistence.LevelUp.prototype.lookupRetained)
- description and source-code
```javascript
lookupRetained = function (pattern, cb) {
  var that = this;
  var matched = [];
  var matcher = new Matcher();
  var stream = this._retained.createReadStream();
  this._streams.push(stream);
  matcher.add(pattern, true);

  stream.on("error", cb);

  stream.on("end", function() {
    that._cleanupStream(stream);
    cb(null, matched);
  });

  stream.on("close", function() {
    that._cleanupStream(stream);
  });

  stream.on("data", function(data) {
    if (matcher.match(data.key).size > 0) {
      matched.push(data.value);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.lookupSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>lookupSubscriptions (client, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.lookupSubscriptions)
- description and source-code
```javascript
lookupSubscriptions = function (client, done) {
  var that = this;
  this._clientSubscriptions.get(client.id, function(err, subscriptions) {
    var toRemove = [];

    subscriptions = subscriptions || {};

    Object.keys(subscriptions).forEach(function(key) {
      var levelKey = util.format("%s:%s", key, client.id);
      if (subscriptions[key].ttl <= Date.now()) {
        delete subscriptions[key];
        that._subMatcher.remove(key, levelKey);
        toRemove.push(levelKey);
      }
    });

    if (client.clean) {
      that._clientSubscriptions.del(client.id, function() {
        Object.keys(subscriptions).forEach(function(key) {
          // TODO we need to remove these from the subMatcher every time.
          var levelKey = util.format("%s:%s", key, client.id);
          that._subMatcher.remove(key, levelKey);
          toRemove.push(levelKey);
        });

        that.streamOfflinePackets(client, nop, function() {
          that._subscriptions.batch(toRemove.map(function(levelKey) {
            return {
              key: levelKey,
              type: 'del'
            };
          }), function(err) {
            done(err, {});
          });
        });
      });
    } else if (done) {
      done(null, subscriptions);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.storeOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>storeOfflinePacket (packet, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.storeOfflinePacket)
- description and source-code
```javascript
storeOfflinePacket = function (packet, done) {
  var that = this;
  var subs = this._subMatcher.match(packet.topic);
  steed.map(from(subs), function(key, cb) {
    that._subscriptions.get(key, function(err, sub) {
      if (err) {
        return cb(err);
      }
      that._storePacket(sub.client, packet, cb);
    });
  }, done);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.storeRetained"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>storeRetained (packet, cb)](#apidoc.element.mosca.persistence.LevelUp.prototype.storeRetained)
- description and source-code
```javascript
storeRetained = function (packet, cb) {
  if (packet.payload.length > 0) {
    this._retained.put(packet.topic, packet, cb);
  } else {
    this._retained.del(packet.topic, cb);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.storeSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>storeSubscriptions (client, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.storeSubscriptions)
- description and source-code
```javascript
storeSubscriptions = function (client, done) {
  var that = this;
  var subscriptions = {};
  var now = Date.now();

  if (!client.clean) {
    Object.keys(client.subscriptions).forEach(function(key) {
      if (client.subscriptions[key].qos > 0) {
        subscriptions[key] = client.subscriptions[key];
        subscriptions[key].ttl = that.options.ttl.subscriptions + now;
      }
    });
    this._clientSubscriptions.put(client.id, subscriptions, done);
    Object.keys(subscriptions).forEach(function(key) {
      var sub = {
        client: client.id,
        topic: key,
        ttl: that.options.ttl.subscriptions + now,
        qos: subscriptions[key].qos
      };
      var levelKey = util.format("%s:%s", key, client.id);
      that._subMatcher.add(key, levelKey);
      that._subscriptions.put(levelKey, sub);
    });
  } else if (done) {
    done();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.streamOfflinePackets"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>streamOfflinePackets (client, cb, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.streamOfflinePackets)
- description and source-code
```javascript
streamOfflinePackets = function (client, cb, done) {
  var that = this;
  var prefix = util.format('%s:', client.id);
  var count = 0;
  var ended = false;
  var stream = that._offlinePackets.createReadStream({
    start : prefix,
    end : prefix + '~'
  });
  this._streams.push(stream);

  stream.on("data", function(data) {

    if (client.clean || data.value.ttl <= Date.now()) {
      count++;
      that._offlinePackets.del(data.key, function() {
        count--;

	// for testing
        if (ended && count === 0 && done) {
          done();
        }
      });
    } else {
      cb(null, data.value);
    }
  });

  stream.on("end", function() {
    that._cleanupStream(stream);
    ended = true;

    // for testing
    if (count === 0 && done) {
      done();
    }
  });

  stream.on("close", function() {
    that._cleanupStream(stream);
  });

  // for testing
  if (done) {
    stream.on("error", done);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.prototype.updateOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.prototype.</span>updateOfflinePacket (client, messageId, packet, done)](#apidoc.element.mosca.persistence.LevelUp.prototype.updateOfflinePacket)
- description and source-code
```javascript
updateOfflinePacket = function (client, messageId, packet, done) {
  var that = this;
  var prefix = util.format('%s:', client.id);
  var found = false;
  var stream = that._offlinePackets.createReadStream({
    start : prefix,
    end : prefix + '~'
  });
  this._streams.push(stream);

  stream.on("data", function(data) {
    if (data.value.messageId !== messageId) {
      return;
    }

    found = true;

    data.value.messageId = packet.messageId;

    that._offlinePackets.put(data.key, data.value, function() {
      if (done) {
        done(null, packet);
      }
    });
  });

  stream.on("end", function() {
    that._cleanupStream(stream);
  });

  stream.on("close", function() {
    that._cleanupStream(stream);
  });

  if (done) {
    stream.on("error", done);
    stream.on("end", function() {
      if (!found) {
        done(null, packet);
      }
    });
  }
}
```
- example usage
```shell
...
    if (forward) {
      if (options._dedupId === undefined) {
        options._dedupId = that.server.nextDedupId();
        that._lastDedupId = options._dedupId;
      }

      if (qos && options.messageId) {
        that.server.updateOfflinePacket(that, options.messageId, packet, doForward);
      } else {
        doForward(null, packet);
      }
    }
  };
};
...
```



# <a name="apidoc.module.mosca.persistence.LevelUp.super_.prototype"></a>[module mosca.persistence.LevelUp.super_.prototype](#apidoc.module.mosca.persistence.LevelUp.super_.prototype)

#### <a name="apidoc.element.mosca.persistence.LevelUp.super_.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.super_.prototype.</span>close (done)](#apidoc.element.mosca.persistence.LevelUp.super_.prototype.close)
- description and source-code
```javascript
close = function (done) {
  if (done) {
    done(new Error("not implemented yet"));
  }
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```

#### <a name="apidoc.element.mosca.persistence.LevelUp.super_.prototype.wire"></a>[function <span class="apidocSignatureSpan">mosca.persistence.LevelUp.super_.prototype.</span>wire (server)](#apidoc.element.mosca.persistence.LevelUp.super_.prototype.wire)
- description and source-code
```javascript
wire = function (server) {
  var that = this;
  var nop = function() {};
  server.persistence = this;

  server.storePacket = function(packet, cb) {

    // store qos 0 packets only if storeMessagesQos0 is true or retain is true
    if(packet.qos === 0 && packet.retain === false && ! that.options.storeMessagesQos0){
      return cb();
    }

    var total = 1;
    var done = function() {
      if (--total === 0 && cb) {
        cb();
      }
    };
    if (packet.retain) {
      total++;
      that.storeRetained(packet, done);
    }
    if (packet.qos !== 0 || that.options.storeMessagesQos0) {
      total++;
      that.storeOfflinePacket(packet, done);
    }
    done();
  };

  server.deleteOfflinePacket = function(client, messageId, cb) {
    that.deleteOfflinePacket(client, messageId, cb);
  };

  server.updateOfflinePacket = function(client, messageId, packet, cb) {
    that.updateOfflinePacket(client, messageId, packet, cb);
  };

  server.forwardRetained = function(pattern, client, done) {
    that.lookupRetained(pattern, function(err, matches) {
      if (err) {
        client.connection.emit("error", err);
        return;
      }
      steed.each(matches, function(match, cb) {
        client.forward(match.topic, match.payload, match, pattern, match.qos, cb);
      }, done);
    });
  };

  server.on("close", function() {
    that.close();
  });

  server.restoreClientSubscriptions = function restoreClientSubscriptions(client, done) {
    that.lookupSubscriptions(client, function(err, subscriptions) {
      if (err) {
        client.connection.emit("error", err);
        return;
      }

      var subs = Object.keys(subscriptions);

      steed.each(subs, function(topic, inCb) {
        client.logger.debug({ topic: topic, qos: subscriptions[topic].qos }, "restoring subscription");
        client.handleAuthorizeSubscribe(
          null, true, {
          topic: topic,
          qos: subscriptions[topic].qos
        }, inCb);
      }, function(){done(subs.length === 0 ? false : true);});
    });
  };

  server.forwardOfflinePackets = function(client, done) {
    // do not waste cpu time find in stored packets...
    // if client is clean lookupSubscriptions already delete stored packets
    if(client.clean)
      return done && done();

    that.streamOfflinePackets(client, function(err, packet) {
      packet.offline = true;
      client.logger.debug({ packet: packet }, "Forwarding offline packet");
      client.forward(packet.topic, packet.payload, packet, packet.topic, packet.qos);
    }, done);
  };

  server.persistClient = function(client, done) {
    client.logger.debug("Storing offline subscriptions");
    that.storeSubscriptions(client, done);
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.persistence.Memory"></a>[module mosca.persistence.Memory](#apidoc.module.mosca.persistence.Memory)

#### <a name="apidoc.element.mosca.persistence.Memory.Memory"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>Memory (options, callback)](#apidoc.element.mosca.persistence.Memory.Memory)
- description and source-code
```javascript
function MemoryPersistence(options, callback) {
  if (!(this instanceof MemoryPersistence)) {
    return new MemoryPersistence(options, callback);
  }

  options = options || {};
  options.db = factory;
  options.path = "RAM";
  LevelUpPersistence.call(this, options, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Memory.super_"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Memory.</span>super_ (options, callback)](#apidoc.element.mosca.persistence.Memory.super_)
- description and source-code
```javascript
function LevelUpPersistence(options, callback) {
  if (!(this instanceof LevelUpPersistence)) {
    return new LevelUpPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);


  this.db = levelup(this.options.path, this.options);

  var db = sublevel(this.db);

  this._retained = db.sublevel("retained");
  this._clientSubscriptions = db.sublevel("clientSubscriptions");
  this._subscriptions = db.sublevel("subscriptions");
  this._offlinePackets = db.sublevel("offlinePackets");
  this._subMatcher = new Matcher();
  this._packetCounter = 0;
  this._lastStoredPacketTime = Date.now();
  this._streams = [];

  var that = this;
  var stream = this._subscriptions.createReadStream();
  this._streams.push(stream);
  stream.on("data", function(data) {
    that._subMatcher.add(data.value.topic, data.key);
  });
  stream.on("end", function() {
    that._cleanupStream(stream);
    if (callback) {
      callback(null, that);
    }
  });
  stream.on("close", function() {
    that._cleanupStream(stream);
  });
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.persistence.Memory.prototype"></a>[module mosca.persistence.Memory.prototype](#apidoc.module.mosca.persistence.Memory.prototype)

#### <a name="apidoc.element.mosca.persistence.Memory.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Memory.prototype.</span>close (cb)](#apidoc.element.mosca.persistence.Memory.prototype.close)
- description and source-code
```javascript
close = function (cb) {

  MemDOWN.clearGlobalStore();

  this._streams.forEach(function(stream) {
    stream.destroy();
  });
  this.db.close(cb);
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```



# <a name="apidoc.module.mosca.persistence.Mongo"></a>[module mosca.persistence.Mongo](#apidoc.module.mosca.persistence.Mongo)

#### <a name="apidoc.element.mosca.persistence.Mongo.Mongo"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>Mongo (options, done)](#apidoc.element.mosca.persistence.Mongo.Mongo)
- description and source-code
```javascript
function MongoPersistence(options, done) {
  if (!(this instanceof MongoPersistence)) {
    return new MongoPersistence(options, done);
  }


  this.options = extend(true, {}, defaults, options);
  this.options.mongo.safe = true;

  // This offlineMessageTimeout(in milliseconds) can set the maximum life time for stored offline messages. This is a
  // Mongo-only feature which relies on TTL index. Since Mongo checks expired entries on a minute-based clock, the
  // actual lifetime is ceil(offlineMessageTimeout/60000) minutes. For this reason, we do not have an unit test
  // for this feature.
  if (options.offlineMessageTimeout) {
    this.options.ttl.packets = options.offlineMessageTimeout;
  }

  var that = this;

  var connected = function(err, db) {
    if (err) {
      if (done) {
        return done(err);
      }
      // we have no way of providing an error handler
      throw err;
    }

    that.db = db;
    steed.parallel([
      function(cb) {
        db.collection("subscriptions", function(err, coll) {
          that._subscriptions = coll;
          steed.parallel([
            that._subscriptions.ensureIndex.bind(that._subscriptions, "client"),
            that._subscriptions.ensureIndex.bind(that._subscriptions, { "added": 1 }, { expireAfterSeconds: Math.round(that.options
.ttl.subscriptions / 1000 )} )
          ], cb);
        });
      },
      function(cb) {
        db.collection("packets", function(err, coll) {
          if (err) {
            return cb(err);
          }

          that._packets = coll;
          steed.series([
            that._packets.ensureIndex.bind(that._packets, "client"),
            function(cb){
              // Check expiration indexes. If not exist, create; If exist but with different TTL, delete and recreate; Otherwise
, do nothing.
              that._packets.indexes(function(error, colIndexes){
                if (error) {
                  cb(error);
                } else {
                  var addedIndexKey = {"added": 1};
                  var addedIndexKeyString = 'added_1'; // If addedIndex changes, this value should also be changed accordingly.
                  var addedIndexObj = colIndexes.filter(function(obj){
                    return obj.name == addedIndexKeyString;
                  });
                  var packetTTLInSeconds = Math.round(that.options.ttl.packets / 1000);
                  if (addedIndexObj.length <= 0 || addedIndexObj[0].expireAfterSeconds != packetTTLInSeconds) {
                    if (addedIndexObj.length > 0) {
                      // Different index TTL, recreate index to make sure the TTL is set to the new number.
                      that._packets.dropIndex(addedIndexKeyString, function (error, result){
                        if (error) {
                          cb(error);
                        } else {
                          that._packets.createIndex(addedIndexKey, {expireAfterSeconds: packetTTLInSeconds}, cb);
                        }
                      });
                    } else {
                      // Create Index for the first time.
                      that._packets.createIndex(addedIndexKey, {expireAfterSeconds: packetTTLInSeconds}, cb);
                    }
                  } else {
                    cb(null);
                  }
                }
              });
            }
          ], cb);
        });
      },
      function(cb) {
        db.collection("retained", function(err, coll) {
          that._retained = coll;
          that._retained.ensureIndex("topic", { unique: true }, cb);
        });
      }
    ], function(err) {
      if (done) {
        done(err, that);
      }
    });
  };

  // Connect to the db
  if (options.connection) {
    connected(null, this.options.connection);
  } else {
    MongoClient.connect(this.options.url, this.options.mongo, connected);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.super_"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.</span>super_ ()](#apidoc.element.mosca.persistence.Mongo.super_)
- description and source-code
```javascript
function AbstractPersistence() {

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.persistence.Mongo.prototype"></a>[module mosca.persistence.Mongo.prototype](#apidoc.module.mosca.persistence.Mongo.prototype)

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype._storePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>_storePacket (client, packet, cb)](#apidoc.element.mosca.persistence.Mongo.prototype._storePacket)
- description and source-code
```javascript
_storePacket = function (client, packet, cb) {
  var toStore = {
    client: client,
    packet: packet,
    added: new Date()
  };

  this._packets.insert(toStore, {w:1}, cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>close (cb)](#apidoc.element.mosca.persistence.Mongo.prototype.close)
- description and source-code
```javascript
close = function (cb) {
  if (this.db && this.options.autoClose !== false) {
    this.db.close(cb);
  } else {
    cb();
  }
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.deleteOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>deleteOfflinePacket (client, messageId, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.deleteOfflinePacket)
- description and source-code
```javascript
deleteOfflinePacket = function (client, messageId, cb) {
  var toSearch = {
    client: client.id,
    'packet.messageId': messageId
  };

  this._packets.remove(toSearch, {w:1}, cb);
}
```
- example usage
```shell
...
var that = this;

logger.debug({ packet: packet }, "puback");
if (this.inflight[packet.messageId]) {
  this.server.emit("delivered", this.inflight[packet.messageId], that);
  this.inflightCounter--;
  delete this.inflight[packet.messageId];
  this.server.deleteOfflinePacket(this, packet.messageId, function(err) {
    if (err) {
      return that.client && that.client.emit("error", err);
    }
    logger.debug({ packet: packet }, "cleaned offline packet");
  });
} else {
  logger.info({ packet: packet }, "no matching packet");
...
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.lookupRetained"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>lookupRetained (pattern, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.lookupRetained)
- description and source-code
```javascript
lookupRetained = function (pattern, cb) {
  var regexp = new RegExp(pattern.replace(/(#|\+)/, ".+").replace('\\', '\\\\'));
  var stream = this._retained.find({ topic: { $regex: regexp } }).stream();
  var matched = [];
  var matcher = new Matcher();
  matcher.add(pattern, true);

  stream.on("error", cb);

  stream.on("end", function() {
    cb(null, matched);
  });

  stream.on("data", function(data) {
    if (matcher.match(data.topic).size > 0) {
      data.payload = data.payload.buffer;
      matched.push(data);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.lookupSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>lookupSubscriptions (client, done)](#apidoc.element.mosca.persistence.Mongo.prototype.lookupSubscriptions)
- description and source-code
```javascript
lookupSubscriptions = function (client, done) {
  var that = this;
  this._subscriptions.find({ client: client.id })
                     .toArray(function(err, subscriptions) {

    var now = Date.now();

    subscriptions = (subscriptions || []).reduce(function(obj, sub) {
      // mongodb TTL is not precise
      if (sub.added.getTime() + that.options.ttl.subscriptions > now) {
        obj[sub.topic] = {
          qos: sub.qos
        };
      }
      return obj;
    }, {});

    if (!client.clean) {
      done(err, subscriptions);
      return;
    }

    var toExecute = [
      function removeSubscriptions(cb) {
        that._subscriptions.remove({ client: client.id }, cb);
      },
      function removePackets(cb) {
        that._packets.remove({ client: client.id }, cb);
      }
    ];

    steed.parallel(toExecute, function(err) {
      done(null, {});
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.storeOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>storeOfflinePacket (packet, done)](#apidoc.element.mosca.persistence.Mongo.prototype.storeOfflinePacket)
- description and source-code
```javascript
storeOfflinePacket = function (packet, done) {

  var patterns = topicPatterns(packet.topic);

  var stream = this._subscriptions.find({ topic: { $in: patterns } }).stream();
  var ended = false;
  var completed = 0;
  var started = 0;
  var that = this;

  if (done) {
    stream.on("error", done);
  }

  stream.on("data", function(data) {
    started++;

    that._storePacket(data.client, packet, function(err) {
      if (err) {
        return stream.emit("error", err);
      }

      // TODO handle the err in case of no callback
      completed++;

      if (done && ended && started === completed) {
        done();
      }
    });
  });

  stream.on("end", function() {
    ended = true;
    if (done && started === completed) {
      done();
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.storeRetained"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>storeRetained (packet, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.storeRetained)
- description and source-code
```javascript
storeRetained = function (packet, cb) {
  if (packet.payload.length > 0) {
    this._retained.update(
      { topic: packet.topic },
      packet,
      {
        upsert: true,
        w: 1
      },
      function(err, n, result){
        if(cb) {
          return cb(err);
        }
      });
  } else {
    this._retained.remove(
      { topic: packet.topic },
      { w: 1 },
      cb);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.storeSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>storeSubscriptions (client, done)](#apidoc.element.mosca.persistence.Mongo.prototype.storeSubscriptions)
- description and source-code
```javascript
storeSubscriptions = function (client, done) {

  var subscriptions;
  var that = this;

  if (!client.clean) {
    subscriptions = Object.keys(client.subscriptions).filter(function(key) {
      return client.subscriptions[key].qos > 0;
    });

    steed.each(subscriptions, function(key, cb) {
      that._subscriptions.findAndModify({
        client: client.id,
        topic: key
      }, [['date', -1]], {
        $set: {
          client: client.id,
          topic: key,
          qos: client.subscriptions[key].qos,
          added: new Date()
        }
      }, { upsert: true}, cb);
    }, done);
  } else if (done) {
    return done();
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.streamOfflinePackets"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>streamOfflinePackets (client, cb, done)](#apidoc.element.mosca.persistence.Mongo.prototype.streamOfflinePackets)
- description and source-code
```javascript
streamOfflinePackets = function (client, cb, done) {

  var stream = this._packets.find({ client: client.id }).stream();
  var that = this;

  var now = Date.now();

  // for testing
  if(done)
    stream.on("end", done);

  stream.on("error", cb);

  stream.on("data", function(data) {
    // mongodb TTL is not precise
    // mongodb automaticly remove the packet
    if (data.added.getTime() + that.options.ttl.packets > now) {
      data.packet.payload = data.packet.payload.buffer;
      cb(null, data.packet);
    }
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Mongo.prototype.updateOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Mongo.prototype.</span>updateOfflinePacket (client, messageId, packet, cb)](#apidoc.element.mosca.persistence.Mongo.prototype.updateOfflinePacket)
- description and source-code
```javascript
updateOfflinePacket = function (client, messageId, packet, cb) {
  this._packets.update({
    client: client.id,
    'packet.messageId': messageId
  }, {
    $set: { 'packet.messageId': packet.messageId }
  }, {w:1}, function(err) {
    cb(err, packet);
  });
}
```
- example usage
```shell
...
    if (forward) {
      if (options._dedupId === undefined) {
        options._dedupId = that.server.nextDedupId();
        that._lastDedupId = options._dedupId;
      }

      if (qos && options.messageId) {
        that.server.updateOfflinePacket(that, options.messageId, packet, doForward);
      } else {
        doForward(null, packet);
      }
    }
  };
};
...
```



# <a name="apidoc.module.mosca.persistence.Redis"></a>[module mosca.persistence.Redis](#apidoc.module.mosca.persistence.Redis)

#### <a name="apidoc.element.mosca.persistence.Redis.Redis"></a>[function <span class="apidocSignatureSpan">mosca.persistence.</span>Redis (options, callback)](#apidoc.element.mosca.persistence.Redis.Redis)
- description and source-code
```javascript
function RedisPersistence(options, callback) {
  if (!(this instanceof RedisPersistence)) {
    return new RedisPersistence(options, callback);
  }

  this.options = extend(true, {}, defaults, options);

  this._subMatcher = new Matcher();

  this._client = this._buildClient();
  this._pubSubClient = this._buildClient();
  this._id = shortid.generate();

  this._packetKeyTTL = this.options.ttl.packets;
  this._listKeyTTL = this._packetKeyTTL * 2; // list key should live longer than packet key
  this._closing = false;
  this._closed = false;

  var fetchAndUpdateLocalSub = function(key, unsubs, retried, cb) {
    that._client.get(key, function(err, result) {
      if (err) {
        if (cb) {
          cb(err);
        } else {
          return;
        }
      }

      var subs = JSON.parse(result);
      if (!result || typeof subs !== 'object') {
        if (!retried) {
          setTimeout(fetchAndUpdateLocalSub.bind(null, key, unsubs, true, cb), 500);
        } else {
          cb && cb();
        }
        return;
      }

      updateLocalSub(key, subs, unsubs);

      if (cb) {
        cb();
      }
    });
  };

  var updateLocalSub = function(key, subs, unsubs) {
    var xs = key.split(":");
    var id = key.substr(xs[0].length + xs[1].length + 2);

    Object.keys(subs).forEach(function(sub) {
      that._subMatcher.add(sub, id);
    });

    if( unsubs ) {
      unsubs.forEach(function(unsub) {
        that._subMatcher.remove(unsub, id);
      });
    }
  };

  var that = this;

  this._pubSubClient.subscribe(this.options.channel, function(){
    if (that._explicitlyClosed()) {
      return;
    }
    var subsStream = that._client.scanStream({
      match: "client:sub:*",
      count: 25000
    });
    var pipeline = that._client.pipeline();
    var total = 0;
    var done = null;

    subsStream.on('data', function(moreKeys){
      total += moreKeys.length;
      moreKeys.map(function(k){
        pipeline.get(k, function(err, result) {
          if (err) {
            done && done(err);
            return;
          }
          var subs = JSON.parse(result);
          if (!result || typeof subs !== 'object') {
            done && done();
            return;
          }
          updateLocalSub(k, subs);
          done && done();
        });
      });
    });

    subsStream.on('end', function(){
      if (total === 0) {
        return callback(null, that);
      }
      done = function() {
        if (--total === 0 && callback) {
          callback(null, that);
          callback = null;
        }
      };
      pipeline.exec();
    });
  });

  this._pubSubClient.on("message", function(channel, message) {
    if (that._explicitlyClosed()) {
      return;
    }
    var parsed = JSON.parse(message);
    if (parsed.process !== that._id) {
      updateLocalSub(parsed.key, parsed.subs, parsed.unsubs);
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.super_"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.</span>super_ ()](#apidoc.element.mosca.persistence.Redis.super_)
- description and source-code
```javascript
function AbstractPersistence() {

}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.mosca.persistence.Redis.prototype"></a>[module mosca.persistence.Redis.prototype](#apidoc.module.mosca.persistence.Redis.prototype)

#### <a name="apidoc.element.mosca.persistence.Redis.prototype._buildClient"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_buildClient ()](#apidoc.element.mosca.persistence.Redis.prototype._buildClient)
- description and source-code
```javascript
_buildClient = function () {
  var options = this.options.redisOptions || {};

  if (this.options.url) {
    options.url = this.options.url;
  }

  if (this.options.host) {
    options.host = this.options.host;
  }

  if (this.options.port) {
    options.port = this.options.port;
  }

  if (this.options.db) {
    options.db = this.options.db;
  }

  if (this.options.password) {
    options.password = this.options.password;
  }

  return new Redis(options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype._cleanClient"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_cleanClient (client, done)](#apidoc.element.mosca.persistence.Redis.prototype._cleanClient)
- description and source-code
```javascript
_cleanClient = function (client, done) {
  var that = this;

  var key = "client:sub:" + client.id;

  this._client.get(key, function(err, subs) {
    subs = JSON.parse(subs) || {};

    Object.keys(subs).forEach(function(sub) {
      that._subMatcher.remove(sub, client.id);
    });

    steed.parallel([
      function(cb) {
        that._client.del(key, cb);
      },
      function(cb) {
        that._client.del("packets:" + client.id, cb);
      }
    ], function(err) {
      if (done) {
        done(err, {});
      }
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype._explicitlyClosed"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_explicitlyClosed (done)](#apidoc.element.mosca.persistence.Redis.prototype._explicitlyClosed)
- description and source-code
```javascript
_explicitlyClosed = function (done) {
  return this._closing || this._closed;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype._storePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>_storePacket (client, packet, pipeline, cb)](#apidoc.element.mosca.persistence.Redis.prototype._storePacket)
- description and source-code
```javascript
_storePacket = function (client, packet, pipeline, cb) {
  if (this._explicitlyClosed()) {
    return cb && cb(new Error('Explicitly closed'));
  }

  var packetKey = "packets:" + client + ":" + packet.messageId,
      listKey = "packets:" + client;

  pipeline.multi()
    .set(packetKey, JSON.stringify(packet))
    .pexpire(packetKey, this._packetKeyTTL)
    .rpush(listKey, packetKey)
    .pexpire(listKey, this._listKeyTTL)
    .exec();

  cb();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.close"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>close (done)](#apidoc.element.mosca.persistence.Redis.prototype.close)
- description and source-code
```javascript
close = function (done) {
  if (this._closed) {
    return done && done();
  }
  if (this._closing) {
    return done && this.once('close', done);
  }
  this._closing = true;

  var that = this;

  steed.each([
    "_client", "_pubSubClient"
  ], function(client, cb) {
    if (that[client]) {
      that[client].quit(function quit(err) {
        delete that[client];
        cb(err);
      });
    } else {
      cb();
    }
  }, function() {
    that._closed = true;
    that.emit('close');
    done();
  });
}
```
- example usage
```shell
...

    client.on("unsubscribe", function(packet) {
that.setUpTimer();
that.logger.info({ packet: packet }, "unsubscribe received");
steed.map(that, packet.unsubscriptions, that.unsubscribeMapTo, function(err) {
  if (err) {
    that.logger.warn(err);
    that.close(null, err.message);
    return;
  }
  that.server.persistClient(that);
  client.unsuback({
    messageId: packet.messageId
  });
});
...
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.deleteOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>deleteOfflinePacket (client, messageId, done)](#apidoc.element.mosca.persistence.Redis.prototype.deleteOfflinePacket)
- description and source-code
```javascript
deleteOfflinePacket = function (client, messageId, done) {
  if (this._explicitlyClosed()) {
    return done && done(new Error('Explicitly closed'));
  }

  var that = this;
  var packetKey = "packets:" + client.id + ":" + messageId;

  this._client.multi()
    .del(packetKey)
    .lrem("packets:" + client.id, 1, packetKey)
    .exec(done);
}
```
- example usage
```shell
...
var that = this;

logger.debug({ packet: packet }, "puback");
if (this.inflight[packet.messageId]) {
  this.server.emit("delivered", this.inflight[packet.messageId], that);
  this.inflightCounter--;
  delete this.inflight[packet.messageId];
  this.server.deleteOfflinePacket(this, packet.messageId, function(err) {
    if (err) {
      return that.client && that.client.emit("error", err);
    }
    logger.debug({ packet: packet }, "cleaned offline packet");
  });
} else {
  logger.info({ packet: packet }, "no matching packet");
...
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.lookupRetained"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>lookupRetained (pattern, done)](#apidoc.element.mosca.persistence.Redis.prototype.lookupRetained)
- description and source-code
```javascript
lookupRetained = function (pattern, done) {
  if (this._explicitlyClosed()) {
    return done && done(new Error('Explicitly closed'));
  }
  var that = this;
  var matched = [];
  var match = function(topic, cb) {
    that._client.hget("retained", topic, function(err, packet) {
      if (packet) {

        packet = JSON.parse(packet);
        packet.payload = new Buffer(packet.payload);

        matched.push(packet);
      }

      cb(err, matched);
    });
  };

  if (pattern.indexOf("#") >= 0 || pattern.indexOf("+") >= 0) {
    var matcher = new Matcher();
    matcher.add(pattern, true);

    this._client.hkeys("retained", function(err, topics) {
      topics.sort();
      topics = topics.filter(function(topic) {
        return matcher.match(topic).size > 0;
      });

      steed.each(topics, match, function(err) {
        done(err, matched);
      });
    });

    // do something
  } else {
    match(pattern, done);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.lookupSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>lookupSubscriptions (client, cb)](#apidoc.element.mosca.persistence.Redis.prototype.lookupSubscriptions)
- description and source-code
```javascript
lookupSubscriptions = function (client, cb) {
  if (this._explicitlyClosed()) {
    return cb && cb(new Error('Explicitly closed'));
  }

  if (client.clean) {
    this._cleanClient(client, cb);
  }else{
    var key = "client:sub:" + client.id;
    var subscriptions;

    var multi = this._client.multi();

    multi.get(key);

    multi.exec(function(err, result) {
      subscriptions = JSON.parse(result[0][1]) || {};
      cb(err, subscriptions);
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.storeOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>storeOfflinePacket (packet, done)](#apidoc.element.mosca.persistence.Redis.prototype.storeOfflinePacket)
- description and source-code
```javascript
storeOfflinePacket = function (packet, done) {
  if (this._explicitlyClosed()) {
    return done && done(new Error('Explicitly closed'));
  }

  var that = this;

  var matches = this._subMatcher.match(packet.topic);
  var pipeline = this._client.pipeline();
  steed.each(from(matches), function(client, cb) {
    that._storePacket(client, packet, pipeline, cb);
  }, function(){
    pipeline.exec(done);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.storeRetained"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>storeRetained (packet, cb)](#apidoc.element.mosca.persistence.Redis.prototype.storeRetained)
- description and source-code
```javascript
storeRetained = function (packet, cb) {
  if (this._explicitlyClosed()) {
    return cb && cb(new Error('Explicitly closed'));
  }
  if (packet.payload.length > 0) {
    this._client.hset("retained", packet.topic, JSON.stringify(packet), cb);
  } else {
    this._client.hdel("retained", packet.topic, cb);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.storeSubscriptions"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>storeSubscriptions (client, cb)](#apidoc.element.mosca.persistence.Redis.prototype.storeSubscriptions)
- description and source-code
```javascript
storeSubscriptions = function (client, cb) {
  if (this._explicitlyClosed()) {
    return cb && cb(new Error('Explicitly closed'));
  }
  if (client.clean) {
    return cb && cb();
  }
  var clientSubKey = "client:sub:" + client.id;
  var that = this;
  var subscriptions = {};

  Object.keys(client.subscriptions).forEach(function(key) {
    if (client.subscriptions[key].qos > 0) {
      subscriptions[key] = client.subscriptions[key];
    }
  });

  this._client.get(clientSubKey, function(err, currentSubs){
    var unsubs;
    if( !err && currentSubs ) {
      currentSubs = JSON.parse(currentSubs);
      unsubs = Object.keys(currentSubs).filter(function (topic) {
        return !subscriptions[topic];
      });
      unsubs.forEach(function (topic) {
        that._subMatcher.remove(topic, client.id);
      });
    }
    var op = that._client.multi()
      .set(clientSubKey, JSON.stringify(subscriptions))
      .publish(that.options.channel, JSON.stringify({
        key: clientSubKey,
        subs: subscriptions,
        unsubs: unsubs,
        process: that._id
      }))
      .pexpire(clientSubKey, that.options.ttl.subscriptions);

    Object.keys(subscriptions).forEach(function(e) {
      that._subMatcher.add(e, client.id);
    });

    op.exec(cb);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.streamOfflinePackets"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>streamOfflinePackets (client, cb, done)](#apidoc.element.mosca.persistence.Redis.prototype.streamOfflinePackets)
- description and source-code
```javascript
streamOfflinePackets = function (client, cb, done) {
  if (this._explicitlyClosed()) {
    return cb && cb(new Error('Explicitly closed'));
  }

  var that = this,
      listKey = "packets:" + client.id;

  that._client.lrange(listKey, 0, 10000, function(err, results) {

    var total = results.length;

    // for testing
    if(done && total === 0)
      done();

    function emit(key, result) {
      if (result) {
        var match = key.match(keyRegexp);
        result = JSON.parse(result);
        result.payload = new Buffer(result.payload);
        result.messageId = match[3];

        cb(null, result);
      }
    }

    function fetch(multi, key) {
      return multi.get(key);
    }

    results.reduce(fetch, that._client.multi()).exec(function(err,multiResults){
      if(!multiResults && done) {
        done(err);
        return;
      }
      multiResults.forEach(function(multiResult, i){
        var key = results[i];
        var result = multiResult[1];
        total --;
        // If we don't get result for given packet key. It means
        // that packet has expired. Just clean it from client packets key
        if(!result) {
          that._client.lrem(listKey, 0, key);
          // for testing
          if(done && total === 0)
            done();
          return;
        }
        emit(key, result);
      });
    });
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.persistence.Redis.prototype.updateOfflinePacket"></a>[function <span class="apidocSignatureSpan">mosca.persistence.Redis.prototype.</span>updateOfflinePacket (client, messageId, packet, done)](#apidoc.element.mosca.persistence.Redis.prototype.updateOfflinePacket)
- description and source-code
```javascript
updateOfflinePacket = function (client, messageId, packet, done) {
  if (this._explicitlyClosed()) {
    return done && done(new Error('Explicitly closed'));
  }

  var that = this;
  var oldPacketKey = "packets:" + client.id + ":" + messageId;
  var newPacketKey = "packets:" + client.id + ":" + packet.messageId;
  var listKey = "packets:" + client.id;

  that._client.multi()
      .rename(oldPacketKey, newPacketKey)
      .lrem(listKey, 1, oldPacketKey)
      .rpush(listKey, newPacketKey)
      .pexpire(listKey, this._listKeyTTL)
      .exec(function(err) {
        done(err, packet);
      });
}
```
- example usage
```shell
...
    if (forward) {
      if (options._dedupId === undefined) {
        options._dedupId = that.server.nextDedupId();
        that._lastDedupId = options._dedupId;
      }

      if (qos && options.messageId) {
        that.server.updateOfflinePacket(that, options.messageId, packet, doForward);
      } else {
        doForward(null, packet);
      }
    }
  };
};
...
```



# <a name="apidoc.module.mosca.serializers"></a>[module mosca.serializers](#apidoc.module.mosca.serializers)

#### <a name="apidoc.element.mosca.serializers.clientSerializer"></a>[function <span class="apidocSignatureSpan">mosca.serializers.</span>clientSerializer (client)](#apidoc.element.mosca.serializers.clientSerializer)
- description and source-code
```javascript
function clientSerializer(client) {
  return client.id;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.mosca.serializers.packetSerializer"></a>[function <span class="apidocSignatureSpan">mosca.serializers.</span>packetSerializer (packet)](#apidoc.element.mosca.serializers.packetSerializer)
- description and source-code
```javascript
function packetSerializer(packet) {
  var result = {};

  if (packet.messageId) {
    result.messageId = packet.messageId;
  }

  if (packet.topic) {
    result.topic = packet.topic;
  }

  if (packet.qos) {
    result.qos = packet.qos;
  }

  if (packet.unsubscriptions) {
    result.unsubscriptions = packet.unsubscriptions;
  }

  if (packet.subscriptions) {
    result.subscriptions = packet.subscriptions;
  }

  return result;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
