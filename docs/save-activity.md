# Save Activities

Add your activity.

## API Call


````
POST https://localhost:7121/api/lrd/saveActivity/context
Content-Type: application/json
Authorization: Bearer {{accessToken}}
X-API-KEY: aaa

{ 
  "title": "Context Test Saturday",                        
  "summary": "This is a summary.",                            
  "description": "<p>Description...</p>",                            
  "begin":"2024-07-15T00:00:00+02:00",
  "end":"2024-07-15T00:01:00+02:00",
  "recording": false,  
  "url":"https://deltlabs.com/csssontext2"
} 
````

````
{
  "uri": "https://activities.mylearnerdata.com/1/KFlYV6m07mh",
  "id": "KFlYV6m07mh",
  "track": "https://localhost:7121/track/KFlYV6m07mh",
  "title": "Context Test Saturday",
  "type": "context"
}
````



