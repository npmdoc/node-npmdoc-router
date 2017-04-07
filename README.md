# api documentation for  [router (v1.3.0)](https://github.com/pillarjs/router#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-router.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-router) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-router.svg)](https://travis-ci.org/npmdoc/node-npmdoc-router)
#### Simple middleware-style router

[![NPM](https://nodei.co/npm/router.png?downloads=true)](https://www.npmjs.com/package/router)

[![apidoc](https://npmdoc.github.io/node-npmdoc-router/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-router_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-router/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-router/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-router/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Douglas Christopher Wilson",
        "email": "doug@somethingdoug.com"
    },
    "bugs": {
        "url": "https://github.com/pillarjs/router/issues"
    },
    "contributors": [
        {
            "name": "Blake Embrey",
            "email": "hello@blakeembrey.com"
        }
    ],
    "dependencies": {
        "array-flatten": "2.1.1",
        "debug": "2.6.1",
        "methods": "~1.1.2",
        "parseurl": "~1.3.1",
        "path-to-regexp": "0.1.7",
        "setprototypeof": "1.0.3",
        "utils-merge": "1.0.0"
    },
    "description": "Simple middleware-style router",
    "devDependencies": {
        "after": "0.8.2",
        "finalhandler": "1.0.0",
        "istanbul": "0.4.5",
        "mocha": "2.5.3",
        "supertest": "1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "15b24075c1de4a3d3f39808c5d7344a1564417c8",
        "tarball": "https://registry.npmjs.org/router/-/router-1.3.0.tgz"
    },
    "engines": {
        "node": ">= 0.8"
    },
    "files": [
        "lib/",
        "LICENSE",
        "HISTORY.md",
        "README.md",
        "index.js"
    ],
    "gitHead": "89aacfa4b74279b4f09632d7dc90b1ef61e91dcc",
    "homepage": "https://github.com/pillarjs/router#readme",
    "license": "MIT",
    "maintainers": [
        {
            "name": "dougwilson",
            "email": "doug@somethingdoug.com"
        }
    ],
    "name": "router",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/pillarjs/router.git"
    },
    "scripts": {
        "test": "mocha --reporter spec --bail --check-leaks test/",
        "test-cov": "istanbul cover node_modules/mocha/bin/_mocha -- --reporter dot --check-leaks test/",
        "test-travis": "istanbul cover node_modules/mocha/bin/_mocha --report lcovonly -- --reporter spec --check-leaks test/"
    },
    "version": "1.3.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module router](#apidoc.module.router)
1.  [function <span class="apidocSignatureSpan">router.</span>Route (path)](#apidoc.element.router.Route)
1.  [function <span class="apidocSignatureSpan">router.</span>layer (path, options, fn)](#apidoc.element.router.layer)
1.  object <span class="apidocSignatureSpan">router.</span>Route.prototype
1.  object <span class="apidocSignatureSpan">router.</span>layer.prototype

#### [module router.Route](#apidoc.module.router.Route)
1.  [function <span class="apidocSignatureSpan">router.</span>Route (path)](#apidoc.element.router.Route.Route)

#### [module router.Route.prototype](#apidoc.module.router.Route.prototype)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>_handles_method (method)](#apidoc.element.router.Route.prototype._handles_method)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>_methods ()](#apidoc.element.router.Route.prototype._methods)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>acl (handler)](#apidoc.element.router.Route.prototype.acl)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>all (handler)](#apidoc.element.router.Route.prototype.all)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>bind (handler)](#apidoc.element.router.Route.prototype.bind)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>checkout (handler)](#apidoc.element.router.Route.prototype.checkout)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>connect (handler)](#apidoc.element.router.Route.prototype.connect)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>copy (handler)](#apidoc.element.router.Route.prototype.copy)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>delete (handler)](#apidoc.element.router.Route.prototype.delete)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>dispatch (req, res, done)](#apidoc.element.router.Route.prototype.dispatch)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>get (handler)](#apidoc.element.router.Route.prototype.get)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>head (handler)](#apidoc.element.router.Route.prototype.head)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>link (handler)](#apidoc.element.router.Route.prototype.link)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>lock (handler)](#apidoc.element.router.Route.prototype.lock)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>m-search (handler)](#apidoc.element.router.Route.prototype.m-search)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>merge (handler)](#apidoc.element.router.Route.prototype.merge)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>mkactivity (handler)](#apidoc.element.router.Route.prototype.mkactivity)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>mkcalendar (handler)](#apidoc.element.router.Route.prototype.mkcalendar)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>mkcol (handler)](#apidoc.element.router.Route.prototype.mkcol)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>move (handler)](#apidoc.element.router.Route.prototype.move)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>notify (handler)](#apidoc.element.router.Route.prototype.notify)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>options (handler)](#apidoc.element.router.Route.prototype.options)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>patch (handler)](#apidoc.element.router.Route.prototype.patch)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>post (handler)](#apidoc.element.router.Route.prototype.post)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>propfind (handler)](#apidoc.element.router.Route.prototype.propfind)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>proppatch (handler)](#apidoc.element.router.Route.prototype.proppatch)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>purge (handler)](#apidoc.element.router.Route.prototype.purge)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>put (handler)](#apidoc.element.router.Route.prototype.put)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>rebind (handler)](#apidoc.element.router.Route.prototype.rebind)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>report (handler)](#apidoc.element.router.Route.prototype.report)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>search (handler)](#apidoc.element.router.Route.prototype.search)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>subscribe (handler)](#apidoc.element.router.Route.prototype.subscribe)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>trace (handler)](#apidoc.element.router.Route.prototype.trace)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>unbind (handler)](#apidoc.element.router.Route.prototype.unbind)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>unlink (handler)](#apidoc.element.router.Route.prototype.unlink)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>unlock (handler)](#apidoc.element.router.Route.prototype.unlock)
1.  [function <span class="apidocSignatureSpan">router.Route.prototype.</span>unsubscribe (handler)](#apidoc.element.router.Route.prototype.unsubscribe)

#### [module router.layer](#apidoc.module.router.layer)
1.  [function <span class="apidocSignatureSpan">router.</span>layer (path, options, fn)](#apidoc.element.router.layer.layer)

#### [module router.layer.prototype](#apidoc.module.router.layer.prototype)
1.  [function <span class="apidocSignatureSpan">router.layer.prototype.</span>handle_error (error, req, res, next)](#apidoc.element.router.layer.prototype.handle_error)
1.  [function <span class="apidocSignatureSpan">router.layer.prototype.</span>handle_request (req, res, next)](#apidoc.element.router.layer.prototype.handle_request)
1.  [function <span class="apidocSignatureSpan">router.layer.prototype.</span>match (path)](#apidoc.element.router.layer.prototype.match)



# <a name="apidoc.module.router"></a>[module router](#apidoc.module.router)

#### <a name="apidoc.element.router.Route"></a>[function <span class="apidocSignatureSpan">router.</span>Route (path)](#apidoc.element.router.Route)
- description and source-code
```javascript
function Route(path) {
  debug('new %o', path)
  this.path = path
  this.stack = []

  // route handlers for various http methods
  this.methods = {}
}
```
- example usage
```shell
...
Using 'router.route(path)' is a recommended approach to avoiding duplicate
route naming and thus typo errors.

'''js
var api = router.route('/api/')
'''

## Router.Route(path)

Represents a single route as an instance that can be used can be used to handle
http 'methods' with it's own, optional middleware.

### route\[method](handler)

These are functions which you can directly call on a route to register a new
...
```

#### <a name="apidoc.element.router.layer"></a>[function <span class="apidocSignatureSpan">router.</span>layer (path, options, fn)](#apidoc.element.router.layer)
- description and source-code
```javascript
function Layer(path, options, fn) {
  if (!(this instanceof Layer)) {
    return new Layer(path, options, fn)
  }

  debug('new %o', path)
  var opts = options || {}

  this.handle = fn
  this.name = fn.name || '<anonymous>'
  this.params = undefined
  this.path = undefined
  this.regexp = pathRegexp(path, this.keys = [], opts)

  // set fast path flags
  this.regexp.fast_star = path === '*'
  this.regexp.fast_slash = path === '/' && opts.end === false
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.router.Route"></a>[module router.Route](#apidoc.module.router.Route)

#### <a name="apidoc.element.router.Route.Route"></a>[function <span class="apidocSignatureSpan">router.</span>Route (path)](#apidoc.element.router.Route.Route)
- description and source-code
```javascript
function Route(path) {
  debug('new %o', path)
  this.path = path
  this.stack = []

  // route handlers for various http methods
  this.methods = {}
}
```
- example usage
```shell
...
Using 'router.route(path)' is a recommended approach to avoiding duplicate
route naming and thus typo errors.

'''js
var api = router.route('/api/')
'''

## Router.Route(path)

Represents a single route as an instance that can be used can be used to handle
http 'methods' with it's own, optional middleware.

### route\[method](handler)

These are functions which you can directly call on a route to register a new
...
```



# <a name="apidoc.module.router.Route.prototype"></a>[module router.Route.prototype](#apidoc.module.router.Route.prototype)

#### <a name="apidoc.element.router.Route.prototype._handles_method"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>_handles_method (method)](#apidoc.element.router.Route.prototype._handles_method)
- description and source-code
```javascript
function _handles_method(method) {
  if (this.methods._all) {
    return true
  }

  // normalize name
  var name = method.toLowerCase()

  if (name === 'head' && !this.methods['head']) {
    name = 'get'
  }

  return Boolean(this.methods[name])
}
```
- example usage
```shell
...
if (layerError) {
  // routes do not match with a pending error
  match = false
  continue
}

var method = req.method;
var has_method = route._handles_method(method)

// build up automatic options response
if (!has_method && method === 'OPTIONS' && methods) {
  methods.push.apply(methods, route._methods())
}

// don't even bother matching route
...
```

#### <a name="apidoc.element.router.Route.prototype._methods"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>_methods ()](#apidoc.element.router.Route.prototype._methods)
- description and source-code
```javascript
function _methods() {
  var methods = Object.keys(this.methods)

  // append automatic head
  if (this.methods.get && !this.methods.head) {
    methods.push('head')
  }

  for (var i = 0; i < methods.length; i++) {
    // make upper case
    methods[i] = methods[i].toUpperCase()
  }

  return methods
}
```
- example usage
```shell
...
}

var method = req.method;
var has_method = route._handles_method(method)

// build up automatic options response
if (!has_method && method === 'OPTIONS' && methods) {
  methods.push.apply(methods, route._methods())
}

// don't even bother matching route
if (!has_method && method !== 'HEAD') {
  match = false
  continue
}
...
```

#### <a name="apidoc.element.router.Route.prototype.acl"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>acl (handler)](#apidoc.element.router.Route.prototype.acl)
- description and source-code
```javascript
acl = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.all"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>all (handler)](#apidoc.element.router.Route.prototype.all)
- description and source-code
```javascript
function all(handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    var layer = Layer('/', {}, fn)
    layer.method = undefined

    this.methods._all = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
...

status.get(function (req, res) {
  res.setHeader('Content-Type', 'text/plain; charset=utf-8')
  res.end('All Systems Green!')
})
'''

### route.all(handler)

Adds a handler for all HTTP methods to this route.

The handler can behave like middleware and call 'next' to continue processing
rather than responding.

'''js
...
```

#### <a name="apidoc.element.router.Route.prototype.bind"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>bind (handler)](#apidoc.element.router.Route.prototype.bind)
- description and source-code
```javascript
bind = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.checkout"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>checkout (handler)](#apidoc.element.router.Route.prototype.checkout)
- description and source-code
```javascript
checkout = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.connect"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>connect (handler)](#apidoc.element.router.Route.prototype.connect)
- description and source-code
```javascript
connect = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.copy"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>copy (handler)](#apidoc.element.router.Route.prototype.copy)
- description and source-code
```javascript
copy = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.delete"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>delete (handler)](#apidoc.element.router.Route.prototype.delete)
- description and source-code
```javascript
delete = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.dispatch"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>dispatch (req, res, done)](#apidoc.element.router.Route.prototype.dispatch)
- description and source-code
```javascript
function dispatch(req, res, done) {
  var idx = 0
  var stack = this.stack
  if (stack.length === 0) {
    return done()
  }

  var method = req.method.toLowerCase()
  if (method === 'head' && !this.methods['head']) {
    method = 'get'
  }

  req.route = this

  next()

  function next(err) {
    // signal to exit route
    if (err && err === 'route') {
      return done()
    }

    // signal to exit router
    if (err && err === 'router') {
      return done(err)
    }

    // no more matching layers
    if (idx >= stack.length) {
      return done(err)
    }

    var layer
    var match

    // find next matching layer
    while (match !== true && idx < stack.length) {
      layer = stack[idx++]
      match = !layer.method || layer.method === method
    }

    // no match
    if (match !== true) {
      return done(err)
    }

    if (err) {
      layer.handle_error(err, req, res, next)
    } else {
      layer.handle_request(req, res, next)
    }
  }
}
```
- example usage
```shell
...
  var layer = new Layer(path, {
    sensitive: this.caseSensitive,
    strict: this.strict,
    end: true
  }, handle)

  function handle(req, res, next) {
    route.dispatch(req, res, next)
  }

  layer.route = route

  this.stack.push(layer)
  return route
}
...
```

#### <a name="apidoc.element.router.Route.prototype.get"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>get (handler)](#apidoc.element.router.Route.prototype.get)
- description and source-code
```javascript
get = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
...

'''js
var finalhandler = require('finalhandler')
var http         = require('http')
var Router       = require('router')

var router = Router()
router.get('/', function (req, res) {
  res.setHeader('Content-Type', 'text/plain; charset=utf-8')
  res.end('Hello World!')
})

var server = http.createServer(function(req, res) {
  router(req, res, finalhandler(req, res))
})
...
```

#### <a name="apidoc.element.router.Route.prototype.head"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>head (handler)](#apidoc.element.router.Route.prototype.head)
- description and source-code
```javascript
head = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.link"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>link (handler)](#apidoc.element.router.Route.prototype.link)
- description and source-code
```javascript
link = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.lock"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>lock (handler)](#apidoc.element.router.Route.prototype.lock)
- description and source-code
```javascript
lock = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.m-search"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>m-search (handler)](#apidoc.element.router.Route.prototype.m-search)
- description and source-code
```javascript
m-search = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.merge"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>merge (handler)](#apidoc.element.router.Route.prototype.merge)
- description and source-code
```javascript
merge = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.mkactivity"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>mkactivity (handler)](#apidoc.element.router.Route.prototype.mkactivity)
- description and source-code
```javascript
mkactivity = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.mkcalendar"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>mkcalendar (handler)](#apidoc.element.router.Route.prototype.mkcalendar)
- description and source-code
```javascript
mkcalendar = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.mkcol"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>mkcol (handler)](#apidoc.element.router.Route.prototype.mkcol)
- description and source-code
```javascript
mkcol = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.move"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>move (handler)](#apidoc.element.router.Route.prototype.move)
- description and source-code
```javascript
move = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.notify"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>notify (handler)](#apidoc.element.router.Route.prototype.notify)
- description and source-code
```javascript
notify = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.options"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>options (handler)](#apidoc.element.router.Route.prototype.options)
- description and source-code
```javascript
options = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.patch"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>patch (handler)](#apidoc.element.router.Route.prototype.patch)
- description and source-code
```javascript
patch = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
...
var api = Router()
router.use('/api/', api)

// add a body parsing middleware to our API
api.use(bodyParser.json())

// handle 'PATCH' requests to '/api/set-message'
api.patch('/set-message', function (req, res) {
if (req.body.value) {
  message = req.body.value

  res.statusCode = 200
  res.setHeader('Content-Type', 'text/plain; charset=utf-8')
  res.end(message + '\n')
} else {
...
```

#### <a name="apidoc.element.router.Route.prototype.post"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>post (handler)](#apidoc.element.router.Route.prototype.post)
- description and source-code
```javascript
post = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.propfind"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>propfind (handler)](#apidoc.element.router.Route.prototype.propfind)
- description and source-code
```javascript
propfind = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.proppatch"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>proppatch (handler)](#apidoc.element.router.Route.prototype.proppatch)
- description and source-code
```javascript
proppatch = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.purge"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>purge (handler)](#apidoc.element.router.Route.prototype.purge)
- description and source-code
```javascript
purge = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.put"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>put (handler)](#apidoc.element.router.Route.prototype.put)
- description and source-code
```javascript
put = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.rebind"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>rebind (handler)](#apidoc.element.router.Route.prototype.rebind)
- description and source-code
```javascript
rebind = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.report"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>report (handler)](#apidoc.element.router.Route.prototype.report)
- description and source-code
```javascript
report = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.search"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>search (handler)](#apidoc.element.router.Route.prototype.search)
- description and source-code
```javascript
search = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.subscribe"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>subscribe (handler)](#apidoc.element.router.Route.prototype.subscribe)
- description and source-code
```javascript
subscribe = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.trace"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>trace (handler)](#apidoc.element.router.Route.prototype.trace)
- description and source-code
```javascript
trace = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.unbind"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>unbind (handler)](#apidoc.element.router.Route.prototype.unbind)
- description and source-code
```javascript
unbind = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.unlink"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>unlink (handler)](#apidoc.element.router.Route.prototype.unlink)
- description and source-code
```javascript
unlink = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.unlock"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>unlock (handler)](#apidoc.element.router.Route.prototype.unlock)
- description and source-code
```javascript
unlock = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.router.Route.prototype.unsubscribe"></a>[function <span class="apidocSignatureSpan">router.Route.prototype.</span>unsubscribe (handler)](#apidoc.element.router.Route.prototype.unsubscribe)
- description and source-code
```javascript
unsubscribe = function (handler) {
  var callbacks = flatten(slice.call(arguments))

  if (callbacks.length === 0) {
    throw new TypeError('argument handler is required')
  }

  for (var i = 0; i < callbacks.length; i++) {
    var fn = callbacks[i]

    if (typeof fn !== 'function') {
      throw new TypeError('argument handler must be a function')
    }

    debug('%s %s', method, this.path)

    var layer = Layer('/', {}, fn)
    layer.method = method

    this.methods[method] = true
    this.stack.push(layer)
  }

  return this
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.router.layer"></a>[module router.layer](#apidoc.module.router.layer)

#### <a name="apidoc.element.router.layer.layer"></a>[function <span class="apidocSignatureSpan">router.</span>layer (path, options, fn)](#apidoc.element.router.layer.layer)
- description and source-code
```javascript
function Layer(path, options, fn) {
  if (!(this instanceof Layer)) {
    return new Layer(path, options, fn)
  }

  debug('new %o', path)
  var opts = options || {}

  this.handle = fn
  this.name = fn.name || '<anonymous>'
  this.params = undefined
  this.path = undefined
  this.regexp = pathRegexp(path, this.keys = [], opts)

  // set fast path flags
  this.regexp.fast_star = path === '*'
  this.regexp.fast_slash = path === '/' && opts.end === false
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.router.layer.prototype"></a>[module router.layer.prototype](#apidoc.module.router.layer.prototype)

#### <a name="apidoc.element.router.layer.prototype.handle_error"></a>[function <span class="apidocSignatureSpan">router.layer.prototype.</span>handle_error (error, req, res, next)](#apidoc.element.router.layer.prototype.handle_error)
- description and source-code
```javascript
function handle_error(error, req, res, next) {
  var fn = this.handle

  if (fn.length !== 4) {
    // not a standard error handler
    return next(error)
  }

  try {
    fn(error, req, res, next)
  } catch (err) {
    next(err)
  }
}
```
- example usage
```shell
...
        ? removed.substring(0, removed.length - 1)
        : removed)
    }

    debug('%s %s : %s', layer.name, layerPath, req.originalUrl)

    if (layerError) {
      layer.handle_error(layerError, req, res, next)
    } else {
      layer.handle_request(req, res, next)
    }
  }
}

/**
...
```

#### <a name="apidoc.element.router.layer.prototype.handle_request"></a>[function <span class="apidocSignatureSpan">router.layer.prototype.</span>handle_request (req, res, next)](#apidoc.element.router.layer.prototype.handle_request)
- description and source-code
```javascript
function handle(req, res, next) {
  var fn = this.handle

  if (fn.length > 3) {
    // not a standard request handler
    return next()
  }

  try {
    fn(req, res, next)
  } catch (err) {
    next(err)
  }
}
```
- example usage
```shell
...
  // this should be done for the layer
  self.process_params(layer, paramcalled, req, res, function (err) {
    if (err) {
      return next(layerError || err)
    }

    if (route) {
      return layer.handle_request(req, res, next)
    }

    trim_prefix(layer, layerError, layerPath, path)
  })
}

function trim_prefix(layer, layerError, layerPath, path) {
...
```

#### <a name="apidoc.element.router.layer.prototype.match"></a>[function <span class="apidocSignatureSpan">router.layer.prototype.</span>match (path)](#apidoc.element.router.layer.prototype.match)
- description and source-code
```javascript
function match(path) {
  var match

  if (path != null) {
    // fast path non-ending match for / (any path matches)
    if (this.regexp.fast_slash) {
      this.params = {}
      this.path = ''
      return true
    }

    // fast path for * (everything matched in a param)
    if (this.regexp.fast_star) {
      this.params = {'0': decode_param(path)}
      this.path = path
      return true
    }

    // match the path
    match = this.regexp.exec(path)
  }

  if (!match) {
    this.params = undefined
    this.path = undefined
    return false
  }

  // store values
  this.params = {}
  this.path = match[0]

  // iterate matches
  var keys = this.keys
  var params = this.params

  for (var i = 1; i < match.length; i++) {
    var key = keys[i - 1]
    var prop = key.name
    var val = decode_param(match[i])

    if (val !== undefined || !(hasOwnProperty.call(params, prop))) {
      params[prop] = val
    }
  }

  return true
}
```
- example usage
```shell
...
* @param {Layer} layer
* @param {string} path
* @private
*/

function matchLayer(layer, path) {
 try {
   return layer.match(path);
 } catch (err) {
   return err;
 }
}

/**
* Merge params with parent params
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
