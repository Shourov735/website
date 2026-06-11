# GitHub Pages Deployment Guide

Complete step-by-step instructions for deploying your portfolio to GitHub Pages.

## Prerequisites

- GitHub account
- Git installed on your computer
- Your portfolio files ready

## Step 1: Create a GitHub Repository

### If you haven't already:

1. **Go to GitHub** and sign in
2. **Create a new repository**
   - Click the `+` icon in the top right
   - Select "New repository"
   - Name it: `portfolio` or any name you prefer
   - Choose "Public" (required for free GitHub Pages)
   - Click "Create repository"

### If you already have a repository:

You can use any existing repository. Just follow the next steps.

## Step 2: Upload Your Portfolio Files

### Option A: Using Git (Recommended)

1. **Open terminal/command prompt**

2. **Navigate to your portfolio folder**
   ```bash
   cd /path/to/portfolio
   ```

3. **Initialize Git** (if not already done)
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio commit"
   ```

4. **Add remote repository**
   ```bash
   git remote add origin https://github.com/yourusername/portfolio.git
   ```

5. **Push to GitHub**
   ```bash
   git branch -M main
   git push -u origin main
   ```

### Option B: Using GitHub Desktop

1. **Download GitHub Desktop** from desktop.github.com
2. **Login with your GitHub account**
3. **Create new repository** or open existing one
4. **Add your portfolio files** to the folder
5. **Commit and push** to GitHub

### Option C: Manual Upload

1. **Go to your GitHub repository**
2. **Click "Add file" → "Upload files"**
3. **Drag and drop your portfolio files**
4. **Commit changes**

## Step 3: Enable GitHub Pages

1. **Go to your repository**

2. **Click "Settings"**
   - Find the gear icon in the top right

3. **Scroll to "Pages" section** (left sidebar)

4. **Configure GitHub Pages**
   - Source: "Deploy from a branch"
   - Branch: Select `main`
   - Folder: Select `/ (root)`
   - Click "Save"

5. **Wait for deployment**
   - GitHub will show "Your site is live at..."
   - It may take a few minutes (refresh the page)

## Step 4: Access Your Portfolio

Your portfolio will be available at:

```
https://yourusername.github.io/portfolio
```

Or if your repo is named your-username:

```
https://yourusername.github.io
```

## Troubleshooting

### Site not showing up after 10 minutes

1. **Verify settings**
   - Go to Settings → Pages
   - Ensure branch is set to `main`
   - Ensure folder is set to `/ (root)`

2. **Check file structure**
   ```
   Your Repository Root/
   ├── index.html
   ├── style.css
   ├── script.js
   ├── README.md
   └── assets/
   ```

3. **Force refresh your browser**
   - Press Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)

### Custom Domain

To use your own domain:

1. **Purchase a domain** (GoDaddy, Namecheap, etc.)

2. **Update DNS settings**
   - Add CNAME record pointing to `yourusername.github.io`
   - Or add A records pointing to GitHub IPs

3. **Configure in GitHub**
   - Settings → Pages
   - Add your domain in "Custom domain" field
   - Click "Save"

4. **Wait for DNS propagation** (can take up to 48 hours)

## Making Updates

After your site is live, to update it:

1. **Make changes to your files locally**

2. **Commit and push to GitHub**
   ```bash
   git add .
   git commit -m "Update portfolio"
   git push
   ```

3. **GitHub will automatically redeploy**
   - Changes appear within seconds to minutes

## Security

Your GitHub Pages site is:
- ✅ HTTPS enabled by default
- ✅ Publicly accessible
- ✅ Free SSL certificate

## Performance

GitHub Pages provides:
- ✅ Fast CDN delivery
- ✅ No bandwidth limits
- ✅ Automatic GZIP compression
- ✅ HTTP/2 support

## Analytics

To track visitors:

1. **Use Google Analytics**
   - Create account at analytics.google.com
   - Get your tracking ID
   - Add to your `index.html` before closing `</body>` tag:
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
   <script>
       window.dataLayer = window.dataLayer || [];
       function gtag(){dataLayer.push(arguments);}
       gtag('js', new Date());
       gtag('config', 'GA_ID');
   </script>
   ```

## Common Questions

**Q: Can I use a custom domain?**
A: Yes! Update your DNS settings and configure in GitHub Pages settings.

**Q: How long does deployment take?**
A: Usually 1-2 minutes. Refresh after 5 minutes if not showing.

**Q: Can I have HTTPS?**
A: Yes! GitHub Pages provides free HTTPS with automatic certificates.

**Q: What if I need to see build logs?**
A: GitHub shows deployment status and errors in the repository's Actions tab.

**Q: Can I keep my portfolio private?**
A: No, GitHub Pages requires public repositories for free hosting.

## Alternative: Private Repository

If you need a private repo:
- Use GitHub Pro (paid)
- Or use Netlify/Vercel (free, supports private repos)

## Advanced: Custom GitHub Actions

For more control, create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: .
```

## Next Steps

After deployment:

1. **Share your portfolio** on social media
2. **Update contact links** to real email/social profiles
3. **Add your projects** with screenshots
4. **Collect feedback** from friends and mentors
5. **Keep it updated** with new projects and skills

## Support

- GitHub Pages Docs: https://pages.github.com
- GitHub Help: https://help.github.com
- Portfolio Issues: Check the README.md

---

**Your portfolio is now live! 🎉**

Good luck with your career!
