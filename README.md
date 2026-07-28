# Authentication Project

This is a secure Express + EJS authentication app using PostgreSQL, featuring encrypted password hashing for user security.

## Features

- User registration and login functionality.
- Secure password hashing using `bcrypt` (passwords are no longer stored in plain text).
- Frontend rendering using EJS templates.
- PostgreSQL database integration for persistent storage.

## Project structure

- `index.js` — main server file
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

1. Install dependencies (this will install `express`, `pg`, `body-parser`, and `bcrypt`):

```bash
npm install
