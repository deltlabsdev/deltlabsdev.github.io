

GET https://lrs.deltlabs.com/xapi/statements
Content-Type: application/json
Authorization: Basic f25736a648caf22e63be9e85ceb246b33e5e01d02136a168dcbf1212a1325e79:3b26c7fd24f3d75e14a2748a09e44e2d694f544ba7e9c5cbf4c9264ffde56673
X-Experience-API-Version: 1.0



![ <alt-text> ]( ../../../images/lrscreds.png )


```json
POST https://localhost:8443/xapi/statements
Content-Type: application/json
Authorization: Basic a32df9c62066cf8ebdac9dcf63c5b8e26d45840a8e11e6d21bdb4a557359e6e7:635ef6d70b6149e435dbe2810d7f0cc4093abc1e765149e13e670f92e359c6c1
X-Experience-API-Version: 1.0

 {
  "actor": {
    "account": {
      "homePage": "https://mylearnertoken.com",
      "name": "unidentified"
    }
  },
  "verb": {
    "id": "http://adlnet.gov/expapi/verbs/registered",
    "display": {
      "en-US": "registered"
    }
  },
  "object": {
    "id": "http://mylearnertoken.com/xapi/activities/clTG0ZBh6fh",
    "definition": {
      "name": {
        "en": "Test"
      },
      "description": {
        "en": "Test"
      },
      "extensions": {
        "https://mylearnertoken.com/xapi/mylearnertoken/extensions/url": "https://activities.deltlabs.com/79221cb7-0961-4ef4-9f0c-085b50cd624d"
      }
    },
    "objectType": "Activity"
  },
  "context": {
    "extensions": {
      "https://mylearnertoken.com/xapi/mylearnertoken/extensions/type": "LwvRmqfEDmz",
      "https://mylearnertoken.com/xapi/mylearnertoken/extensions/version": "1.0",
      "https://mylearnertoken.com/xapi/mylearnertoken/extensions/culture": "en-US",
      "https://mylearnertoken.com/xapi/mylearnertoken/extensions/description": "Test",
      "https://mylearnertoken.com/xapi/mylearnertoken/extensions/url": "https://activities.deltlabs.com/79221cb7-0961-4ef4-9f0c-085b50cd624d"
    }
  },
  "timestamp": "2024-01-26T11:12:27.3210939+01:00"
}

```




