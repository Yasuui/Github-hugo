# Personal Portfolio

A modern, responsive portfolio website built with Hugo and the GitHub-style theme. This repository documents my personal website's development process, customizations, and technical decisions.

## 🎯 Key Features

### Design & UI
- Clean, GitHub-inspired interface
- Responsive design for all devices
- Dark/Light mode support
- Custom typography and color scheme

### Technical Implementation
- Built with Hugo static site generator
- GitHub-style theme with custom modifications
- Custom CSS for enhanced styling
- Optimized performance and SEO

### Content Management
- Blog section for technical articles
- Project showcase with detailed case studies
- About page with professional background
- Skills and experience presentation

## 🛠️ Development Process

### Theme Customization
The site uses the GitHub-style theme as a base, with several custom modifications:

1. **Custom CSS**
   - Location: `assets/css/custom.css`
   - Purpose: Enhanced styling and responsive design
   - Key features:
     - Custom color scheme
     - Typography improvements
     - Responsive layout adjustments

2. **Custom Templates**
   - Location: `layouts/`
   - Purpose: Extended functionality
   - Key features:
     - Project showcase layout
     - Custom blog post format
     - Enhanced navigation

3. **JavaScript Enhancements**
   - Location: `assets/js/`
   - Purpose: Interactive features
   - Key features:
     - Dark mode toggle
     - Smooth scrolling
     - Dynamic content loading

### Configuration
- Main config: `hugo.toml`
- Personal info: `config/personal.local.toml` (not tracked in git)
- Environment-specific: `config/environments/`

## 📝 Development Notes

### Key Decisions
1. **Theme Selection**
   - Chose GitHub-style for its clean, professional look
   - Easy to customize and extend
   - Good documentation and community support

2. **Custom Features**
   - Added dark mode for better user experience
   - Implemented custom project showcase
   - Enhanced blog post formatting

3. **Performance Optimizations**
   - Optimized images and assets
   - Implemented lazy loading
   - Minimized CSS and JavaScript

### Challenges & Solutions
1. **Theme Customization**
   - Challenge: Limited theme documentation
   - Solution: Created custom layouts and CSS

2. **Responsive Design**
   - Challenge: Mobile layout issues
   - Solution: Custom media queries and flexbox

3. **Content Organization**
   - Challenge: Complex content structure
   - Solution: Implemented clear directory structure

## 🚀 Getting Started

### Prerequisites
- Hugo (Extended version)
- Git
- Node.js (for theme customization)

### Local Development
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd portfolio
   ```

2. Copy personal configuration:
   ```bash
   cp config/personal.toml config/personal.local.toml
   # Edit personal.local.toml with your information
   ```

3. Start the development server:
   ```bash
   hugo server -D
   ```

4. Visit `http://localhost:1313` in your browser

## 📚 Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [GitHub-style Theme](https://github.com/MeiK2333/github-style)
- [Custom CSS Guide](./docs/css-guide.md)
- [Template Customization](./docs/templates.md)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 