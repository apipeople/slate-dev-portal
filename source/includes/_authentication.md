# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: secret"
```

```java
HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("api_endpoint_here"))
    .header("Authorization", "secret")
    .method("GET", HttpRequest.BodyPublishers.noBody())
    .build();
HttpResponse<String> response = HttpClient.newHttpClient().send(request, HttpResponse.BodyHandlers.ofString());
System.out.println(response.body());
```

> Make sure to replace `secret` with your API key.

We use keys to allow access to the API. Ask to your contact.

<aside class="notice">
You must replace <code>secret</code> with your personal API key.
</aside>
