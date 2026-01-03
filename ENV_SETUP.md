# Backend Environment Variables

Create a `.env` file in the `rooms-back` directory with the following variables:

```env
# Server Configuration
PORT=3001
SECRET_KEY=your_super_secret_key_for_jwt
FRONTEND_URL=http://localhost:3000
NODE_ENV=development

# Supabase Configuration
SUPABASE_URL=https://qzzxywzgoqiqfcrthmiu.supabase.co
SUPABASE_SERVICE_ROLE_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InF6enh5d3pnb3FpcWZjcnRobWl1Iiwicm9sZSI6InNlcnZpY2Vfcm9sZSIsImlhdCI6MTc2NzQyODcxMiwiZXhwIjoyMDgzMDA0NzEyfQ.ZR083jDwKhcnCfgBs3QQdWSWukP-nYbjKberfZtLmqo
SUPABASE_ANON_KEY=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6InF6enh5d3pnb3FpcWZjcnRobWl1Iiwicm9sZSI6ImFub24iLCJpYXQiOjE3Njc0Mjg3MTIsImV4cCI6MjA4MzAwNDcxMn0.GQekTukDpX04XK-5Ycfn59Lr98HQ-Wec0d6fmvIvZXs
```

**Important Security Notes:**
- Never commit the `.env` file to git
- Use a strong `SECRET_KEY` in production
- The `SUPABASE_SERVICE_ROLE_KEY` has full access - keep it secure

