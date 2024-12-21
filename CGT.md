### * **Create CGT Company Information**

* **Endpoint** : `POST /createCGTCompanyInfo`
* **Description** : Creates a new CGT company information record along with property details.

```json
{
  "companyInfo": {
    "filingType": "Unit Filling",
    "filingMode":"Monthly",
    "name":"Frank Admin",
    "esbn": "ES3559087686543",
    "billYear":"2024",
    "billMonth":"november",
    "email": "admin@test.com",
    "phone": "09085859594",
    "address": "35 abba street",
    "sector": "00012",
    "startDate": "2024-02-01",
    "endDate": "2024-02-28",
    "discount": 700,
    "discountReason": "test purpose",
    "outstanding": 600,
    "outstandingReason": "test",
    "remark":"remark"
  },
  "propertyDetails": [
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":500,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":1000,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":2500,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":5000,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    }
  ],
  "files": [
    {
      "File": "data:application/pdf;base64,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MSAwIG9iago8PC9UeXBlIC9QYWdlcwovS2lkcyBbMyAwIFIgNSAwIFIgXQovQ291bnQgMgovTWVkaWFCb3ggWzAgMCA1OTUuMjggODQxLjg5XQo+PgplbmRvYmoKNyAwIG9iago8PC9UeXBlIC9Gb250Ci9CYXNlRm9udCAvSGVsdmV0aWNhLUJvbGQKL1N1YnR5cGUgL1R5cGUxCi9FbmNvZGluZyAvV2luQW5zaUVuY29kaW5nCj4+CmVuZG9iago4IDAgb2JqCjw8L1R5cGUgL0ZvbnQKL0Jhc2VGb250IC9IZWx2ZXRpY2EKL1N1YnR5cGUgL1R5cGUxCi9FbmNvZGluZyAvV2luQW5zaUVuY29kaW5nCj4+CmVuZG9iagoyIDAgb2JqCjw8Ci9Qcm9jU2V0IFsvUERGIC9UZXh0IC9JbWFnZUIgL0ltYWdlQyAvSW1hZ2VJXQovRm9udCA8PAovRjEgNyAwIFIKL0YyIDggMCBSCj4+Ci9YT2JqZWN0IDw8Cj4+Cj4+CmVuZG9iago5IDAgb2JqCjw8Ci9Qcm9kdWNlciAoUHlGUERGIDEuNy4yIGh0dHA6Ly9weWZwZGYuZ29vZ2xlY29kZS5jb20vKQovQ3JlYXRpb25EYXRlIChEOjIwMjQxMDE5MDY1NTAyKQo+PgplbmRvYmoKMTAgMCBvYmoKPDwKL1R5cGUgL0NhdGFsb2cKL1BhZ2VzIDEgMCBSCi9PcGVuQWN0aW9uIFszIDAgUiAvRml0SCBudWxsXQovUGFnZUxheW91dCAvT25lQ29sdW1uCj4+CmVuZG9iagp4cmVmCjAgMTEKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAxODAwIDAwMDAwIG4gCjAwMDAwMDIwOTAgMDAwMDAgbiAKMDAwMDAwMDAwOSAwMDAwMCBuIAowMDAwMDAwMDg3IDAwMDAwIG4gCjAwMDAwMDA5NjQgMDAwMDAgbiAKMDAwMDAwMTA0MiAwMDAwMCBuIAowMDAwMDAxODkzIDAwMDAwIG4gCjAwMDAwMDE5OTQgMDAwMDAgbiAKMDAwMDAwMjIwNCAwMDAwMCBuIAowMDAwMDAyMzEzIDAwMDAwIG4gCnRyYWlsZXIKPDwKL1NpemUgMTEKL1Jvb3QgMTAgMCBSCi9JbmZvIDkgMCBSCj4+CnN0YXJ0eHJlZgoyNDE3CiUlRU9GCg=="
    }
  ]
}

```

### * Get All CGT Company Information

* **Endpoint** : `GET /getAllCGTCompanyInfo`
* **Description** : Retrieves all CGT company records.

### **Create CGT Setup**

* **Endpoint** : `POST /createCGTSetUp`
* **Description** : Creates a new CGT setup record.

```json
{
  "type": "Goods",
  "name": "Toyota Camry",
  "code": "0003",
  "rate": 7.5,
  "revenue": "Test Revenue",
  "tariff": "test traiff",
  "description": "Test Description"
}
```

4. Get Active CGT Setups
   * **Endpoint** : `GET /getActiveCGTSetUps`
   * **Description** : Retrieves all active CGT setups.
5. Get All CGT Setups
   * **Endpoint** : `GET /getAllCGTSetup`
   * **Description** : Retrieves all CGT setup records.
6. Get CGT Company Information Record
   * **Endpoint** : `GET /getCGTCompanyInfoRecord/:id`
   * **Description** : Retrieves a single CGT company information record by ID.
7. Get CGT Receipt
   * **Endpoint** : `GET /getCGTReceipt/:id`
   * **Description** : Retrieves a CGT receipt by ID.
8. Update CGT Setup
   * **Endpoint** : `PUT /updateCGTSetUp/:id`
   * **Description** : Updates a CGT setup record by ID.

```json
{
  "type": "Goods",
  "name": "Toyota Camry",
  "code": "0003",
  "rate": 7.5,
  "revenue": "Test Revenue",
  "tariff": "test traiff",
  "description": "Test Description"
}
```

9. Deactivate CGT Setup Record
   * **Endpoint** : `DELETE /deactivateCGTSetUpRecord/:id`
   * **Description** : Deactivates a CGT setup record by ID.
10. Activate CGT Setup Record
    * **Endpoint** : `PATCH /activateCGTSetUpRecord/:id`
    * **Description** : Activates a CGT setup record by ID.
11. Delete CGT Company Information Record
    * **Endpoint** : `DELETE /deleteCGTCompanyInfoRecord/:id`
    * **Description** : Deletes a CGT company information record by ID.
12. Calculate CGT Tax
    * **Endpoint** : `POST /calculateCGTax`
    * **Description** : Calculates CGT tax.

```json
[
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":500,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":1000,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":2500,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":5000,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    }
  ][
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":500,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":1000,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":2500,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    },
    {
      "TypeOfCGT": "Electronics",
      "TypeOfProperty": "Smartphone",
      "AquisitionAmount": 5000,
      "CurrentMarketValue":200,
      "CGTRate":10,
      "SalesAmount":180,
      "Profit":5000,
      "AquisitionDate": "2024-01-01",
      "SaleDate": "2024-01-01",
      "PropertyLocation": "Lagos",
      "PropertyNature": "New"
    }
  ]
```
