# **E-Commerce Backend API**

![Express](https://img.shields.io/badge/Express-4.x-green)
![MongoDB](https://img.shields.io/badge/MongoDB-4.x-brightgreen)
![Node.js](https://img.shields.io/badge/Node.js-14.x-blue)
![JWT](https://img.shields.io/badge/JWT-Authentication-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)

## **Table of Contents**

- [Project Overview](#project-overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [Usage](#usage)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## **Project Overview**

The **E-Commerce Backend API** is a comprehensive backend solution designed for managing an e-commerce platform. It provides all the essential functionalities required for running an online store, including user authentication, product management, order processing, payment integration, and more.

This project is built using **Node.js** with **Express** as the web framework and **MongoDB** as the database. The architecture is modular and scalable, making it easy to extend and maintain.

## **Features**

- **User Authentication & Authorization**
  - Role-based access control (Admin, Customer)
  - Secure password hashing and JWT-based authentication

- **Product Management**
  - CRUD operations for products and categories
  - Inventory management and product variants

- **Shopping Cart & Checkout**
  - Persistent shopping cart for users
  - Secure and seamless checkout process

- **Order Management**
  - Order creation, tracking, and history management
  - Integration with payment gateways (Stripe, PayPal)

- **Search & Filtering**
  - Advanced search with filters and sorting options

- **Security & Performance**
  - Secure API endpoints with validation and error handling
  - Performance optimization with caching and background processing

## **Project Structure**

```plaintext
ecommerce-backend/
├── src/
│   ├── auth/                   # Authentication module
│   ├── config/                 # Configuration files
│   ├── controllers/            # Route handlers/controllers
│   ├── middleware/             # Custom middleware
│   ├── models/                 # Database models
│   ├── routes/                 # API routes
│   ├── services/               # Business logic and services
│   ├── utils/                  # Utility functions
│   ├── validators/             # Input validation logic
│   ├── app.js                  # Express app setup
│   └── server.js               # Server entry point
├── .env                        # Environment variables
├── .gitignore                  # Files to ignore in git
├── package.json                # Project dependencies and scripts
└── README.md                   # Project documentation
```

## Installation

To get started with this project, follow the steps below:

1. **Clone the repository:**

    ```bash
    git clone https://github.com/uciboy14/ecommerce-backend-api.git
    cd ecommerce-backend
    ```

2. **Install dependencies:**

    ```bash
    npm install
    ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory with the following variables:

   ```plaintext
   PORT=5000
   DB_CONNECTION_STRING=mongodb://localhost:27017/ecommerce
   JWT_SECRET=your_jwt_secret_key
   STRIPE_SECRET_KEY=your_stripe_secret_key
   ```

4. **Start the development server:***
    
    ```bash
    npm run dev
    ```
## Environment Variables

The project requires the following environment variables:

- `PORT`: The port on which the server will run.
- `DB_CONNECTION_STRING`: The connection string for MongoDB.
- `JWT_SECRET`: The secret key for signing JWT tokens.
- `STRIPE_SECRET_KEY`: Your Stripe API secret key for payment processing.

## API Endpoints

The following are the main API endpoints available in this project:

### Authentication

- `POST /api/auth/register`: Register a new user
- `POST /api/auth/login`: User login
- `POST /api/auth/refresh-token`: Refresh JWT token

### Products

- `GET /api/products`: Get all products
- `GET /api/products/:id`: Get a single product by ID
- `POST /api/products`: Create a new product (Admin)
- `PUT /api/products/:id`: Update product details (Admin)
- `DELETE /api/products/:id`: Delete a product (Admin)

### Orders

- `POST /api/orders`: Create a new order
- `GET /api/orders`: Get all orders for the logged-in user
- `GET /api/orders/:id`: Get order details by ID

### Cart

- `POST /api/cart`: Add items to cart
- `GET /api/cart`: Get the user's cart
- `DELETE /api/cart/:itemId`: Remove item from cart

### Payment

- `POST /api/payment/charge`: Process a payment

For detailed API documentation, please refer to the [API Documentation](#) (link to your API documentation if available).



