# Prisma Setup Guide

### 1. Initialize an empty Node.js project

```bash
npm init -y
```

### 2. Add dependencies
```bash
npm install prisma typescript ts-node @types/node --save-dev
```

### 3. Initialise typescript
```bash
npx tsc --init
Change 'rootDir' to src
Change 'outDir' to dist
```

### 4. Initialise fresh prisma project
```bash
npx prisma init
```

### 5. Setup schema.prisma file
Replace database url and output path for prisma client

### 6. Generate migrations
You have created a single schema file. You haven’t yet run the CREATE TABLE  commands. To run those and create migration files , run 
```bash
npx prisma migrate dev --name Initialize the schema
```

### 7. How to generate client
Client represent all the functions that convert
```bash
User.create({email:"demo@gmail.com"})
```
into
```bash
INSERT INTO User VALUES ...
```
Once you've created the prisma/schema.prisma , you can generate these clients that you can use in your Node.js app
```bash
npx prisma generate
```
