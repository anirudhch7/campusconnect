# CampusConnect

A full-stack social platform designed for campus communities, enabling students to share posts, engage with content, and connect with peers.

## 🚀 Features

- **User Authentication**: Secure registration and login with JWT-based authentication
- **Create & Share Posts**: Share thoughts, updates, and content with the campus community
- **Engage with Content**: Like, comment, and interact with posts from other users
- **User Profiles**: Personalized profiles to showcase your posts and activity
- **Image Upload**: Support for uploading and sharing images with posts
- **Responsive Design**: Modern, mobile-friendly interface built with Tailwind CSS
- **Real-time Updates**: Dynamic content updates for a seamless user experience

## 🛠️ Tech Stack

### Frontend
- **React** - UI library for building interactive user interfaces
- **Vite** - Fast build tool and development server
- **React Router** - Client-side routing
- **Axios** - HTTP client for API requests
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **FontAwesome & React Icons** - Icon libraries
- **RSuite** - Component library

### Backend
- **Node.js** - JavaScript runtime
- **Express** - Web application framework
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - JSON Web Tokens for authentication
- **Bcrypt** - Password hashing
- **Multer** - File upload handling
- **CORS** - Cross-origin resource sharing

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v14 or higher)
- **npm** or **yarn**
- **MongoDB** (local installation or MongoDB Atlas account)

## 🔧 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/anirudhch7/campusconnect.git
cd campusconnect
```

### 2. Backend Setup

```bash
cd Backend
npm install
```

Create a `.env` file in the `Backend` directory with the following variables:

```env
MONGO_URL=your_mongodb_connection_string
PORT=5000
JWT_SECRET=your_jwt_secret_key
```

### 3. Frontend Setup

```bash
cd ../Frontend/campusconnect
npm install
```

## 🚀 Running the Application

### Start the Backend Server

```bash
cd Backend
npm run dev
```

The backend server will start on `http://localhost:5000`

### Start the Frontend Development Server

```bash
cd Frontend/campusconnect
npm run dev
```

The frontend will start on `http://localhost:5173`

## 📁 Project Structure

```
campusconnect/
├── Backend/
│   ├── Controllers/       # Request handlers
│   ├── Middlewares/       # Authentication & validation middleware
│   ├── models/           # MongoDB schemas
│   ├── routes/           # API route definitions
│   │   ├── authRoute.js
│   │   ├── userRoute.js
│   │   ├── postRoute.js
│   │   └── commentRoute.js
│   ├── uploads/          # Uploaded images storage
│   ├── index.js          # Express app configuration
│   └── package.json
│
└── Frontend/
    └── campusconnect/
        ├── src/
        │   ├── Components/   # Reusable React components
        │   ├── Context/      # React Context for state management
        │   ├── Pages/        # Page components
        │   │   ├── Home.jsx
        │   │   ├── Login.jsx
        │   │   ├── SignUp.jsx
        │   │   ├── CreatePost.jsx
        │   │   ├── PostDetails.jsx
        │   │   ├── ProfilePage.jsx
        │   │   └── ...
        │   ├── utils/        # Utility functions
        │   └── App.jsx       # Main app component
        ├── public/
        └── package.json
```

## 🔌 API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Users
- `GET /api/users/:id` - Get user profile
- `PUT /api/users/:id` - Update user profile
- `DELETE /api/users/:id` - Delete user account

### Posts
- `GET /api/posts` - Get all posts
- `GET /api/posts/:id` - Get single post
- `POST /api/posts` - Create new post
- `PUT /api/posts/:id` - Update post
- `DELETE /api/posts/:id` - Delete post

### Comments
- `POST /api/comments` - Create comment
- `GET /api/comments/post/:postId` - Get comments for a post
- `PUT /api/comments/:id` - Update comment
- `DELETE /api/comments/:id` - Delete comment

### Upload
- `POST /api/upload` - Upload image

## 🔒 Security Features

- Password hashing with bcrypt
- JWT-based authentication
- HTTP-only cookies for token storage
- CORS configuration
- Input validation and sanitization

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the [ISC License](LICENSE).

## 👨‍💻 Author

[anirudhch7](https://github.com/anirudhch7)

## 📧 Contact

For any queries or suggestions, please open an issue on GitHub.

---

**Note**: Make sure to never commit your `.env` file containing sensitive credentials to version control.
