# api v1
public api for integration with Zurili

## Auth
Authentication is by using a bearer token in the auth header:
`Authorization bearer: jwt`

Create your jwt by
1. Create an account in Zurili: https://app.zurili.com/signup
1. Create an api key at: https://app.zurili.com/settings/api
1. Login using the api key to get a jwt: `POST /login apiKey=[your-api-key]`. You will get a jwt which is valid for 14 days. Typical response:
```
{
  "jwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOnsiX2lkIjoiNTczYWNmMjNjZDkyYzA0MDBiZWEwNjMzIiwiZW1haWwiOiJtZXpnZXJsb2NhbEA1NmExY2NjZjAxYTlhMmRjMWIyNGQzOGYuY29tIiwiZGlzcGxheU5hbWUiOiJtZXpnZXJMb2NhbCIsInJvbGVzIjpbImFwaSJdLCJjdXJyZW50U2l0ZSI6IjU2YTFjY2NmMDFhOWEyZGMxYjI0ZDM4ZiJ9LCJpYXQiOjE0OTI2Njg5MDIsImV4cCI6MTQ5Mzg3ODUwMn0.Nqm65y2k353HCgBfuKaE1mI2zpaI8FlD93n9B3JaaG8",
  "user": {
    "_id": "573acf23cd92c0400bea0633",
    "displayName": "My Practice",
    "verified": "2016-05-17T07:58:27.419Z",
    "roles": [
      "api"
    ],
    "activeRole": "api",
    "currentSite": "56a1cccf01a9a2dc1b24d38f",
    "jwtExpiry": "2017-05-04T06:15:02.568Z"
  }
}
```
4. Use the jwt in the Authorization header like `Authorization bearer: jwt`

## Value formatting

Dates formatted as ISO 8601 string.

Prices and ledger amounts are integers which represent the cent value.

## APIs
1. [Resources](resources.md) - the entities with which appointments can be made
1. [Appointment Templates](appointmentTemplates.md) - template used to create or update an appointment. Not required to make an appointment but recommended.
