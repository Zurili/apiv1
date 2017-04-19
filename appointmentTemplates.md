# Appointment Templates
## `GET /api/appointmentTemplates`
Retrive a list of Appointment Templates (ATs).

## `GET /api/appointmentTemplates/:id`
Retrive full details of an individual Appointment Template.
Typical response:
```
{
    "_id": "57888dd8b5dded0814d5482a",
    "name": "Comparative Exam",
    "automations": [],
    "availability": [
      "existing client",
      "concierge"
    ],
    "hideFromClient": false,
    "duration": 10,
    "textColor": "black",
    "color": "#dbe80b",
    "resources": [
      "57888804b5dded0814d52b2a"
    ]
}
```
`availability` can contain `['existing client', 'new client', 'concierge']`. For a client with no previous appointment, use an AT with 'new client' availability etc.
