# Requests

You can use the API to get the request information.

{% api-method method="get" host="https://api.tiledesk.com" path="/v1/:project\_id/requests" %}
{% api-method-summary %}
Get all requests
{% endapi-method-summary %}

{% api-method-description %}
Allows an account to list all the requests for the project.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="string" required=true %}
the Project Id is a unique code assigned to your project when you create it in Tiledesk.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
authorization token. Basic Auth or JWT
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
use "application/json" value
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="sortField" type="string" required=false %}
what field to sort the results by.
{% endapi-method-parameter %}

{% api-method-parameter name="direction" type="string" required=false %}
sort direction: 1 or -1. Return the results in ascending or descending order. _defaults to desc_
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="string" required=false %}
what page of results to fetch. defaults to first page.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
   "perPage":40,
   "count":179,
   "requests":[
      {
            "_id":"5c81593adf767b0017d1aa67",
            "updatedAt":"2019-03-07T17:48:05.934Z",
            "createdAt":"2019-03-07T17:47:38.405Z",
            "request_id":"support-group-L_OG76RYhR0XFiMf2PK",
            "requester_id":"5c81593adf767b0017d1aa66",
            "first_text":"first text message",
            "department":"5c34ba232c62730016da250e",
            "sourcePage":"https://www.tiledesk.com",
            "language":"it",
            "userAgent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_2) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/72.0.3626.119 Safari/537.36",
            "id_project":"5b55e806c93dde00143163dd",
            "createdBy":"5c81593adf767b0017d1aa66",
            "__v":2,
            "waiting_time":21709,
            "agents":[
               {
                  "__v":0,
                  "createdBy":"5aaa99024c3b110014b478f0",
                  "user_available":true,
                  "role":"admin",
                  "id_user":"5ab0f3fa57066e0014bfd71e",
                  "id_project":"5b55e806c93dde00143163dd",
                  "createdAt":"2018-10-03T14:40:19.521Z",
                  "updatedAt":"2019-03-07T17:47:38.405Z",
                  "_id":"5bb4d4d39214830015742b00"
               }
            ],
            "tags":[
            ],
            "messages_count":7,
            "participants":[
               "5aaa99024c3b110014b478f0"
            ],
            "status":200,
            "lead":{..}
         }
      ...
   ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Example

```text
curl -v -X GET -H 'Content-Type: application/json' -u andrea.leo@f21.it:123456 https://api.tiledesk.com/v1/5b55e806c93dde00143163dd/requests
```

{% api-method method="get" host="https://api.tiledesk.com" path="/v1/:project\_id/requests/:id" %}
{% api-method-summary %}
Get a request by id
{% endapi-method-summary %}

{% api-method-description %}
Fetches a lead by his or her request\_id
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
the request identifier
{% endapi-method-parameter %}

{% api-method-parameter name="project\_id" type="string" required=true %}
the Project Id is a unique code assigned to your project when you create it in Tiledesk.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
authorization token. Basic Auth or JWT
{% endapi-method-parameter %}

{% api-method-parameter name="Content-Type" type="string" required=true %}
use "application/json" value
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="sortField" type="string" required=false %}
what field to sort the results by.
{% endapi-method-parameter %}

{% api-method-parameter name="direction" type="string" required=false %}
sort direction: 1 or -1. Return the results in ascending or descending order. _defaults to desc_
{% endapi-method-parameter %}

{% api-method-parameter name="page" type="string" required=false %}
what page of results to fetch. defaults to first page.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
   "_id":"5c81593adf767b0017d1aa67",
   "updatedAt":"2019-03-07T17:48:05.934Z",
   "createdAt":"2019-03-07T17:47:38.405Z",
   "request_id":"support-group-L_OG76RYhR0XFiMf2PK",
   "requester_id":"5c81593adf767b0017d1aa66",
   "first_text":"first text message",
   "department":"5c34ba232c62730016da250e",
   "sourcePage":"https://www.tiledesk.com",
   "language":"it",
   "userAgent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_2) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/72.0.3626.119 Safari/537.36",
   "id_project":"5b55e806c93dde00143163dd",
   "createdBy":"5c81593adf767b0017d1aa66",
   "__v":2,
   "waiting_time":21709,
   "agents":[
      {
         "__v":0,
         "createdBy":"5aaa99024c3b110014b478f0",
         "user_available":true,
         "role":"admin",
         "id_user":"5ab0f3fa57066e0014bfd71e",
         "id_project":"5b55e806c93dde00143163dd",
         "createdAt":"2018-10-03T14:40:19.521Z",
         "updatedAt":"2019-03-07T17:47:38.405Z",
         "_id":"5bb4d4d39214830015742b00"
      }
   ],
   "tags":[
   ],
   "messages_count":7,
   "participants":[
      "5aaa99024c3b110014b478f0"
   ],
   "status":200,
   "lead":{..}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Example:

```text
curl -v -X GET -H 'Content-Type: application/json' -u andrea.leo@f21.it:123456 https://api.tiledesk.com/v1/5b55e806c93dde00143163dd/requests/support-group-L_OG76RYhR0XFiMf2PK
```
