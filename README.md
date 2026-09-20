# 🧪 API Testing - Platzi Fake Store API (Postman Project)

This project showcases an **API Testing and Automation workflow** using **Postman** to test the **Platzi Fake Store API**.

The project focuses on testing several API resources, including **Categories, Users, Products, and Locations**, with automated JavaScript assertions to validate API responses.

---

## 📚 Project Overview

The purpose of this project is to demonstrate practical **API Testing and Automation skills** using Postman.

The collection covers:

- Testing REST API endpoints
- Testing `GET`, `POST`, and `PUT` requests
- Validating HTTP status codes
- Validating API response times
- Validating response body content
- Validating JSON response properties
- Validating created and updated data
- Creating automated assertions using Postman

---

## 🚀 Features Tested

| Feature | Method | Endpoint |
|---|:---:|---|
| Get All Categories | GET | `/categories` |
| Create Category | POST | `/categories` |
| Update Category | PUT | `/categories/:id` |
| Get Category by ID | GET | `/categories/:id` |
| Get Category by Slug | GET | `/categories/slug/:slug` |
| Get All Users | GET | `/users` |
| Create User | POST | `/users` |
| Update User | PUT | `/users/:id` |
| Get User by ID | GET | `/users/:id` |
| Create Product | POST | `/products` |
| Get All Products | GET | `/products` |
| Get Product by ID | GET | `/products/:id` |
| Get All Locations | GET | `/locations` |

---

## 🌐 API Under Test

**Platzi Fake Store API**

The API provides REST endpoints for managing:

- Products
- Categories
- Users
- Locations

Base URL:

```text
https://api.escuelajs.co/api/v1
```
## 🧰 Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| **Postman** | API testing and automation |
| **JavaScript** | Writing automated test scripts |
| **REST API** | API architecture under test |
| **JSON** | Request and response data format |
| **Git & GitHub** | Version control and portfolio documentation |

---

## 🧪 Automated Assertions

The project uses JavaScript test scripts in Postman to validate API responses.

### Status Code Validation

    pm.test("Status code is 200", function () {
        pm.response.to.have.status(200);
    });

### Response Time Validation

    pm.test("Response time is below 1000ms", function () {
        pm.expect(pm.response.responseTime).to.be.below(1000);
    });

### Response Body Validation

    pm.test("Response body contains Electronics", function () {
        pm.expect(pm.response.text()).to.include("Electronics");
    });

### JSON Property Validation

    pm.test("Response has ID", function () {
        const response = pm.response.json();

        pm.expect(response).to.have.property("id");
    });

### Specific Value Validation

    pm.test("Category ID is correct", function () {
        const response = pm.response.json();

        pm.expect(response.id).to.eql(199);
    });

---

## 📝 API Test Case Examples

| TC ID | Scenario | Method | Endpoint | Expected Status | Expected Result |
|---|---|---|---|---:|---|
| TC-001 | Get all categories | GET | `/categories` | 200 | List of categories is returned |
| TC-002 | Create new category | POST | `/categories` | 201 | New category is created |
| TC-003 | Update category | PUT | `/categories/199` | 200 | Category is updated successfully |
| TC-004 | Get category by ID | GET | `/categories/199` | 200 | Correct category data is returned |
| TC-005 | Get category by slug | GET | `/categories/slug/electronics` | 200 | Category data is returned |
| TC-006 | Get all users | GET | `/users` | 200 | List of users is returned |
| TC-007 | Create new user | POST | `/users` | 201 | New user is created |
| TC-008 | Update user | PUT | `/users/234` | 200 | User is updated successfully |
| TC-009 | Get user by ID | GET | `/users/1` | 200 | Correct user data is returned |
| TC-010 | Create new product | POST | `/products` | 201 | New product is created |
| TC-011 | Get all products | GET | `/products` | 200 | List of products is returned |
| TC-012 | Get product by ID | GET | `/products/38` | 200 | Correct product data is returned |
| TC-013 | Get all locations | GET | `/locations` | 200 | Location data is returned |

---

## 🔍 Validation Coverage

| Validation | Description |
|---|---|
| Status Code | Verifies the API returns the expected HTTP status |
| Response Time | Verifies the API responds within the defined threshold |
| Response Body | Verifies expected data exists in the response |
| JSON Property | Verifies required properties such as `id` and `slug` |
| Specific Value | Verifies returned values match expected data |
| Create Validation | Verifies newly created data is returned correctly |
| Update Validation | Verifies updated data is returned correctly |

---

## 💻 How to Run

### 1. Import Collection

Open **Postman** and import the Postman collection.

### 2. Configure Environment

Set the API base URL using the Postman environment variable:

    {{base_urlPlatzi}}

Example:

    https://api.escuelajs.co/api/v1

### 3. Run the Collection

In Postman:

    Collections
        ↓
    sanbercode- Automation API
        ↓
    Run Collection

### 4. Review Test Results

After running the collection, Postman displays:

- Passed assertions
- Failed assertions
- Response status
- Response time
- Request results

---

## 🎯 Testing Scope

### Categories

- Get all categories
- Create category
- Update category
- Get category by ID
- Get category by slug

### Users

- Get all users
- Create user
- Update user
- Get user by ID

### Products

- Get all products
- Create product
- Get product by ID

### Locations

- Get all locations

---

## 👨‍💻 Author

**Muhammad Resandi Sholahuddin**

---

