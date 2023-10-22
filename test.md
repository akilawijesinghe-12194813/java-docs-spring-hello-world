Certainly, here is the information you provided in a two-column table for each case:

**List Users**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | View all registered users          |
| HTTP Method                           | GET                                |
| API Pattern                           | /users                             |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 403, 500                       |

**Get User Details**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Retrieve user profile data         |
| HTTP Method                           | GET                                |
| API Pattern                           | /users/<id>                        |
| Parameters                            | id (User ID)                       |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 500, 403                       |

**Create User**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Register users                     |
| HTTP Method                           | POST                               |
| API Pattern                           | /users/register                     |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 500, 550                       |

**Update User**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Update user profile data           |
| HTTP Method                           | PUT                                |
| API Pattern                           | /users/<id>                        |
| Parameters                            | id (User ID)                       |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 403, 404, 500                       |

**Delete User**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Change user's status as 'Inactive' |
| HTTP Method                           | DELETE                             |
| API Pattern                           | /users/<id>                        |
| Parameters                            | id (User ID)                       |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 403, 404, 500                       |

**Assign Role**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Assigning user privileges           |
| HTTP Method                           | POST                               |
| API Pattern                           | /users/assign/<id>                 |
| Parameters                            | id (User ID)                       |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 403, 500                            |
