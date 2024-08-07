
---

## Test Endpoints Documentation

### GET /navigations

#### Description
Fetches the list of navigations.

#### Request

- **Method:** `GET`
- **URL:** `/navigations`
- **Headers:**
  - `Content-Type: application/json`
  - `Authorization: Bearer <token>`


- **Failure:**
  - **Status Code:** `401 Unauthorized`
  
  - **Status Code:** `500 Internal Server Error`
  

---

### POST /verify-code

#### Description
Verifies the given code for a user identified by their identification number.

#### Request

- **Method:** `POST`
- **URL:** `/verify-code`
- **Body:**
  ```json
  {
    "identification_number": "string",
    "code": "string"
  }
  ```
- **Headers:**
  - `Content-Type: application/json`

#### Response

- **Success:**
  - **Status Code:** `200 OK`
  - **Body:**
    ```json
    {
     {
    "success": true,
    "code": "success",
    "status": 200,
    "result": {
    ....
    }
    }
    ```
- **Failure:**
  - **Status Code:** `400 Bad Request`
  - **Body:**
    ```json
    {
     
    }
    ```
  - **Status Code:** `500 Internal Server Error`
  - **Body:**
    ```json
    {
     
    }
    ```

---

### POST /find-user

#### Description
Finds a user by their identification number.

#### Request

- **Method:** `POST`
- **URL:** `/find-user`
- **Body:**
  ```json
  {
    "identification_number": "string"
  }
  ```
- **Headers:**
  - `Content-Type: application/json`

#### Response

- **Success:**
  - **Status Code:** `200 OK`
  - **Body:**
    ```json
   {
    "success": true,
    "code": "success",
    "status": 200,
    "result":
  }
    ```
- **Failure:**
  - **Status Code:** `404 Not Found`
  - **Body:**
    ```json
    {
      "error": "User not found."
    }
    ```


---

### POST /signin

#### Description
Signs in a user with their email and password.

#### Request

- **Method:** `POST`
- **URL:** `/signin`
- **Body:**
  ```json
  {
    "email": "string",
    "password": "string"
  }
  ```
- **Headers:**
  - `Content-Type: application/json`

#### Response

- **Success:**
  - **Status Code:** `200 OK`
  - **Body:**
    ```json
    {
    "success": true,
    "code": "success",
    "status": 200,
    "result": {
    ....
    }
    }
    ```

---
