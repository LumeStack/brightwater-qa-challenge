# Brightwater Billing Portal, staging build

This is a staging build of the Brightwater Billing Portal. Treat it as a black box: the source code is not provided.

## How to run

No `npm install` is needed. Requires Node.js 20 or Docker.

```bash
node app/server.min.js
```

or

```bash
docker compose up
```

Base URL: `http://localhost:3000` (set `PORT` to use another port).

## Credentials

- Email: `qa.candidate@brightwater.example`
- Password: `Brightwater#2026`

## Reset endpoint

`POST /api/test/reset` restores the seed data. It is idempotent and needs no session.

```bash
curl -X POST http://localhost:3000/api/test/reset
```

## Reminder

The ticket text lives in the challenge email ([CHALLENGE.md](CHALLENGE.md)). The business rules are answered by the product owner in Part 0.
