# Rooms Backend

Backend API server for the SmartRoom Meeting Room Booking System.

## 🚀 Features

- **Authentication API**: JWT-based authentication with HTTP-only cookies
- **Session Management**: Secure session restoration and logout endpoints
- **CORS Configuration**: Configured for frontend communication

## 📦 Technologies

- **Express.js**: Web application framework
- **JWT**: JSON Web Tokens for authentication
- **CORS**: Cross-Origin Resource Sharing
- **Cookie Parser**: HTTP cookie parsing middleware

## 🛠️ Installation

```bash
npm install
```

## 🏃 Development

```bash
npm run dev
```

The server will run on `http://localhost:3001`

## 🏗️ Production

```bash
npm start
```

## 📂 Project Structure

```
rooms-back/
├── server.js          # Main Express server
├── backend_logic.js   # Backend documentation and notes
└── database/          # Database related files
```

## 🔐 API Endpoints

### Authentication

- `POST /auth/login` - User login
  - Body: `{ user: { id, name, role } }`
  - Returns: `{ success: true, user }`
  - Sets HTTP-only cookie with JWT token

- `GET /auth/me` - Get current user session
  - Returns: `{ id, name, role }`
  - Requires valid JWT token in cookie

- `POST /auth/logout` - User logout
  - Returns: `{ success: true }`
  - Clears authentication cookie

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
PORT=3001
SECRET_KEY=your_super_secret_key_for_jwt
FRONTEND_URL=http://localhost:3000
NODE_ENV=development
```

**Important**: In production, always use environment variables for sensitive data like `SECRET_KEY`.

### CORS Configuration

The server is configured to accept requests from `http://localhost:3000` by default. Update the CORS origin in `server.js` or use environment variables for different environments.

## 🔒 Security Notes

- JWT tokens are stored in HTTP-only cookies for security
- In production, set `secure: true` in cookie options (requires HTTPS)
- Always use a strong `SECRET_KEY` in production
- Consider implementing rate limiting for authentication endpoints

