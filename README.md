# Blog-App

A full-stack MERN (MongoDB, Express.js, React, Node.js) blog application that allows users to create, read, update, and delete blog posts. Users can sign up, log in, and manage their own blogs with image uploads.

## Features

- User authentication (signup, login, logout)
- Create, edit, and delete blog posts
- Image upload for blog posts
- Responsive design with React
- RESTful API with Express.js
- MongoDB for data storage
- JWT-based authentication
- Dashboard for managing user blogs

## Tech Stack

### Frontend
- React
- Vite (build tool)
- CSS (styling)
- Context API (state management)

### Backend
- Node.js
- Express.js
- MongoDB (database)
- Multer (file uploads)
- JWT (authentication)
- bcrypt (password hashing)

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- Git

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/rajan3081/Blog-App.git
   cd Blog-App
   ```

2. **Backend Setup:**
   ```bash
   cd backend
   npm install
   ```

   Create a `.env` file in the backend directory with the following variables:
   ```
   PORT=5000
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   ```

   Start the backend server:
   ```bash
   npm start
   ```

3. **Frontend Setup:**
   ```bash
   cd ../frontend
   npm install
   npm run dev
   ```

4. **Access the application:**
   - Frontend: http://localhost:5173 (default Vite port)
   - Backend: http://localhost:5000

## Usage

1. Register a new account or login with existing credentials.
2. Create new blog posts with title, content, and images.
3. View all blogs on the home page.
4. Edit or delete your own blog posts from the dashboard.
5. Browse latest blogs and contact information.

## API Endpoints

### User Routes
- `POST /api/user/register` - Register a new user
- `POST /api/user/login` - Login user
- `GET /api/user/profile` - Get user profile (authenticated)

### Blog Routes
- `GET /api/blog/all` - Get all blogs
- `POST /api/blog/create` - Create a new blog (authenticated)
- `GET /api/blog/:id` - Get single blog by ID
- `PUT /api/blog/:id` - Update blog (authenticated, owner only)
- `DELETE /api/blog/:id` - Delete blog (authenticated, owner only)

## Project Structure

```
Full-stack-mern-blog-app/
├── backend/
│   ├── config/
│   │   └── connectionDB.js
│   ├── controllers/
│   │   ├── blog.controller.js
│   │   └── user.controller.js
│   ├── middlewares/
│   │   ├── isAuthenticated.js
│   │   └── multer.js
│   ├── models/
│   │   ├── blog.model.js
│   │   └── user.model.js
│   ├── routes/
│   │   ├── blog.routes.js
│   │   └── user.routes.js
│   ├── uploads/
│   ├── index.js
│   └── package.json
└── frontend/
    ├── public/
    ├── src/
    │   ├── components/
    │   │   ├── BlogCard.jsx
    │   │   ├── Footer.jsx
    │   │   ├── Hero.jsx
    │   │   ├── LatestBlogs.jsx
    │   │   └── Navbar.jsx
    │   ├── context/
    │   │   └── StoreContext.jsx
    │   ├── pages/
    │   │   ├── About.jsx
    │   │   ├── Blogs.jsx
    │   │   ├── Contact.jsx
    │   │   ├── Dashboard.jsx
    │   │   ├── Home.jsx
    │   │   ├── Login.jsx
    │   │   ├── Signup.jsx
    │   │   └── SingleBlog.jsx
    │   ├── App.jsx
    │   ├── index.css
    │   ├── main.jsx
    │   └── App.css
    ├── index.html
    ├── package.json
    ├── vite.config.js
    └── eslint.config.js
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, please contact the project maintainer.