- **Endpoint** `POST /getReducingBalReceiptInfo`
```json
{
  "receiptId": "string"
}
```
- **Description:** Retrieves reducing balance receipt information.



- **Endpoint** `POST /createTaxInfo`
```json
{
  "taxInfo": {
    // Tax information fields here
  }
}
```
- **Description:** Creates a new tax information record.


- **Endpoint** `POST /createTaxPayerInfo`
```json
{
  "taxPayerInfo": {
    // Taxpayer information fields here
  }
}
```
- **Description:** Creates a new taxpayer information record.


- **Endpoint** `GET /getReducingBalanceDetails/:id`
```json
{
  "receiptDetails": {
    // Receipt details here
  }
}
```
- **Description:** Retrieves the reducing balance receipt information by ID.



- **Endpoint** `GET /getReducingTaxInfo/:id`
```json
{
  "taxInfo": {
    // Tax information fields here
  }
}
```
- **Description:** Retrieves single tax information by ID.



- **Endpoint** `PUT /updateTaxInfo/:id`
```json
{
  "taxInfo": {
    // Updated tax information fields here
  }
}
```
- **Description:** Updates the tax information record by ID.



- **Endpoint** `PUT /updateTaxPayerInfo/:id`
```json
{
  "taxPayerInfo": {
    // Updated taxpayer information fields here
  }
}
```
- **Description:** Updates the taxpayer information record by ID.



- **Endpoint** `DELETE /deleteTaxInfoRecord/:id`
```json
{
  "message": "Tax information record deleted successfully"
}
```
- **Description:** Deletes the tax information record by ID.


- **Endpoint** `DELETE /deleteTaxPayerInfoRecord/:id`
```json
{
  "message": "Taxpayer information record deleted successfully"
}
```
- **Description:** Deletes the taxpayer information record by ID.



- **Endpoint** `GET /getTaxPayerInfo/:id`
```json
{
  "taxPayerInfo": {
    // Taxpayer information fields here
  }
}
```
- **Description:** Retrieves single taxpayer information by ID.