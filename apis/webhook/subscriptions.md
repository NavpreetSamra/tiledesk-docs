# Subscriptions

{% api-method method="post" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions" %}
{% api-method-summary %}
Create a new subscription
{% endapi-method-summary %}

{% api-method-description %}
Allows to add more subscriptions.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="string" required=true %}
The project\_id is a unique code assigned to your project when you create it in Tiledesk
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

{% api-method-body-parameters %}
{% api-method-parameter name="event" type="string" required=true %}
the event method
{% endapi-method-parameter %}

{% api-method-parameter name="target" type="string" required=true %}
the target url
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
   {
   "__v":0,
   "updatedAt":"2019-03-12T12:01:56.462Z",
   "createdAt":"2019-03-12T12:01:56.462Z",
   "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51",
   "event":"request.create",
   "id_project":"5b55e806c93dde00143163dd",
   "createdBy":"5ab11c6b83dc240014d46095",
   "_id":"5c879fb4f1ae6600173b8c75",
   "secret":"56c189c8-33ae-4930-bd98-410a12aa45ce"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

```text
curl -v -X POST -H 'Content-Type:application/json' -u andrea.leo@f21.it:123456 -d '{"event":"request.create", "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51"}' https://api.tiledesk.com/v1/5b55e806c93dde00143163dd/subscriptions
```

{% api-method method="get" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions" %}
{% api-method-summary %}
Get all subscriptions
{% endapi-method-summary %}

{% api-method-description %}
Allows an account to list all active subscriptions.
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
[
{
   {
   "__v":0,
   "updatedAt":"2019-03-12T12:01:56.462Z",
   "createdAt":"2019-03-12T12:01:56.462Z",
   "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51",
   "event":"request.create",
   "id_project":"5b55e806c93dde00143163dd",
   "createdBy":"5ab11c6b83dc240014d46095",
   "_id":"5c879fb4f1ae6600173b8c75",
   "secret":"56c189c8-33ae-4930-bd98-410a12aa45ce"
},
...
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions/:id" %}
{% api-method-summary %}
Get a subscription by id
{% endapi-method-summary %}

{% api-method-description %}
Fetches a subscription by his or her ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
the subscription identifier
{% endapi-method-parameter %}

{% api-method-parameter name="project\_id" type="string" required=true %}
The project\_id is a unique code assigned to your project when you create it in Tiledesk
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
   {
   "__v":0,
   "updatedAt":"2019-03-12T12:01:56.462Z",
   "createdAt":"2019-03-12T12:01:56.462Z",
   "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51",
   "event":"request.create",
   "id_project":"5b55e806c93dde00143163dd",
   "createdBy":"5ab11c6b83dc240014d46095",
   "_id":"5c879fb4f1ae6600173b8c75",
   "secret":"56c189c8-33ae-4930-bd98-410a12aa45ce"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Subscription

## Create a subscription

{% api-method method="post" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions" %}
{% api-method-summary %}
Create a new subscription
{% endapi-method-summary %}

{% api-method-description %}
Allows to add more subscriptions.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="project\_id" type="string" required=true %}
The project\_id is a unique code assigned to your project when you create it in Tiledesk
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

{% api-method-body-parameters %}
{% api-method-parameter name="event" type="string" required=false %}
the event
{% endapi-method-parameter %}

{% api-method-parameter name="target" type="string" required=true %}
the target url
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{  
         "_id":"5c81593adf767b0017d1aa66",
         "updatedAt":"2019-03-07T17:47:38.393Z",
         "createdAt":"2019-03-07T17:47:38.393Z",
         "lead_id":"SRbb2PfbSFcgICv9VQBcURZeloh1",
         "fullname":"Guest",
         "attributes":{ ... },
         "id_project":"5b55e806c93dde00143163dd",
         "createdBy":"system",
         "__v":0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Example:

```text
curl -v -X POST -H 'Content-Type:application/json' -u <email>:<password> -d '{"event":"<event>", "target":"<target>"}' https://api.tiledesk.com/v1/<project_id>/subscriptions
```

{% api-method method="get" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions" %}
{% api-method-summary %}
Get all subscriptions
{% endapi-method-summary %}

{% api-method-description %}
Allows an account to list all active subscriptions.
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
   {
   "__v":0,
   "updatedAt":"2019-03-12T12:01:56.462Z",
   "createdAt":"2019-03-12T12:01:56.462Z",
   "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51",
   "event":"request.create",
   "id_project":"5b55e806c93dde00143163dd",
   "createdBy":"5ab11c6b83dc240014d46095",
   "_id":"5c879fb4f1ae6600173b8c75",
   "secret":"56c189c8-33ae-4930-bd98-410a12aa45ce"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Example

```text
curl -v -X POST -H 'Content-Type:application/json' -u andrea.leo@f21.it:123456 -d '{"event":"request.create", "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51"}' https://api.tiledesk.com/v1/5b55e806c93dde00143163dd/subscriptions
```

{% api-method method="get" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions/:id" %}
{% api-method-summary %}
Get a subscription by id
{% endapi-method-summary %}

{% api-method-description %}
Fetches a subscription by his or her ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
the subscription identifier
{% endapi-method-parameter %}

{% api-method-parameter name="project\_id" type="string" required=true %}
The project\_id is a unique code assigned to your project when you create it in Tiledesk
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{  
         "_id":"5c81593adf767b0017d1aa66",
         "updatedAt":"2019-03-07T17:47:38.393Z",
         "createdAt":"2019-03-07T17:47:38.393Z",
         "lead_id":"SRbb2PfbSFcgICv9VQBcURZeloh1",
         "fullname":"Guest",
         "attributes":{ ... },
         "id_project":"5b55e806c93dde00143163dd",
         "createdBy":"system",
         "__v":0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Example

```text
curl -v -X GET -H 'Content-Type: application/json' -u andrea.leo@f21.it:123456 https://api.tiledesk.com/v1/5b55e806c93dde00143163dd/subscriptions/5c81593adf767b0017d1aa66
```

{% api-method method="delete" host="https://api.tiledesk.com" path="/v1/:project\_id/subscriptions/:id" %}
{% api-method-summary %}
Delete a subscription by id
{% endapi-method-summary %}

{% api-method-description %}
Delete a subscription by his or her ID
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
the subscription identifier
{% endapi-method-parameter %}

{% api-method-parameter name="project\_id" type="string" required=true %}
The project\_id is a unique code assigned to your project when you create it in Tiledesk
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
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{  
         "_id":"5c81593adf767b0017d1aa66",
         "updatedAt":"2019-03-07T17:47:38.393Z",
         "createdAt":"2019-03-07T17:47:38.393Z",
         "lead_id":"SRbb2PfbSFcgICv9VQBcURZeloh1",
         "fullname":"Guest",
         "attributes":{ ... },
         "id_project":"5b55e806c93dde00143163dd",
         "createdBy":"system",
         "__v":0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

