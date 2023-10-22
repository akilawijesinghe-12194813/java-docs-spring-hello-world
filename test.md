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


Certainly, here's the information you provided in a two-column table format for each case:

**Search User**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search a User                      |
| HTTP Method                           | GET                                |
| API Pattern                           | /users                             |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 403, 404, 500                  |

**Create HSC**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Register healthcare service center |
| HTTP Method                           | POST                               |
| API Pattern                           | /hsc                               |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                             |
| Response Error Codes                  | 400, 500, 400                       |

**List HSC**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | View all HSC's data                |
| HTTP Method                           | GET                                |
| API Pattern                           | /hsc                               |
| Parameters                            | None                               |
| FHIR Compliance                       | Yes (https://facilityregistry.health.gov.lk/fhir/Organization) |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 500                            |

**Update HSC**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Update HSC data such as name change and grade upgrade |
| HTTP Method                           | PUT                                |
| API Pattern                           | /hsc/<id>                          |
| Parameters                            | id (HSC ID)                        |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 403, 404, 500                       |

**Delete HSC**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Change HSC's status as 'Inactive'   |
| HTTP Method                           | DELETE                             |
| API Pattern                           | /hsc/<id>                          |
| Parameters                            | id (HSC ID)                        |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 403, 404, 500                       |

**Search HSC**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search HSC                         |
| HTTP Method                           | GET                                |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Search a list of organizations under ID 2223**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search a list of organizations under ID 2223 |
| HTTP Method                           | GET                                |
| FHIR Compliance                       | Yes (https://facilityregistry.health.gov.lk/fhir/Organization?partof=2223) |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Search organizations with exact name "Base Hospital, Kamburupitiya"**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search organizations with the exact name "Base Hospital, Kamburupitiya" |
| HTTP Method                           | GET                                |
| FHIR Compliance                       | Yes (https://facilityregistry.health.gov.lk/fhir/Organization?name:exact=Base%20Hospital,%20Kamburupitiya) |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Search organizations with name like "Kamburupitiya"**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search organizations with names containing "Kamburupitiya" |
| HTTP Method                           | GET                                |
| FHIR Compliance                       | Yes (https://facilityregistry.health.gov.lk/fhir/Organization?name:contains=Kamburupitiya) |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Create Unit**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Create a location under an organization |
| HTTP Method                           | POST                               |
| API Pattern                           | /unit                              |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 500, 400                       |

**List Unit under an organization**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | View all locations under an organization |
| HTTP Method                           | GET                                |
| API Pattern                           | /unit                              |
| Parameters                            | organization=<Organization_ID>     |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 500                            |

**Update Unit**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Update a location under an organization |
| HTTP Method                           | PUT                                |
| API Pattern                           | /unit/<id>                         |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 403, 404, 500                  |

**Delete Unit**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Delete a location under an organization |
| HTTP Method                           | DELETE                             |
| API Pattern                           | /unit/<id>                         |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 403, 404, 500                       |

**Search Locations with exact name "Medical Clinic, DH Baddegama"**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search a location with the exact name "Medical Clinic, DH Baddegama" |
| HTTP Method                           | GET                                |
| FHIR Compliance                       | Yes (https://facilityregistry.health.gov.lk/fhir/Location?name:exact=Medical%20Clinic,%20DH%20Baddegama) |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Search Location**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search a location                   |
| HTTP Method                           | GET                                |
| API Pattern                           | /location                           |
| Parameters                            | name:contains=HLC%20Rathgama       |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Search Locations of type HLC**

| Property                             

 | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search location based on its type  |
| HTTP Method                           | GET                                |
| API Pattern                           | /location?type=HLC                 |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Public                            |
| Response Error Codes                  | 400, 404, 500                       |

**Create DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Generate data change request for HSC and Users |
| HTTP Method                           | POST                               |
| API Pattern                           | /dcr                               |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 500, 400                       |

**List DCRs**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | View all data change requests       |
| HTTP Method                           | GET                                |
| API Pattern                           | /dcr                               |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 500                            |

**Approve/Reject DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | DCR can be rejected or approved by super administrator or administrator |
| HTTP Method                           | POST                               |
| API Pattern                           | /dcr/status/<id>                   |
| Parameters                            | id (DCR ID)                        |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 400, 500                            |

**Forward DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | DCR can be recommended and forwarded to the next upper level for further action |
| HTTP Method                           | To be filled                        |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | To be filled                        |

**Update DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | DCR can be edited by registered users before forwarding it |
| HTTP Method                           | PUT                                |
| API Pattern                           | /dcr/<id>                          |
| Parameters                            | id (DCR ID)                        |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 403, 404, 500                       |

**Delete DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | The status of DCR can be changed as 'Active' or 'Inactive' by super administrator or administrator |
| HTTP Method                           | DELETE                             |
| API Pattern                           | /dcr/<id>                          |
| Parameters                            | id (DCR ID)                        |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | 403, 404, 500                       |

**Archive DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | All DCRs should be archived for auditing purposes |
| HTTP Method                           | POST                               |
| API Pattern                           | To be filled                        |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | To be filled                        |

**Search DCR**

| Property                              | Value                              |
|---------------------------------------|------------------------------------|
| Description                           | Search 'Data Change Request'       |
| HTTP Method                           | GET                                |
| Parameters                            | None                               |
| FHIR Compliance                       | No                                 |
| API Pattern Visibility (Public/Private)| Private                            |
| Response Error Codes                  | To be filled                        |

### 9.2 API Pattern for Data Fields

**HSC Management Data Fields**

- Institution Code
- Other ID
- Official Name
- Other Name
- Health Institution Type
- Divisional Secretariat Division
- MOH Area
- Parent Organization
- Ownership
- T.P No
- Address
- Operational Status
- Latitude
- Longitude

**Unit Management Data Fields**

- Unit code
- Unit name
- Other name
- Description
- Mode
- Type
- Contact number
- Address
- Physical form
- Status

**User Management Data Fields**

- User ID
- Name
- NIC No.
- Designation
- User Type
- Assigned Roles
- Contact Number
- Email Address
- Address
- Gender
- Name of Health Institution
- Address of Health Institution
- Status
- HSC DCR HSC ID
- Requester Name
- Requester ID / NIC
- Requester Contact Number
- Requester Email Address
- Description for Change
- Reason for Change
- Any Official Documents regarding this request
- Remarks

**User Profile DCR Data Fields**

- DCR ID
- Requester Name
- Requester ID / NIC
- User name to be changed / edited
- User ID to be changed / edited
- Description of Change
- Reason for Change
- Any Official Documents regarding this request
- Remarks

This comprehensive API documentation includes details of API endpoints, their descriptions, HTTP methods, parameters, FHIR compliance, visibility, response error codes, and data fields for different modules.
