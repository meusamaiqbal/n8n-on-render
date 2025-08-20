# n8n on Render (Free Plan) with PostgreSQL

This repo deploys [n8n](https://n8n.io) on Render’s free plan using PostgreSQL for persistent storage.

## 🚀 Deploy Steps
1. Fork this repo.
2. Go to [Render](https://dashboard.render.com/) → **New Blueprint (YAML)**.
3. Connect your GitHub repo with this `render.yaml` file.
4. Render will auto-provision:
   - A **Web Service** for n8n
   - A **PostgreSQL database**
5. Build Command: `npm install`
6. Start Command: `npm run start`
7. Render will inject all required environment variables automatically.

## ⚡ Notes
- Workflows are stored in PostgreSQL (persistent, safe across redeploys).
- Free plan includes 750 compute hours/month and a free Postgres tier.
- Add your own domain + SSL for production use.

## 🔑 Environment Variables
Already handled by `render.yaml`, but if adding manually:
```
N8N_PORT=10000
N8N_HOST=0.0.0.0
N8N_EDITOR_BASE_URL=https://your-app.onrender.com
N8N_ENCRYPTION_KEY=your-secret
DB_TYPE=postgresdb
DB_POSTGRESDB_HOST=...
DB_POSTGRESDB_PORT=5432
DB_POSTGRESDB_DATABASE=...
DB_POSTGRESDB_USER=...
DB_POSTGRESDB_PASSWORD=...
```
