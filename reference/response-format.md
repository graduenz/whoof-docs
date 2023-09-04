# Response Format

Response formats are well standardized in the back end. Though everything is covered in the [openapi-specification.md](../openapi-specification.md "mention") page, this page can help you to create some common artifacts in the front end as well (in case the front end is a React application, for example).

## Errors

Every error that happens in the system should return a `ServiceError`. To know what happened, check the combination of the HTTP Status Code (let's say 404) and the following body:

```json
{
  "code": 995,
  "message": "The specified resource was not found."
}
```

For a list of all mapped errors, check [errors-reference.md](errors-reference.md "mention").

## Paginated lists

Paginated lists are the result of requests that have the intention of fetching records. They have the following body:

```json
{
  "items": [
    <list of records>
  ],
  "pageIndex": 1,
  "pageSize": 20,
  "totalPages": 7,
  "totalCount": 123,
  "hasPreviousPage": false,
  "hasNextPage": true
}
```

## Other requests

### Regular resource requests

The regular CRUD requests include the ones for getting, creating, modifying, and deleting a record:

* `GET/{id}`
* `POST /`
* `PUT /{id}`
* `DELETE /{id}`

They will return the record itself. Let's say a pet, the body will be (as long as it's successful):

```json
{
  "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "createdAt": "2023-09-04T11:50:06.701Z",
  "createdBy": "john@doe.com",
  "modifiedAt": "2023-09-04T11:50:06.701Z",
  "modifiedBy": "john@doe.com",
  "ownerId": "john@doe.com",
  "name": "Scooby-Doo",
  "petType": "Dog"
}
```

* It has the same properties as defined in [resources.md](../features/resources.md "mention").
* Plus, some audit fields are included:
  * Creation and modification users.
  * Creation and modification dates.
  * Pet's owner.

### Other requests

For other requests that are not the regular CRUD ones, you must check them on [openapi-specification.md](../openapi-specification.md "mention").
