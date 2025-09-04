# 🚀 Hocche Setup Instructions

## Prerequisites

Before setting up Hocche, make sure you have the following installed:

1. **Node.js** (v14 or higher) - Download from [nodejs.org](https://nodejs.org/)
2. **MongoDB** - Download from [mongodb.com](https://www.mongodb.com/try/download/community) or use MongoDB Atlas (cloud)
3. **Git** (optional) - For version control

## Installation Steps

### 1. Install Node.js and npm
- Download and install Node.js from https://nodejs.org/
- This will also install npm (Node Package Manager)
- Verify installation by opening a new terminal and running:
  ```bash
  node --version
  npm --version
  ```

### 2. Install MongoDB
**Option A: Local MongoDB**
- Download MongoDB Community Server from https://www.mongodb.com/try/download/community
- Follow installation instructions for your operating system
- Start MongoDB service

**Option B: MongoDB Atlas (Recommended for beginners)**
- Sign up for free at https://www.mongodb.com/atlas
- Create a new cluster
- Get your connection string and update the `MONGODB_URI` in the server/.env file

### 3. Install Project Dependencies

Open your terminal/command prompt and navigate to the project directory:

```bash
# Navigate to the project directory
cd "C:\Users\Admin\Downloads\Hocche!"

# Install root dependencies
npm install

# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install

# Go back to root directory
cd ..
```

### 4. Environment Configuration

The server `.env` file has been created with default values. You may need to update:

**Server Environment Variables (`server/.env`):**
```env
NODE_ENV=development
PORT=5000
MONGODB_URI=mongodb://localhost:27017/hocche
JWT_SECRET=hocche_super_secret_jwt_key_2025_change_in_production
JWT_EXPIRE=30d
```

For production, make sure to:
- Change the `JWT_SECRET` to a secure random string
- Update `MONGODB_URI` if using MongoDB Atlas
- Add any additional API keys (Google Maps, Cloudinary, etc.)

### 5. Starting the Application

**Option A: Start both client and server together (Recommended)**
```bash
npm run dev
```

**Option B: Start client and server separately**

Terminal 1 (Server):
```bash
cd server
npm run dev
```

Terminal 2 (Client):
```bash
cd client
npm start
```

### 6. Access the Application

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5000
- **API Health Check**: http://localhost:5000/api/health

## 🧪 Testing the Setup

1. Open http://localhost:3000 in your browser
2. You should see the Hocche homepage
3. Try registering a new account
4. Create a test event
5. Browse events

## 📁 Project Structure

```
hocche-event-management/
├── client/                 # React frontend
│   ├── public/            # Static files
│   ├── src/
│   │   ├── components/    # Reusable React components
│   │   ├── pages/         # Page components
│   │   ├── context/       # React context for state management
│   │   ├── services/      # API service functions
│   │   ├── styles/        # Styled components and global styles
│   │   └── utils/         # Utility functions
│   └── package.json       # Client dependencies
├── server/                # Express backend
│   ├── config/           # Configuration files
│   ├── controllers/      # Route controllers
│   ├── middleware/       # Custom middleware
│   ├── models/           # MongoDB models
│   ├── routes/           # API routes
│   ├── .env              # Environment variables
│   └── server.js         # Main server file
├── package.json          # Root package.json for scripts
└── README.md             # Project documentation
```

## 🔧 Available Scripts

**Root level:**
- `npm run dev` - Start both client and server
- `npm run client` - Start only React client
- `npm run server` - Start only Express server
- `npm run install-all` - Install dependencies for both client and server

**Client:**
- `npm start` - Start development server
- `npm run build` - Build for production
- `npm test` - Run tests

**Server:**
- `npm run dev` - Start with nodemon (auto-restart)
- `npm start` - Start production server

## 🎨 Features Implemented

### ✅ Completed Features
1. **User Authentication**
   - User registration and login
   - JWT-based authentication
   - Password hashing with bcrypt
   - Protected routes

2. **User Management**
   - User profiles with avatar and bio
   - User interests and location
   - Follow/unfollow functionality

3. **Event Management**
   - Event creation with rich details
   - Event categories and tags
   - Location-based event discovery
   - Event search and filtering
   - Join/leave events
   - Event reviews and ratings

4. **Frontend Features**
   - Responsive design with styled-components
   - Modern UI with gradients and animations
   - Interactive components
   - Form validation
   - Toast notifications
   - Loading states

5. **Backend Features**
   - RESTful API design
   - MongoDB integration with Mongoose
   - Input validation and sanitization
   - Error handling middleware
   - Security middleware (helmet, rate limiting)
   - CORS configuration

### 🚧 Features to Implement

1. **Maps Integration**
   - Interactive event location maps
   - Location picker for event creation
   - Nearby events visualization

2. **Image Upload**
   - Event image upload (using Cloudinary)
   - User avatar upload
   - Image optimization and resizing

3. **Real-time Features**
   - Live event updates
   - Real-time notifications
   - Chat functionality

4. **Advanced Features**
   - Email notifications
   - Event recommendations
   - Social sharing
   - Event analytics
   - Payment integration
   - QR code check-ins

## 🔍 Troubleshooting

### Common Issues

1. **npm not recognized**
   - Install Node.js from nodejs.org
   - Restart your terminal after installation

2. **MongoDB connection failed**
   - Make sure MongoDB is running locally, or
   - Use MongoDB Atlas and update the connection string

3. **Port already in use**
   - Change the PORT in server/.env file
   - Or stop other applications using ports 3000/5000

4. **CORS errors**
   - Check that the client is running on http://localhost:3000
   - Update CORS settings in server.js if needed

### Getting Help

If you encounter any issues:
1. Check the console for error messages
2. Verify all dependencies are installed
3. Ensure MongoDB is running
4. Check that environment variables are set correctly

## 🚀 Next Steps

1. **Set up MongoDB** (local or Atlas)
2. **Install dependencies** using the commands above
3. **Start the application** with `npm run dev`
4. **Explore the codebase** and start customizing
5. **Add new features** based on your requirements

## 📚 Technologies Used

- **Frontend**: React, React Router, Styled Components, Axios
- **Backend**: Node.js, Express, MongoDB, Mongoose
- **Authentication**: JWT, bcryptjs
- **Styling**: Styled Components, CSS3
- **Icons**: React Icons (Feather Icons)
- **State Management**: React Context API
- **Development**: Nodemon, Concurrently

---

**Happy coding! 🎉** 

Your Hocche event management platform is ready to bring communities together through amazing events!
