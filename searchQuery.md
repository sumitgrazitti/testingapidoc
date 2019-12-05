# Analytics API
Export analytics data to a platform of your choice.

## Endpoints
All the Analytics API endpoints are listed here.
### GET searchQuery/all
Prints a list of the ```count``` most popular searches. For ```count=5```, you will get 5 results. The data is from between ```startDate``` and ```endDate``` on a search client whose ID is ```searchClientID```. If the ```searchClientID``` is not specified, then the call fetches data from all the search clients.

```console
GET searchQuery/all
```

#### Parameters

Parameter | Type | Format | Essential 
--- | --- | --- | --- 
```startDate``` | YYYY-DD-MM | string | Yes
```endDate``` | YYYY-DD-MM | string | Yes
```count``` | Decimal literals | string | Yes
```searchClientId``` | abcdefgh-ijkl-mnop-qrst-uvwzyzABCDEF | string | No


#### Example Request

```http
curl -X GET 'https://mycompany.searchunify.com/api/v2/searchQuery/all? \
  startDate=2019-05-01&endDate=2019-05-05&count=3&searchClientId=fa1c40fe-5664-11e9-9905-f23c91e2022e' \ 
  -H 'Content-Type: application/json' \
  -H "authorization: Bearer 0d763196b4873064e348570c01cbd0a02f370935"
 ```

#### Example Response

```json
[
	{
		"value": "install searchunify",
		"count": 5
	},
	{
		"value": "servicenow content source",
		"count": 4
	},
	{
		"value": "servicenow",
		"count": 3
	}
]					
```
