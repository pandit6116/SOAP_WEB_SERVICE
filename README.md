# SOAP_WEB_SERVICE
This is a TIBCO-based integration project-

I created a project folder inside the Designer, which includes the following key components:
Shared Resources
Processes
Services
Connections
Schemas
WSDLs

Shared Resources & Connections
Within Shared Resources, I set up the necessary database connection by providing details such as URL, username, and password. Additionally, I created an HTTP Connection, specifying the host, port, and endpoint required for the web service.

Service Configuration
In the UsersService, I defined the endpoint binding, where I utilized the HTTP connection. Based on the endpoint type, I selected SOAP and specified the transport as HTTP to ensure proper communication.

Schemas
I created a User Schema for the User WSDL. This schema is essential when calling the AddUser operation, as it defines the user object that needs to be passed as an input using  XML Schema.

WSDLs
I created a User WSDL, which includes a User Port Type containing the following operations:
AddUser
DeleteUser
GetUser
GetUsers

For each operation, I defined the required messages (input/output) in the message table, such as:
reqAddUser / respAddUser
reqDeleteUser / respDeleteUser
reqGetUser / respGetUser
reqGetUsers / respGetUsers

Service Implementation
I added a UsersService, selected the appropriate WSDL, and ensured all operations were correctly listed under the service.

Processes & Implementation
To implement each operation, I created corresponding processes such as AddUserImpl, DeleteUserImpl, etc. These processes handle the actual execution logic for each operation.

Testing the Web Service
Once the implementation was complete, I:
Saved the WSDL file locally.
Opened SOAP UI and imported the saved WSDL.
Started the tester in Designer to ensure the web service was running correctly.
Executed test cases for each operation (AddUser, DeleteUser, GetUser, GetUsers) to validate functionality.

