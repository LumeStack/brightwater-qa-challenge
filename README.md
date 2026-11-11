# Brightwater Billing Portal, staging build

This is a staging build of the Brightwater Billing Portal. Treat it as a black box: the source code is not provided.

## Staging environment

Base URL: **https://brightwater-billing-portal.onrender.com**

The staging server sleeps when idle. The first request after a pause can take about a minute, and waking up restores the seed data (same as a reset). Open the URL once before you start a test run.

## How to run locally (optional)

No `npm install` is needed. Requires Node.js 20 or Docker.

```bash
node app/server.min.js
```

or

```bash
docker compose up
```

Local base URL: `http://localhost:3000` (set `PORT` to use another port).

## Credentials

- Email: `qa.candidate@brightwater.example`
- Password: `Brightwater#2026`

## Reset endpoint

`POST /api/test/reset` restores the seed data. It is idempotent and needs no session.

```bash
curl -X POST https://brightwater-billing-portal.onrender.com/api/test/reset
```

## Reminder

The ticket text lives in the challenge email ([CHALLENGE.md](CHALLENGE.md)). The business rules are answered by the product owner in Part 0.
