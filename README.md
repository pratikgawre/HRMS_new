# HRMS

This repository contains the HRMS frontend and backend.

## Clone and setup

1. Clone the repository:
   ```bash
   git clone https://github.com/pratikgawre/HRMS_new.git
   ```
2. Open the project folder and copy the example env files:
   ```bash
   Copy-Item Frontend\.env.example Frontend\.env
   Copy-Item backend\.env.example backend\.env
   ```
3. Update the values in those `.env` files if your local setup differs from the defaults.

## Environment variables

### Frontend

- `VITE_BACKEND_URL`
- Default: `http://localhost:8080`
- Used by Vite to proxy API and upload requests to the backend.

### Backend

- `SERVER_PORT`
- Default: `8080`
- Changes the Spring Boot server port.

- `SMTP_HOST`
- Default: empty
- Required only if you want email delivery to work.

- `SMTP_PORT`
- Default: `587`

- `SMTP_USERNAME`
- Default: empty

- `SMTP_PASSWORD`
- Default: empty

- `SMTP_FROM`
- Default: empty
- If left blank, the app falls back to `SMTP_USERNAME`.

## Run locally

### Backend

```bash
cd backend
mvn spring-boot:run
```

### Frontend

```bash
cd Frontend
npm install
npm run dev
```

## Notes

- `.env` files are ignored by git, so each developer keeps their own local secrets.
- The example files are committed so new contributors know which settings they need.
