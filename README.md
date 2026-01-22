# TeamRun Azure APIs

Azure-based REST API implementation for the TeamRun knowledge hub system using Logic Apps and Cosmos DB.

## Project Overview

This project implements a serverless CRUD API for managing TeamRun documentation and runbooks using Azure services.

## Architecture

- **Azure Logic Apps (Consumption)**: Serverless REST API endpoints
- **Azure Cosmos DB (NoSQL)**: Document storage for files and metadata
- **Azure Application Insights**: Monitoring and logging

## API Endpoints

### CREATE - Upload File
- **Method**: POST
- **File**: `CREATE.json`
- **Description**: Uploads a new file with metadata to Cosmos DB

### READ - Retrieve File
- **Method**: GET
- **File**: `READ.json`
- **Description**: Retrieves file data and metadata by ID

### UPDATE - Update Metadata
- **Method**: PUT
- **File**: `UPDATE.json`
- **Description**: Updates description and tags for existing files

### DELETE - Remove File
- **Method**: DELETE
- **File**: `DELETE.json`
- **Description**: Deletes a file and its metadata from the database

## Data Structure

Files are stored in Cosmos DB with the following schema:
```json
{
  "id": "document-id",
  "fileName": "example.pdf",
  "fileContent": "base64-encoded-content",
  "description": "Document description",
  "tags": "tag1,tag2",
  "uploadDate": "2026-01-22T12:00:00Z"
}
```

## Student Information

- **Student ID**: B00915249
- **Module**: COM682
- **Project**: TeamRun Knowledge Hub
