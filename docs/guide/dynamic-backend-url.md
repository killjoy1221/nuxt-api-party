# Dynamic Backend URL

If you need to change the backend URL at runtime, you can do so by using a custom header based on the endpoint name. This is useful for example when you have a multi-tenant application where each tenant has its own backend URL.

## Example

::: info
The examples below assume that you have set up an API endpoint called `jsonPlaceholder`. In this case you can use the `Json-Placeholder-Endpoint-Url` header to change the backend URL at runtime.
:::

```ts
const { data } = await useJsonPlaceholderData(
  'comments',
  {
    headers: {
      'Json-Placeholder-Endpoint-Url': 'https://jsonplaceholder-v2.typicode.com'
    }
  }
)
```