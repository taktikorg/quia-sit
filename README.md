# @taktikorg/quia-sit

[![Downloads][downloads-badge]][downloads]
[![Size][size-badge]][size]

Web socket API support for yaschema.

## Basic Example

```typescript
export const stream = makeWsApi({
  routeType: 'stream',
  url: '/stream',
  requests: {
    ping: schema.object({ echo: schema.string().allowEmptyString().optional() }).optional(),
    hello: schema.any().optional()
  },
  responses: {
    pong: schema.object({
      body: schema.string()
    }),
    hello: schema.object({
      body: schema.string()
    })
  }
});
```

## Thanks

Thanks for checking it out.  Feel free to create issues or otherwise provide feedback.

[API Docs](https://typescript-oss.github.io/@taktikorg/quia-sit/)

Be sure to check out our other [TypeScript OSS](https://github.com/TypeScript-OSS) projects as well.

<!-- Definitions -->

[downloads-badge]: https://img.shields.io/npm/dm/@taktikorg/quia-sit.svg

[downloads]: https://www.npmjs.com/package/@taktikorg/quia-sit

[size-badge]: https://img.shields.io/bundlephobia/minzip/@taktikorg/quia-sit.svg

[size]: https://bundlephobia.com/result?p=@taktikorg/quia-sit
