# GeoTrade Analytics Dashboard

GeoTrade-X is a DBMS-backed geopolitical trade analytics dashboard. It combines a MySQL schema, Express API, and Tailwind-powered frontend for monitoring regional geopolitical tension, article intelligence, market impact, watchlists, user trades, and role-based database views.

## Features

- Role-based login and registration for admin, analyst, and viewer users.
- Dashboard cards for top regional geopolitical tension index values.
- Intelligence terminal backed by news article, sentiment, severity, and category tables.
- Market impact and watchlist views connected to asset and price data.
- User trade capture workflow.
- Admin table explorer with database role and grant visibility.
- MySQL schema with tables, relationships, functions, procedures, views, roles, and sample app users.

## Project Structure

```text
.
├── backend/
│   ├── db_schema.sql
│   └── server.js
├── frontend/
│   └── index.html
├── package.json
└── README.md
```

## Setup

Install dependencies:

```bash
npm install
```

Create a MySQL database from the schema:

```bash
mysql -u root -p < backend/db_schema.sql
```

Optionally create a `.env` file:

```bash
DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=GeoTradeX
PORT=3000
```

Start the app:

```bash
npm start
```

Then open `http://localhost:3000`.

## Demo Users

The server seeds these default app users when the schema exists:

| Username | Password | Role |
| --- | --- | --- |
| `admin` | `admin123` | admin |
| `analyst1` | `pass123` | analyst |
| `viewer1` | `pass123` | viewer |
