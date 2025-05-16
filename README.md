# Personal Portfolio Website

This is a personal portfolio website built with Hugo, using the GitHub-style theme. The site is designed to showcase professional work, projects, and skills in a clean, modern interface.

## 🚀 Quick Start

### Prerequisites
- Hugo (Extended version)
- Git
- Node.js (for theme customization)

### Local Development
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd portfolio
   ```

2. Start the development server:
   ```bash
   hugo server -D
   ```

3. Visit `http://localhost:1313` in your browser

## 📁 Project Structure

```
portfolio/
├── archetypes/          # Content templates
├── assets/             # Processed assets (CSS, JS, images)
├── content/            # Site content
│   ├── posts/         # Blog posts
│   └── projects/      # Project showcases
├── data/              # Site configuration data
├── layouts/           # Custom layouts
├── public/            # Generated site
├── static/            # Static assets
└── themes/            # Hugo themes
```

## 🌿 Branch Structure

- `main` - Production-ready code
- `develop` - Development branch
- `feature/*` - Feature branches
- `bugfix/*` - Bug fix branches
- `release/*` - Release preparation branches

## 🛠️ Development Workflow

1. Create a new feature branch from `develop`:
   ```bash
   git checkout develop
   git checkout -b feature/your-feature-name
   ```

2. Make your changes and commit:
   ```bash
   git add .
   git commit -m "feat: your feature description"
   ```

3. Push and create a pull request to `develop`

## 📝 Content Management

### Adding New Content
```bash
# Create a new blog post
hugo new content posts/my-new-post.md

# Create a new project
hugo new content projects/my-new-project.md
```

### Content Structure
- Blog posts: `content/posts/`
- Projects: `content/projects/`
- Pages: `content/`

## 🎨 Theme Customization

The site uses the GitHub-style theme with custom modifications. Theme files are located in `themes/github-style/`.

### Customizing Styles
1. Create a new CSS file in `assets/css/custom.css`
2. Import it in your theme's main CSS file

## 🔧 Configuration

Main configuration is in `config.toml`. Key sections:
- Site metadata
- Navigation
- Social links
- Theme settings

## 📚 Documentation

- [Hugo Documentation](https://gohugo.io/documentation/)
- [GitHub-style Theme Documentation](https://github.com/MeiK2333/github-style)

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🔍 Troubleshooting

Common issues and their solutions are documented in the [TROUBLESHOOTING.md](./TROUBLESHOOTING.md) file. 