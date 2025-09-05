# JustMeet - Video Conferencing Application

JustMeet is a modern, real-time video conferencing application built with React.js frontend and Node.js backend. It provides seamless video calling experience with features like screen sharing, chat functionality, and meeting history tracking.

## 🚀 Features

### Core Features
- **Real-time Video Conferencing**: High-quality video calls using WebRTC technology
- **Audio/Video Controls**: Toggle camera and microphone on/off during calls
- **Screen Sharing**: Share your screen with other participants
- **Live Chat**: Real-time messaging during video calls
- **Meeting History**: Track and view your past meeting activities
- **User Authentication**: Secure registration and login system
- **Guest Access**: Join meetings without registration

### Technical Features
- **WebRTC Integration**: Peer-to-peer video communication
- **Socket.IO**: Real-time bidirectional communication
- **MongoDB**: Persistent data storage for users and meeting history
- **Material-UI**: Modern and responsive user interface
- **JWT Authentication**: Secure token-based authentication
- **Responsive Design**: Works on desktop and mobile devices

## 🛠️ Tech Stack

### Frontend
- **React.js 18.2.0**: Modern JavaScript library for building user interfaces
- **Material-UI (MUI) 5.15.4**: React component library for consistent design
- **React Router DOM 6.21.1**: Client-side routing
- **Socket.IO Client 4.7.3**: Real-time communication
- **Axios 1.6.5**: HTTP client for API requests

### Backend
- **Node.js**: JavaScript runtime environment
- **Express.js 4.18.2**: Web application framework
- **Socket.IO 4.7.3**: Real-time bidirectional event-based communication
- **MongoDB**: NoSQL database with Mongoose ODM
- **bcrypt 5.1.1**: Password hashing
- **CORS 2.8.5**: Cross-origin resource sharing

### Database
- **MongoDB Atlas**: Cloud-hosted MongoDB database
- **Mongoose 8.0.3**: MongoDB object modeling for Node.js

## 📁 Project Structure

```
JustMeet/
├── backend/
│   ├── src/
│   │   ├── app.js                 # Main server file
│   │   ├── controllers/
│   │   │   ├── socketManager.js   # Socket.IO connection handling
│   │   │   └── user.controller.js # User authentication logic
│   │   ├── models/
│   │   │   ├── user.model.js      # User data model
│   │   │   └── meeting.model.js   # Meeting data model
│   │   └── routes/
│   │       └── users.routes.js    # User API routes
│   ├── package.json
│   └── package-lock.json
├── frontend/
│   ├── src/
│   │   ├── App.js                 # Main React component
│   │   ├── contexts/
│   │   │   └── AuthContext.jsx    # Authentication context
│   │   ├── pages/
│   │   │   ├── landing.jsx        # Landing page
│   │   │   ├── authentication.jsx # Login/Register page
│   │   │   ├── home.jsx           # Dashboard page
│   │   │   ├── VideoMeet.jsx      # Video call interface
│   │   │   └── history.jsx        # Meeting history page
│   │   ├── styles/
│   │   │   └── videoComponent.module.css # Video component styles
│   │   ├── utils/
│   │   │   └── withAuth.jsx       # Authentication HOC
│   │   └── environment.js         # Environment configuration
│   ├── public/                    # Static assets
│   ├── package.json
│   └── package-lock.json
└── README.md
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn
- MongoDB Atlas account (or local MongoDB instance)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd JustMeet
   ```

2. **Install backend dependencies**
   ```bash
   cd backend
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Environment Setup**
   - Update the MongoDB connection string in `backend/src/app.js`
   - Configure the server URL in `frontend/src/environment.js`

### Running the Application

1. **Start the backend server**
   ```bash
   cd backend
   npm run dev
   ```
   The backend will run on `http://localhost:8000`

2. **Start the frontend development server**
   ```bash
   cd frontend
   npm start
   ```
   The frontend will run on `http://localhost:3000`

3. **Access the application**
   Open your browser and navigate to `http://localhost:3000`

## 📱 Usage

### For Registered Users
1. **Registration**: Create an account with name, username, and password
2. **Login**: Sign in with your credentials
3. **Join Meeting**: Enter a meeting code to join an existing meeting
4. **Create Meeting**: Share a unique meeting code with others
5. **View History**: Check your meeting history from the dashboard

### For Guest Users
1. **Guest Access**: Click "Join as Guest" on the landing page
2. **Enter Meeting**: Use any meeting code to join a call
3. **Participate**: Enjoy video calling without registration

### During Video Calls
- **Camera Control**: Click the camera icon to toggle video on/off
- **Microphone Control**: Click the microphone icon to mute/unmute audio
- **Screen Share**: Click the screen share icon to share your screen
- **Chat**: Click the chat icon to open the messaging panel
- **End Call**: Click the red phone icon to leave the meeting

## 🔧 API Endpoints

### User Routes (`/api/v1/users`)
- `POST /register` - User registration
- `POST /login` - User authentication
- `GET /get_all_activity` - Get user meeting history
- `POST /add_to_activity` - Add meeting to user history

### Socket.IO Events
- `join-call` - Join a video call room
- `signal` - WebRTC signaling for peer connections
- `chat-message` - Send chat messages
- `user-joined` - Notify when user joins
- `user-left` - Notify when user leaves

## 🎨 UI Components

### Pages
- **Landing Page**: Welcome screen with navigation options
- **Authentication**: Login and registration forms
- **Home Dashboard**: Meeting controls and history access
- **Video Meet**: Main video calling interface
- **History**: Past meeting records

### Video Interface Features
- **Local Video**: Your own video feed
- **Remote Videos**: Other participants' video feeds
- **Control Panel**: Audio/video controls and chat
- **Chat Panel**: Real-time messaging interface

## 🔒 Security Features

- **Password Hashing**: bcrypt encryption for user passwords
- **JWT Tokens**: Secure authentication tokens
- **CORS Protection**: Cross-origin request security
- **Input Validation**: Server-side data validation

## 🌐 Browser Compatibility

- **Chrome**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support

**Note**: WebRTC features require HTTPS in production environments.

## 🚀 Deployment

### Backend Deployment
1. Set up a cloud server (AWS, DigitalOcean, etc.)
2. Install Node.js and MongoDB
3. Configure environment variables
4. Use PM2 for process management: `npm run prod`

### Frontend Deployment
1. Build the production version: `npm run build`
2. Deploy the `build` folder to a static hosting service
3. Configure the backend URL in environment settings

### Environment Variables
```env
# Backend
PORT=8000
MONGODB_URI=your_mongodb_connection_string

# Frontend
REACT_APP_SERVER_URL=your_backend_url
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -m 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## 📝 License

This project is licensed under the ISC License.

## 👥 Authors

- **Aman Verma** - Initial work

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Check the documentation
- Review the code comments for implementation details

## 🔮 Future Enhancements

- [ ] Recording functionality
- [ ] Meeting scheduling
- [ ] File sharing
- [ ] Virtual backgrounds
- [ ] Mobile app development
- [ ] Advanced chat features
- [ ] Meeting analytics
- [ ] Integration with calendar apps

---

**JustMeet** - Connecting people through seamless video communication. Built with ❤️ using modern web technologies.
