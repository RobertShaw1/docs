---
layout: default
description: Database API
---

# Database API

## ArangoDB.db

`ArangoDB.db(String name) : ArangoDatabase`

Returns a _ArangoDatabase_ instance for the given database name.

**Arguments**

- **name**: `String`

  Name of the database

**Examples**

```Java
ArangoDB arango = new ArangoDB.Builder().build();
ArangoDatabase db = arango.db("myDB");
```
