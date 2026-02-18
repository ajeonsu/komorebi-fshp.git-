# GitHub Repository Setup for Komorebi

## Step 1: Create a GitHub Repository

1. Go to GitHub: https://github.com/new
2. Fill in the details:
   - **Repository name**: `komorebi-fshp` (or any name you prefer)
   - **Description**: "Komorebi Cooking Service Website - 料理代行 こもれび"
   - **Visibility**: Choose Public or Private
   - **⚠️ IMPORTANT**: Do NOT initialize with README, .gitignore, or license (we already have these)
3. Click **Create repository**

## Step 2: Copy Your Repository URL

After creating, GitHub will show you a URL like:
- `https://github.com/YOUR-USERNAME/komorebi-fshp.git`
- OR `git@github.com:YOUR-USERNAME/komorebi-fshp.git`

Copy this URL!

## Step 3: I'll Push the Code

Once you have the URL, give it to me and I'll:
1. Add the remote repository
2. Push your code to GitHub
3. Connect Vercel to the GitHub repository

---

## Alternative: Quick Setup

If you're comfortable with GitHub, you can also:

```bash
# After creating the repo on GitHub, run:
git remote add origin https://github.com/YOUR-USERNAME/komorebi-fshp.git
git branch -M main
git push -u origin main
```

Then in Vercel dashboard:
1. Go to: Settings → Git
2. Click "Connect Git Repository"
3. Select your GitHub repository
