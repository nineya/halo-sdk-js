<h3 align="center">Content API Client</h3>

<p align="center">
  <a href="https://www.npmjs.com/package/@nineya/halo-content-api">
    <img src="https://img.shields.io/npm/v/@nineya/halo-content-api.svg" alt="npm version"/>
  </a>
  <a href="https://www.npmjs.com/package/@nineya/halo-content-api">
      <img alt="npm" src="https://img.shields.io/npm/dm/@nineya/halo-content-api" alt="Downloads"/>
  </a>
  <a href="https://github.com/nineya/halo-sdk-js/blob/master/packages/content-api/package.json">
      <img alt="node-current" src="https://img.shields.io/node/v/@nineya/halo-content-api?color=blue">
  </a>
  <a href="https://github.com/nineya/halo-sdk-js/blob/master/LICENSE">
    <img alt="NPM" src="https://img.shields.io/npm/l/@nineya/halo-content-api" alt="LICENSE">
  </a>
</p>

<p>JavaScript SDK for Halo's Content API,implemented with TypeScript,encapsulating parameter types and return value types to make the use of API more brief.</p>

## Installation

```shell
npm install @nineya/halo-content-api --save
```

## Usage

Here is a simple code for obtaining a list of posts.

```javascript
import { ContentApiClient, HaloRestAPIClient } from '@nineya/halo-content-api'

// http request tool for halo rest api.
const haloRestApiClient = new HaloRestAPIClient({
  baseUrl: process.env.HALO_BASE_URL,
  auth: { apiToken: process.env.HALO_API_TOKEN },
})

// create contentApiClient by haloRestApiCLient.
const haloContentClient = new ContentApiClient(haloRestApiClient)

// obtaining a list of articles.
haloContentClient.post.list().then((res) => {
  console.log(res)
})
```

### License

[MIT license](../../LICENSE)
