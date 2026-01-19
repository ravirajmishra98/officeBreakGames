# Quick Vercel Deployment Guide

## Step 1: Get Vercel Blob Token

1. Go to: https://vercel.com/dashboard
2. Navigate to: **Storage** → **Create Database** → **Blob**
3. Create a new Blob store (or use existing)
4. Copy the **Read/Write Token**

## Step 2: Deploy via Dashboard

1. **Import Repository**:
   - Visit: https://vercel.com/new
   - Select: `ravirajmishra98/officeBreakGames`
   - Click "Import"

2. **Configure Project** (Auto-detected):
   - Framework: Vite ✅
   - Build Command: `npm run build` ✅
   - Output Directory: `dist` ✅

3. **Add Environment Variables**:
   ```
   BLOB_READ_WRITE_TOKEN = <your-blob-token>
   VITE_ADMIN_ANALYTICS_KEY = <your-secret-key>
   ```
   - Apply to: Production, Preview, Development

4. **Deploy**:
   - Click "Deploy"
   - Wait ~2-3 minutes

## Step 3: Post-Deployment

After deployment completes:

1. **Visit your site**: `https://your-app.vercel.app`
2. **Test analytics dashboard**: 
   `https://your-app.vercel.app/__admin/analytics?key=<your-secret-key>`
3. **Verify**:
   - ✅ Home page loads
   - ✅ Games play correctly
   - ✅ No console errors
   - ✅ Analytics tracking works

## Troubleshooting

- **Build fails?** Check build logs in Vercel dashboard
- **Analytics not working?** Verify `BLOB_READ_WRITE_TOKEN` is set correctly
- **Dashboard 404?** Check `VITE_ADMIN_ANALYTICS_KEY` matches your query param

## Your Repository

🔗 https://github.com/ravirajmishra98/officeBreakGames

Ready to deploy! 🚀
