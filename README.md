---

# Manual Reconciliation Data API Endpoints
<h3>Base Url</h3>
<p>https://enugutest1-zwbxjl4eea-uc.a.run.app/api/</p>

## API Endpoints
```http
GET /manualRecon/getAllManualReconRecords
```
> Get all manual reconciliation records


```http
GET /getAManualReconRecord/:id
```
> Get a manual reconciliation record by Id


```http
POST /manualRecon/createRecords
```
> Register a new manual reconciliation record.

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

```http
PUT /manualRecon/updateManualReconRecord/:id
```
> update a manual reconciliation record.

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


```http
PATCH /authorizeManualReconRecord/:id
```
> Update a manual reconciliation record by Id


```http
DELETE /authorizeManualReconRecord/:id
```
> Delete a manual reconciliation record by Id
