# Authentication Project

This is a simple Express + EJS authentication app using PostgreSQL.

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

1. Install dependencies:

```bash
npm install
```

2. Create the database table:

```bash
psql -U postgres -d secrets -f queries.sql
```

3. Start the app:

```bash
node index.js
```

4. Open in browser:

```
http://localhost:3000
```


