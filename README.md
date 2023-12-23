---

# Manual Reconciliation Data API Endpoints
<h3>Base Url</h3>
<p>https://enugutest1-zwbxjl4eea-uc.a.run.app/api/</p>

## API Endpoints
```http
GET /manualRecon/getAllManualReconRecords
```
```json
{
  "message": "Manual Reconciliation details retrieved",
  "data": [
    {
      "id": "16eb5238-0013-44fc-aa81-79a9e29b6f01",
      "esbn": "222222",
      "billNumber": "334344",
      "customerName": "Franklin Raphael Edu",
      "depositorsPhone": "08139362969",
      "depositorsRcNumber": "124578",
      "totalAmountPaid": "10,000",
      "paymentMethod": "transfer",
      "paymentDate": "2023-11-26T00:00:00.000Z",
      "branchName": "Lagos Branch",
      "depositSlipNumber": "123456",
      "paymentRefNumber": "123456",
      "receiptNumber": "12345556",
      "revenue": "Land Use Charge",
      "approveRejectFlag": 2,
      "approveRejectReason": "Invalid Document",
      "inputter": "Raphael",
      "authoriser": "Edward",
      "lastModifiedBy": "41611cbc-e1c5-4e0a-9152-64c655c6f0d0",
      "lastModifiedByTime": "2023-11-28 09:02:53",
      "inputterTime": "2023-11-28T08:56:42.000Z",
      "AuthoriserTime": "2023-11-28T09:42:15.000Z"
    },
    {
      "id": "53e476f4-dde4-40e6-84fe-79018c8f27c6",
      "esbn": "222222",
      "billNumber": "334344",
      "customerName": "Rahael",
      "depositorsPhone": "08139362969",
      "depositorsRcNumber": "124578",
      "totalAmountPaid": "10,000",
      "paymentMethod": "cash",
      "paymentDate": "2023-11-26T00:00:00.000Z",
      "branchName": "Enugu Branch",
      "depositSlipNumber": "123456",
      "paymentRefNumber": "123456",
      "receiptNumber": "12345556",
      "revenue": "Land Use Charge",
      "approveRejectFlag": 2,
      "approveRejectReason": "Document is fraudulent",
      "inputter": "Raphael",
      "authoriser": "Frank",
      "lastModifiedBy": "41611cbc-e1c5-4e0a-9152-64c655c6f0d0",
      "lastModifiedByTime": "2023-11-28 09:55:39",
      "inputterTime": "2023-11-28T09:53:50.000Z",
      "AuthoriserTime": "2023-11-28T10:23:42.000Z"
    },
    {
      "id": "674fae98-6d58-4fe5-aece-59d6fd9d2474",
      "esbn": "222222",
      "billNumber": "334344",
      "customerName": "Franklin Raphael Edu",
      "depositorsPhone": "08139362969",
      "depositorsRcNumber": "124578",
      "totalAmountPaid": "10,000",
      "paymentMethod": "transfer",
      "paymentDate": "2023-11-26T00:00:00.000Z",
      "branchName": "Lagos Branch",
      "depositSlipNumber": "123456",
      "paymentRefNumber": "123456",
      "receiptNumber": "12345556",
      "revenue": "Land Use Charge",
      "approveRejectFlag": 1,
      "approveRejectReason": "An invalid document",
      "inputter": "Raphael",
      "authoriser": "Frank Ralph",
      "lastModifiedBy": "41611cbc-e1c5-4e0a-9152-64c655c6f0d0",
      "lastModifiedByTime": null,
      "inputterTime": "2023-11-28T09:45:12.000Z",
      "AuthoriserTime": "2023-11-29T15:27:00.000Z"
    }
  ],
  "description": {
    "status": 200,
    "description": "successful",
    "code": "ANSP-2000",
    "range": "2000 - 2019"
  }
}
```
> Get all manual reconciliation records


```http
GET /getAManualReconRecord/:id
```
```json
{
  "message": "Record retrieved successfully",
  "data": {
    "id": "674fae98-6d58-4fe5-aece-59d6fd9d2474",
    "esbn": "222222",
    "billNumber": "334344",
    "customerName": "Franklin Raphael Edu",
    "depositorsPhone": "08139362969",
    "depositorsRcNumber": "124578",
    "totalAmountPaid": "10,000",
    "paymentMethod": "transfer",
    "paymentDate": "2023-11-26T00:00:00.000Z",
    "branchName": "Lagos Branch",
    "depositSlipNumber": "123456",
    "paymentRefNumber": "123456",
    "receiptNumber": "12345556",
    "revenue": "Land Use Charge",
    "approveRejectFlag": 1,
    "approveRejectReason": "An invalid document",
    "inputter": "Raphael",
    "authoriser": "Frank Ralph",
    "lastModifiedBy": "41611cbc-e1c5-4e0a-9152-64c655c6f0d0",
    "lastModifiedByTime": null,
    "inputterTime": "2023-11-28T09:45:12.000Z",
    "AuthoriserTime": "2023-11-29T15:27:00.000Z"
  },
  "description": {
    "status": 200,
    "description": "successful",
    "code": "ANSP-2000",
    "range": "2000 - 2019"
  }
}
```
> Get a manual reconciliation record by Id


```http
POST /manualRecon/createRecords
```

  Request Body:

  ```json
    {
      "esbn": "222222",
      "billNumber": "334344",
      "customerName": "Franklin Raphael Edu",
      "depositorsPhone": "08139362969",
      "depositorsRcNumber": "124578",
      "totalAmountPaid": "10,000",
      "paymentMethod": "transfer",
      "paymentDate": "2023-11-26",
      "branchName": "Lagos Branch",
      "depositSlipNumber": "123456",
      "paymentRefNumber": "123456",
      "receiptNumber": "12345556",
      "revenue": "Land Use Charge",
      "approveRejectFlag": 2,
      "approveRejectReason": "Invalid Document",
      "inputter": "Raphael",
      "authoriser": "Edward"
    }
  ```
  > Register a new manual reconciliation record.


```http
PUT /manualRecon/updateManualReconRecord/:id
```
  Request Body:

  ```json
    {
      "esbn": "22245",
      "billNumber": "334344",
      "customerName": "Franklin Raphael Edu",
      "depositorsPhone": "08139362969",
      "depositorsRcNumber": "124578",
    }
  ```
  > update a manual reconciliation record.


```http
PATCH /authorizeManualReconRecord/:id
```
```json
{
  "approveRejectFlag":1,
  "authoriser":"Frank Ralph",
  "approveRejectReason":"An invalid document"
}
```
> Update a manual reconciliation record by Id


```http
DELETE /authorizeManualReconRecord/:id
```
> Delete a manual reconciliation record by Id
