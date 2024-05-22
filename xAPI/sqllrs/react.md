# SQLLRS React

SQLLRS Version 0.7+ supports Reactions.

Tipp:

> [!TIP]
> Reactions will only be shown in the menu if the enableReactions parameter is set to true.

```json
{
  "lrs" : {
    "adminUserDefault": "",
    "adminPassDefault": "",
    "enableReactions": true
  },
  "webserver":   
}
```

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
  "object": {
    "id": "http://mylearnertoken.com/xapi/activities/cc1"
  },
  "verb": {
    "id": "https://adlnet.gov/expapi/verbs/completed"
  }
}
```

```json
[
  "f65543b8-3ae0-4a2e-bd22-88eb9e6b4c85"
]
```

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
  "object": {
    "id": "http://mylearnertoken.com/xapi/activities/cc2"
  },
  "verb": {
    "id": "https://adlnet.gov/expapi/verbs/completed"
  }
}
```

```json
[
  "1ffe3344-43d0-4669-8f90-ade9144fa38c"
]
```




/xapi/statements?unwrap_html=true&statementId=1525f6c9-0998-4869-9ad8-6082a428f74e


/xapi/statements?unwrap_html=true&activity=https%3A//www.yetanalytics.com/xapi/activities/example_activity&related_activities=true






























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




