# Initialise a Worker in Cloudflare

### 1. Initialise a worker
```bash
npm create cloudflare -- my-app
```
Select `no` for `do you want to deploy?`

### 2. Start the worker locally
```bash
npm run dev
```

### 3. To deploy a worker
1. Login to cloudflare via the `wrangler cli`
   ```bash
   npx wrangler login
   ```
2. Deploy your worker
   ```bash
   npm run deploy
   ```

# Using hono
Working with cloudflare worker using hono
1. Initialise a new app
   ```bash
   npm create hono@latest my-app
   ```
2. cd to my-app and install dependencies
   ```bash
   cd my-app
   npm i
   ```
3. Deploying
   to deploy your code (make sure you're logged into cloudflare(wrangler login)
   ```bash
   npm run deploy
   ```
