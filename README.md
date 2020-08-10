# collection-update-websocket-protocol
Specification of the collection-update websocket protocol

Version 1.0

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
const websocket = new WebSocket(url , "collection-update");
```

# WebSocket Message

Every websocket message is an array of objects. Each object will have the following fields: `idField`, `operation`, `collectionName` and `document`.

## idField: string

## operation: string

The `operation` will be 'put' or 'delete'.

## collectionName: string

## document: object

The `document` is an object that has a key of the same name as `idField`.




# Copyright
(c) 2020 Jon Lachlan
