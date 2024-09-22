# Ticket Management System => Ticky

This is a simple RESTful API-based ticket management system built with Node.js, Express, and MongoDB.

## Prerequisites

- Node.js
- MongoDB

## Installation

1. Clone the repository:

    code/git clone
    cd backend
    nodemon index.js

2. Validation and Error Handling
This section explains how validation and error handling are implemented in the Ticket Management System API to ensure data integrity and provide meaningful feedback to the user.

# Field Validation
When creating or updating a ticket, the following fields are validated:

Title:
Required field.
Must be at least 5 characters long.
Description:

Required field.
Must be at least 10 characters long.
Status:

Optional field.
Must be one of the following values: "open", "in progress", or "closed".
Defaults to "open" if not provided.

# Error Handling
The API handles errors at various levels, including invalid input, non-existent resources, and general server errors.

Validation Errors
When required fields are missing or invalid data is provided, the API responds with a 400 Bad Request status, along with a descriptive error message. This ensures that only valid data is processed.

Example: Missing title in the request
    code/{
      "error": "Title is required"
      }

Example: Invalid status value
    code/{
      "error": "Status must be either open, in progress, or closed"
      }

Non-existent Ticket Errors
When attempting to retrieve, update, or delete a ticket that does not exist, the API responds with a 404 Not Found status and an error message.

Example: Ticket not found
    code/{
      "error": "Ticket not found"
      }

Invalid ID Format
If the ticket ID provided in the request does not conform to MongoDB's ID format, the API responds with a 400 Bad Request status and an error message.

Example: Invalid ID format
    code/{
      "error": "Invalid ticket ID format"
      }

Server Errors
In the event of an internal server issue, the API responds with a 500 Internal Server Error status and a general error message.

Example: Server-side error
    code/{
      "error": "Server error"
      }


## API Testing using Postman

   Postman Collection Link - [text](https://api.postman.com/collections/23827736-247f6a51-b245-4175-bfd6-a1b470766909?access_key=PMAT-01J8DGVT1SKH9MFNE5PAVV76YB)

Made By Yash Parmar
yashpsct001@gmail.com