# Talksy - Real Time Quick Chat Application

Talksy is a modern real-time chat application built with React, Vite, Node.js, Express, MongoDB, and Socket.IO. It allows users to sign up, log in, update their profiles, and chat instantly with other users. Media sharing and online status indicators are supported.

## Features

- Real-time messaging with Socket.IO
- User authentication (sign up, login, JWT-based)
- Profile management with image upload (Cloudinary)
- Online/offline user status
- Media (image) sharing in chat
- Responsive UI with Tailwind CSS
- Sidebar with user search and unseen message count
- Profile bio and avatar support

## Tech Stack

- **Frontend:** React, Vite, Tailwind CSS
- **Backend:** Node.js, Express, MongoDB (Mongoose), Socket.IO
- **Image Hosting:** Cloudinary
- **Authentication:** JWT
- **Notifications:** react-hot-toast

## Project Structure

```
client/
  src/
    assets/           # Images and icons
    components/       # React components (Sidebar, ChatContainer, etc.)
    lib/              # Utility functions
    pages/            # Page components (HomePage, LoginPage, ProfilePage)
    context/          # React Context (AuthContext, ChatContext)
    main.jsx          # App entry point
    App.jsx           # Main app component
  public/             # Static files
  index.html
  package.json
  vite.config.js

server/
  controllers/        # Express controllers
  lib/                # Utility libraries (db, cloudinary, utils)
  middleware/         # Express middleware (auth)
  models/             # Mongoose models (User, Message)
  routes/             # Express routes (userRoutes, messageRoutes)
  server.js           # Express app entry point
  package.json
```

## Getting Started

### Prerequisites

- Node.js (v18+ recommended)
- MongoDB Atlas account (or local MongoDB)
- Cloudinary account

### Environment Variables

#### Server (`server/.env`)

```
MONGODB_URI=your_mongodb_connection_string
PORT=5000
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

#### Client (`client/.env`)

```
VITE_BACKEND_URL=http://localhost:5000
```

### Installation

#### 1. Clone the repository

```sh
git clone https://github.com/yourusername/talksy.git
cd talksy
```

#### 2. Install dependencies

```sh
# In the root directory, install server dependencies
cd server
npm install

# In another terminal, install client dependencies
cd ../client
npm install
```

#### 3. Run the development servers

```sh
# Start the backend server
cd server
npm run server

# Start the frontend dev server
cd ../client
npm run dev
```

#### 4. Open in browser

Visit [http://localhost:5173](http://localhost:5173) (or the port shown in your terminal).

## Deployment

- The project includes `vercel.json` files for both client and server for easy deployment on [Vercel](https://vercel.com/).
- Make sure to set the environment variables in your Vercel dashboard.

## Screenshots

### Sign Up Page

![Sign Up Page](client/src/assets/Screenshot (1).png)

### Profile Page

![Profile Page](client/src/assets/Screenshot (3).png)


### Chat Interface

![Chat Interface](client/src/assets/Screenshot (2).png)


---

**Made with ❤️ using React, Node.js, and Socket.IO**