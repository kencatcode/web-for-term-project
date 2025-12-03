# MatchaZuki - Responsive Bootstrap Website

A modern, responsive website inspired by MatchaZuki's design, built with Bootstrap 5, optimized for SEO and accessibility.

## 🌟 Features

### ✅ **Responsive Design**
- Mobile-first Bootstrap 5 grid system
- Responsive navigation with hamburger menu
- Flexible layouts that work on all screen sizes
- Touch-friendly interface for mobile devices

### ✅ **SEO Optimized**
- Semantic HTML structure with proper heading hierarchy
- Meta tags for search engines and social media
- Open Graph and Twitter Card support
- Schema.org structured data for products
- Optimized page titles and descriptions
- Clean URLs and proper navigation structure

### ✅ **Performance Optimized**
- Lazy loading for images
- Optimized CSS and JavaScript
- Preloading of critical resources
- Efficient Bootstrap components
- Minified external resources

### ✅ **Accessibility Features**
- WCAG 2.1 compliant
- Proper ARIA labels and roles
- Keyboard navigation support
- Screen reader friendly
- High contrast support
- Skip to content link

### ✅ **Modern Features**
- Smooth scrolling navigation
- Interactive shopping cart
- CSS animations and transitions
- Modern CSS Grid and Flexbox
- Bootstrap 5 utilities
- Custom matcha-themed design

## 📁 Project Structure

```
matcha-website/
├── index.html          # Main HTML file
├── css/
│   └── custom.css      # Custom styles and theme
├── js/
│   └── custom.js       # Interactive functionality
├── images/             # Image assets
│   ├── logo.png
│   ├── logo-white.png
│   ├── matcha-hero.jpg
│   ├── ceremonial-matcha.jpg
│   ├── culinary-matcha.jpg
│   └── matcha-set.jpg
└── README.md           # This file
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (optional but recommended)

### Installation

1. **Clone or download** the project files
2. **Add images** to the `images/` folder:
   - `logo.png` - Main logo (40x40px recommended)
   - `logo-white.png` - White version for footer
   - `matcha-hero.jpg` - Hero section image
   - `ceremonial-matcha.jpg` - Product image
   - `culinary-matcha.jpg` - Product image
   - `matcha-set.jpg` - Product image
   - `favicon.ico` - Website favicon

3. **Open the website**:
   ```bash
   # Option 1: Simple file opening
   open index.html
   
   # Option 2: Local server (recommended)
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```

4. **View the website**:
   Open `http://localhost:8000` in your browser

## 🛠️ Customization

### Colors and Branding
Edit the CSS variables in `css/custom.css`:
```css
:root {
    --matcha-primary: #4a7c59;    /* Main brand color */
    --matcha-secondary: #6b8e7a;  /* Secondary color */
    --matcha-light: #e8f5e8;      /* Light background */
    --matcha-dark: #2d4a37;       /* Dark variant */
}
```

### Content
- Edit `index.html` to update text, links, and structure
- Replace placeholder images with your own
- Update contact information and social media links
- Modify product information and pricing

### SEO Settings
Update meta tags in the `<head>` section:
```html
<title>Your Site Title</title>
<meta name="description" content="Your site description">
<meta property="og:title" content="Your site title">
<!-- Add your specific keywords and descriptions -->
```

## 📱 Responsive Breakpoints

The website uses Bootstrap 5's responsive grid system:
- **xs**: < 576px (phones)
- **sm**: ≥ 576px (landscape phones)
- **md**: ≥ 768px (tablets)
- **lg**: ≥ 992px (desktops)
- **xl**: ≥ 1200px (large desktops)
- **xxl**: ≥ 1400px (extra large desktops)

## 🎨 Bootstrap Components Used

- **Navbar**: Responsive navigation with collapse
- **Grid System**: 12-column responsive layout
- **Cards**: Product and testimonial displays
- **Buttons**: Call-to-action and interactive elements
- **Badges**: Cart counter and product labels
- **Icons**: Bootstrap Icons for UI elements
- **Utilities**: Spacing, typography, and display classes

## ⚡ Performance Features

### JavaScript Optimizations
- Lazy loading images
- Debounced scroll events
- Intersection Observer for animations
- Local storage for cart functionality
- Efficient DOM manipulation

### CSS Optimizations
- CSS custom properties for theming
- Optimized animations with `transform` and `opacity`
- Print-friendly styles
- Dark mode support (ready to enable)

## 🔧 Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- iOS Safari 14.5+
- Chrome Android 90+

## 📈 SEO Checklist

✅ **Technical SEO**
- Semantic HTML structure
- Proper heading hierarchy (H1, H2, H3)
- Meta descriptions under 160 characters
- Alt text for all images
- Responsive design
- Fast loading times

✅ **Content SEO**
- Descriptive page titles
- Keyword-optimized content
- Internal linking structure
- Social media meta tags
- Schema.org markup

✅ **User Experience**
- Mobile-friendly design
- Accessible navigation
- Fast page load
- Clear call-to-actions
- Easy contact methods

## 📞 Support

For questions about this implementation:
1. Check the browser console for any errors
2. Verify all image files are in the correct location
3. Ensure you're serving the site from a web server for full functionality
4. Test on multiple devices and browsers

## 🚀 Deployment

### For Production:
1. **Optimize images** (compress and convert to modern formats)
2. **Minify CSS and JavaScript**
3. **Set up proper caching headers**
4. **Configure HTTPS**
5. **Add Google Analytics** (update tracking code in JS)
6. **Submit sitemap** to search engines
7. **Test with Google PageSpeed Insights**

### Hosting Options:
- **GitHub Pages** (free)
- **Netlify** (free tier available)
- **Vercel** (free tier available)
- **AWS S3 + CloudFront**
- **Traditional web hosting**

## 📄 License

This project is created for educational purposes. Bootstrap and other dependencies maintain their respective licenses.

---

**Built with ❤️ using Bootstrap 5, modern CSS, and vanilla JavaScript**