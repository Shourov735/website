# Md. Shourov - Portfolio Website

A modern, responsive personal portfolio website built with vanilla HTML, CSS, and JavaScript. Designed to showcase software engineering projects, skills, and achievements to recruiters and potential collaborators.

## 🌟 Features

- **Responsive Design**: Mobile-first approach, works seamlessly on all devices
- **Dark Mode**: Toggle between light and dark themes with local storage persistence
- **Smooth Navigation**: Sticky navbar with active section highlighting and smooth scrolling
- **Modern Animations**: Scroll animations and transitions throughout the site
- **Contact Form**: Functional contact form with validation (backend integration ready)
- **Performance Optimized**: Fast loading, no external framework dependencies
- **SEO Friendly**: Semantic HTML, proper meta tags, and accessibility features
- **Accessibility**: WCAG compliant, keyboard navigation support, reduced motion preferences

## 📁 Project Structure

```
portfolio/
├── index.html           # Main HTML file with all sections
├── style.css            # Comprehensive CSS with dark mode support
├── script.js            # Vanilla JavaScript for interactivity
├── assets/
│   ├── images/          # Place your images here
│   ├── icons/           # Place your icons here
│   └── documents/       # Place your CV/documents here
└── README.md            # This file
```

## 🚀 Getting Started

### Local Development

1. **Clone or download the repository**
   ```bash
   git clone https://github.com/yourusername/portfolio.git
   cd portfolio
   ```

2. **Open in a browser**
   - Simply open `index.html` in your web browser
   - Or use a local server (recommended):

   ```bash
   # Using Python 3
   python -m http.server 8000

   # Using Node.js (with http-server)
   npx http-server

   # Using Node.js (with live-server)
   npx live-server
   ```

3. **Visit in your browser**
   - Open `http://localhost:8000` (or the port shown in your terminal)

## 🛠️ Customization

### Update Your Information

1. **Hero Section** (`index.html`):
   - Change your name, title, and introduction
   - Replace profile picture placeholder with your image

2. **About Section**:
   - Update your bio and career goals
   - Modify the stats cards

3. **Skills Section**:
   - Add/remove programming languages, frameworks, and tools
   - Organize by categories

4. **Projects Section**:
   - Add your project details
   - Replace placeholder images with actual project screenshots
   - Update GitHub links

5. **Education Section**:
   - Add your education details
   - Modify timeline entries

6. **Achievements Section**:
   - Add your achievements and certifications
   - Use emoji icons or custom icons

7. **Contact Section**:
   - Update your email and social media links
   - Connect the form to your backend service

### Styling Customization

The website uses CSS custom properties (variables) for easy theming:

```css
:root {
    --primary-color: #6366f1;      /* Change primary color */
    --secondary-color: #8b5cf6;    /* Change secondary color */
    --accent-color: #ec4899;       /* Change accent color */
    /* ... other variables ... */
}
```

## 🚀 Deployment

### Deploy on GitHub Pages

**Method 1: Using GitHub Actions (Automatic)**

1. **Push your code to GitHub**
   ```bash
   git add .
   git commit -m "Initial portfolio commit"
   git push origin main
   ```

2. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Select "Deploy from a branch"
   - Select `main` branch and root folder
   - Save

3. **Your site will be live at**
   ```
   https://yourusername.github.io/portfolio/
   ```

**Method 2: Manual Deployment**

1. **Build your site** (no build step needed for this project!)

2. **Push to GitHub**
   ```bash
   git add .
   git commit -m "Deploy portfolio"
   git push origin main
   ```

3. **Enable GitHub Pages in settings**

### Deploy on Netlify

1. **Create a Netlify account** at [netlify.com](https://netlify.com)

2. **Connect your GitHub repository**
   - Click "New site from Git"
   - Select your repository
   - Set build command: (leave empty)
   - Set publish directory: `.` (root)
   - Click "Deploy site"

3. **Your site will be deployed automatically**

### Deploy on Vercel

1. **Create a Vercel account** at [vercel.com](https://vercel.com)

2. **Import your project**
   - Click "New Project"
   - Select your GitHub repository
   - Click "Import"

3. **Deploy**
   - Vercel will automatically detect and deploy your site

### Deploy on Your Own Server

1. **Upload files via FTP or SSH**
   ```bash
   scp -r portfolio/* user@yourserver:/var/www/portfolio/
   ```

2. **Configure your web server** (Apache/Nginx)

3. **Access your portfolio** at your domain

## 📝 Adding Projects with Images

1. **Prepare your images**
   - Save project screenshots to `assets/images/`
   - Recommended size: 800x600px or larger

2. **Update project card in `index.html`**
   ```html
   <div class="project-card">
       <div class="project-image">
           <img src="assets/images/project-name.jpg" alt="Project Name">
       </div>
       <!-- ... rest of card ... -->
   </div>
   ```

3. **Update CSS** (add to `style.css`):
   ```css
   .project-image img {
       width: 100%;
       height: 100%;
       object-fit: cover;
   }
   ```

## 🔗 Connecting the Contact Form

To receive messages from the contact form, you need backend processing:

### Option 1: Formspree (Easiest)

1. **Go to [formspree.io](https://formspree.io)**
2. **Sign up and create a form**
3. **Get your form endpoint**
4. **Update the form action in `index.html`**:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
       <!-- ... form fields ... -->
   </form>
   ```

### Option 2: Custom Backend

Update the form submission in `script.js`:
```javascript
function handleFormSubmit(e) {
    e.preventDefault();
    
    // Send to your backend
    fetch('/api/contact', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(formData)
    })
    .then(res => res.json())
    .then(data => {
        // Handle response
    });
}
```

## 🎨 Design Highlights

- **Color Scheme**: Modern gradient with primary, secondary, and accent colors
- **Typography**: Clean, readable fonts with proper hierarchy
- **Spacing**: Consistent use of CSS custom properties for spacing
- **Animations**: Smooth transitions and scroll-triggered animations
- **Dark Mode**: Fully functional dark theme with local storage persistence
- **Mobile First**: Responsive breakpoints at 768px and 480px

## ♿ Accessibility

The website includes several accessibility features:

- Semantic HTML structure
- ARIA labels for interactive elements
- Keyboard navigation support
- Proper color contrast ratios
- Respects `prefers-reduced-motion` preference
- Accessible form with proper labels

## ⚡ Performance

- **No external dependencies**: Pure HTML, CSS, and JavaScript
- **Fast loading**: Minimal CSS and optimized animations
- **Lighthouse friendly**: High scores on performance and accessibility
- **Mobile optimized**: Responsive images and touch-friendly interactions

## 🔐 Security

- No sensitive data stored in the frontend
- Contact form data validation
- Content Security Policy ready
- HTTPS recommended for production

## 🐛 Troubleshooting

### Images not loading
- Ensure images are in the `assets/images/` directory
- Check image paths are correct
- Verify image file names match the src attribute

### Form not working
- Ensure backend is configured
- Check browser console for errors
- Verify email validation

### Dark mode not persisting
- Check if localStorage is enabled
- Clear browser cache and try again

### Styles not applying
- Clear browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Check CSS file path in HTML
- Verify file encoding is UTF-8

## 📚 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

This portfolio template is open source and available for personal use. Feel free to modify and customize it for your needs.

## 👤 Author

**Md. Shourov**
- University of Dhaka
- Software Engineering Student
- Email: shourov@example.com
- GitHub: [@Shourov735](https://github.com/Shourov735)
- LinkedIn: [Md. Shourov](https://linkedin.com/in/shourov)
- Codeforces: [Shourov](https://codeforces.com/profile/Shourov)

## 🤝 Contributing

If you find bugs or have suggestions:

1. Open an issue describing the problem
2. Submit a pull request with improvements
3. Share feedback and ideas

## 📞 Support

For issues, questions, or support:
- Open an issue on GitHub
- Send an email to shourov@example.com
- Check the documentation in this README

---

**Happy coding! 🎉**

Last Updated: 2026
