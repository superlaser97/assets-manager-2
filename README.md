# Asset Manager 2
Work In Progress
## Design
- Frontend (NextJS)
- Backend (NextJS)
- Database (Postgres SQL)
- Database Dashboard (pgAdmin)

# Set Up Development Environment (Windows)
1. Install NodeJS from [here](https://nodejs.org/en/download/prebuilt-installer)
2. Install NPM by running the following command in Terminal `npm install -g npm`
> Check if they are installed by running `node -v` and `npm -v`
3.  Install Docker Desktop from [here](https://docs.docker.com/desktop/setup/install/windows-install/)
4. Install dependencies (`cd app`)
    - Prisma
        - `npm install prisma @prisma/client`
        - `npx prisma init`
5. Create `.env` file in `/code` and populate the following variables
> This enviroment file is not excluded from git at this moment
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
6. Open two terminal windows and run the following
```
cd ./code/backend
npm install nextjs
```
```
cd ./code/frontend
npm install nextjs
```
## Start Development Server (No database at the moment)
> Open two terminal windows and run the following
```
cd ./code/backend
npm run build && npm run start
```
```
cd ./code/frontend
npm run build && npm run start
```
## Start Development Server (Dockerized)
```
cd ./code/backend
npm run build

cd ./code/frontend
npm run build

cd ./code
docker compose --env-file .env -f ./docker-compose.yml up
```
# Documentations
- [Project Requirements](documentation/Project%20Requirements.md)