# Reducing Balance API Documentation

## Overview
This API provides endpoints to manage reducing balance receipt information, tax information, and taxpayer information. It includes operations for creating, retrieving, updating, and deleting records. All endpoints require authentication and audit logging.

## Base URL
`/api/reducing-balance`

## Authentication
All endpoints require authentication. Ensure that the `Authorization` header with a valid token is included in the request.

## Endpoints

### 1. Get Reducing Balance Receipt Information
- **Endpoint:** `POST /getReducingBalReceiptInfo`
- **Middleware:** `authenticate`, `auditLogger`
- **Description:** Retrieves reducing balance receipt information.
- **Request Body:**
  ```json
  {
    "receiptId": "string"
  }
