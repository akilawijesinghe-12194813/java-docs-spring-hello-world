Certainly! Here are the REST API representations for all the tables with sample request body JSON and response body JSON:

**List Users:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/users` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "userID": "USR123",
    "name": "John Doe",
    "designation": "Data Entry Operator",
    "userType": "Data Entry Operator",
    "contactNumber": "+1234567890",
    "emailAddress": "john.doe@example.com",
    "status": "Active"
  },
  {
    "userID": "USR456",
    "name": "Jane Smith",
    "designation": "Data Approver",
    "userType": "Data Approver",
    "contactNumber": "+9876543210",
    "emailAddress": "jane.smith@example.com",
    "status": "Active"
  }
]
```

**Get User Details:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/users/USR123` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "userID": "USR123",
  "name": "John Doe",
  "designation": "Data Entry Operator",
  "userType": "Data Entry Operator",
  "contactNumber": "+1234567890",
  "emailAddress": "john.doe@example.com",
  "status": "Active"
}
```

**Create User:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/users/register` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "name": "John Doe",
  "NIC No.": "1234567890",
  "designation": "Data Entry Operator",
  "userType": "Data Entry Operator",
  "assignedRoles": ["Data Entry Operator", "Data Approver"],
  "contactNumber": "+1234567890",
  "emailAddress": "john.doe@example.com",
  "address": "123 Main Street, City, Country",
  "gender": "Male",
  "nameOfHealthInstitution": "City Hospital",
  "addressOfHealthInstitution": "456 Hospital Road, City, Country",
  "status": "Active",
  "HSC DCR HSC ID": "HSC123",
  "requesterName": "Jane Smith",
  "requesterIDNIC": "9876543210",
  "requesterContactNumber": "+9876543210",
  "requesterEmailAddress": "jane.smith@example.com",
  "descriptionForChange": "User role change to Data Approver",
  "reasonForChange": "Government decision",
  "anyOfficialDocuments": ["document1.pdf", "document2.docx"],
  "remarks": "No additional remarks"
}
```

| Response | 
| Status | 201 Created |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "User 'John Doe' registered successfully.",
  "userID": "USR7890"
}
```

**Update User:**

| Property | Value |
| --- | --- |
| Method | PUT |
| URL | `/users/USR123` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "name": "Updated John Doe",
  "designation": "Data Approver",
  "userType": "Data Approver",
  "contactNumber": "+9876543210",
  "emailAddress": "updated.john.doe@example.com",
  "status": "Active"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "User 'John Doe' updated successfully."
}
```

**Delete User:**

| Property | Value |
| --- | --- |
| Method | DELETE |
| URL | `/users/USR123` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 204 No Content |

**Assign Role:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/users/USR123/assign-role` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "role": "Data Approver"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Role 'Data Approver' assigned to user 'John Doe'."
}
```

**Search User:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/users?name:contains=John%20Doe` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "userID": "USR123",
    "name": "John Doe",
    "designation": "Data Entry Operator",
    "userType": "Data Entry Operator",
    "contactNumber": "+1234567890",
    "emailAddress": "john.doe@example.com",
    "status": "Active"
  }
]
```

**Create HSC:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/hsc` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "officialName": "City Hospital",
  "otherName": "Downtown Clinic",
  "healthInstitutionType": "National",
  "divisionalSecretariatDivision": "City Division",
  "MOHArea": "Central MOH Area",
 

 "parentOrganization": "Health Ministry",
  "ownership": "Public",
  "contactNumber": "+1234567890",
  "address": "456 Hospital Road, City, Country",
  "operationalStatus": "Active",
  "latitude": 123.456,
  "longitude": 45.678
}
```

| Response | 
| Status | 201 Created |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Healthcare Service Center 'City Hospital' registered successfully.",
  "hscID": "HSC123"
}
```

**List HSC:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/hsc` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "hscID": "HSC123",
    "officialName": "City Hospital",
    "otherName": "Downtown Clinic",
    "healthInstitutionType": "National",
    "divisionalSecretariatDivision": "City Division",
    "MOHArea": "Central MOH Area",
    "parentOrganization": "Health Ministry",
    "ownership": "Public",
    "contactNumber": "+1234567890",
    "address": "456 Hospital Road, City, Country",
    "operationalStatus": "Active"
  }
]
```

**Update HSC:**

| Property | Value |
| --- | --- |
| Method | PUT |
| URL | `/hsc/HSC123` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "officialName": "Updated City Hospital",
  "operationalStatus": "Inactive"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Healthcare Service Center 'City Hospital' updated successfully."
}
```

**Delete HSC:**

| Property | Value |
| --- | --- |
| Method | DELETE |
| URL | `/hsc/HSC123` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 204 No Content |

**Search HSC:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/hsc?name:exact=City%20Hospital` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "hscID": "HSC123",
    "officialName": "City Hospital",
    "otherName": "Downtown Clinic",
    "healthInstitutionType": "National",
    "divisionalSecretariatDivision": "City Division",
    "MOHArea": "Central MOH Area",
    "parentOrganization": "Health Ministry",
    "ownership": "Public",
    "contactNumber": "+1234567890",
    "address": "456 Hospital Road, City, Country",
    "operationalStatus": "Active"
  }
]
```

**Search Organizations Under ID 2223:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/organizations/2223` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "organizationID": "ORG2223",
  "name": "Base Hospital, Kamburupitiya",
  "type": "Hospital",
  "contactNumber": "+9876543210",
  "address": "123 Hospital Street, Kamburupitiya, Country",
  "status": "Active"
}
```

**Search Organizations with Exact Name "Base Hospital, Kamburupitiya":**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/organizations?name:exact=Base%20Hospital,%20Kamburupitiya` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "organizationID": "ORG2223",
    "name": "Base Hospital, Kamburupitiya",
    "type": "Hospital",
    "contactNumber": "+9876543210",
    "address": "123 Hospital Street, Kamburupitiya, Country",
    "status": "Active"
  }
]
```

**Search Organizations with Name Like "Kamburupitiya":**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/organizations?name:contains=Kamburupitiya` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "organizationID": "ORG2223",
    "name": "Base Hospital, Kamburupitiya",
    "type": "Hospital",
    "contactNumber": "+9876543210",
    "address": "123 Hospital Street, Kamburupitiya, Country",
    "status": "Active"
  }
]
```

**Create Unit:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/unit` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "unitCode": "UNIT123",
  "unitName": "Emergency Ward",
  "otherName": "ER Ward",
  "description": "Emergency care unit",
  "mode": "Ward",
  "type": "Emergency",
  "contactNumber": "+1234567890",
  "address": "789 Hospital Wing, City

, Country",
  "physicalForm": "Building",
  "status": "Active"
}
```

| Response | 
| Status | 201 Created |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Unit 'Emergency Ward' created successfully.",
  "unitID": "UNIT123"
}
```

**List Units Under an Organization:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/organizations/ORG2223/units` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application/json |
| Response Body (JSON) | 
```json
[
  {
    "unitID": "UNIT123",
    "unitCode": "Emergency Ward",
    "unitName": "ER Ward",
    "description": "Emergency care unit",
    "mode": "Ward",
    "type": "Emergency",
    "status": "Active"
  }
]
```

**Update Unit:**

| Property | Value |
| --- | --- |
| Method | PUT |
| URL | `/unit/UNIT123` |
| Headers | 
| - Content-Type | application/json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "unitName": "Updated Emergency Ward",
  "status": "Inactive"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Unit 'Emergency Ward' updated successfully."
}
```

**Delete Unit:**

| Property | Value |
| --- | --- |
| Method | DELETE |
| URL | `/unit/UNIT123` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 204 No Content |

**Search Locations with Exact Name "Medical Clinic, DH Baddegama":**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/locations?name:exact=Medical%20Clinic,%20DH%20Baddegama` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
[
  {
    "locationID": "LOC123",
    "name": "Medical Clinic, DH Baddegama",
    "type": "HLC",
    "contactNumber": "+9876543210",
    "address": "456 Clinic Street, DH Baddegama, Country",
    "status": "Active"
  }
]
```

**Search Locations:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/locations?name:contains=Medical%20Clinic` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
[
  {
    "locationID": "LOC123",
    "name": "Medical Clinic, DH Baddegama",
    "type": "HLC",
    "contactNumber": "+9876543210",
    "address": "456 Clinic Street, DH Baddegama, Country",
    "status": "Active"
  }
]
```

**Search Locations of Type HLC:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/locations?type:exact=HLC` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
[
  {
    "locationID": "LOC123",
    "name": "Medical Clinic, DH Baddegama",
    "type": "HLC",
    "contactNumber": "+9876543210",
    "address": "456 Clinic Street, DH Baddegama, Country",
    "status": "Active"
  }
]
```

**Create DCR:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/dcr` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "requesterName": "Jane Smith",
  "requesterIDNIC": "9876543210",
  "userNameToBeChangedEdited": "John Doe",
  "userIDToBeChangedEdited": "USR123",
  "descriptionOfChange": "User role change to Data Approver",
  "reasonForChange": "Government decision",
  "anyOfficialDocuments": ["document1.pdf", "document2.docx"],
  "remarks": "No additional remarks"
}
```

| Response | 
| Status | 201 Created |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Data Change Request created successfully.",
  "dcrID": "DCR123"
}
```

**List DCRs:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/dcr` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
[
  {
    "dcrID": "DCR123",
    "requesterName": "Jane Smith",
    "descriptionOfChange": "User role change to Data Approver",
    "status": "Pending"
  }
]
```

**Approve/Reject DCR:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/dcr/DCR123/approve` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "approvalStatus": "Approved"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type |

 application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Data Change Request 'DCR123' has been approved."
}
```

**Forward DCR:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/dcr/DCR123/forward` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "forwardToUserID": "USR456"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Data Change Request 'DCR123' has been forwarded to user 'Jane Smith'."
}
```

**Update DCR:**

| Property | Value |
| --- | --- |
| Method | PUT |
| URL | `/dcr/DCR123` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | 
```json
{
  "descriptionOfChange": "Updated user role to Data Reviewer"
}
```

| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Data Change Request 'DCR123' updated successfully."
}
```

**Delete DCR:**

| Property | Value |
| --- | --- |
| Method | DELETE |
| URL | `/dcr/DCR123` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 204 No Content |

**Archive DCR:**

| Property | Value |
| --- | --- |
| Method | POST |
| URL | `/dcr/DCR123/archive` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
{
  "status": "Success",
  "message": "Data Change Request 'DCR123' has been archived."
}
```

**Search DCR:**

| Property | Value |
| --- | --- |
| Method | GET |
| URL | `/dcr?requesterName:contains=Jane%20Smith` |
| Headers | 
| - Content-Type | application.json |
| - Authorization | Bearer \<Your_Auth_Token\> |
| Request Body (JSON) | None |
| Response | 
| Status | 200 OK |
| Headers | 
| - Content-Type | application.json |
| Response Body (JSON) | 
```json
[
  {
    "dcrID": "DCR123",
    "requesterName": "Jane Smith",
    "descriptionOfChange": "User role change to Data Reviewer",
    "status": "Pending"
  }
]
```

These REST API representations provide examples of requests and responses for each of the tables based on the provided information.
