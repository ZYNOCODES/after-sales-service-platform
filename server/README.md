# API server

Express API. Part of [After-Sales Service Platform](../README.md).

> **Structure only.** The source code is private. Source files here are intentionally empty so you can see how the project is organized. Commands describe the private codebase.

## Responsibilities

- Tickets with a six-step progress flow
- PDF deposit and delivery slips, including Arabic fonts
- SMS and email notifications
- Dashboards built with aggregated queries
- Request identifiers and structured logs
- Specific rate limits for public routes

## Main dependencies

`axios`, `cors`, `crypto-js`, `dotenv`, `express`, `express-rate-limit`, `jsonwebtoken`, `moment`, `multer`, `mysql2`, `nodemailer`, `nodemon`, `pdfkit`, `pdfkit-table`, `pino`, `pino-http`, `sequelize`, `validator`

## Structure

```text
config/                           1 file
controllers/                      13 files
documents/                        3 files
fonts/                            2 files
images/                           2 files
middleware/                       5 files
models/                           11 files
public/                           20 files
routes/                           12 files
scripts/                          8 files
services/                         1 file
test/                             1 file
util/                             1 file
utils/                            11 files
```

## Commands

```bash
npm install
npm start
```
