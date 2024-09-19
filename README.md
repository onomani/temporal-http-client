# Temporal HTTP Client

**Nota bene**: This is currently experimental.

Provides a typesafe API client for [Temporal](https://temporal.io)'s HTTP API. This is primarily intended for use in [Temporal's UI](https://github.com/temporalio/ui).

## Updating the Schema

`pnpm generate`

This will download [Temporal's API repository](https://github.com/temporalio/api), generate types based on the OpenAPI specification, and write the types to `src/schema.d.ts`.

It will also create a set of client methods in `src/client.ts`.

## Usage

```ts
import { getClusterInfo } from 'temporal-http-client';

const client = new Client({ baseUrl: 'http://localhost:8233' });

const response = await getClusterInfo();

console.log(response);
```
