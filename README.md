---

# Manual Reconciliation Data API Endpoints

Base Url 

## API Endpoints

- **POST /signup**

  Register a new user.

  Request Body:

  ```json
  {
    "email": "user@example.com",
    "username":"Jogn",
    "password": "password"
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

