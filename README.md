# Restaurant Management System

A full-stack restaurant management application built with React, TypeScript, Node.js, Express, and MongoDB.

## Features

- 🍽️ Menu Management
- 📦 Order Processing with Real-time Updates
- 👨‍🍳 Chef Dashboard
- 👤 User Authentication & Authorization
- ⭐ Customer Reviews
- 📊 Admin Dashboard
- 🔔 Real-time Notifications (Socket.IO)
- 📱 Responsive Design

## Tech Stack

### Frontend
- **React 18** with TypeScript
- **Vite** - Fast build tool
- **TailwindCSS** - Styling
- **React Router** - Navigation
- **Socket.IO Client** - Real-time updates
- **Chart.js** - Data visualization
- **React Hot Toast** - Notifications
- **Axios** - HTTP requests

### Backend
- **Node.js** with Express
- **MongoDB** with Mongoose
- **Socket.IO** - Real-time communication
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Multer** - File uploads

## Project Structure

```
restarent-main/
├── backend/              # Backend API
│   ├── models/          # Database models
│   ├── routes/          # API routes
│   ├── middleware/      # Custom middleware
│   ├── server.js        # Server entry point
│   └── package.json
├── src/                 # Frontend source
├── public/              # Static files
├── package.json         # Frontend dependencies
└── .env                 # Environment variables
```

## Getting Started

### Prerequisites
- Node.js (v16 or higher)
- MongoDB account or local MongoDB instance
- npm or yarn

### Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd restarent-main
```

2. **Install Frontend Dependencies**
```bash
npm install
```

3. **Install Backend Dependencies**
```bash
cd backend
npm install
cd ..
```

4. **Environment Variables**

Create a `.env` file in the root directory:
```env
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
PORT=5000
NODE_ENV=development
```

### Running the Application

#### Option 1: Using Separate Terminals

**Terminal 1 - Start Backend:**
```bash
cd backend
npm run dev
```
Backend runs on `http://localhost:5000`

**Terminal 2 - Start Frontend:**
```bash
npm run dev
```
Frontend runs on `http://localhost:5173`

#### Option 2: Quick Start (Windows)

Create `start.bat` in the root folder:
```batch
@echo off
start cmd /k "cd backend && npm run dev"
start cmd /k "npm run dev"
```

Then run:
```bash
start.bat
```

### Seeding Initial Data

To populate the database with initial data:
```bash
cd backend
npm run seed
```

## Available Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run typecheck` - TypeScript type checking

### Backend
- `npm start` - Start production server
- `npm run dev` - Start development server with nodemon
- `npm run seed` - Seed database with initial data

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login

### Menu
- `GET /api/menu` - Get all menu items
- `POST /api/menu` - Add menu item (Admin)
- `PUT /api/menu/:id` - Update menu item (Admin)
- `DELETE /api/menu/:id` - Delete menu item (Admin)

### Orders
- `GET /api/orders` - Get all orders
- `POST /api/orders` - Create new order
- `PUT /api/orders/:id` - Update order status

### Reviews
- `GET /api/reviews` - Get all reviews
- `POST /api/reviews` - Create review

### Admin
- `GET /api/admin/dashboard` - Get dashboard statistics

## WebSocket Events

### Client -> Server
- `join-chef` - Chef joins the kitchen room
- `new-order` - New order notification
- `order-status-update` - Order status changed

### Server -> Client
- `order-notification` - New order for chefs
- `order-status-changed` - Order status update broadcast

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License.
