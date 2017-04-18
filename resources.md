# Resources
## `GET /api/resources/:id/availability`
Appointment times available to make appointments with the specified resource.
Required query parameters
1. `at` appointment template id. The id of the appointment template that will describe the appointmen to be created. The appointment tempate contains the Resource to make the appointment with as well as the duration in min required from the resource to make the appointment.
1. `utcOffset` offset of the time zone from utc to return available times. Specified in minutes. e.g. australia/brisbane is 600.
1. `start` date to start looking for available times.
1. `end` date to end looking for available times.
