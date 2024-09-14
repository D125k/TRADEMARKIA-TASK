# Document Retrieval System (Java Version)

## Project Overview
This project implements a document retrieval system using Java (Spring Boot), Redis, and MongoDB. It allows users to query documents and retrieve relevant results, with caching for faster retrieval and rate limiting.

## Features
- Search endpoint to retrieve top-k relevant documents.
- Caching with Redis to improve response time.
- Rate limiting to prevent abuse of the search API.
- Dockerized for easy deployment.

## API Endpoints
- */health*: Check if the API is active.
- */search*: Search for documents based on a query. Returns top-k results and caches them.

## Running the App
1. Clone the repository.
2. Run docker-compose up to start the app, Redis, and MongoDB containers.
3. Access the API at http://localhost:8080.

## Vectorization
The system uses a placeholder vectorizer. You can implement a model like Sentence-BERT to vectorize queries and documents.

## Running with Docker
Run docker-compose up to start all services (Spring Boot app, Redis, MongoDB).

## Caching Strategy
Redis is used to cache search results for faster retrieval, and cached results expire after 1 hour to ensure freshness.

## Rate Limiting
The system implements rate limiting (logic needs to be fully implemented in the service).
