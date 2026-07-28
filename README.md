# Authentication Project

This is a secure Express + EJS authentication app using PostgreSQL, featuring Passport.js local strategy authentication, session-based user management, and encrypted password hashing.

## Features

- User registration and login using **Passport.js** (Local Strategy).
- Session management with `express-session` for persistent user login state.
- Protected routes (e.g., `/secrets` is strictly restricted to authenticated users).
- Secure password hashing using `bcrypt`.
- User logout functionality with session destruction.
- Environment variable support with `dotenv`.
- PostgreSQL database integration for persistent storage.

## Project structure

- `index.js` — main server file with Express, Passport, and PostgreSQL logic
- `package.json` — project dependencies
- `package-lock.json` — installed dependency tree
- `queries.sql` — SQL schema for `users`
- `public/` — static files and styles
- `views/` — EJS templates for pages
- `solution.js` — alternate or reference file
- `.DS_Store` — macOS file, do not submit

## Prerequisites

- Node.js installed
- PostgreSQL installed and running
- A PostgreSQL database named `secrets`

## Setup

1. Install dependencies:

```bash
npm install
