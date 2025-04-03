# MERN Stack Blogging Platform

A full-stack blogging platform built with the MERN stack (MongoDB, Express.js, React.js, Node.js) that allows users to create, read, update, and delete blog posts, as well as interact with other users through comments and likes.

## Features

- User authentication (sign up, sign in, logout)
- Create, read, update, and delete blog posts
- Comment system with likes
- User profiles with personal blog posts
- Responsive design
- Modern UI with Material-UI components
- JWT-based authentication
- MongoDB database integration

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- npm or yarn

## Setup Instructions

1. Clone the repository:

```bash
git clone <repository-url>
cd blog
```

2. Install backend dependencies:

```bash
cd backend
npm install
```

3. Install frontend dependencies:

```bash
cd ../frontend
npm install
```

4. Create a `.env` file in the backend directory with the following variables:

```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/blog-platform
JWT_SECRET=your_jwt_secret_key_here
```

5. Start the backend server:

```bash
cd backend
npm run dev
```

6. Start the frontend development server:

```bash
cd frontend
npm start
```

The application will be available at:

- Frontend: http://localhost:3000
- Backend: http://localhost:5000

## Project Structure

```
blog/
├── backend/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── server.js
│   └── package.json
└── frontend/
    ├── public/
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── context/
    │   └── App.js
    └── package.json
```

## API Endpoints

### Authentication

- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login user
- GET /api/auth/me - Get current user

### Blogs

- GET /api/blogs - Get all blogs
- GET /api/blogs/:id - Get single blog
- POST /api/blogs - Create new blog
- PUT /api/blogs/:id - Update blog
- DELETE /api/blogs/:id - Delete blog
- PUT /api/blogs/:id/like - Like/Unlike blog

### Comments

- GET /api/comments/blog/:blogId - Get comments for a blog
- POST /api/comments - Create comment
- PUT /api/comments/:id - Update comment
- DELETE /api/comments/:id - Delete comment
- PUT /api/comments/:id/like - Like/Unlike comment

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
