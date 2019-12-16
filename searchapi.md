## POST /searchResults
View search results on a platform of your choice.

### Parameters
| Parameter | Optional / Required | Description | Data Type | 
|--- | --- | --- | --- |
| `uid` | Required | It your search client ID. You can find it in Search Clients > UID (column). | string |
| `searchString` | Required | Your search query. | string |
| `email` | Optional | What does it do? | string |
| `orderBy` | Optional | What does it do? | string | 
| `sortby` | Optional | It can have two values, `_score` or `_post_time`. When `sortby=_score`, then the documents with the highest score are presented first. When `sortby=_post_time`, then the lastest documents are on top. | string |
| `exactPhrase` | Optional | Treats all the words in the search query as one contiguous string. `exactPhrase=salesforce console` becomes "salesforce console". | string |
| `withOneOrMore` | Optional | Inserts the Boolean operator OR between each keyword. `withOneOrMore=salesforce console` becomes "salesforce OR console". | string | 
| `withoutTheWords` | Optional | Inserts the Boolean operator NOT after each keyword. `withoutTheWords=salesforce console` becomes "NOT salesforce NOT console" | string |
| `from` | Optional | It's an offset. If `from="10"`, then the call will fetch results starting from 11. | string |
| `resultsPerPage` | Optional | If `resultsPerPage=30`, then each search will produce 30 results on each page. | string |
| `indexEnabled` | Optional | What does it do? | boolean | 
| `aggregations` | Optional | You can use `aggregations` to refine your search with facets. For example: `type: ${facet name}, filter: [ ${facet filter name1}, ${facet filter name2} ]`. A common pattern for nested facets is `[{type: ${facet name},children: [ childname: ${facet child name1}, level: ${facet level} ]}]` | object |
| `pagingAggregation` | Optional | What does it do? `{key: ${facet name},keyword: ${facet search keyword},offset: ${number of filters to shown}}` | object | 

#### Salesforce-Specific Parameters
| Parameter | Optional / Required | Description | Data Type | 
|--- | --- | --- | --- |
| `UserId` | Optional | Your user ID. | string | 
| `UserType` | Optional | Your user type. For example, Standard, Admin, and Developer. | string | 
| `AccountId` | Optional | Your Salesforce ID. | string | 
| `ProfileId` | Optional | Your profile ID in your org. | string | 
| `ContactId` | Optional | Your contact ID. | string | 

#### Lithium-Specific Parameters
| Parameter | Optional / Required | Description | Data Type | 
|--- | --- | --- | --- |
| `boardsArr` | Optional | What does it do? | string

### Example Request
```curl
curl -X POST 'https://mycompany.searchunify.com/api/v2_search/searchResults' \
	-H 'Content-Type: application/json' \
	-H "authorization: Bearer 9c9675626daf5f928e0bd307a518be32b15776e0" \
	--data-binary $'{\n"uid":"3a70b1f3-06c3-11ea-9de0-ea4d55341fa1", \n"searchString":"salesforce console", \n"from": "20", "sortby"="_post_time"\n}'
```
### Example Response
```json
{
    "result": {
        "total": 266,
        "max_score": null,
        "hits": [
            {
                "_id": "335352487",
                "_score": 0.20343336,
                "highlight": {
                    "SummaryToDisplay": [
                        "  335352487...."
                    ],
                    "TitleToDisplay": [
                        "test issue for a crawler"
                    ],
                    "TitleToDisplayString": [
                        "test issue for a crawler"
                    ],
                    "AttachmentToDisplay": [],
                    "Id": [
                        335352487
                    ],
                    "Created Date": [
                        "6/25/2018 4:11 PM"
                    ]
                },
                "metadata": [
                    {
                        "key": "Id",
                        "value": [
                            335352487
                        ]
                    },
                    {
                        "key": "Created Date",
                        "value": [
                            "6/25/2018 4:11 PM"
                        ]
                    }
                ],
                "href": "335352487",
                "client_href": "ddf",
                "Id": 335352487,
                "objName": "issues",
                "solved": "Unsolved",
                "sourceName": "github2",
                "author": "",
                "authorHref": "",
                "boardName": "",
                "boardHref": ""
            },
            {
                "_id": "18524",
                "_score": 0.034366135,
                "highlight": {
                    "SummaryToDisplay": [
                        "You can submit Support using report below. \n  ...."
                    ],
                    "TitleToDisplay": [
                        "How to Submit A Bug Report"
                    ],
                    "TitleToDisplayString": [
                        "How to Submit A Bug Report"
                    ],
                    "AttachmentToDisplay": []
                },
                "metadata": [],
                "href": "18524",
                "client_href": "ddf",
                "Id": 18524,
                "objName": "forum",
                "solved": "Unsolved",
                "sourceName": "lithium",
                "author": "vu_phan",
                "authorHref": "https://community.com/t5/user/user-id/20",
                "boardName": "Welcome Board",
                "boardHref": "https://community.com/t5/Welcome-Board/bd-p"
            },
            {
                "_id": "4258",
                "_score": 0.034366135,
                "highlight": {
                    "SummaryToDisplay": [
                        "As you engage more which gi  ...."
                    ],
                    "TitleToDisplay": [
                        "Community Rank Rewards"
                    ],
                    "TitleToDisplayString": [
                        "Community Rank Rewards"
                    ],
                    "AttachmentToDisplay": []
                },
                "metadata": [],
                "href": "4258",
                "client_href": "ddf",
                "Id": 4258,
                "objName": "forum",
                "solved": "Unsolved",
                "sourceName": "lithium",
                "author": "Support",
                "authorHref": "https://community.com/t5/user/user-id/6",
                "boardName": "Welcome Board",
                "boardHref": "https://community.com/t5/Welcome-Board/bd-p"
            },
            {
                "_id": "20857",
                "_score": 0.03433732,
                "highlight": {
                    "SummaryToDisplay": [
                        " \n \nCommunity Solutions Articles are written ...."
                    ],
                    "TitleToDisplay": [
                        "What is a Customer Solutions Article?"
                    ],
                    "TitleToDisplayString": [
                        "What is a Customer Solutions Article?"
                    ],
                    "AttachmentToDisplay": []
                },
                "metadata": [],
                "href": "20857",
                "client_href": "ddf",
                "Id": 20857,
                "objName": "forum",
                "solved": "Unsolved",
                "sourceName": "lithium",
                "author": "Lana",
                "authorHref": "https://community..com/t5/user/user-id/4",
                "boardName": "Welcome Board",
                "boardHref": "https://community.com/t5/Welcome-Board/bd-p"
            },
            {
                "_id": "110",
                "_score": 0.034135293,
                "highlight": {
                    "SummaryToDisplay": [
                        "The Community is an online platform that  ...."
                    ],
                    "TitleToDisplay": [
                        "Terms of Use"
                    ],
                    "TitleToDisplayString": [
                        "Terms of Use"
                    ],
                    "AttachmentToDisplay": []
                },
                "metadata": [],
                "href": "110",
                "client_href": "ddf",
                "Id": 110,
                "objName": "forum",
                "solved": "Unsolved",
                "sourceName": "lithium",
                "author": "Support",
                "authorHref": "https://community..com/t5/user/user-id/6",
                "boardName": "Welcome Board",
                "boardHref": "https://community..com/t5/bd-p/welcome"
            },
   "aggregationsArray": [
        {
            "order": 0,
            "key": "_index",
            "values": [
                {
                    "displayName": "lithium",
                    "Contentname": "lithium",
                    "value": 265,
                    "sort_order": null
                },
                {
                    "displayName": "github2",
                    "Contentname": "github2",
                    "value": 1,
                    "sort_order": null
                }
            ],
            "label": "Index"
        },
        {
            "order": 1,
            "key": "_type",
            "values": [
                {
                    "displayName": "Discussion",
                    "Contentname": "forum",
                    "value": 265
                },
                {
                    "displayName": "Issue",
                    "Contentname": "issues",
                    "value": 1
                }
            ],
            "label": "Sources"
        },
        {
            "key": "assignee",
            "values": [],
            "order": 2,
            "label": "Assignee"
        },
        {
            "key": "labels_nested",
            "values": [],
            "order": 3,
            "label": "Label"
        },
        {
            "key": "viewCount",
            "values": [
                {
                    "Contentname": "1131",
                    "value": 3,
                    "childName": "Views_1",
                    "level": 1
               },
                {
                    "Contentname": "580",
                    "value": 3,
                    "childName": "Views_1",
                    "level": 1
                },
                {
                    "Contentname": "593",
                    "value": 3,
                    "childName": "Views_1",
                    "level": 1
                },
                {
                    "Contentname": "613",
                    "value": 3,
                    "childName": "Views_1",
                    "level": 1
                },
                {
                    "Contentname": "539",
                    "value": 2,
                    "childName": "Views_1",
                    "level": 1
                }
            ],
            "order": 4,
            "label": "Views"
        },
                {
            "key": "rootCategoryName",
            "values": [],
            "order": 7,
            "label": "Root Category"
        },
        {
            "key": "metadata",
            "values": [],
            "order": 8,
            "label": "Metadata"
        },
        {
            "key": "label",
            "values": [],
            "order": 9,
            "label": "Label"
        },
        {
            "key": "post_time",
            "label": "Created Date",
            "order": 10,
            "values": [
                {
                    "Contentname": "All Time",
                    "value": 266
                },
                {
                    "Contentname": "Past Day",
                    "value": 0
                },
                {
                    "Contentname": "Past Week",
                    "value": 0
                },
                {
                    "Contentname": "Past Month",
                    "value": 0
                },
                {
                    "Contentname": "Past Year",
                    "value": 48
                }
            ]
        },
        {
            "key": "author",
            "values": [
                 {
                    "Contentname": "Rolando",
                    "value": 19,
                    "childName": "Author_1",
                    "level": 1
                },
                {
                    "Contentname": "Robert",
                    "value": 12,
                    "childName": "Author_1",
                    "level": 1
                },
                {
                    "Contentname": "Jyoti_Sinha",
                    "value": 11,
                    "childName": "Author_1",
                    "level": 1
                },
                {
                    "Contentname": "irachamreddy",
                    "value": 10,
                    "childName": "Author_1",
                    "level": 1
                },
                {
                    "Contentname": "Daniel_L",
                    "value": 6,
                    "childName": "Author_1",
                    "level": 1
                },
                {
                    "Contentname": "Jia",
                    "value": 6,
                    "childName": "Author_1",
                    "level": 1
                },
            ],
            "order": 11,
            "label": "Author"
        },
        {
            "key": "type",
            "values": [
                {
                    "Contentname": "thread",
                    "value": 265,
                    "childName": "Type_1",
                    "level": 1
                },
                {
                    "Contentname": "issues",
                    "value": 1,
                    "childName": "Type_1",
                    "level": 1
                }
            ],
            "order": 12,
            "label": "Type"
        }
    ],
    "suggest": {
        "simple_phrase": [
            {
                "text": "",
                "offset": 0,
                "length": 0,
                "options": []
            }
        ]
    },
    "message": "success"
}
```

