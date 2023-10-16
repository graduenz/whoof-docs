# Authentication

Authentication and authorization are handled by Auth0.

## Authenticate requests

You will have to include a Bearer token in the requests in order to authenticate them.

```
Authorization: Bearer <token>
```

## Client applications

Every client application developed for the Whoof API will have its application set up in Auth0, and they should use their libraries in order to help develop the authentication features.

Let's use a React application as an example that makes requests to the back-end using Axios. The React SDK can be used to authenticate the user and to get the JWT, then the token can be used in the requests made with Axios.
