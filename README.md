# AutoHub React landing page

Responsive React + Vite landing page for automotive accessories, repair/maintenance, vehicle scrapping, and tyre/wheel care. The booking form submits to the companion Spring Boot API.

## Run locally

1. Start the Spring Boot API (see `../autohub-api/README.md`).
2. In this directory run:

```bash
npm install
cp .env.example .env.local
npm run dev
```

The form calls `http://localhost:8080/api/v1/bookings` by default. Set `VITE_API_BASE_URL` to the deployed API base URL when deploying the frontend.

## Configure business details

Edit `src/config.js` and replace the demo phone, email, address, hours and map URL. Replace social links in `src/main.jsx`.

## Deploy

Deploy this folder as a Vite project on Vercel. Configure `VITE_API_BASE_URL` in Vercel project environment variables to your deployed Spring Boot API URL, then redeploy. The API must allow the frontend origin through its `app.cors.allowed-origins` setting.
