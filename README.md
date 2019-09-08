# mevn-chat

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm start
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```


### Testing

Run the server in one terminal `npm start` and in other terminal test the REST API by running this command:

```sh
curl -i -H "Accept: application/json" localhost:3000/api/room
```

It should output:

```
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 2
ETag: W/"2-l9Fw4VUO7kr8CvBlt4zaMCqXZ0w"
Date: Sat, 07 Sep 2019 23:58:01 GMT
Connection: keep-alive

[]
```

Now, populate Room collection by running this command:

```sh
curl -i -X POST -H "Content-Type: application/json" -d '{ "room_name":"Javascript" }' localhost:3000/api/room
```

It should output something like this:

```sh
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: application/json; charset=utf-8
Content-Length: 109
ETag: W/"6d-S6yEpa79n7rUE6EvbXQVugT1Y5Q"
Date: Sun, 08 Sep 2019 00:02:15 GMT
Connection: keep-alive

{"_id":"5d744507d30eec117ea52a48","room_name":"Javascript","created_date":"2019-09-08T00:02:15.291Z","__v":0}
```
