# Resources
## `GET /api/resources/:id/availability`
Appointment times available to make appointments with the specified resource.

Required query parameters:
1. `at` appointment template id. The id of the appointment template that will describe the appointmen to be created. The appointment tempate contains the Resource to make the appointment with as well as the duration in min required from the resource to make the appointment.
1. `utcOffset` offset of the time zone from utc to return available times. Specified in minutes. e.g. australia/brisbane is 600.

Optional query parameters:
1. `start` date to start looking for available times. Defaults to today.
1. `end` date to end looking for available times. Defaults to today + 7d

### response
Typical reponse:
[
  "2017-04-18T03:00:00.000Z",
  "2017-04-18T03:45:00.000Z",
  "2017-04-18T04:30:00.000Z",
  "2017-04-19T03:00:00.000Z",
  "2017-04-19T03:45:00.000Z",
  "2017-04-19T04:30:00.000Z",
  "2017-04-20T03:00:00.000Z",
  "2017-04-20T03:45:00.000Z",
  "2017-04-20T04:30:00.000Z",
  "2017-04-21T03:00:00.000Z",
  "2017-04-21T03:45:00.000Z",
  "2017-04-21T04:30:00.000Z"
]

All times in UTC
