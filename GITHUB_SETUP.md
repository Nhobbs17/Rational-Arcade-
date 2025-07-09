# GitHub Setup Guide

Follow these steps to upload your Rational Arcade project to GitHub and deploy it anywhere.

## Step 1: Prepare Your Project

### 1.1 Create a GitHub Repository
1. Go to [GitHub.com](https://github.com)
2. Click "New repository"
3. Name it: `rational-arcade-game`
4. Add description: "Educational game platform for learning rational functions"
5. Set to Public (or Private if preferred)
6. Click "Create repository"

### 1.2 Download/Clone Your Project
If you're on Replit:
1. Go to your Replit project
2. Click the three dots menu
3. Select "Download as ZIP"
4. Extract the files to your computer

## Step 2: Upload to GitHub

### Option A: Using GitHub Desktop (Recommended for beginners)
1. Download [GitHub Desktop](https://desktop.github.com/)
2. Sign in to your GitHub account
3. Click "Clone a repository from the Internet"
4. Select your repository
5. Copy all your project files to the cloned folder
6. In GitHub Desktop, write a commit message: "Initial commit"
7. Click "Commit to main"
8. Click "Push origin"

### Option B: Using Command Line
```bash
# Navigate to your project folder
cd path/to/your/project

# Initialize git
git init

# Add all files
git add .

# Create first commit
git commit -m "Initial commit"

# Connect to GitHub
git remote add origin https://github.com/YOUR_USERNAME/rational-arcade-game.git

# Push to GitHub
git push -u origin main
```

## Step 3: Deploy Your App

### Option 1: Deploy to Vercel (Recommended)
1. Go to [vercel.com](https://vercel.com)
2. Sign in with GitHub
3. Click "New Project"
4. Select your repository
5. Configure:
   - Build Command: `npm run build`
   - Output Directory: `dist`
   - Install Command: `npm install`
6. Click "Deploy"
7. Your app will be live at `https://your-project.vercel.app`

### Option 2: Deploy to Netlify
1. Go to [netlify.com](https://netlify.com)
2. Sign up/Sign in
3. Click "New site from Git"
4. Choose GitHub and select your repository
5. Configure:
   - Build command: `npm run build`
   - Publish directory: `dist`
6. Click "Deploy site"

### Option 3: Deploy to Railway
1. Go to [railway.app](https://railway.app)
2. Sign in with GitHub
3. Click "New Project"
4. Select "Deploy from GitHub repo"
5. Choose your repository
6. Railway will automatically detect and deploy your app

### Option 4: Deploy to Render
1. Go to [render.com](https://render.com)
2. Sign up/Sign in
3. Click "New +" → "Web Service"
4. Connect your GitHub repository
5. Configure:
   - Build Command: `npm run build`
   - Start Command: `npm start`
6. Click "Create Web Service"

## Step 4: Environment Variables (If Using Database)

If you want to use a real PostgreSQL database instead of in-memory storage:

### 4.1 Get a Database
- [Neon](https://neon.tech) - Free PostgreSQL
- [Supabase](https://supabase.com) - Free PostgreSQL
- [Railway](https://railway.app) - PostgreSQL addon

### 4.2 Set Environment Variables
In your deployment platform, add:
- `DATABASE_URL=postgresql://username:password@host:port/database`
- `NODE_ENV=production`

## Step 5: Running Locally

Anyone can now run your app locally:

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/rational-arcade-game.git

# Navigate to project
cd rational-arcade-game

# Install dependencies
npm install

# Start development server
npm run dev
```

## Step 6: Continuous Deployment

Once set up, any changes you push to GitHub will automatically deploy:

1. Make changes to your code
2. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Add new feature"
   git push
   ```
3. Your deployment platform will automatically update

## Troubleshooting

### Common Issues:
1. **Build fails**: Check that all dependencies are in `package.json`
2. **Database errors**: Ensure `DATABASE_URL` environment variable is set
3. **404 errors**: Make sure the server is configured to serve the React app

### Getting Help:
- Check the deployment platform's logs
- Review the README.md for specific setup instructions
- Test locally first with `npm run dev`

## Files Created for GitHub:
- ✅ `README.md` - Project documentation
- ✅ `.gitignore` - Files to exclude from Git
- ✅ `vercel.json` - Vercel deployment config
- ✅ `render.yaml` - Render deployment config
- ✅ `Dockerfile` - Docker deployment config

Your project is now ready to be shared and deployed anywhere! 🚀