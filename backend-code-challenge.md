# Backend Code Challenge

Design a REST API endpoint that provides auto-complete suggestions from a list of contacts.

## Overview

* The endpoint is exposed at /suggestions
* The partial (or complete) search team is passed as a query string parameter ‘q’
* The contact can optionally be filtered by query string parameters ‘min_rate’ and ‘verified_skills’
* The endpoint returns a JSON response with an array of scored suggested matches
	* The suggestions are sorted by descending score
	* Each suggestion has a score between 0 and 1 (inclusive) indicating confidence in the suggestion (1 is most confident)
	* Each suggestion has a name which can be used to disambiguate between similarly named contacts
	* Each suggestion has a contact email address

## Requirements

* You can use the language and technology of your choosing. Feel free to use something you’re comfortable with.
* End result should be deployed on a public cloud (there are free tiers available).

## Sample Responses 

`GET /suggestions?q=Bran&rate_minimum=75&verified_skills=facebook_advertising`

```json
[
  {
    "_id": "5e2f3a706185a65d93c1e4cd",
    "index": 0,
    "guid": "a421d5c8-9da1-4dfa-99be-683d351e0021",
    "min_rate": "$268.45",
    "age": 31,
    "eyeColor": "green",
    "first_name": "Juliana",
    "last_name": "Dunn",
    "contact_email": "julianadunn@codax.com",
    "verified_skills": [
      "commodo",
      "officia",
      "do",
      "consectetur",
      "laboris",
      "ullamco",
      "cillum"
    ],
    "score": 0.6729
  },
  {
    "_id": "5e2f3a7074e54b91e8a5d2dc",
    "index": 1,
    "guid": "818e21ed-309c-4260-a0d0-f1045a667d39",
    "min_rate": "$179.85",
    "age": 35,
    "eyeColor": "blue",
    "first_name": "Lenora",
    "last_name": "Delacruz",
    "contact_email": "lenoradelacruz@codax.com",
    "verified_skills": [
      "irure",
      "dolore",
      "anim",
      "deserunt",
      "esse",
      "voluptate",
      "magna"
    ],
    "score": 0.6677
  },
  {
    "_id": "5e2f3a70861b24f261e97530",
    "index": 2,
    "guid": "60a601b6-ff75-4e62-9f2f-88fff91d31dc",
    "min_rate": "$288.50",
    "age": 22,
    "eyeColor": "green",
    "first_name": "Elsa",
    "last_name": "Ruiz",
    "contact_email": "elsaruiz@codax.com",
    "verified_skills": [
      "pariatur",
      "officia",
      "occaecat",
      "officia",
      "consectetur",
      "deserunt",
      "ullamco"
    ],
    "score": 0.3374
  }
]
```







