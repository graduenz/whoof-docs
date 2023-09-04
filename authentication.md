# Authentication

Authentication and authorization is handled by Auth0.

## Authenticate requests

You will have to inform a Bearer token in the requests in order to authenticate them.

```
Authorization: Bearer <token>
```

## Client applications

Every client application developed for the Whoof API will have its application set up in Auth0, and should use their libraries in order to help develop the authentication features.

Let's use a React application as an example, that does requests to back end using Axios. The React SDK can be used to authenticate the user and to get the JWT, then the token can be used in the requests made with Axios.
