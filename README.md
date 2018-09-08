# open-api
[![Build Status](https://travis-ci.org/netlify/open-api.svg?branch=master)](https://travis-ci.org/netlify/open-api) [![Build status](https://ci.appveyor.com/api/projects/status/qrmvxk957ou2yrd9/branch/master?svg=true)](https://ci.appveyor.com/project/netlify/open-api/branch/master)

This repository contains Netlify's API definition in the [Open API format](https://github.com/OAI/OpenAPI-Specification/blob/master/versions/2.0.md) (AKA Swagger).

The spec is currently incomplete but includes many common endpoints.

## Usage

The `swagger.yml` file is the master copy of the Open API 2.0 definition.  Additional context on using the API can be found on our [docs site](https://www.netlify.com/docs/api/).

The spec is published and versioned for various ecosystems:

### SwaggerUI (Web UI)

You can view the definition using [Swagger UI](https://swagger.io/tools/swagger-ui/) by visiting [open-api.netlify.com](http://open-api.netlify.com) which provides limited interaction with the API from the browser.

![screenshot of netlify swagger ui](ui/screenshot.png)

### Go Client

[![GoDoc](https://godoc.org/github.com/netlify/open-api/go?status.svg)](https://godoc.org/github.com/netlify/open-api/go) [![Go Report Card](https://goreportcard.com/badge/github.com/netlify/open-api)](https://goreportcard.com/report/github.com/netlify/open-api) [![Github release](https://img.shields.io/github/release/qubyte/rubidium.svg)](https://github.com/netlify/open-api/releases/latest)

```console
$ go get github.com/netlify/open-api/...
```

- [Porcelain](https://godoc.org/github.com/netlify/open-api/go/porcelain): High level interactions and operations
- [Plumbing](https://godoc.org/github.com/netlify/open-api/go/plumbing): Low level client operations
- [Models](https://godoc.org/github.com/netlify/open-api/go/porcelain): Models generated by [go-swagger]()

See [CONTRIBUTING.md#go-client](CONTRIBUTING.md) for details on how this client is developed and generated.

### npm module

[![npm version][2]][3]

You can also consume the swagger spec as an npm module:

```console
$ npm install @netlify/open-api
# or
$ yarn add @netlify/open-api
```

```js
import spec from '@netlify/open-api' // import the spec object into your project
```

The module also ships a copy of the original `yml` spec file at `@netlify/open-api/js/dist/swagger.yml`.  You can use these with generic swagger/open-api clients:

#### swagger-js

Swagger's JS client can dynamically create a client from a spec either from a URL or spec object.

See [swagger-js](https://github.com/swagger-api/swagger-js)


##### Usage
```js
<script src='browser/swagger-client.js' type='text/javascript'></script>
<script>
var swaggerClient = new SwaggerClient('https://open-api.netlify.com/swagger.json');
</script>
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for more info on how to make contributions to this project.

## License

MIT. See [LICENSE](LICENSE) for more details.

[2]: https://img.shields.io/npm/v/@netlify/open-api.svg
[3]: https://npmjs.org/package/@netlify/open-api
