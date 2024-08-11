### 1. Get Reducing Balance Receipt Information
- **Endpoint** `POST /getReducingBalReceiptInfo`
- **Description:** Retrieves reducing balance receipt information.
```json
{
  "receiptId": "string"
}
```


### 2. Create Tax Information
- **Endpoint** `POST /createTaxInfo`
- **Description:** Creates a new tax information record.
```json
{
  "taxInfo": {
    // Tax information fields here
  }
}
```


### 3. Create Tax Payer Information
- **Endpoint** `POST /createTaxPayerInfo`
- **Description:** Creates a new taxpayer information record.
```json
{
  "taxPayerInfo": {
    // Taxpayer information fields here
  }
}
```

### 4. Get Reducing Balance Details by ID
- **Endpoint** `GET /getReducingBalanceDetails/:id`
- **Description:** Retrieves the reducing balance receipt information by ID.
```json
{
  "receiptDetails": {
    // Receipt details here
  }
}
```


### 5. Get Single Tax Information by ID
- **Endpoint** `GET /getReducingTaxInfo/:id`
- **Description:** Retrieves single tax information by ID.
```json
{
  "taxInfo": {
    // Tax information fields here
  }
}
```


### 6. Update Tax Information by ID
- **Endpoint** `PUT /updateTaxInfo/:id`
- **Description:** Updates the tax information record by ID.
```json
{
  "taxInfo": {
    // Updated tax information fields here
  }
}
```


### 7. Update Tax Payer Information by ID
- **Endpoint** `PUT /updateTaxPayerInfo/:id`
- **Description:** Updates the taxpayer information record by ID.
```json
{
  "taxPayerInfo": {
    // Updated taxpayer information fields here
  }
}
```


### 8. Delete Tax Information Record by ID
- **Endpoint** `DELETE /deleteTaxInfoRecord/:id`
- **Description:** Deletes the tax information record by ID.
```json
{
  "message": "Tax information record deleted successfully"
}
```


### 9. Delete Tax Payer Information Record by ID
- **Endpoint** `DELETE /deleteTaxPayerInfoRecord/:id`
- **Description:** Deletes the taxpayer information record by ID.
```json
{
  "message": "Taxpayer information record deleted successfully"
}
```


### 10. Get Single Tax Payer Information by ID
- **Endpoint** `GET /getTaxPayerInfo/:id`
- **Description:** Retrieves single taxpayer information by ID.
```json
{
  "taxPayerInfo": {
    // Taxpayer information fields here
  }
}
```