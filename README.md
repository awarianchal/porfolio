# Anchal Awari — MERN Portfolio

A responsive dark-purple personal portfolio built with React (Vite), Express, Node.js and MongoDB.

## Included
- Hero, About, Education, Skills, Projects, Internship and Contact sections
- Responsive navigation and mobile layout
- Resume download link (add your PDF to `client/public/Anchal_Awari_Resume.pdf`)
- Contact form backed by an Express API and MongoDB
- Ready-to-deploy configuration for Vercel (frontend) and Render (backend)

## 1. Requirements
- Node.js 18+
- MongoDB Atlas account (or local MongoDB)
- GitHub account for deployment

## 2. Run locally

### Backend
```bash
cd server
npm install
cp .env.example .env
```
Edit `server/.env` and set `MONGODB_URI` and `CLIENT_ORIGIN`.

```bash
npm run dev
```
API runs at `http://localhost:5000`.

### Frontend
Open another terminal:
```bash
cd client
npm install
cp .env.example .env
npm run dev
```
Open the local URL printed by Vite (usually `http://localhost:5173`).

## 3. Add your resume and personal links
1. Copy your resume PDF to `client/public/Anchal_Awari_Resume.pdf`.
2. Edit `client/src/data.js` and replace the placeholder email, LinkedIn and GitHub URLs.
3. Update any project descriptions or internship details to match your actual experience.

## 4. Deploy the backend to Render
1. Push this project to a GitHub repository.
2. In Render, create **New + → Web Service** and connect the repository.
3. Set **Root Directory** to `server`.
4. Build command: `npm install`
5. Start command: `npm start`
6. Add environment variables:
   - `MONGODB_URI` = your MongoDB Atlas connection string
   - `CLIENT_ORIGIN` = your deployed Vercel URL (for example `https://your-site.vercel.app`)
   - `NODE_ENV` = `production`
7. Deploy and copy the Render service URL.

## 5. Deploy the frontend to Vercel
1. In Vercel, import the same GitHub repository.
2. Set **Root Directory** to `client`.
3. Add environment variable `VITE_API_URL` = your Render URL plus `/api` (for example `https://your-api.onrender.com/api`).
4. Deploy.
5. After deployment, update `CLIENT_ORIGIN` in Render to your exact Vercel domain and redeploy the backend.

## Important
- Do not commit `.env` files or expose your MongoDB password.
- The contact form stores messages in MongoDB. Add spam protection and rate limiting before public production use.
- This project cannot be published to your personal accounts without you connecting/authorizing those accounts.
