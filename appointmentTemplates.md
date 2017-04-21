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
  "productIds": [
    1,
    2
  ],
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

`products` is the default products or services that will be billed for appointments based on this template

You can also get entended versions of products and/or resources by adding parameter `includes[]` like this:
`/api/appointmentTemplates/:id?includes[]=resources&includes[]=products`

You'll get something like this:
```
{
  "_id": "56cd21c444c4e62824cefddb",
  "name": "Initial Consult",
  "script": "Booking script / notes for receptionist / concierge,
  "automations": [],
  "availability": [
    "concierge",
    "new client"
  ],
  "hideFromClient": false,
  "duration": 40,
  "textColor": "black",
  "color": "rgb(102, 198, 131)",
  "resources": [
    {
      "_id": "56a1d4dff2ff141025e2a1dd",
      "name": "Shane"
    }
  ],
  "products": [
    {
      "id": 1,
      "name": "Initial Consult",
      "type": "service",
      "priceExTax": 12000,
      "priceIncTax": 12000,
      "taxes": []
    },
    {
      "id": 2,
      "name": "Adjustment",
      "type": "service",
      "priceExTax": 7000,
      "priceIncTax": 7000,
      "taxes": []
    }
  ]
}
```
