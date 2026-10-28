# MarineCossy Restaurant: Backend

REST API for a restaurant ordering and POS system. It handles authentication, menu, orders, reservations, and real-time kitchen updates.

**Live API:** https://cm-restopos-backend.onrender.com
**Live frontend:** https://cm-resto-pos-frontend.vercel.app
**Frontend repo:** https://github.com/cosmy13647/resto-pos-frontend

## Features

- JWT authentication with role-based access (cashier, waiter, kitchen, manager, admin)
- Menu management
- Order creation, tracking, and receipts
- Table reservations
- Void requests with manager approval
- Shift reconciliation
- Real-time order updates with Socket.io

## Tech Stack

- Node.js + Express
- MongoDB (Mongoose)
- JSON Web Tokens (JWT)
- Socket.io
- Deployed on Render

## Getting Started

```bash
git clone https://github.com/cosmy13647/resto-pos-backend.git
cd resto-pos-backend
npm install
```

Create a `.env` file:

```
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
CLIENT_URL=http://localhost:5173
```

Run the server:

```bash
npm run dev
```

## API Overview

| Route | Purpose |
|-------|---------|
| `/api/auth` | Register and login |
| `/api/menu` | Menu items |
| `/api/orders` | Create and manage orders |
| `/api/reservations` | Table bookings |

## Deployment

Deployed on Render. Set `MONGODB_URI`, `JWT_SECRET`, and `CLIENT_URL` (the frontend's Vercel URL) in the Render environment settings.

## Notes

- `CLIENT_URL` must match the frontend's address, or CORS will block requests.
- On Render's free plan, the server sleeps when idle, so the first request can take about a minute.

## Author

Cosmy Techs
GitHub: [@cosmy13647](https://github.com/cosmy13647)
