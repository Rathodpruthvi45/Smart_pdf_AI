# FastAPI React Authentication System

A comprehensive, secure, and production-ready authentication system built with FastAPI and React.

## Features

### Backend (FastAPI)

- User registration with email verification
- Secure login with JWT tokens stored in HTTP-only cookies
- Refresh token mechanism
- Password reset functionality
- Role-based access control (RBAC)
- Rate limiting to prevent brute force attacks
- CSRF protection
- Secure headers
- Database migrations with Alembic

### Frontend (React)

- User registration and login forms
- Email verification
- Password reset
- Protected routes based on authentication and roles
- Responsive design
- Context API for state management

## Project Structure

```
/
├── backend/                # FastAPI backend
│   ├── alembic/            # Database migrations
│   ├── app/                # Application code
│   │   ├── api/            # API endpoints
│   │   ├── core/           # Core functionality
│   │   ├── db/             # Database models and connection
│   │   ├── models/         # SQLAlchemy models
│   │   ├── schemas/        # Pydantic schemas
│   │   ├── services/       # Business logic
│   │   └── utils/          # Utility functions
│   ├── .env                # Environment variables
│   └── requirements.txt    # Python dependencies
│
└── frontend/               # React frontend
    ├── public/             # Static files
    ├── src/                # Source code
    │   ├── components/     # Reusable components
    │   ├── context/        # Context providers
    │   ├── hooks/          # Custom hooks
    │   ├── pages/          # Page components
    │   ├── services/       # API services
    │   ├── styles/         # CSS styles
    │   └── utils/          # Utility functions
    └── package.json        # Node.js dependencies
```

## Requirements

- Python 3.8+
- Node.js 14+
- MySQL 5.7+
- Redis 6.0+

## Installation

### Backend

1. Navigate to the backend directory:

   ```bash
   cd backend
   ```

2. Create a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Create a MySQL database:

   ```sql
   CREATE DATABASE auth_db;
   ```

5. Copy `.env.example` to `.env` and update the environment variables.

6. Run database migrations:

   ```bash
   alembic upgrade head
   ```

7. Start the server:
   ```bash
   uvicorn app.main:app --reload
   ```

### Frontend

1. Navigate to the frontend directory:

   ```bash
   cd frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

## API Documentation

Once the backend server is running, you can access the API documentation at:

- Swagger UI: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

## Security Features

- Passwords are hashed using bcrypt
- JWT tokens are stored in HTTP-only, secure cookies
- CSRF protection with double submit cookie pattern
- Rate limiting to prevent brute force attacks
- Secure headers to prevent common web vulnerabilities
- Role-based access control
- Email verification
- Refresh token rotation

## License

MIT
