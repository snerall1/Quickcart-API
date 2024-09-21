# Quickcart-API

Welcome to QuickCart API! This application offers a variety of endpoints for managing users, products, reviews, and orders in an online shopping environment. Built with a focus on simplicity, security, and efficiency, this API encourages you to explore its essential features that facilitate smooth e-commerce interactions!

Table of Contents
Introduction
Features
Installation
Usage
API Endpoints
Security
Documentation
API Documentation
Postman Documentation
Useful Takeaways
Introduction
This Express.js application serves as the backend for an e-commerce platform, drawing inspiration from John Smilga's insightful Node.js course. It enables users to register, log in, browse products, submit reviews, and place orders. The API is designed to be secure, scalable, and user-friendly.

Features
User authentication and authorization.
CRUD operations for users, products, reviews, and orders.
File upload capabilities for product images.
Enhanced security measures, including rate limiting, helmet protection, and data sanitization.
Comprehensive error handling and logging for improved debugging.
Installation
Clone the repository: git clone https://github.com/edriso/ecommerce-api.git
Install dependencies: npm install
Rename the .env.example file to .env.
Open the .env file and configure the specified environment variables.
Usage
To start the server, execute the following command:

bash
Copy code
npm start
The server will launch on the designated port (default: 5000 if not modified in the .env file).

API Endpoints
Authentication:
POST /api/v1/auth/register - Register a new user.
POST /api/v1/auth/login - Log in a user.
GET /api/v1/auth/logout - Log out a user.
Users:
GET /api/v1/users - Retrieve all users (admin only).
GET /api/v1/users/:id - Retrieve a user by ID (admin only).
PUT /api/v1/users/:id - Update a user by ID (admin only).
DELETE /api/v1/users/:id - Remove a user by ID (admin only).
Products:
GET /api/v1/products - Retrieve all products.
GET /api/v1/products/:id - Retrieve a product by ID.
POST /api/v1/products - Add a new product (admin only).
PUT /api/v1/products/:id - Update a product by ID (admin only).
DELETE /api/v1/products/:id - Delete a product by ID (admin only).
Reviews:
GET /api/v1/reviews - Retrieve all reviews.
GET /api/v1/reviews/:id - Retrieve a review by ID.
POST /api/v1/reviews - Add a new review.
PUT /api/v1/reviews/:id - Update a review by ID.
DELETE /api/v1/reviews/:id - Remove a review by ID.
Orders:
GET /api/v1/orders - Retrieve all orders (admin only).
GET /api/v1/orders/:id - Retrieve an order by ID (admin only).
POST /api/v1/orders - Create a new order.
PUT /api/v1/orders/:id - Update an order by ID (admin only).
DELETE /api/v1/orders/:id - Delete an order by ID (admin only).
Security
This API incorporates several security measures, including:

Rate Limiting: Controls the number of requests a client can make within a set time.
Helmet Protection: Adds various HTTP headers to enhance security.
XSS Protection: Sanitizes user input to prevent cross-site scripting attacks.
Data Sanitization: Protects against NoSQL query injection by sanitizing user data.
CORS: Manages Cross-Origin Resource Sharing to control which domains can access the API.
