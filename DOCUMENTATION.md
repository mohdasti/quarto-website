# Technical Documentation

This document provides detailed technical information about the website structure, customization options, and development workflow.

## 🏗️ Architecture Overview

### Technology Stack

- **Framework**: Quarto (v1.4+)
- **Styling**: Custom CSS with Bootstrap integration
- **Icons**: Font Awesome 6.0 + Academicons
- **Deployment**: Netlify with continuous deployment
- **Version Control**: Git with GitHub

### Project Structure

```
quarto-website/
├── _quarto.yml              # Main Quarto configuration
├── _publish.yml             # Publishing and deployment settings
├── index.qmd                # Homepage content
├── cv.qmd                   # CV page
├── about/                   # About section
│   └── index.qmd
├── portfolio/               # Portfolio showcase
│   └── index.qmd
├── publications/            # Research publications
│   ├── index.qmd
│   ├── peer-reviewed/
│   └── publication[1-8]/
├── projects/                # Case studies and projects
│   ├── dual-task-case-study.qmd
│   ├── memory-and-meditation.qmd
│   └── surgeon-performance-predict.qmd
├── research/                # Research overview
│   └── index.qmd
├── skills/                  # Skills and methodology
│   └── index.qmd
├── assets/                  # Static assets
│   ├── css/
│   │   ├── main.css         # Main stylesheet
│   │   ├── index.css        # Homepage styles
│   │   ├── publications.css # Publication-specific styles
│   │   └── skills.css       # Skills page styles
│   └── listing-default.css  # Default listing styles
├── images/                  # Images and media files
├── CV/                      # CV and resume files
├── _extensions/             # Quarto extensions
│   └── mcanouil/iconify/    # Iconify extension
└── supporting_docs/         # Supporting documents
```

## ⚙️ Configuration Files

### _quarto.yml

Main configuration file controlling:

- **Site metadata**: Title, description, URL
- **Navigation**: Menu structure and links
- **Theme**: Visual appearance and styling
- **Features**: Search, social links, footer
- **Execution**: Code execution settings

Key sections:
```yaml
website:
  title: "Mohammad Dastgheib"
  site-url: https://mdastgheib.com
  description: "Vision science researcher..."
  navbar: # Navigation menu
  page-footer: # Footer content and social links

format:
  html:
    theme:
      light: cosmo
    css: 
      - assets/css/main.css
    include-in-header: # External CSS and JS
```

### _publish.yml

Deployment configuration for Netlify:

```yaml
- source: project
  netlify:
    - id: 676bfb81-9a40-4de6-990b-6fcd2ae00e10
      url: https://mdastgheib.com
```

## 🎨 Styling and Theming

### CSS Architecture

#### Main Stylesheet (`assets/css/main.css`)
- Global styles and variables
- Typography and layout
- Component-specific styles
- Responsive design rules

#### Component Stylesheets
- `index.css`: Homepage-specific styling
- `publications.css`: Publication listing styles
- `skills.css`: Skills page layout

#### Color Scheme
- **Primary**: `#e63946` (Red)
- **Secondary**: Bootstrap default colors
- **Background**: White/light gray
- **Text**: Dark gray/black

### Custom Styling

#### CSS Variables
```css
:root {
  --primary-color: #e63946;
  --secondary-color: #f1faee;
  --text-color: #1d3557;
  --background-color: #ffffff;
}
```

#### Responsive Design
- Mobile-first approach
- Bootstrap grid system
- Custom breakpoints for academic content
- Optimized for tablets and mobile devices

## 📱 Responsive Design

### Breakpoints
- **Mobile**: < 768px
- **Tablet**: 768px - 1024px
- **Desktop**: > 1024px

### Mobile Optimizations
- Touch-friendly navigation
- Optimized image sizes
- Readable typography
- Simplified layouts

## 🔧 Development Workflow

### Local Development

1. **Setup**
   ```bash
   git clone https://github.com/mohdasti/quarto-website.git
   cd quarto-website
   npm install  # Optional: for package.json dependencies
   ```

2. **Development Server**
   ```bash
   quarto preview --watch
   # or
   npm run dev
   ```

3. **Build for Production**
   ```bash
   quarto render
   # or
   npm run build
   ```

### File Organization

#### Content Files (`.qmd`)
- Use YAML front matter for metadata
- Markdown for content structure
- Quarto-specific features for interactivity

#### Asset Management
- Images in `images/` directory
- CSS in `assets/css/`
- Organized by functionality

### Version Control

#### Git Workflow
1. Feature branches for new content
2. Pull requests for review
3. Main branch for production
4. Automatic deployment via Netlify

#### Commit Conventions
- `Add:` for new content
- `Update:` for content changes
- `Fix:` for bug fixes
- `Style:` for styling changes

## 🚀 Deployment

### Netlify Configuration

#### Build Settings
- **Build Command**: `quarto render`
- **Publish Directory**: `_site`
- **Node Version**: 18.x

#### Environment Variables
- No sensitive data required
- Public repository deployment

#### Custom Domain
- `mdastgheib.com` configured
- SSL certificate automatic
- Redirects from www to non-www

### Build Process

1. **Trigger**: Push to main branch
2. **Build**: Quarto renders site
3. **Deploy**: Netlify publishes to CDN
4. **Cache**: Automatic caching for performance

## 📊 Performance Optimization

### Image Optimization
- WebP format where supported
- Responsive image sizing
- Lazy loading for large images
- Alt text for accessibility

### CSS Optimization
- Minified CSS in production
- Critical CSS inlining
- Unused CSS removal
- Font loading optimization

### JavaScript Optimization
- Minimal JavaScript usage
- Async loading where possible
- No external dependencies for core functionality

## 🔍 SEO and Accessibility

### SEO Features
- Meta tags and descriptions
- Open Graph tags
- Twitter Card support
- Structured data markup
- XML sitemap generation

### Accessibility Features
- Semantic HTML structure
- Alt text for images
- Keyboard navigation support
- Screen reader compatibility
- Color contrast compliance

## 🛠️ Customization Guide

### Adding New Pages

1. **Create `.qmd` file**
   ```yaml
   ---
   title: "Page Title"
   ---
   
   # Page Content
   ```

2. **Update navigation** in `_quarto.yml`
   ```yaml
   navbar:
     right:
       - text: "New Page"
         href: new-page.qmd
   ```

### Adding New Projects

1. **Create project file** in `projects/`
2. **Use consistent front matter**
3. **Add to portfolio** if needed
4. **Update navigation** if required

### Styling Changes

1. **Global styles**: Edit `assets/css/main.css`
2. **Page-specific**: Create new CSS file
3. **Include in config**: Add to `_quarto.yml`

### Content Updates

1. **Publications**: Add to `publications/`
2. **About**: Update `about/index.qmd`
3. **Skills**: Modify `skills/index.qmd`
4. **CV**: Update `cv.qmd` and PDF files

## 🐛 Troubleshooting

### Common Issues

#### Build Errors
- Check Quarto version compatibility
- Verify YAML syntax
- Check file paths and references

#### Styling Issues
- Clear browser cache
- Check CSS file paths
- Verify Bootstrap integration

#### Deployment Issues
- Check Netlify build logs
- Verify build command
- Check file permissions

### Debug Tools

#### Local Debugging
```bash
quarto check  # Check configuration
quarto render --debug  # Verbose output
```

#### Browser Tools
- Developer tools for CSS debugging
- Network tab for asset loading
- Console for JavaScript errors

## 📚 Resources

### Documentation
- [Quarto Documentation](https://quarto.org/docs/)
- [Bootstrap Documentation](https://getbootstrap.com/docs/)
- [Font Awesome Icons](https://fontawesome.com/icons)

### Tools
- [Quarto CLI](https://quarto.org/docs/get-started/)
- [Netlify CLI](https://docs.netlify.com/cli/get-started/)
- [Git](https://git-scm.com/docs)

### Best Practices
- Semantic HTML structure
- Mobile-first responsive design
- Performance optimization
- Accessibility compliance
- SEO best practices

---

For questions or issues, please refer to the [Contributing Guidelines](CONTRIBUTING.md) or open an issue on GitHub.
