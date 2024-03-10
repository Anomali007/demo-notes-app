<!-- Create a note -->

### Request:
curl -X POST \
-H 'Content-Type: application/json' \
-d '{"content":"Hello World","attachment":"hello.jpg"}' \
https://q65w48nvle.execute-api.us-east-1.amazonaws.com/notes

### Response:
```json
{
    "userId":"123",
    "noteId":"fbd59800-de85-11ee-b6ff-fb91db3f0a08",
    "content":"Hello World",
    "attachment":"hello.jpg",
    "createdAt":1710037753216
}
```


<!-- Get a note -->

### Request:


```bash
curl <ApiEndpoint>/notes/<NOTE_ID>
curl https://q65w48nvle.execute-api.us-east-1.amazonaws.com/notes/fbd59800-de85-11ee-b6ff-fb91db3f0a08
```


### Response:

```json
{
    "attachment":"hello.jpg",
    "content":"Hello World",
    "createdAt":1710037753216,
    "noteId":"fbd59800-de85-11ee-b6ff-fb91db3f0a08",
    "userId":"123"
}
```

<!-- List all the notes -->

### Request:


```bash
curl <ApiEndpoint>/notes
curl https://q65w48nvle.execute-api.us-east-1.amazonaws.com/notes
```


### Response:

```json
[
    {
        "attachment":"hello.jpg",
        "content":"Hello World",
        "createdAt":1710037753216,
        "noteId":"fbd59800-de85-11ee-b6ff-fb91db3f0a08",
        "userId":"123"
    }
]
```

<!-- Update a note -->

### Request:


```bash
curl -X PUT \
-H 'Content-Type: application/json' \
-d '{"content":"New World","attachment":"new.jpg"}' \
<ApiEndpoint>/notes/<NOTE_ID>

curl -X PUT \
-H 'Content-Type: application/json' \
-d '{"content":"New World","attachment":"new.jpg"}' \
https://q65w48nvle.execute-api.us-east-1.amazonaws.com/notes/fbd59800-de85-11ee-b6ff-fb91db3f0a08
```


### Response:

```json
{
    "status":true
}
```


<!-- Delete a note -->

### Request:

```bash
curl -X DELETE <ApiEndpoint>/notes/<NOTE_ID>

curl -X DELETE https://q65w48nvle.execute-api.us-east-1.amazonaws.com/notes/fbd59800-de85-11ee-b6ff-fb91db3f0a08

```


### Response:

```json
{
    "status":true
}
```