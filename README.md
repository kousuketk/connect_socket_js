# connect_socket_js

- socketを使ったclient通信

### server
```
$ node server.js
Listening Start on Server - 127.0.0.1:11111
Connection Start(1/3) - 127.0.0.1:52305
(node:93883) [DEP0020] DeprecationWarning: Server.connections property is deprecated. Use Server.getConnections method instead.
Connection Start(2/3) - 127.0.0.1:52306
[127.0.0.1:52305] - test data
Connection End(2/3) - 127.0.0.1:52306
Connection End(1/3) - 127.0.0.1:52305
^CServer Closed
```

### client
- sender
```
$ node client.js 127.0.0.1 11111
Connection - 127.0.0.1:11111
52305
[S] 52305
^CConnection Closed - 127.0.0.1:11111
Connection End - 127.0.0.1:11111
Client Closed
```

- reciever
```
$ node client.js 127.0.0.1 11111
Connection - 127.0.0.1:11111
[R] test data
^CConnection Closed - 127.0.0.1:11111
Connection End - 127.0.0.1:11111
Client Closed
```
