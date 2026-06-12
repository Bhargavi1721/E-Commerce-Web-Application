# E-Commerce Store 🛒

A full-stack e-commerce application with authentication, product browsing, cart management, coupon support, Stripe checkout, and an admin dashboard.

![Demo App](frontend/public/screenshot-for-readme.png)

## Features

- User signup/login with JWT authentication
- Product listing and category-based browsing
- Shopping cart and checkout flow
- Coupon code support
- Stripe payment integration
- Admin dashboard for product management and analytics
- MongoDB + Redis-backed backend
- React + Vite frontend with Tailwind CSS

## Tech Stack

- Frontend: React, Vite, Tailwind CSS
- Backend: Express.js, MongoDB, Mongoose, Redis
- Payments: Stripe
- Media: Cloudinary

## Project Structure

- backend/ - Express API and database logic
- frontend/src/ - React pages, components, stores
- frontend/public/ - Static assets and demo images

## Prerequisites

Before running this project locally, make sure you have:

- Node.js 18+ installed
- MongoDB running and accessible
- Redis running or a valid Upstash Redis URL
- Stripe secret key
- Cloudinary credentials

## Environment Variables

Create a .env file in the project root with the following variables:

```env
PORT=5000
MONGO_URI=your_mongo_uri
UPSTASH_REDIS_URL=your_redis_url
ACCESS_TOKEN_SECRET=your_access_token_secret
REFRESH_TOKEN_SECRET=your_refresh_token_secret
CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret
STRIPE_SECRET_KEY=your_stripe_secret_key
CLIENT_URL=http://localhost:5173
NODE_ENV=development
```

## Installation

Install the root dependencies and the frontend dependencies:

```bash
npm install
npm install --prefix frontend
```

## Run Locally

### 1. Start the backend

```bash
npm run dev
```

The backend API will run on:

http://localhost:5000

### 2. Start the frontend

Open a second terminal and run:

```bash
npm run dev --prefix frontend
```

The frontend will run on:

http://localhost:5173

## Production Build

To build the frontend for production:

```bash
npm run build
```

To start the production server:

```bash
npm run start
```

## Notes

- The frontend uses Vite and communicates with the backend API on port 5000.
- The admin dashboard route is available under /secret-dashboard.
- Stripe checkout and Cloudinary uploads require valid credentials in your environment file.

