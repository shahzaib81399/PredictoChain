# PredictoChain

PredictoChain is an AI‑powered crypto prediction and insights platform. It combines macroeconomic analysis, custom trading signals, and token‑gated access to deliver premium dashboards for retail and institutional traders.

This repository contains the monorepo for the platform, including the frontend (Next.js), backend (Node/Express), and Python microservice (FastAPI) used to run the trading signal script.

## Structure

```
predictochain/
  frontend/      # Next.js application (TypeScript + Tailwind)
  backend/       # Node.js/Express API server
  python_service/ # FastAPI microservice for trading signals
  prisma/        # Prisma schema and migrations
  docker-compose.yml # Compose file for local development
```

### Frontend

The `frontend` directory contains a bare‑bones Next.js app set up with TypeScript and Tailwind CSS. You can run the development server with `npm run dev` after installing dependencies.

### Backend

The `backend` directory contains an Express.js server stub. It is prepared for authentication, Stripe, and Web3 integration. A Prisma schema is included under `prisma/schema.prisma`.

### Python Service

The `python_service` directory holds a minimal FastAPI application. This service is intended to run user‑provided trading signal scripts securely. Dependencies are listed in `requirements.txt`.

## Getting Started

```bash
cd predictochain

# Install dependencies for each service
cd frontend && npm install && cd ..
cd backend && npm install && cd ..
cd python_service && pip install -r requirements.txt && cd ..

# Start services (local development)
docker-compose up
```

This repository is a starting point. Please extend each module with the actual application code, authentication logic, payment integrations, and AI pipelines as described in the project specification.
