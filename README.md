# Node.js & React E-Commerce Application

A full-stack e-commerce application built with Node.js, Express, React, Redux, and MongoDB. This project demonstrates modern web development practices and provides a complete online shopping experience.

## Features

- **User Authentication & Authorization**
- **Product Management** (Admin panel)
- **Shopping Cart** with Redux state management
- **Order Processing** and history
- **Payment Integration** (PayPal)
- **Product Reviews & Ratings**
- **Image Upload** (Local & AWS S3)
- **Responsive Design**
- **Admin Dashboard**

## Tech Stack

### Frontend

- React 18
- Redux for state management
- React Router for navigation
- Axios for API calls
- CSS3 with modern styling

### Backend

- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Multer for file uploads
- AWS S3 integration

### Development Tools

- ESLint for code quality
- Babel for transpilation
- Git for version control

## Installation

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or cloud)
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/muratkazma0/full-stack-ecommerce.git
cd full-stack-ecommerce
```

### 2. Install Dependencies

```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd frontend
npm install
cd ..
```

### 3. Environment Setup

Create a `.env` file in the root directory:

```env
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/amazona
JWT_SECRET=your_jwt_secret_here
PAYPAL_CLIENT_ID=your_paypal_client_id
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
AWS_BUCKET_NAME=your_bucket_name
```

### 4. Database Setup

Make sure MongoDB is running on your system. The application will automatically create the necessary collections.

### 5. Run the Application

#### Start Backend Server

```bash
npm start
```

#### Start Frontend (in a new terminal)

```bash
cd frontend
npm start
```

The application will be available at:

- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## Admin Setup

1. Visit: http://localhost:5000/api/users/createadmin
2. Note the admin email and password returned
3. Login at: http://localhost:3000/signin

## Usage

### For Customers

1. Browse products on the homepage
2. View product details
3. Add items to cart
4. Proceed to checkout
5. Complete payment

### For Admins

1. Login with admin credentials
2. Manage products at `/products`
3. View and manage orders
4. Upload product images

## Deployment

### Heroku Deployment

1. Create a Heroku account
2. Install Heroku CLI
3. Create a new Heroku app
4. Set environment variables
5. Deploy using Git

```bash
heroku create your-app-name
heroku config:set NODE_ENV=production
heroku config:set MONGODB_URI=your_mongodb_atlas_uri
git push heroku main
```

### Environment Variables for Production

- `MONGODB_URI`: MongoDB Atlas connection string
- `JWT_SECRET`: Secure JWT secret
- `PAYPAL_CLIENT_ID`: PayPal client ID
- `AWS_ACCESS_KEY_ID`: AWS access key
- `AWS_SECRET_ACCESS_KEY`: AWS secret key
- `AWS_BUCKET_NAME`: S3 bucket name

## Project Structure

```
full-stack-ecommerce/
├── backend/
│   ├── models/          # MongoDB models
│   ├── routes/          # API routes
│   ├── middleware/      # Custom middleware
│   └── utils/           # Utility functions
├── frontend/
│   ├── public/          # Static files
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── screens/     # Page components
│   │   ├── store/       # Redux store
│   │   └── utils/       # Utility functions
│   └── package.json
├── uploads/             # Local file uploads
└── package.json
```

---

**Happy Coding!**
