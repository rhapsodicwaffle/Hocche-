# 🎉 Hocche - Event Management Platform

A modern, location-based event management platform built with the MERN stack where users can discover, create, and manage events around them.

## ✨ Features

- **Event Discovery**: Find events happening around your location
- **Event Creation**: Post and manage your own events
- **Location-Based Search**: Discover events based on proximity
- **Interactive Maps**: Visual event location display
- **Real-time Updates**: Live event information
- **User Authentication**: Secure user accounts
- **Responsive Design**: Works on all devices
- **Event Categories**: Filter events by type
- **Event Reviews**: Rate and review events

## 🚀 Tech Stack

- **Frontend**: React.js, React Router, Axios, Leaflet Maps
- **Backend**: Node.js, Express.js, JWT Authentication
- **Database**: MongoDB with Mongoose
- **Styling**: CSS3, Styled Components
- **Maps**: Leaflet/OpenStreetMap integration

## 🛠️ Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB
- npm or yarn

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/hocche-event-management.git
   cd hocche-event-management
   ```

2. **Install dependencies**
   ```bash
   npm run install-all
   ```

3. **Environment Setup**
   
   Create `.env` file in the server directory:
   ```env
   NODE_ENV=development
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/hocche
   JWT_SECRET=your_jwt_secret_key
   GOOGLE_MAPS_API_KEY=your_google_maps_api_key
   ```

4. **Start the application**
   ```bash
   npm run dev
   ```

   This will start both the client (http://localhost:3000) and server (http://localhost:5000)

## 📁 Project Structure

```
hocche-event-management/
├── client/                 # React frontend
│   ├── public/
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── context/        # React context
│   │   ├── services/       # API services
│   │   └── utils/          # Utility functions
│   └── package.json
├── server/                 # Express backend
│   ├── config/             # Configuration files
│   ├── controllers/        # Route controllers
│   ├── middleware/         # Custom middleware
│   ├── models/             # MongoDB models
│   ├── routes/             # API routes
│   └── server.js
└── package.json
```

## 🌟 Key Features Explained

### Location-Based Discovery
- Users can find events within a specified radius
- Map integration for visual event exploration
- GPS location detection for personalized results

### Event Management
- Create detailed event listings with photos
- Manage attendees and RSVPs
- Event categories and tags for better organization

### User Experience
- Modern, intuitive interface
- Mobile-responsive design
- Fast loading and smooth interactions

## 🔧 Available Scripts

- `npm run dev` - Start both client and server in development mode
- `npm run client` - Start only the React client
- `npm run server` - Start only the Express server
- `npm run build` - Build the client for production
- `npm run install-all` - Install dependencies for both client and server

## 🚀 Deployment

The app is ready to be deployed on platforms like Heroku, Vercel, or Netlify. Make sure to:

1. Set up environment variables on your hosting platform
2. Configure MongoDB Atlas for production database
3. Update CORS settings for your domain

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support, email support@hocche.com or join our Slack channel.

---

Made with ❤️ by the Hocche Team
