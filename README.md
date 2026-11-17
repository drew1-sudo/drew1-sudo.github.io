# BudgetBook – Business Budget Tracker

Track income, expenses, budgets and reports for a business, in Philippine Peso (₱).

## Run

Requires Node.js 22.13 or newer (uses the built-in `node:sqlite`). No `npm install` needed.

```
npm start
```

Open http://localhost:5050. To use another port: `PORT=5051 npm start`.

Demo account (12 months of sample café data): `demo@example.com` / `demo1234`.

## What's inside

| File | Purpose |
| --- | --- |
| `server.js` | HTTP server, JSON API, auth (scrypt passwords, HttpOnly session cookie), validation, sample data |
| `index.html` | Page shell: sign-in/register and app layout |
| `app.js` | Dashboard, income, expenses, budgets, reports, transactions, settings |
| `styles.css` | Navy / white / gray theme with green accents, responsive layout |
| `data/budget.db` | SQLite database, created on first start |

Charts (Chart.js), PDF export (jsPDF) and Excel export (SheetJS) load from cdnjs, so those need an internet connection.
Everything else works offline.

## Reset

Stop the server and delete the `data/` folder. The demo account is recreated on the next start.
