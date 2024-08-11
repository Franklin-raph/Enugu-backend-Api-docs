### 1. Get Reducing Balance Receipt Information
- **Endpoint** `POST /getReducingBalReceiptInfo`
```json
{
  "receiptId": "string"
}
```
- **Description:** Retrieves reducing balance receipt information.


### 2. Create Tax Information
- **Endpoint** `POST /createTaxInfo`
```json
{
  "taxInfo": {
    // Tax information fields here
  }
}
```
- **Description:** Creates a new tax information record.


### 3. Create Tax Payer Information
- **Endpoint** `POST /createTaxPayerInfo`
```json
{
  "taxPayerInfo": {
    // Taxpayer information fields here
  }
}
```
- **Description:** Creates a new taxpayer information record.

### 4. Get Reducing Balance Details by ID
- **Endpoint** `GET /getReducingBalanceDetails/:id`
```json
{
  "receiptDetails": {
    // Receipt details here
  }
}
```
- **Description:** Retrieves the reducing balance receipt information by ID.


### 5. Get Single Tax Information by ID
- **Endpoint** `GET /getReducingTaxInfo/:id`
```json
{
  "taxInfo": {
    // Tax information fields here
  }
}
```
- **Description:** Retrieves single tax information by ID.


### 6. Update Tax Information by ID
- **Endpoint** `PUT /updateTaxInfo/:id`
```json
{
  "taxInfo": {
    // Updated tax information fields here
  }
}
```
- **Description:** Updates the tax information record by ID.


### 7. Update Tax Payer Information by ID
- **Endpoint** `PUT /updateTaxPayerInfo/:id`
```json
{
  "taxPayerInfo": {
    // Updated taxpayer information fields here
  }
}
```
- **Description:** Updates the taxpayer information record by ID.


### 8. Delete Tax Information Record by ID
- **Endpoint** `DELETE /deleteTaxInfoRecord/:id`
```json
{
  "message": "Tax information record deleted successfully"
}
```
- **Description:** Deletes the tax information record by ID.


### 9. Delete Tax Payer Information Record by ID
- **Endpoint** `DELETE /deleteTaxPayerInfoRecord/:id`
```json
{
  "message": "Taxpayer information record deleted successfully"
}
```
- **Description:** Deletes the taxpayer information record by ID.


### 10. Get Single Tax Payer Information by ID
- **Endpoint** `GET /getTaxPayerInfo/:id`
```json
{
  "taxPayerInfo": {
    // Taxpayer information fields here
  }
}
```
- **Description:** Retrieves single taxpayer information by ID.