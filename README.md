# Flask API Lab

This repository contains a simple Flask API project developed as an exercise to practice creating RESTful endpoints, handling HTTP responses, and managing data in a Python Flask environment. The purpose of this project is to understand how to build and test basic CRUD operations in a web API while implementing best practices for error handling and response codes.

## Project Purpose

The goal of this lab is to create a foundational API that allows for:
- Retrieving data via different types of endpoints.
- Performing operations like adding, retrieving, and deleting resources.
- Handling various HTTP response statuses to give informative feedback to the client.
  
This exercise provides experience in setting up a Python Flask API and working with different HTTP methods and endpoints.

## What I Practiced

Throughout this lab, I practiced:

- **Flask Basics**: Setting up and running a Flask application.
- **HTTP Methods and Status Codes**: Learning how to respond with appropriate HTTP status codes (200, 404, 422, etc.) for different scenarios.
- **Creating Endpoints**: Implementing routes with different HTTP methods (GET, POST, DELETE) to handle CRUD operations.
- **Dynamic URL Routing**: Using dynamic URL parameters to fetch specific resources based on unique identifiers (UUID).
- **Mock Data Management**: Working with mock data stored as a list of dictionaries to simulate database-like operations.
- **Request Parsing**: Extracting data from URL query parameters and JSON payloads in request bodies.
- **Error Handling**: Adding custom error handlers to provide meaningful error messages for the client.

## Endpoints Overview

### 1. Basic Routes
- `/` : Returns a simple "Hello World" message.
- `/no_content` : Responds with a `204 No Content` status.
- `/exp` : Returns a "Hello World" message with a custom `200 OK` response.

### 2. Data Management Routes
- `/data` : Returns the length of the data if available or a `500` status if no data is found.
- `/count` : Returns the total number of entries in the data list.
  
### 3. Search and CRUD Routes
- `/name_search` : Searches the data for a person by their first name using the `q` query parameter.
- `/person/<uuid:id>` (GET) : Retrieves a specific person by UUID.
- `/person/<uuid:id>` (DELETE) : Deletes a person by UUID.
- `/person` (POST) : Adds a new person to the data list using JSON data provided in the request body.

### 4. Error Handling
- Custom error handler for `404 Not Found` errors.

## Running the Project

To run this project locally:
1. Clone the repository.
2. Install Flask by running:
   ```bash
   pip install Flask
