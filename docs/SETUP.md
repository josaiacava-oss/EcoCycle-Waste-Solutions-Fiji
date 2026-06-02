# EcoCycle Setup Guide

## Prerequisites

Before you begin, ensure you have installed:
- Git
- [Required runtime/framework]
- [Required database]
- [Required tools]

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/josaiacava-oss/EcoCycle-Waste-Solutions-Fiji.git
cd EcoCycle-Waste-Solutions-Fiji
```

### 2. Environment Setup

```bash
# Copy environment template
cp .env.example .env

# Edit the .env file with your configuration
nano .env
```

### 3. Install Dependencies

```bash
# Frontend
cd frontend
npm install

# Backend
cd ../backend
npm install

# Mobile App
cd ../mobile-app
npm install
```

### 4. Database Setup

```bash
# Navigate to backend
cd backend

# Run migrations
npm run migrate

# Seed initial data
npm run seed
```

### 5. Start Development Servers

```bash
# Terminal 1: Backend
cd backend
npm run dev

# Terminal 2: Frontend
cd frontend
npm run dev

# Terminal 3: Mobile App
cd mobile-app
npm run dev
```

## Verification

Once all services are running, verify:

- Backend API: http://localhost:3000/api/health
- Frontend: http://localhost:3001
- Mobile App: http://localhost:3002

## Troubleshooting

### Port Already in Use

```bash
# Find process using port
lsof -i :3000

# Kill process
kill -9 <PID>
```

### Database Connection Error

- Verify database is running
- Check connection string in .env
- Verify credentials are correct

### Dependencies Not Installing

```bash
# Clear npm cache
npm cache clean --force

# Reinstall
rm -rf node_modules package-lock.json
npm install
```

## Production Deployment

See [DEPLOYMENT.md](DEPLOYMENT.md) for production setup instructions.

## Getting Help

If you encounter issues:
1. Check existing issues and discussions
2. Review documentation
3. Create a new GitHub issue with details
