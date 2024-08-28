# Booking_API_Test Using Postman  
Url-(https://restful-booker.herokuapp.com/booking)
 

What is API?
An API (Application Programming Interface) is a set of rules and protocols that allows different software applications to communicate with each other. It defines the methods and data formats applications can use to request and exchange information.

Key Points about APIs:

Interface: APIs serve as an interface between different software components, enabling them to interact without knowing each other's internal workings.

Requests and Responses: Typically, an application requests the API, which then processes the request and sends back a response.
For example, a weather app might use an API to request current weather data from a server, which then responds with the information.

HTTP Methods: In web APIs, common methods include:

GET: Retrieve data from a server.

POST: Send data to a server to create a new resource.

PUT: Update an existing resource on the server.

DELETE: Remove a resource from the server.

JSON/XML: Data exchanged between an API and an application is often in formats like JSON (JavaScript Object Notation) or XML (eXtensible Markup Language).

# Booking API Testing with Postman

## Prerequisites

- Install [Postman](https://www.postman.com/downloads/).
- Ensure the Booking API is running.

## Setup

1. **Import Collection**: Import the Booking API collection into Postman.
2. **Environment Setup**: Create an environment with the following variables:
   - `base_url`: Base URL (https://restful-booker.herokuapp.com/booking) of the API.
   - `api_key`: API key (if required).
   - `booking_id`: (Optional) Used to store a booking ID.

## Test Cases 
We have 2 Test case Scenario:
1. Positive Endpoints:
   a) Get Booking IDs
   b) Get Booking Details
   c) Create Booking
   d) Token Generator
   e) Update Booking
   f) Delete Booking
   g) Curl Command Import

  3. Negative Endpoints:
     a) Get Booking Details Invalid Id
     b) Create Booking Invalid chars
      
   

1. **Create a Booking**
   - **Endpoint**: `POST /bookings`
   - **Tests**: Check for `201 Created` and store `booking_id`.

2. **Get a Booking**
   - **Endpoint**: `GET /bookings/:id`
   - **Tests**: Check for `200 OK` and verify booking details.

3. **Update a Booking**
   - **Endpoint**: `PUT /bookings/:id`
   - **Tests**: Check for `200 OK` and verify updated details.

4. **Delete a Booking**
   - **Endpoint**: `DELETE /bookings/:id`
   - **Tests**: Check for `204 No Content` and confirm deletion.

5. **Additional Tests**
   - Invalid ID, missing fields, unauthorized access.

## Running Tests

- Open the collection in Postman and click `Run`.
- Review results to ensure all tests pass.

## Troubleshooting

- **400**: Check request body.
- **401**: Verify API key.
- **500**: Check API server status.

# Newman:
Newman is a command-line tool used to run Postman collections. Here are the steps to install Newman:

Step 1: Install Node.js and npm
Newman requires Node.js and npm (Node Package Manager). If you don't have these installed, follow these steps:

Download Node.js:

Go to the Node.js official website.
Download the latest LTS version (which includes npm).
Install Node.js:

Run the installer and follow the installation instructions.
Ensure the option to install npm is checked during the installation.
Verify Installation:

Open a terminal or command prompt.
Run the following commands to verify the installation:
bash
Copy code
node -v
npm -v
You should see version numbers for both Node.js and npm.
Step 2: Install Newman
With Node.js and npm installed, you can now install Newman:

Open Terminal/Command Prompt:

On Windows, you can use Command Prompt or PowerShell.
On macOS/Linux, use the Terminal.
Install Newman Globally:

Run the following command to install Newman globally on your system:
bash
Copy code
npm install -g newman
The -g flag installs Newman globally, making it accessible from anywhere on your system.
Verify Newman Installation:

After installation, verify that Newman was installed correctly by running:
bash
Copy code
newman -v
You should see the version number of Newman.
Step 3: Run a Postman Collection with Newman
Once Newman is installed, you can run Postman collections using the following command:

Run a Collection:

Navigate to the directory where your Postman collection is located, or provide the path to the collection.
Run the collection with Newman:
bash
Copy code
newman run your_collection.json
Replace your_collection.json with the path to your Postman collection file.
Example Command:

bash
Copy code
newman run my_postman_collection.json
If your collection requires an environment file, you can include it with the -e flag:
bash
Copy code
newman run my_postman_collection.json -e my_environment.json
Step 4: Explore Additional Newman Features (Optional)
Generate HTML Report:
bash
Copy code
newman run my_postman_collection.json -r html
Run a Collection from a URL:
bash
Copy code
newman run https://www.example.com/your_collection.json
These steps will set up Newman and allow you to run your Postman collections directly from the command line.

# Screenshots:

![image](https://github.com/user-attachments/assets/69a9325e-f81b-4d06-8316-05fe704ed32e)






