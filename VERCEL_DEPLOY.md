# Vercel Deployment Guide

## Quick Deploy Steps

1. **Connect Repository to Vercel**
   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "New Project"
   - Import `chay0354/rooms-back` from GitHub
   - Select the repository and click "Deploy"

2. **Configure Project Settings**
   - **Framework Preset**: Other (or Express.js if available)
   - **Root Directory**: `./` (default)
   - **Build Command**: Leave empty (or `npm install`)
   - **Output Directory**: Leave empty

3. **Set Environment Variables**
   Click on "Environment Variables" and add:

   ```
   PORT=3001
   SECRET_KEY=your_super_secret_key_for_jwt
   FRONTEND_URL=https://your-frontend-domain.vercel.app
   NODE_ENV=production
   
   SUPABASE_URL=https://qzzxywzgoqiqfcrthmiu.supabase.co
   SUPABASE_SERVICE_ROLE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InF6enh5d3pnb3FpcWZjcnRobWl1Iiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTc2NzQyODcxMiwiZXhwIjoyMDgzMDA0NzEyfQ.ZR083jDwKhcnCfgBs3QQdWSWukP-nYbjKberfZtLmqo
   SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InF6enh5d3pnb3FpcWZjcnRobWl1Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3Njc0Mjg3MTIsImV4cCI6MjA4MzAwNDcxMn0.GQekTukDpX04XK-5Ycfn59Lr98HQ-Wec0d6fmvIvZXs
   ```

4. **Deploy**
   - Click "Deploy"
   - Wait for deployment to complete
   - Your API will be available at: `https://your-project-name.vercel.app`

## Important Notes

- **FRONTEND_URL**: Update this to your actual frontend URL (Vercel deployment URL or custom domain)
- **CORS**: The backend is configured to accept requests from the FRONTEND_URL
- **Serverless**: The app runs as serverless functions on Vercel
- **Environment Variables**: Make sure all variables are set before deploying

## Testing the Deployment

After deployment, test your API:
- `https://your-project-name.vercel.app/api/users`
- `https://your-project-name.vercel.app/api/rooms`
- `https://your-project-name.vercel.app/api/bookings`

## Update Frontend

After deployment, update your frontend `.env` file:
```
VITE_API_URL=https://your-project-name.vercel.app
```

