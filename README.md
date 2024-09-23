![Tickets](https://github.com/user-attachments/assets/36abb8f9-b6c2-4039-9519-ff3ec542f703)
# Ticket_Management_System
Develop a RESTful API for a ticket management system using Node.js and MongoDB and the API should support basic CRUD operation.
Files is in master branch.

## Features

- Create new tickets.
- Retrieve all tickets or a single ticket by its ID.
- Update tickets by their unique identifier.
- Delete tickets by their unique identifier.

## Technologies Used

- **Node.js**: JavaScript runtime for building the backend.
- **Express.js**: Web framework for building RESTful APIs.
- **MongoDB**: NoSQL database for storing tickets.
- **Mongoose**: ODM library for MongoDB and schema validation.

## Prerequisites

- **Node.js** (v12.x or higher)
- **MongoDB** (Running locally or using MongoDB Atlas)

Steps to Setup Locally:

Clone the repository:
git clone https://github.com/your-username/ticket-management-system.git cd ticket-management-system

Install dependencies:
npm install

Set up environment variables:
Create a .env file in the project root and add the following: PORT=3000 MONGO_URI = mongodb://localhost:27017/your-database

Start the application: npm start

Install postman to test the API using this link for windows https://dl.pstmn.io/download/latest/win64

API Documentation

Base URL The API runs locally on http://localhost:3000/api/tickets.

Endpoints

Create Ticket 
Method: POST 
Endpoint: http://localhost:3000/api/tickets 
Request: { "title": "First", "description": "It's a first ticket", "status": "Open"}

Response: [ {
        "_id": "66f033b511b03ec8df8a5398",
        "title": "First",
        "description": "It's a first ticket",
        "status": "open",
        "createdAt": "2024-09-22T15:11:49.297Z",
        "updatedAt": "2024-09-22T15:11:49.297Z",
        "__v": 0
    } ]

Get All Tickets
Method: GET 
Endpoint: http://localhost:3000/api/tickets 

Response: [ {
        "_id": "66f033b511b03ec8df8a5398",
        "title": "First",
        "description": "It's a first ticket",
        "status": "open",
        "createdAt": "2024-09-22T15:11:49.297Z",
        "updatedAt": "2024-09-22T15:11:49.297Z",
        "__v": 0
    },
    {
        "_id": "66f0347211b03ec8df8a539a",
        "title": "Second",
        "description": "It's a second ticket",
        "status": "open",
        "createdAt": "2024-09-22T15:14:58.525Z",
        "updatedAt": "2024-09-22T15:14:58.525Z",
        "__v": 0
    } ]

Get Single Ticket
Method: GET 
Endpoint: http://localhost:3000/api/tickets/:id 

Response: [ {
        "_id": "66f0347211b03ec8df8a539a",
        "title": "Second",
        "description": "It's a second ticket",
        "status": "open",
        "createdAt": "2024-09-22T15:14:58.525Z",
        "updatedAt": "2024-09-22T15:14:58.525Z",
        "__v": 0
    } ]

Update Ticket
Method: PUT 
Endpoint:  http://localhost:3000/api/tickets/:id 
Request Body:
{ "title": "Sample", "description": "Sample ticket", "status": "Open"}

Response: [ {
        "_id": "66f0347211b03ec8df8a539a",
        "title": "Sample",
        "description": "Sample ticket",
        "status": "open",
        "createdAt": "2024-09-22T15:14:58.525Z",
        "updatedAt": "2024-09-22T15:14:58.525Z",
        "__v": 0
    } ]

Delete Ticket
Method: DELETE 
Endpoint: http://localhost:3000/api/tickets/:id 

Response: { "message": "Ticket deleted successfully" }
