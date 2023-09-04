# Resources

The resources present in the Web API can be created, modified and read through HTTP requests.&#x20;

Every resource has an `id` field.

```json
{
  "id": "3fa85f64-5717-4562-b3fc-2c963f66afa6"
}
```

## Pets

Pets are the main resource of the application. They are only yours, and you can't see other users' pets.

```json
{
  "name": "Scooby-Doo",
  "petType": "Dog"
}
```

## Vaccine

Vaccines are also part of the core of the application. They are all public, created and modified by administrators, and can be read by all users in order to register their pets' vaccination. A vaccine entry is exclusive for a specific pet type.

```json
{
  "name": "Acme",
  "description": "Acme is a vaccine that prevents dogs from walking over water",
  "petType": "Dog",
  "duration": 365
}
```

## Pet Vaccination

Pet vaccination are entries of a given moment that a vaccine was applied to a pet. It references a pet, a vaccine and has a _timestamp with timezone_ field.

```json
{
  "petId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "vaccineId": "3fa85f64-5717-4562-b3fc-2c963f66afa6",
  "appliedAt": "2023-09-04T02:00:00.000Z"
}
```
