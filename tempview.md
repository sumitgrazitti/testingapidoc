# GET searchSession/bySearchSessionId/15306139130638560
Returns a log of user activity in a session. The log includes six kinds of information: Viewed Page, Text Searched, Clicked Search Results, Created a Case, Visited Support, and Case Deflection.

## Parameters
| Parameter | Optional / Required | Description | Data Type | 
|--- | --- | --- | --- |
| `searchSessionId` | Required | Found in Search Analytics > Conversions > Session Tracking - Details. | string | 
| `startDate` | Required | ??? | string |
| `endDate` | Required | ??? | string |
| `count` | Required | ??? | integer | 
| `searchClientId` | Required | ??? | string |


## Example Request

```curl
curl -X GET 'https://grazitti.searchunify.com/dev/api/v2/searchSession/bySearchSessionId/15306139130638560? \
startDate=2019-11-01&endDate=2019-12-09&count=5&searchClientId=3a70b1f3-06c3-11ea-9de0-ea4d55341fa1' \
-H 'Content-Type: application/json' \
-H "authorization: Bearer edd7c247cba8c429e802eb83de3cfe10da73d26f"
```

## Example Response

```json
[
  {
    "sessionId": "15306139130638560",
    "logs": [
      {
        "query": "lithium",
        "count": 7,
        "conversions": []
      },
      {
        "query": "customize search client",
        "count": 3,
        "conversions": []
      },
      {
        "query": "search unify",
        "count": 3,
        "conversions": []
      },
      {
        "query": "console",
        "count": 2,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Addons/KCS-Support-Console.htm",
            "count": 1
          },
          {
            "doc": "https://docs.searchunify.com/Content/Search-Clients/Salesforce-Console-Chatter-Feed.htm",
            "count": 1
          },
          {
            "doc": "https://docs.searchunify.com/Content/Search-Clients/Salesforce-Console.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "bharat",
        "count": 1,
        "conversions": []
      },
      {
        "query": "chatter",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Search-Clients/Salesforce-Console.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "console features",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Release-Notes/Release-Notes.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "customize",
        "count": 1,
        "conversions": []
      },
      {
        "query": "end us",
        "count": 1,
        "conversions": []
      },
      {
        "query": "end users",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Features-for-End-Users/Hide-Facet-Categories.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "facet preference",
        "count": 1,
        "conversions": []
      },
      {
        "query": "facet preferences",
        "count": 1,
        "conversions": []
      },
      {
        "query": "features for end users",
        "count": 1,
        "conversions": []
      },
      {
        "query": "kcs",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Addons/KCS-Support-Console.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "mamba '20 release notes",
        "count": 1,
        "conversions": []
      },
      {
        "query": "merge facets",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Search-Clients/Merge-Facets.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "next best actions",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Release-Notes/Release-Notes.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "nlp manager",
        "count": 1,
        "conversions": []
      },
      {
        "query": "page rating",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Search-Clients/Page-Rating.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "search client",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Search-Clients/Slack.htm",
            "count": 1
          }
        ]
      },
      {
        "query": "search tuning",
        "count": 1,
        "conversions": [
          {
            "doc": "https://docs.searchunify.com/Content/Search-Tuning/Search-Tuning.htm",
            "count": 1
          }
        ]
      }
    ]
  }
]
```
