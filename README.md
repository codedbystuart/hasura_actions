# Hasura Actions

This is a demonstration of Hasura actions Development

```
npm ci
npm start
```

## Development

The entrypoint for the server lives in `src/server.js`.

If you wish to add a new route (say `/greet`) , you can add it directly in the `server.js` as:

```js
app.post('/greet', (req, res) => {
  return res.json({
    "greeting": "have a nice day"
  });
});
```

### Throwing erros

You can throw an error object or a list of error objects from your handler. The response must be 4xx and the error object must have a string field called `message`.

```js
retun res.status(400).json({
  message: 'invalid email'
});
```
