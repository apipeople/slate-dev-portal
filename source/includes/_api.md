# Core Banking API

## Get All Accounts

```shell
curl "http://example.com/api/accounts" \
  -H "Authorization: secret"
```

```java
HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("http://example.com/api/accounts"))
    .header("Authorization", "secret")
    .method("GET", HttpRequest.BodyPublishers.noBody())
    .build();
HttpResponse<String> response = HttpClient.newHttpClient().send(request, HttpResponse.BodyHandlers.ofString());
System.out.println(response.body());
```

> The above command returns JSON structured like this:

```json
{
	"id": 1,
	"name": "Jane Doe",
	"ssn": 6000000,
	"phoneNumber": 6000000000,

}
```

This endpoint retrieves all accounts.

### HTTP Request

`GET http://example.com/api/accounts`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
ssn | false | To return a specific ssn
state | false | To filter accounts from a specific state

<aside class="success">
You are able to retrieve accounts
</aside>

## Get a Specific Accounts

```shell
curl "http://example.com/api/accounts/2" \
  -H "Authorization: secret"
```

```java
HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("http://example.com/api/accounts/2"))
    .header("Authorization", "secret")
    .method("GET", HttpRequest.BodyPublishers.noBody())
    .build();
HttpResponse<String> response = HttpClient.newHttpClient().send(request, HttpResponse.BodyHandlers.ofString());
System.out.println(response.body());
```

> The above command returns JSON structured like this:

```json
{
	"id": 2,
	"name": "Jane Doe",
	"ssn": 6000000,
	"phoneNumber": 6000000000,

}
```

This endpoint retrieves a specific account.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/accounts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the account to retrieve

## Delete a Specific Account

```shell
curl "http://example.com/api/accounts/2" \
  -X DELETE \
  -H "Authorization: secret"
```

```java
HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("http://example.com/api/accounts/2"))
    .header("Authorization", "secret")
    .method("DELETE", HttpRequest.BodyPublishers.noBody())
    .build();
HttpResponse<String> response = HttpClient.newHttpClient().send(request, HttpResponse.BodyHandlers.ofString());
System.out.println(response.body());

```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : true
}
```

This endpoint deletes a specific account.

### HTTP Request

`DELETE http://example.com/accounts/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the account to delete

