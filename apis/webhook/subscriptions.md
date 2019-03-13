
# Subscription

## Create a subscription

```text
curl -v -X POST -H 'Content-Type:application/json' -u <email>:<password> -d '{"event":"<event>", "target":"<target>"}' https://api.tiledesk.com/v1/<project_id>/subscriptions
```

Example:

```text
curl -v -X POST -H 'Content-Type:application/json' -u andrea.leo@f21.it:123456 -d '{"event":"request.create", "target":"https://webhook.site/c312005b-5042-49e9-a769-0f3ba4245b51"}' https://api.tiledesk.com/v1/5b55e806c93dde00143163dd/subscriptions
```

Response example:

```text
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
