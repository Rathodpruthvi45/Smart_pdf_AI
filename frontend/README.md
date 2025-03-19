# React Authentication Frontend

This is a secure, production-ready authentication frontend built with React and React Router.

## Features

- User registration with email verification
- Secure login with JWT tokens stored in HTTP-only cookies
- Refresh token mechanism
- Password reset functionality
- Role-based access control (RBAC)
- Protected routes
- Responsive design

## Requirements

- Node.js 14+
- npm 6+

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the development server:
   ```bash
   npm start
   ```

## Environment Variables

Create a `.env` file in the root directory with the following variables:

```
REACT_APP_API_URL=http://localhost:8000/api/v1
```

## Project Structure

```
/src
  /components        # Reusable components
  /context           # Context providers
  /hooks             # Custom hooks
  /pages             # Page components
  /services          # API services
  /styles            # CSS styles
  /utils             # Utility functions
  App.js             # Main application component
  index.js           # Entry point
```

## Authentication Flow

1. **Registration**: User registers with email, username, and password
2. **Email Verification**: User verifies email by clicking on a link sent to their email
3. **Login**: User logs in with email and password
4. **Token Storage**: Access token is stored in HTTP-only cookies
5. **Protected Routes**: Routes are protected based on authentication and roles
6. **Token Refresh**: Access token is refreshed automatically when expired
7. **Logout**: Cookies are cleared on logout

## Security Features

- HTTP-only cookies for token storage (prevents XSS attacks)
- CSRF protection with double submit cookie pattern
- Role-based access control
- Form validation
- Error handling

## License

MIT
