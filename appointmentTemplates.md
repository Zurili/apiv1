# Appointment Templates
## `GET /api/appointmentTemplates`
Retrive a list of Appointment Templates (ATs).

## `GET /api/appointmentTemplates/:id`
Retrive full details of an individual Appointment Template.
Typical response:
```
{
  "_id": "5787458caeb87364570cd288",
  "name": "Standard Appointment",
  "description": "Full spine adjustment",
  "bookingScript": "Message for client to read after online booking",
  "script": "Booking script / notes for receptionist / concierge",
  "automations": [],
  "availability": [
    "existing client",
    "concierge"
  ],
  "hideFromClient": false,
  "duration": 15,
  "textColor": "black",
  "color": "#39cccc",
  "resources": [
    "57888804b5dded0814d52b2a"
  ]
}
```
`availability` can contain `['existing client', 'new client', 'concierge']`. For a client with no previous appointment, use an AT with 'new client' availability etc.
