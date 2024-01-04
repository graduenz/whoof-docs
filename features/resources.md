# Resources

The resources that are part of the Web API can be created, modified and read through HTTP requests.

Every resource has an `id` field.

```json
{
  "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
}
```

## Pets

Pets are the main resource. They are only yours, and as a user, you can't see other users' pets.

```json
{
  "name": "Scooby-Doo",
  "petType": "Dog"
}
```

## Vaccines

Vaccines are visible by all users, but created and modified by administrators. A vaccine is exclusive for a specific pet type.

> Though they should be managed by administrators, every user can create and modify them as well, for experimental purposes.

```json
{
  "name": "Acme",
  "description": "Acme is a vaccine that prevents dogs from walking over water",
  "petType": "Dog",
  "duration": 365
}
```

## Pet Vaccination

Pet vaccination are entries representing a given moment that a vaccine was applied to a pet. It references a pet, a vaccine and has a _timestamp with timezone_ field.

```json
{
  "petId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "vaccineId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "appliedAt": "2023-09-04T02:00:00.000Z"
}
```
