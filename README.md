# api v1
public api for integration with Zurili

## Auth
Authentication is by using a bearer token in the auth header:
`Authorization bearer: myapitoken`
Create your api token by
1. creating an account in Zurili: https://app.zurili.com/signup
1. creating an api key at: https://app.zurili.com/settings/api

## APIs
1. [Resources](resources.md) - the entities with which appointments can be made
1. [Appointment Templates](appointmentTemplates.md) - template used to create or update an appointment. Not required to make an appointment but recommended.
