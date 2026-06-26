# �배포 가이드 - How to Deploy "How Many Farts" Website

## What You'll Do

1. ✅ Create a GitHub repository (free code hosting)
2. ✅ Upload your files to GitHub
3. ✅ Connect Cloudflare Pages to GitHub (automatic deployment)
4. ✅ Point your Cloudflare domain to the website

**Estimated Time: 15-20 minutes**

---

## Step 1: Create a GitHub Account (if you don't have one)

1. Go to https://github.com
2. Click **"Sign up"** in the top right
3. Enter your email, create a password, choose a username
4. Follow the prompts and verify your email
5. Done! You now have a GitHub account

---

## Step 2: Create a New Repository on GitHub

1. Log in to GitHub at https://github.com
2. Click the **"+"** icon in the top right corner
3. Select **"New repository"**
4. Fill in:
   - **Repository name:** `howmanyfarts` (or whatever you want)
   - **Description:** "A fun website about flatulence with a Flappy Bird-style game"
   - **Public** (so it's visible to everyone)
   - **Add README file** - Leave UNCHECKED for now
5. Click **"Create repository"**

You'll see a page with instructions. Keep this open!

---

## Step 3: Upload Your Files to GitHub

### Option A: Using GitHub Web Interface (EASIEST - Recommended for beginners)

1. On your new repository page, click **"Add file"** → **"Upload files"**
2. Drag and drop your files OR click "choose your files"
3. Select these files from `D:\agy2-projects\howmanyfarts-claude\`:
   - `index.html`
   - `README.md`
   - `MODERNIZATION.md`
   - `GAME_UPDATE.md`
   - `test.js`
   - `DEPLOYMENT_GUIDE.md` (this file)

4. At the bottom, click **"Commit changes"**
5. Done! Your files are now on GitHub

### Option B: Using Command Line (For experienced users)

If you prefer the terminal:

```bash
cd D:\agy2-projects\howmanyfarts-claude
git init
git add .
git commit -m "Initial commit: Flappy Fart game website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/howmanyfarts.git
git push -u origin main
```

(Replace `YOUR_USERNAME` with your GitHub username)

---

## Step 4: Deploy to Cloudflare Pages

### 4a. Connect GitHub to Cloudflare

1. Go to **Cloudflare Dashboard**: https://dash.cloudflare.com
2. Log in with your Cloudflare account
3. Click **"Pages"** in the left sidebar
4. Click **"Connect to Git"**
5. Select **"GitHub"**
6. Click **"Authorize Cloudflare"**
   - GitHub will ask for permission (allow it)
   - You'll be redirected back to Cloudflare

### 4b. Select Your Repository

1. In Cloudflare Pages, select **your GitHub account**
2. Find and select the **`howmanyfarts`** repository
3. Click **"Begin setup"**

### 4c. Configure Build Settings

1. **Project name**: `howmanyfarts` (or leave default)
2. **Production branch**: `main` (default)
3. **Framework preset**: `None` (select this - it's a static site)
4. **Build command**: Leave EMPTY (no build needed)
5. **Build output directory**: Leave as `public` OR change to `.` (current directory)
6. Environment variables: Leave EMPTY (not needed)

7. Click **"Save and Deploy"**

**That's it!** Cloudflare will now automatically deploy your site!

You'll see a deployment in progress. When it says "✅ Deployment successful", you're done!

---

## Step 5: Connect Your Domain to Cloudflare Pages

### 5a. Get Your Cloudflare Pages URL

1. In Cloudflare Pages, click on your project
2. You'll see a URL like: `https://howmanyfarts.pages.dev`
3. Keep this handy

### 5b. Point Your Domain to Cloudflare Pages

1. Go to **Cloudflare Dashboard**: https://dash.cloudflare.com
2. Select your domain (the one you bought)
3. Go to **"DNS"** → **"Records"**
4. Create a new record:
   - **Type**: `CNAME`
   - **Name**: `@` (or your subdomain like `www`)
   - **Target**: `howmanyfarts.pages.dev` (your Pages URL)
   - **Proxy status**: `Proxied` (orange cloud icon)
   - **TTL**: Auto
5. Click **"Save"**

Wait 1-5 minutes for DNS to propagate, then visit your domain!

### Alternative: If you want both `example.com` AND `www.example.com`:

Create TWO records:
1. `@` → `howmanyfarts.pages.dev` (for example.com)
2. `www` → `howmanyfarts.pages.dev` (for www.example.com)

---

## Step 6: Verify It's Working

1. Go to your domain in a browser (e.g., `howmanyfarts.com`)
2. You should see your website!
3. Test the calculator and game
4. Everything should work

---

## ✅ What Happens Now (Automatic Updates)

Every time you make changes:

1. Edit files in GitHub (or upload new versions)
2. Commit/push changes to GitHub
3. **Cloudflare automatically rebuilds and deploys** (takes 1-2 minutes)
4. Your live website updates automatically!

No manual deployment needed - it's all automatic! 🎉

---

## 📝 Making Changes Later

### To Update Your Website:

**Option A: GitHub Web Interface (Easy)**
1. Go to your GitHub repository
2. Click on a file you want to edit
3. Click the pencil icon to edit
4. Make changes
5. Click "Commit changes"
6. Cloudflare automatically deploys! (2-3 minutes)

**Option B: Command Line**
```bash
cd D:\agy2-projects\howmanyfarts-claude
git add .
git commit -m "Updated game physics"
git push
```

---

## 🐛 Troubleshooting

### "Website shows 404 error"
- Wait 5 minutes for DNS to propagate
- Hard refresh your browser (Ctrl+F5 or Cmd+Shift+R)
- Check your domain spelling

### "Cloudflare deployment failed"
- Go to Pages → Your project → "Deployments"
- Click the failed deployment
- Check the error message
- Common fix: Make sure you don't have a `build` command set

### "Game doesn't work"
- Check browser console (F12) for errors
- Make sure `index.html` is at the root
- Hard refresh (Ctrl+F5)

### "Domain not working"
- Go to Cloudflare DNS
- Make sure your CNAME record shows "Proxied" (orange cloud)
- Wait 5-15 minutes for DNS to update

---

## 🚀 Summary

You now have:

✅ Code on GitHub (version controlled, backed up)
✅ Website deployed to Cloudflare Pages (automatic updates)
✅ Custom domain connected (your domain name)
✅ Automatic deployments (changes push automatically)

**Your website is live! 🎉**

---

## 📚 Quick Reference Commands

```bash
# First time: Clone your repo
git clone https://github.com/YOUR_USERNAME/howmanyfarts.git
cd howmanyfarts

# Every time you make changes:
git add .
git commit -m "describe your change here"
git push
```

---

## 💡 Pro Tips

1. **Add a `.gitignore`** to exclude unwanted files
2. **Use meaningful commit messages** ("Add new game feature" not "fix")
3. **Keep your README updated** with how to play
4. **Test locally** before pushing (just open `index.html`)
5. **Monitor Cloudflare Analytics** to see visitors

---

## 🎯 You're Done!

Your website is published and live! Share the link with friends! 🚀

Got questions? Check GitHub Docs or Cloudflare Support!
