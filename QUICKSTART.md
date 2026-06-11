# Quick Start Guide

Get your portfolio running locally in 30 seconds.

## Option 1: Python (Easiest)

**If you have Python installed:**

```bash
cd /path/to/portfolio
python -m http.server 8000
```

Then visit: `http://localhost:8000`

**For Python 2 (older systems):**
```bash
python -m SimpleHTTPServer 8000
```

## Option 2: Node.js

**Using http-server:**
```bash
npx http-server
```

**Using live-server (with auto-refresh):**
```bash
npx live-server
```

## Option 3: No Installation Needed

Simply double-click `index.html` in your file explorer.

**Note:** Some features may work better with a local server.

## Option 4: VS Code Live Server

1. Install "Live Server" extension in VS Code
2. Right-click `index.html`
3. Select "Open with Live Server"

## Customization Checklist

- [ ] Update your name and title in the hero section
- [ ] Add your profile picture to `assets/images/`
- [ ] Update skills and technologies
- [ ] Add your projects with descriptions
- [ ] Update education information
- [ ] Add achievements and certifications
- [ ] Update contact information and social links
- [ ] Change color scheme if desired
- [ ] Test on mobile devices
- [ ] Connect contact form (see README.md)

## Testing Checklist

- [ ] Navigation works and highlights active section
- [ ] Dark mode toggle works
- [ ] Back-to-top button appears on scroll
- [ ] Mobile menu opens/closes
- [ ] Form validates input
- [ ] Links open correctly
- [ ] Animations play smoothly
- [ ] Images load properly
- [ ] Responsive design works on all sizes

## Browser Testing

Test on multiple browsers:
- Chrome/Chromium
- Firefox
- Safari (if on Mac)
- Edge
- Mobile browsers

## File Structure Reminder

```
portfolio/
├── index.html          ← Main file
├── style.css           ← Styles
├── script.js           ← Functionality
├── README.md           ← Full documentation
├── DEPLOYMENT.md       ← Deployment guide
├── QUICKSTART.md       ← This file
└── assets/
    ├── images/         ← Your project images
    ├── icons/          ← Custom icons
    └── documents/      ← Your CV, etc.
```

## Optimization Tips

1. **Compress Images**
   - Use TinyPNG, ImageOptim, or similar
   - Reduce file sizes without quality loss

2. **Add Favicon**
   - Create a 32x32 PNG image
   - Save as `assets/icons/favicon.ico`
   - Add to `<head>`: `<link rel="icon" href="assets/icons/favicon.ico">`

3. **Add Open Graph Meta Tags**
   - Add to `<head>` for better social sharing:
   ```html
   <meta property="og:title" content="Md. Shourov - Portfolio">
   <meta property="og:description" content="Software Engineering Student">
   <meta property="og:image" content="assets/images/preview.jpg">
   ```

4. **Improve SEO**
   - Update meta description
   - Add keywords to meta tags
   - Create a `sitemap.xml`

## Deployment Reminder

When ready to deploy:

1. Follow DEPLOYMENT.md for GitHub Pages
2. Or use Netlify/Vercel for easier setup
3. Test the live version
4. Update links if using custom domain

## Common Issues

**Images not showing?**
- Check file paths: `assets/images/filename.jpg`
- Ensure files exist in the folder
- Check file names for typos

**Styles not applying?**
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Check file path: `href="style.css"`

**JavaScript not working?**
- Check browser console for errors: F12 or Right-click → Inspect
- Verify script.js exists in root folder
- Check file path: `src="script.js"`

**Dark mode not working?**
- Browser may have localStorage disabled
- Try a different browser
- Check if localStorage is enabled

## Performance Metrics

Target:
- Page load: < 2 seconds
- Lighthouse Performance: > 90
- Lighthouse Accessibility: > 95
- Lighthouse Best Practices: > 90

## Mobile Optimization

- [ ] Test on iPhone
- [ ] Test on Android
- [ ] Check touch targets (minimum 44x44px)
- [ ] Verify text is readable
- [ ] Check form is easy to use

## Accessibility Check

- [ ] Keyboard navigation works
- [ ] Color contrast is sufficient
- [ ] Images have alt text
- [ ] Form labels are present
- [ ] Links are descriptive

## Next Steps

1. Customize your information
2. Test locally
3. Deploy to GitHub Pages
4. Share with recruiters
5. Keep it updated with new projects

## Need Help?

- Read README.md for detailed docs
- Check DEPLOYMENT.md for deployment steps
- Review code comments in HTML/CSS/JS
- Search GitHub for similar issues

---

**Ready to go! Build something amazing! 🚀**
