# Purchasing Tax API Documentation

## Overview

This document provides detailed information about the Purchasing Tax API endpoints, including authentication requirements, request/response formats, and descriptions of each endpoint's functionality.

## Authentication

Most endpoints require authentication using the `authenticate` middleware. Requests to these endpoints must include valid authentication credentials.

## Audit Logging

The `auditLogger` middleware is applied to most endpoints to track and log API usage for auditing purposes.

## Validation

Some endpoints use the `validator` middleware with specific schemas (e.g., `purchaseTaxSetUpSchema`) and profiles (e.g., `purchaseTaxSetUpProfile`) to validate request data.

## Endpoints

### Company Information Management

#### Create Company Information

- **URL**: `/createCompanyInfo`
- **Method**: POST
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Description**: Creates a new company information record in the purchasing tax system.

#### Get All Company Information

- **URL**: `/getAllCompanyInfo`
- **Method**: GET
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.getAllCompanyRecords`
- **Description**: Retrieves all company information records from the purchasing tax system.

#### Get Purchase Tax Authorizer View

- **URL**: `/getPurchaseTaxauthorizerView`
- **Method**: GET
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.getAllCompanyRecordsForAuthorizer`
- **Description**: Retrieves company records formatted for tax authorizers.

#### Get Purchase Tax Reviewer View

- **URL**: `/getPurchaseTaxReviewerView`
- **Method**: GET
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.getAllCompanyRecordsForReviewer`
- **Description**: Retrieves company records formatted for tax reviewers.

#### Get Single Company Information

- **URL**: `/getCompanyInfoRecord/:id`
- **Method**: GET
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.getSingleCompanyInfo`
- **Description**: Retrieves information for a specific company by ID.

#### Update Company Information

- **URL**: `/updateCompanyInfo/:id`
- **Method**: PUT
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.updateCompanyInfoRecord`
- **Description**: Updates information for a specific company by ID.

#### Delete Company Information Record

- **URL**: `/deleteCompanyInfoRecord/:id`
- **Method**: DELETE
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.deleteCompanyInfoRecord`
- **Description**: Deletes a company information record by ID.

#### Delete Company File

- **URL**: `/deleteCompanyFile/:id`
- **Method**: DELETE
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.deleteCompanyFile`
- **Description**: Deletes a file associated with a company by ID.

### Purchase Tax Setup Management

#### Create Purchase Tax Setup

- **URL**: `/createPurchaseTaxSetUp`
- **Method**: POST
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.createSetUpInfo`
- **Description**: Creates a new purchase tax setup configuration.

#### Get Active Purchase Tax Setups

- **URL**: `/getActivePurchaseTaxSetUps`
- **Method**: GET
- **Auth Required**: No (but validated)
- **Middleware**: `auditLogger`, `validator(purchaseTaxSetUpSchema, purchaseTaxSetUpProfile)`
- **Handler**: `purchasingTaxCtrl.getActivePurchaseTaxSetUps`
- **Description**: Retrieves all active purchase tax setup configurations.

#### Get All Purchase Tax Setups

- **URL**: `/getAllPurchaseTaxSetup`
- **Method**: GET
- **Auth Required**: No (but validated)
- **Middleware**: `auditLogger`, `validator(purchaseTaxSetUpSchema, purchaseTaxSetUpProfile)`
- **Handler**: `purchasingTaxCtrl.getAllPurchaseTaxSetUpRecords`
- **Description**: Retrieves all purchase tax setup configurations, including inactive ones.

#### Update Purchase Tax Setup

- **URL**: `/updatePurchaseTaxSetUp/:id`
- **Method**: PUT
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`, `validator(purchaseTaxSetUpSchema, purchaseTaxSetUpProfile)`
- **Handler**: `purchasingTaxCtrl.updateSetUpInfoRecord`
- **Description**: Updates a specific purchase tax setup configuration by ID.

#### Deactivate Setup Record

- **URL**: `/deactivateSetUpRecord/:id`
- **Method**: DELETE
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.deactivateSetUpRecord`
- **Description**: Deactivates (but doesn't delete) a specific setup record by ID.

#### Activate Setup Record

- **URL**: `/activateSetUpRecord/:id`
- **Method**: PATCH
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.activateSetUpRecord`
- **Description**: Activates a previously deactivated setup record by ID.

### Category Management

#### Update Purchase Tax Category Information

- **URL**: `/updatePurchaseTaxCategoryInfo/:id`
- **Method**: PUT
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.updateCategoryInfo`
- **Description**: Updates purchase tax category information by ID.

#### Get Single Category Information

- **URL**: `/getCategoryInfo/:id`
- **Method**: GET
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.getSingleCategoryInfo`
- **Description**: Retrieves information for a specific category by ID.

### Tax Calculation

#### Calculate Tax

- **URL**: `/calculateTax`
- **Method**: POST
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.calculateTax`
- **Description**: Calculates tax for a given purchase.

#### Upload For Bulk Tax Calculation

- **URL**: `/uploadForBulkTaxCalc`
- **Method**: POST
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`, `upload.single("file")`
- **Handler**: `purchasingTaxCtrl.calculateBulkTax`
- **Description**: Calculates tax for multiple purchases using an uploaded file.

### Additional Endpoints

#### Get Purchase Tax Records By ESBN

- **URL**: `/getRecordsByEsbn`
- **Method**: GET
- **Auth Required**: Yes
- **Middleware**: `authenticate`, `auditLogger`
- **Handler**: `purchasingTaxCtrl.getPurchaseTaxRecordsByEsbn`
- **Description**: Retrieves purchase tax records associated with a specific ESBN.

#### Get PT Receipt

- **URL**: `/getPTReceipt/:id`
- **Method**: GET
- **Auth Required**: No
- **Middleware**: None
- **Handler**: `purchasingTaxCtrl.getSingleCompanyPTReceipt`
- **Description**: Retrieves a purchase tax receipt for a specific company by ID.

## Error Handling

All endpoints follow standard HTTP status codes for success and error responses:

- 200 - OK: The request was successful
- 400 - Bad Request: The request contains invalid parameters
- 401 - Unauthorized: Authentication is required
- 403 - Forbidden: The authenticated user doesn't have necessary permissions
- 404 - Not Found: The requested resource was not found
- 500 - Internal Server Error: An unexpected error occurred on the server

## Request Examples

### Create Company Info

```json
POST /createCompanyInfo
Headers: 
  Authorization: Bearer <token>

Body:
{
  "companyInfo": {
    "esbn": "3472300125123",
    "email": "admin12@gmail.com",
    "filingMode":"Period",
    "billYear":"2024",
    "name": "Admin Record",
    "phone": "09085859594",
    "sector": "00012",
    "address": "35 abba street",
    "discount": 700,
    "discountReason": "test purpose",
    "outstanding": 600,
    "outstandingReason": "test",
    "totalProductAmount": 0,
    "totalVatAmount": 0,
    "fileType": "Unit Filling",
    "startDate":"2024-05-10",
    "endDate":"2024-06-10"
  },
  "categories": [
    {
      "Category": "Electronics",
      "Product": "Smartphone",
      "Purchases_Amount": 5000,
      "Transaction_Date": "2024-01-01",
      "Status": "Paid",
      "PT_Rate": 7.5,
      "RevenueCode":"00011",
      "Bill_Amount": 375
    },
    {
      "Category": "Furniture",
      "Product": "Office Chair",
      "Purchases_Amount": 1500,
      "Transaction_Date": "2024-02-28",
      "Status": "Pending",
      "PT_Rate": 7.5,
      "RevenueCode":"00012",
      "Bill_Amount": 12
    },
    {
      "Category": "Clothing",
      "Product": "Jacket",
      "Purchases_Amount": 800,
      "Transaction_Date": "2024-03-31",
      "Status": "Paid",
      "PT_Rate": 7.5,
      "RevenueCode":"00013",
      "Bill_Amount": 6
    },
    {
      "Category": "Beauty",
      "Product": "Skincare Set",
      "Purchases_Amount": 300,
      "Transaction_Date": "2024-04-01",
      "Status": "Overdue",
      "PT_Rate": 7.5,
      "RevenueCode":"00014",
      "Bill_Amount": 2
    }
  ],
  "files": [
    {
      "fileName": "fileDoc.pdf",
      "fileType": "pdf",
      "File": "data:application/pdf;base64,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MSAwIG9iago8PC9UeXBlIC9QYWdlcwovS2lkcyBbMyAwIFIgNSAwIFIgXQovQ291bnQgMgovTWVkaWFCb3ggWzAgMCA1OTUuMjggODQxLjg5XQo+PgplbmRvYmoKNyAwIG9iago8PC9UeXBlIC9Gb250Ci9CYXNlRm9udCAvSGVsdmV0aWNhLUJvbGQKL1N1YnR5cGUgL1R5cGUxCi9FbmNvZGluZyAvV2luQW5zaUVuY29kaW5nCj4+CmVuZG9iago4IDAgb2JqCjw8L1R5cGUgL0ZvbnQKL0Jhc2VGb250IC9IZWx2ZXRpY2EKL1N1YnR5cGUgL1R5cGUxCi9FbmNvZGluZyAvV2luQW5zaUVuY29kaW5nCj4+CmVuZG9iagoyIDAgb2JqCjw8Ci9Qcm9jU2V0IFsvUERGIC9UZXh0IC9JbWFnZUIgL0ltYWdlQyAvSW1hZ2VJXQovRm9udCA8PAovRjEgNyAwIFIKL0YyIDggMCBSCj4+Ci9YT2JqZWN0IDw8Cj4+Cj4+CmVuZG9iago5IDAgb2JqCjw8Ci9Qcm9kdWNlciAoUHlGUERGIDEuNy4yIGh0dHA6Ly9weWZwZGYuZ29vZ2xlY29kZS5jb20vKQovQ3JlYXRpb25EYXRlIChEOjIwMjQxMDE5MDY1NTAyKQo+PgplbmRvYmoKMTAgMCBvYmoKPDwKL1R5cGUgL0NhdGFsb2cKL1BhZ2VzIDEgMCBSCi9PcGVuQWN0aW9uIFszIDAgUiAvRml0SCBudWxsXQovUGFnZUxheW91dCAvT25lQ29sdW1uCj4+CmVuZG9iagp4cmVmCjAgMTEKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAxODAwIDAwMDAwIG4gCjAwMDAwMDIwOTAgMDAwMDAgbiAKMDAwMDAwMDAwOSAwMDAwMCBuIAowMDAwMDAwMDg3IDAwMDAwIG4gCjAwMDAwMDA5NjQgMDAwMDAgbiAKMDAwMDAwMTA0MiAwMDAwMCBuIAowMDAwMDAxODkzIDAwMDAwIG4gCjAwMDAwMDE5OTQgMDAwMDAgbiAKMDAwMDAwMjIwNCAwMDAwMCBuIAowMDAwMDAyMzEzIDAwMDAwIG4gCnRyYWlsZXIKPDwKL1NpemUgMTEKL1Jvb3QgMTAgMCBSCi9JbmZvIDkgMCBSCj4+CnN0YXJ0eHJlZgoyNDE3CiUlRU9GCg=="
    }
  ]
}
```

### Calculate Tax

```json
POST /calculateTax
Headers:
  Authorization: Bearer <token>

Body:
{
  "discount": 700,
  "outstanding": 700,
  "products": [
    {
      "Product": "goods",
      "Bill_Amount": 400,
      "Transaction_Date": "2025-02-09",
      "Purchases_Amount": 8000,
      "Status": "",
      "PT_Rate": 5,
      "Category": "Cement",
      "RevenueCode": "PT-0009"
    },
    {
      "Product": "goods",
      "Bill_Amount": 6300,
      "Transaction_Date": "2025-02-09",
      "Purchases_Amount": 700,
      "Status": "",
      "PT_Rate": 900,
      "Category": "business admin",
      "RevenueCode": "0003445/559044"
    }
  ]
}
```

## Response Examples

### Get All Company Info

```json
GET /getAllCompanyInfo
Headers:
  Authorization: Bearer <token>

Response:
{
  "success": true,
  "count": 2,
  "data": [
    {
      "id": "comp123",
      "companyName": "First Corp",
      "registrationNumber": "REG123",
      "taxId": "TAX123",
      "address": { ... },
      "contactPerson": { ... },
      "createdAt": "2025-01-10T12:00:00Z",
      "updatedAt": "2025-02-01T09:30:00Z"
    },
    {
      "id": "comp456",
      "companyName": "Second Corp",
      "registrationNumber": "REG456",
      "taxId": "TAX456",
      "address": { ... },
      "contactPerson": { ... },
      "createdAt": "2025-01-15T14:20:00Z",
      "updatedAt": "2025-01-15T14:20:00Z"
    }
  ]
}
```

### Calculate Tax

```json
POST /calculateTax
Headers:
  Authorization: Bearer <token>

Response:
{
  "success": true,
  "data": {
    "purchaseAmount": 1000.00,
    "taxRate": 0.08,
    "taxAmount": 80.00,
    "totalAmount": 1080.00,
    "calculationDate": "2025-02-18T10:15:30Z",
    "receiptId": "rcpt789"
  }
}
```

## Notes

- The commented endpoint (`updatePaymentStatus/:id`) is not currently active.
- File uploads for bulk tax calculations should be in an appropriate format (CSV, Excel, etc.).
- Authentication tokens are expected to be included in the Authorization header using the Bearer scheme.
