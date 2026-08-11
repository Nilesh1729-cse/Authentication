# Secrets Project

A Node.js Express app that lets users register, log in, and share a secret.

This project uses:
- Express.js
- EJS templates
- Passport local authentication
- Passport Google OAuth 2.0
- bcrypt password hashing
- PostgreSQL for user storage
- dotenv for managing secrets
- express-session for session handling

## Features

- Register with email and password
- Log in with local credentials
- Log in with Google OAuth
- Submit and view a personal secret
- Protected routes for authenticated users only

## Prerequisites

- Node.js 18+ installed
- PostgreSQL installed and running
- A Google OAuth 2.0 Client ID / Client Secret

## Installation

1. Install dependencies:

   ```bash
   npm install
   ```

2. Create a PostgreSQL database, for example:

   ```sql
   CREATE DATABASE secrets;
   ```

3. Create the users table:

   ```sql
   CREATE TABLE users (
     id SERIAL PRIMARY KEY,
     email TEXT UNIQUE NOT NULL,
     password TEXT NOT NULL,
     secret TEXT
   );
   ```

4. Create a `.env` file in the project root with these values:

   ```env
   GOOGLE_CLIENT_ID=your_google_client_id
   GOOGLE_CLIENT_SECRET=your_google_client_secret
   SESSION_SECRET=some_strong_secret
   PG_USER=your_db_username
   PG_HOST=localhost
   PG_DATABASE=secrets
   PG_PASSWORD=your_db_password
   PG_PORT=5432
   ```

## Running the app

Start the server:

```bash
node index.js
```

Open your browser to:

```text
http://localhost:3000
```

## Routes

- `/` - Home page
- `/register` - Registration page
- `/login` - Login page
- `/secrets` - View secret (requires authentication)
- `/submit` - Submit a secret (requires authentication)
- `/logout` - Log out
- `/auth/google` - Google OAuth login

## Notes

- Local passwords are hashed with bcrypt before storage.
- Google OAuth users are stored in the same `users` table with a placeholder password value.
- The callback URL must match your Google OAuth app settings: `http://localhost:3000/auth/google/secrets`.

## Troubleshooting

- If database connection fails, verify `.env` values and that PostgreSQL is running.
- If Google OAuth redirect fails, check the authorized redirect URL in your Google Cloud credentials.

## License

This project is provided as-is.
