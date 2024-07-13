This project involves the integration of a set of APIs to create a customer management web application. The application will allow users to authenticate, view, create, update, and delete customer records using API calls. The APIs use Bearer authentication for secure access.

##API Endpoints:

Authentication API:
Path: https://qa2.sunbasedata.com/sunbase/portal/api/assignment_auth.jsp
Method: POST
Body: JSON object containing login credentials
Response: Returns a bearer token for further API calls
Create a New Customer API:

Path: https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp
Method: POST
Parameters: cmd=create
Header: Authorization with Bearer token obtained from the Authentication API
Body: JSON object containing customer details (first_name and last_name are mandatory)
Response: Success (201) or Failure (400) with appropriate error messages
Get Customer List API:

Path: https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp
Method: GET
Parameters: cmd=get_customer_list
Header: Authorization with Bearer token obtained from the Authentication API
Response: Returns a list of customer objects in JSON format
Delete a Customer API:

Path: https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp
Method: POST
Parameters: cmd=delete and uuid of a specific customer
Header: Authorization with Bearer token obtained from the Authentication API
Response: Success (200) or Failure (500 or 400) with appropriate error messages
Update a Customer API:

Path: https://qa2.sunbasedata.com/sunbase/portal/api/assignment.jsp
Method: POST
Parameters: cmd=update and uuid of a specific customer
Header: Authorization with Bearer token obtained from the Authentication API
Body: JSON object containing updated customer details
Response: Success (200) or Failure (500 or 400) with appropriate error messages

Application Workflow:
Login Screen:
Users can log in using their credentials. The API will authenticate the user and return a bearer token, which will be stored for further API calls.
Customer List Screen:
After successful login, users can view the list of existing customers. The API call will retrieve the customer data and display it in a table format.
Add New Customer:
Users can create a new customer by filling out a form with the required details and submitting it. The API call will add the new customer to the database.
Delete Customer:
Users can select a customer from the list and choose to delete them. The API call will remove the selected customer from the database.
Update Customer:
Users can select a customer from the list, update their details in a form, and submit the changes. The API call will update the customer information in the database.
Notes:
The application should handle various API responses, such as success, failure, and errors, and display appropriate messages to the user. If invalid command or invalid authorization is passed in the API calls, the application should handle the responses accordingly. The application can be tested using tools like Postman to verify API functionality. The project will consist of a basic UI using HTML with minimal styling. The main focus will be on implementing the functionality to interact with the provided APIs and manage customer records effectively. The web application will allow users to perform CRUD (Create, Read, Update, Delete) operations on customer data, providing a simple and user-friendly interface for managing customer records.

SunbaseData-Assignment
