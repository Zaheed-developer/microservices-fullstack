# Full-Stack Microservices Application

A production-ready microservices application with NestJS backend and Next.js frontend.

## 🚀 Features

- Product Management Microservice (NestJS)
- Order Management Microservice (NestJS)
- Dynamic Form Frontend (Next.js + React)
- TCP-based inter-service communication
- Complete CRUD operations
- Real-time inventory management

## 📦 Prerequisites

- Node.js 18+
- npm 9+

## 🔧 Installation

### Product Service
```bash
cd product-service
npm install
npm run start:dev
```

### Order Service
```bash
cd order-service
npm install
npm run start:dev
```

### Frontend
```bash
cd frontend-app
npm install
npm run dev
```

## 🧪 Testing

**Create a Product:**
```bash
curl -X POST http://localhost:3000/products \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Laptop",
    "description": "High-performance laptop",
    "price": 999.99,
    "stock": 50
  }'
```

**Create an Order:**
```bash
curl -X POST http://localhost:3003/orders \
  -H "Content-Type: application/json" \
  -d '{
    "customerName": "John Doe",
    "customerEmail": "john@example.com",
    "shippingAddress": "123 Main St",
    "items": [{"productId": "PRODUCT_ID", "quantity": 2}]
  }'
```

## 📚 API Endpoints

### Product Service (Port 3000)
- `GET /products` - Get all products
- `POST /products` - Create product
- `GET /products/:id` - Get single product
- `PATCH /products/:id` - Update product
- `DELETE /products/:id` - Delete product

### Order Service (Port 3003)
- `GET /orders` - Get all orders
- `POST /orders` - Create order
- `GET /orders/:id` - Get single order
- `PATCH /orders/:id` - Update order
- `DELETE /orders/:id` - Delete order

## 📁 Project Structure
