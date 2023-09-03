---
title: Users
description: Informacion del usuario
---

## Users
#### Get all users
You can access the list of 3 users by using the /users endpoint.

```json
[
  {
    "id": 1,
    "email": "john@mail.com",
    "password": "changeme",
    "name": "Jhon",
    "role": "customer",
    "avatar": "https://api.lorem.space/image/face?w=640&h=480&r=867",
  },
]
```

#### Get a single user
You can get a single user by adding the id as a parameter: /users/{id}
```
[GET] https://api.escuelajs.co/api/v1/users/1
```
```json
{
  "id": 1,
  "email": "john@mail.com",
  "password": "changeme",
  "name": "Jhon",
  "role": "customer",
  "avatar": "https://api.lorem.space/image/face?w=640&h=480&r=867",
}
```


#### Create a user
You can create a new user by sending an object like the following to /users/
```
[POST] https://api.escuelajs.co/api/v1/users/
# Body
{
  "name": "Nicolas",
  "email": "nico@gmail.com",
  "password": "1234",
  "avatar": "https://api.lorem.space/image/face?w=640&h=480&r=867",
}
```
```json
{
	"email": "nico@gmail.com",
	"password": "1234",
	"name": "Nicolas",
	"avatar": "https://api.lorem.space/image/face?w=640&h=480&r=867",
	"role": "customer",
	"id": 24
}
```
```
Note that the password is will not encrypted.
```


#### Update a user
You can update a user exists by sending an object like the following and adding the id as a parameter: /users/{id}
```
[PUT] https://api.escuelajs.co/api/v1/users/1
# Body
{
  "email": "john@mail.com",
  "name": "Change name",
}
```
```json
{
	"id": 4,
	"email": "john@mail.com",
	"password": "1234",
	"name": "Change name",
	"role": "admin",
	"avatar": "https://api.lorem.space/image/face?w=640&h=480&r=867",
}
```