---
layout: default
description: This function implements the HTTP API for JS transactions
---
# Transactions

This function implements the
[HTTP API for JS transactions](../http/transaction-js-transaction.html).
Also see [ArangoDB Transactions](../transactions.html).

## ArangoDatabase.transaction

`ArangoDatabase.transaction(String action, Class<T> type, TransactionOptions options) : T`

Performs a server-side transaction and returns its return value.

**Arguments**

- **action**: `String`

  A String evaluating to a JavaScript function to be executed on the server.

- **type**: `Class`

  The type of the result (POJO class, `VPackSlice` or `String` for JSON)

- **options**: `TransactionOptions`

  Additional transaction options

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
String action = "function (params) {"
                + "const db = require('@arangodb').db;"
                + "return db._query('FOR i IN test RETURN i._key').toArray();"
              + "}";
String[] keys = arango.db().transaction(
  action, String[].class, new TransactionOptions()
);
```
