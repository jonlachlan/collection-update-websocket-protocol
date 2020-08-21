# collection-update-websocket-protocol
Specification of the collection-update websocket protocol

# Version 2.0

protocol: collection-update

```
[{
 idField
 operation: put/delete
 collectionName
 document
}]
```

`collection-update` is a websocket sub-protocol, i.e., it can be provided to a `WebSocket()` constructor as the `protocol`.

For example,
```
const websocket = new WebSocket(url, "collection-update");
```

## WebSocket Message

Every websocket message is an array of objects. Each object will have the following fields: `idField`, `operation`, `collectionName` and `document`.

### idField: string

### operation: string

The `operation` will be 'put' or 'delete'.

### collectionName: string

### document: object

The `document` is an object that has a key that is the value of `idField`.


# Version 1.1

*This version clarifies version 1.0. Users of version 1.0 should refer to this version.*

protocol: collection-update

```
[{
 idField
 operation: put/delete
 collectionName
 document
}]
```

`collection-update` is a websocket sub-protocol, i.e., it can be provided to a `WebSocket()` constructor as the `protocol`.

For example,
```
const websocket = new WebSocket(url, "collection-update");
```

## WebSocket Message

Every websocket message is an array of objects. Each object will have the following fields: `idField`, `operation`, `collectionName` and `document`.

### idField: string

### operation: string

The `operation` will be 'put' or 'delete'.

### collectionName: string

### document: object

The `document` is an object that has a key of the same name as the value of `idField`.


# Registry

Registered to the WebSocket Subprotocol Name Registry with the identifier collection-update as The Collection Update Websocket Subprotocol.

https://www.iana.org/assignments/websocket/websocket.xhtml

# Copyright
(c) 2020 Jon Lachlan
