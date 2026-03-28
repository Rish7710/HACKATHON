# 🚀 Vercel Deployment Guide

## Step-by-Step Instructions to Deploy Your Financial Assistant

### Method 1: Deploy via Vercel Dashboard (Easiest)

#### Step 1: Export Your Code from Figma Make
1. Look for the **Export** or **Download** button in Figma Make
2. Download all project files as a ZIP
3. Extract the ZIP file to a folder on your computer

#### Step 2: Create a GitHub Repository
1. Go to [github.com](https://github.com)
2. Click the **"+"** icon → **"New repository"**
3. Name it: `ai-financial-assistant` (or any name you prefer)
4. Make it **Public** or **Private** (your choice)
5. Click **"Create repository"**

#### Step 3: Upload Code to GitHub

**Option A - Using GitHub Web Interface:**
1. On your new repository page, click **"uploading an existing file"**
2. Drag and drop ALL files from your extracted folder
3. Add commit message: "Initial commit"
4. Click **"Commit changes"**

**Option B - Using Git Command Line:**
```bash
cd path/to/your/extracted/folder
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ai-financial-assistant.git
git push -u origin main
```

#### Step 4: Deploy on Vercel
1. Go to [vercel.com](https://vercel.com)
2. Click **"Sign Up"** (use your GitHub account)
3. Click **"Add New..."** → **"Project"**
4. Click **"Import"** next to your `ai-financial-assistant` repository
5. Vercel will auto-detect settings:
   - **Framework Preset**: Vite
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
   - **Install Command**: `npm install`
6. Click **"Deploy"**

⏳ **Wait 2-3 minutes** for the build to complete...

✅ **Done!** You'll get a live URL like: `https://ai-financial-assistant.vercel.app`

---

### Method 2: Deploy via Vercel CLI (Advanced)

#### Step 1: Install Vercel CLI
```bash
npm install -g vercel
```

#### Step 2: Navigate to Your Project
```bash
cd path/to/your/project
```

#### Step 3: Deploy
```bash
vercel login
vercel
```

Follow the prompts, and your app will be deployed!

---

## 🔧 Post-Deployment Configuration

### Custom Domain (Optional)
1. In Vercel dashboard, go to your project
2. Click **"Settings"** → **"Domains"**
3. Add your custom domain
4. Update DNS records as instructed

### Environment Variables (For Future Supabase Integration)
1. Go to **"Settings"** → **"Environment Variables"**
2. Add these variables when you integrate Supabase:
   ```
   SUPABASE_URL=your_supabase_project_url
   SUPABASE_ANON_KEY=your_anon_key
   SUPABASE_SERVICE_ROLE_KEY=your_service_role_key
   ```

---

## ✅ Verification Checklist

After deployment, verify:
- [ ] Home page loads correctly
- [ ] Navigation works (Dashboard, Analytics, Insights, Upload, Settings)
- [ ] Charts render properly
- [ ] Mobile responsive design works
- [ ] All luxury styling (black/white/gold) appears correctly
- [ ] Indian Rupee (₹) formatting displays properly

---

## 🐛 Troubleshooting

### Build Failed?
**Check:**
- All dependencies in package.json are correct
- No syntax errors in code
- Node version compatibility (use Node 18+)

**Solution:**
```bash
# Test build locally first
npm run build
```

### Routes Not Working (404 errors)?
**Solution:** The `vercel.json` file should already be configured. If you get 404s on routes:
1. Check `vercel.json` exists in root directory
2. Redeploy the project

### Fonts Not Loading?
**Solution:** Check that `/src/styles/fonts.css` has correct font imports

---

## 📊 What's Deployed

Your live application includes:
- ✅ **Luxury Landing Page** - Premium design showcase
- ✅ **Dashboard** - Financial overview with metrics
- ✅ **Analytics** - Cash flow forecasting & trends
- ✅ **Insights** - AI recommendations & alerts
- ✅ **Upload** - Document upload interface
- ✅ **Settings** - User preferences

---

## 🔄 Continuous Deployment

Once deployed:
- **Automatic Deploys**: Every push to `main` branch auto-deploys
- **Preview Deploys**: Pull requests get preview URLs
- **Instant Rollback**: Can rollback to any previous deployment

---

## 🎉 You're Live!

Share your URL:
```
https://your-project-name.vercel.app
```

---

## 📞 Need Help?

- **Vercel Docs**: https://vercel.com/docs
- **GitHub Issues**: Create an issue in your repository
- **Vercel Support**: support@vercel.com

---

**Note**: This is currently a prototype with mock data. For production use with real financial data, you'll need to add:
- Backend API integration
- Database (Supabase)
- User authentication
- OCR service integration
- Security hardening
