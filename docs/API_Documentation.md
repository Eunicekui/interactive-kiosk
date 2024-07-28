# API Documentation

## Overview
The Wind Turbine Interactive API provides endpoints for accessing educational content, games, and user data related to wind turbines. This document outlines the available endpoints, request/response formats, and authentication requirements.

## Base URL
http://localhost:3000/api

## Endpoints

### GET /content
Retrieve all educational content on wind turbines.

#### Request
GET /content

 

#### Response
[
  {
    "id": 1,
    "title": "How Wind Turbines Work",
    "description": "An overview of wind turbine mechanics.",
    "type": "video",
    "url": "http://"
  }
]
## GET /games
-- Retrieve a list of available interactive games.

## Request
 
GET /games
Response
json
 
[
  {
    "id": 1,
    "name": "Turbine Puzzle",
    "description": "Assemble the parts of a wind turbine.",
    "difficulty": "easy"
  }
]
POST /users
Create a new user profile.

Request
 
POST /users
Request Body
json
 
{
  "name": "John Doe",
  "email": "johndoe@example.com"
}
Response
json
 
{
  "id": 1,
  "name": "John Doe",
  "email": "johndoe@example.com"
}
GET /users/{id}/progress
Retrieve the progress and scores of a specific user.

Request
 
GET /users/{id}/progress
Response
json
 
{
  "userId": 1,
  "progress": [
    {
      "gameId": 1,
      "score": 85,
      "completed": true
    }
  ]
}
### Authentication
Authentication is required for endpoints that modify user data. Please refer to the authentication documentation for more details.

### Error Handling
The API returns standard HTTP status codes to indicate the success or failure of a request.

-- 200 OK: The request was successful.
-- 400 Bad Request: The request was malformed or invalid.
-- 401 Unauthorized: Authentication is required and has failed or not been provided.
-- 404 Not Found: The requested resource could not be found.
### Contact
For support or questions, please contact 0715862938