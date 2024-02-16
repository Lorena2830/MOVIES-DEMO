# MOVIES-DEMO
# movies-demo

### Authentication Endpoints

The Authentication flow for the application is:

### User Signup/Login

METHOD | ENDPOINT         | TOKEN | ROLE | DESCRIPTION              | POST PARAMS                                     | RETURNS
-------|------------------|-------|------|--------------------------|-------------------------------------------------|--------------------
POST   | /auth/signup     | -     | user | User Signup              | `name`, `email`, `password`,                    | { message: `string`, result: `token` }
POST   | /auth/login      | -     | user | User Login               | `email`, `password`                             | { message: `string`, result: `token` }

### User Endpoints

METHOD | ENDPOINT         | TOKEN | ROLE | DESCRIPTION              | POST PARAMS                                     | RETURNS
-------|------------------|-------|------|--------------------------|-------------------------------------------------|--------------------
GET    | /user            | YES   | admin| Get All Users            |                                                 | { message: `string`, result: `array` }
GET    | /user/:id        | YES   | admin| Get One User             |                                                 | { message: `string`, result: `object` }
GET    | /user/profile    | YES   | user | Get Own profile          |                                                 | { message: `string`, result: `object` }
POST   | /user            | YES   | admin| Create One User          |    `name`, `email`, `password`, `role`          | { message: `string`, result: `object` }
PUT    | /user/:id        | YES   | admin| Update One User          |    `name`, `email`, `password`, `role`          | { message: `string`, result: `object` }
PUT    | /user/profile    | YES   | user | Update own Profile       |    `name`, `email`                              | { message: `string`, result: `object` }
PUT    |/user/me/password | YES   | admin| Change Own Password      |    `password`                                   | { message: `string`, result: `object` }
DELETE | /user/:id        | YES   | admin| Delete One User          |    `name`, `email`, `password`, `role           | { message: `string`, result: `object` }
DELETE | /user/profile    | YES   | user | Update Own Profile       |    `name`, `email`, `password`, `role           | { message: `string`, result: `object` }
