# Project: auth-api

## Author: Daniel Frey

## Problem Domain

A simple server combining authentication techniques, CRUD functions on a SQL database, and adaptable routing techniques.

## Links and Resources

- [ci/cd](https://github.com/DSFrey/auth-api/actions)

## Setup

### `.env` requirements 
- `PORT` - Port Number
- `DATABASE_URL` - URL to the running Postgres instance/db
- `SECRET` - Secret for jwt tokens

### How to initialize/run your application (where applicable)

- `npm install` to install dependencies.
- `npm run db:config` then edit the created config file.
- `npm run db:create` to create the database.
- `npm start` to start the application.

### Features / Routes

- User data routes
  - POST : `/signup` - creates a new user
  - POST : `/signin` - verifies a user against the database
  - GET : `/users` - requires admin access to retrieve a list of users in the database
- `api/v2` routes, including `/food` and `/clothes` models
  - GET : retrieve all items or a specified item
  - POST : requires writer role to add an item
  - PUT : requires editor role to edit an item
  - DELETE : requires admin role to delete an item

### UML

![auth-api UML](./auth-api.png)
