# Aspire Full-Stack Application

A modern full-stack web application built with TypeScript, featuring user authentication, college management, reviews, and favorites functionality.

## 📋 Project Overview

This application provides a comprehensive platform for managing college information with the following key features:

- **User Authentication**: Secure JWT-based authentication with refresh tokens
- **College Management**: Browse, search, and filter college information
- **Reviews System**: Add and view reviews for colleges
- **Favorites**: Save and manage favorite colleges
- **Responsive Design**: Modern UI built with Next.js and Tailwind CSS

## 🚀 Tech Stack

### Backend

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **TypeScript** - Type-safe JavaScript
- **Drizzle ORM** - Database ORM
- **PostgreSQL** - Primary database
- **JWT** - Authentication tokens
- **Argon2** - Password hashing
- **Helmet** - Security middleware

### Frontend

- **Next.js 15** - React framework with App Router
- **React 19** - UI library
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS framework
- **Axios** - HTTP client
- **Lucide React** - Icon library

### Development Tools

- **ESLint** - Code linting
- **Turbopack** - Fast bundler for Next.js
- **Nodemon** - Development server auto-restart
- **Drizzle Kit** - Database migrations

## 🛠️ Prerequisites

Before running this application, make sure you have the following installed:

- Node.js (v18 or higher)
- npm or yarn package manager
- PostgreSQL database

## 🏃‍♂️ Steps to Run Locally

### 1. Clone the Repository

```bash
git clone <repository-url>
cd aspirenext
```

### 2. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Install dependencies
npm install
# or
yarn install

# Set up environment variables
cp .env.example .env
# Edit .env file with your database credentials and JWT secrets

# Set up database and run migrations
yarn db:setup

# Start development server
yarn dev
```

The backend server will start on `http://localhost:3001` (or your configured port).

### 3. Frontend Setup

```bash
# Navigate to frontend directory (in a new terminal)
cd frontend

# Install dependencies
npm install
# or
yarn install

# Set up environment variables
cp .env.local.example .env.local
# Edit .env.local file with your API endpoints

# Start development server
yarn dev
```

The frontend application will start on `http://localhost:3000`.

### 4. Access the Application

- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:3001`

## 📁 Project Structure

```
aspirenext/
├── backend/                 # Express.js backend
│   ├── src/
│   │   ├── controllers/     # Route controllers
│   │   ├── services/        # Business logic
│   │   ├── routes/          # API routes
│   │   ├── middlewares/     # Custom middlewares
│   │   ├── db/              # Database schema and config
│   │   └── server.ts        # Entry point
│   ├── drizzle/             # Database migrations
│   └── docs/                # API documentation
│
└── frontend/                # Next.js frontend
    ├── src/
    │   ├── app/             # App Router pages
    │   ├── components/      # Reusable components
    │   ├── contexts/        # Context providers
    │   ├── hooks/           # Custom hooks
    │   ├── lib/             # Utilities and API clients
    │   └── types/           # TypeScript type definitions
    └── public/              # Static assets
```

## 🔧 Available Scripts

### Backend Scripts

- `yarn dev` - Start development server with hot reload
- `yarn build` - Build for production
- `yarn start` - Start production server
- `yarn db-migrate` - Run database migrations
- `yarn db:setup` - Setup database and seed data

### Frontend Scripts

- `yarn dev` - Start development server with Turbopack
- `yarn build` - Build for production
- `yarn start` - Start production server
- `yarn lint` - Run ESLint

## 🔐 Environment Variables

### Backend (.env)

```env
DATABASE_URL=postgresql://username:password@localhost:5432/database_name
JWT_SECRET=your_jwt_secret
JWT_REFRESH_SECRET=your_refresh_secret
PORT=3001
```

### Frontend (.env.local)

```env
NEXT_PUBLIC_API_URL=http://localhost:3001
```

## 📚 API Documentation

API documentation is available in the `backend/docs/` directory:

- [Authentication API](backend/docs/authapi.doc.md)
- [Colleges API](backend/docs/collegesapi.doc.md)
- [Reviews API](backend/docs/reviews.doc.md)
- [Favorites API](backend/docs/favorites.doc.md)

## 🚀 Deployment

### Backend Deployment

1. Build the application: `yarn build`
2. Set production environment variables
3. Deploy to your preferred platform (Heroku, Railway, etc.)

### Frontend Deployment

1. Build the application: `yarn build`
2. Deploy to Vercel, Netlify, or your preferred platform

## 📝 Additional Notes

- **Database**: The application uses PostgreSQL with Drizzle ORM for type-safe database operations
- **Authentication**: JWT-based authentication with refresh token rotation for enhanced security
- **Error Handling**: Comprehensive error handling with custom error classes and middleware
- **Type Safety**: Full TypeScript implementation across both frontend and backend
- **Security**: Implements security best practices with Helmet, CORS, and secure cookie handling
- **Development**: Hot reload enabled for both frontend and backend during development

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-feature`
3. Commit your changes: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature/new-feature`
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Issues

If you encounter any issues or have suggestions, please create an issue in the GitHub repository.
