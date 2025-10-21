# Mohammad Dastgheib - Personal Website

[![Website](https://img.shields.io/badge/Website-mdastgheib.com-e63946?style=flat-square)](https://mdastgheib.com)
[![Built with Quarto](https://img.shields.io/badge/Built%20with-Quarto-4B8BBE?style=flat-square)](https://quarto.org/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

A professional academic website showcasing research in cognitive neuroscience, human factors, and applied psychology. Built with Quarto for modern scientific publishing and deployed on Netlify.

## 🌐 Live Site

Visit the website at: **[mdastgheib.com](https://mdastgheib.com)**

## 🚀 Features

- **Interactive Portfolio**: Tag-based filtering for projects and case studies
- **Research Showcase**: Publications, case studies, and methodology demonstrations
- **Real-time Systems**: Production-ready ML applications with live dashboards
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Academic Integration**: Google Scholar, ORCID, and Neurotree profiles
- **Modern UI**: Clean, professional design with custom CSS styling
- **Search Functionality**: Built-in site search for easy navigation
- **Social Integration**: Links to LinkedIn, GitHub, X (Twitter), and Bluesky

## 🛠️ Built With

- **[Quarto](https://quarto.org/)** - Modern scientific publishing system
- **Custom CSS** - Tailored styling and responsive design
- **JavaScript** - Interactive portfolio filtering
- **Netlify** - Hosting and continuous deployment
- **Font Awesome & Academicons** - Professional iconography

## 📁 Project Structure

```
quarto-website/
├── _quarto.yml          # Quarto configuration
├── _publish.yml         # Publishing settings
├── index.qmd            # Homepage
├── about/               # About page
├── portfolio/           # Portfolio showcase
├── publications/        # Research publications
├── projects/            # Case studies and projects
├── research/            # Research overview
├── skills/              # Skills and methodology
├── assets/              # CSS and styling
├── images/              # Images and media
└── CV/                  # CV and resume files
```

## 🚀 Getting Started

### Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) installed on your system
- Git for version control

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/mohdasti/quarto-website.git
   cd quarto-website
   ```

2. **Install dependencies** (if using package.json)
   ```bash
   npm install
   ```

3. **Preview the site locally**
   ```bash
   quarto preview
   ```

4. **Build the site**
   ```bash
   quarto render
   ```

### Development

- **Live preview**: `quarto preview --watch`
- **Build for production**: `quarto render`
- **Clean build**: `quarto render --clean`

## 🎨 Customization

### Styling
- Main styles: `assets/css/main.css`
- Component-specific styles in `assets/css/`
- Color scheme: Primary color `#e63946` (red)

### Content
- Update `_quarto.yml` for site-wide settings
- Modify individual `.qmd` files for page content
- Add new projects in `projects/` directory
- Update publications in `publications/` directory

### Deployment
- Configured for Netlify deployment
- Settings in `_publish.yml`
- Automatic builds on push to main branch

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Mohammad Dastgheib**
- Website: [mdastgheib.com](https://mdastgheib.com)
- Email: mdast003@ucr.edu
- LinkedIn: [linkedin.com/in/mdastgheib](https://linkedin.com/in/mdastgheib)
- GitHub: [github.com/mohdasti](https://github.com/mohdasti)
- Google Scholar: [scholar.google.com/citations?user=SNVpHcUAAAAJ](https://scholar.google.com/citations?user=SNVpHcUAAAAJ)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [contributing guidelines](CONTRIBUTING.md).

## 📊 Site Statistics

- **Pages**: 8+ pages including portfolio, publications, and case studies
- **Projects**: Multiple research projects and case studies including real-time ML systems
- **Publications**: Peer-reviewed research and conference presentations
- **Technologies**: Quarto, HTML, CSS, JavaScript, R/Shiny, Netlify
- **Case Studies**: Interactive demonstrations of cognitive neuroscience applications

---

*Built with ❤️ using Quarto and deployed on Netlify*
