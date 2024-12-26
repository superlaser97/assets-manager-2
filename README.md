# Setting Up Development Environment (Windows)
1. Install NodeJS [HERE](https://nodejs.org/en/download/prebuilt-installer)
2. Install NPM by running the following command in Terminal `npm install -g npm`
3.  Install Docker Desktop by following instructions [HERE](https://docs.docker.com/desktop/setup/install/windows-install/)
4. Install dependencies (`cd app`)
    - Prisma
        - `npm install prisma @prisma/client`
        - `npx prisma init`
5. Create `.env` file in `/code` and populate the following variables
```
# .env
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_DB=logistics_dev
POSTGRES_HOST=db

# JWT secret or other secrets
JWT_SECRET=my_super_secret_jwt_key

# Next.js environment
NEXT_PUBLIC_API_URL=http://localhost:3000
```
6. Start frontend and backend
> Open two terminal windows and run the following
```
cd code/backend
npm run build && npm run start
```
```
cd code/frontend
npm run build && npm run start
```
# Documentations
- [Project Requirements](documentation/Project%20Requirements.md)