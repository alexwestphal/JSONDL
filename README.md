# JSONDL (JSON Description Language)
A language for describing JSON structures in API documentation.


# Scope 
JSONDL is intended for documenting APIs. It focusses on human readability so at this point there is no parser for JSONDL.

# Describing an HTTP API

A resource can be said to consume a particular type `C` and produce a result of type `P`. A resource can thus be described as a function:

```
POST /api/users : User -> UserId
```

# Describing a JSON Object

Say we want an object of type `User` to look like this:

```json
{
  "user_id": 10,
  "user_email": "john@example.com",
  "user_name": "John Smith",
  "user_age": 32
}
```

We can describe it (along with some obvious constrains) as:
```
User = {
  user_id: UserId,
  user_email: Email,
  user_name: String,
  user_age: UInt
}

UserId = UInt
```

Notice that the quotes are left off the keys and that on the right hand side of each colon is a type name. Also there are actually two type declarations here, `User` and `UserId`. In the case of `UserId` we're just defining it to be an alias of `UInt`.

# Base Types

JSONDL defines the following base types:

- `Boolean` - The literal JSON `true` or `false`. (In type union notation: `Boolean = true | false`)

TODO

# Optional Fields

TODO

# Default Values

TODO

# Unions

TODO
