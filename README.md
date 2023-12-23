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


- **POST /login**

  User login.

  Request Body:

  ```json
  {
    "email": "user@example.com",
    "password": "password"
  }
  ```
- **PUT /update-profile/:id**

  Uodate profile.

  Request Body:

  ```json
  {
    "username":"Jogn",
    "password": "password",
    "new_password":"new_password"
  }
  ```
   ```
- **PUT /uploads/update-pic/:id**

  Uodate profile image.

- **GET /**

  Get all todos for the un-authenticated user.
 
- **GET /tasks**

  Get all todos for the authenticated user.

- **POST /add-todo**

  Create a new todo.

  Request Body:

  ```json
  {
    "title": "Task Title",
  }
  ```

- **PUT /tasks/:id**

  Update a todo by ID.

  Request Body:

  ```json
  {
    "title": "Updated Task Title",
  }
  ```

- **DELETE /tasks/:id**

  Delete a todo by ID.

## Libraries and Technologies Used

- [Express.js](https://expressjs.com/) - Web application framework for Node.js
- [bcrypt](https://www.npmjs.com/package/bcrypt) - Password hashing library
- [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken) - JSON Web Token implementation
- [mongoose](https://mongoosejs.com/) - MongoDB object modeling tool
- [nodemailer](https://nodemailer.com/) - Email sending library
- [dotenv](https://www.npmjs.com/package/dotenv) - Environment variable management
- [cors](https://www.npmjs.com/package/cors) - Cross-origin resource sharing middleware
- [multer](https://www.npmjs.com/package/multer) - Middleware for handling `multipart/form-data`

