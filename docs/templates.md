# Template Customization Guide

This document outlines the custom template modifications made to the GitHub-style theme.

## 📁 Template Structure

```
layouts/
├── _default/           # Default templates
│   ├── baseof.html    # Base template
│   ├── list.html      # List page template
│   └── single.html    # Single page template
├── partials/          # Reusable components
│   ├── header.html    # Site header
│   ├── footer.html    # Site footer
│   └── nav.html       # Navigation
└── shortcodes/        # Custom shortcodes
    ├── project.html   # Project showcase
    └── code.html      # Code block
```

## 🎯 Custom Templates

### Project Showcase
```html
<!-- layouts/_default/project.html -->
<div class="project-card">
  <h2>{{ .Title }}</h2>
  <div class="project-meta">
    <span class="date">{{ .Date.Format "January 2006" }}</span>
    <span class="tags">
      {{ range .Params.tags }}
      <span class="tag">{{ . }}</span>
      {{ end }}
    </span>
  </div>
  <div class="project-content">
    {{ .Content }}
  </div>
</div>
```

### Custom List Page
```html
<!-- layouts/_default/list.html -->
{{ define "main" }}
<div class="container">
  <h1>{{ .Title }}</h1>
  <div class="grid">
    {{ range .Pages }}
    <article class="card">
      <h2><a href="{{ .RelPermalink }}">{{ .Title }}</a></h2>
      <p>{{ .Summary }}</p>
    </article>
    {{ end }}
  </div>
</div>
{{ end }}
```

## 🔧 Shortcodes

### Project Shortcode
```html
<!-- layouts/shortcodes/project.html -->
<div class="project-showcase">
  <div class="project-header">
    <h3>{{ .Get "title" }}</h3>
    <div class="project-links">
      {{ if .Get "github" }}
      <a href="{{ .Get "github" }}" class="github-link">GitHub</a>
      {{ end }}
      {{ if .Get "demo" }}
      <a href="{{ .Get "demo" }}" class="demo-link">Live Demo</a>
      {{ end }}
    </div>
  </div>
  <div class="project-content">
    {{ .Inner }}
  </div>
</div>
```

### Code Block Shortcode
```html
<!-- layouts/shortcodes/code.html -->
<div class="code-block">
  <div class="code-header">
    <span class="language">{{ .Get "language" }}</span>
    {{ if .Get "title" }}
    <span class="title">{{ .Get "title" }}</span>
    {{ end }}
  </div>
  <pre><code class="language-{{ .Get "language" }}">{{ .Inner }}</code></pre>
</div>
```

## 🎨 Partial Templates

### Header
```html
<!-- layouts/partials/header.html -->
<header class="site-header">
  <nav class="main-nav">
    {{ range .Site.Menus.main }}
    <a href="{{ .URL }}" class="nav-link">{{ .Name }}</a>
    {{ end }}
  </nav>
  <div class="theme-toggle" onclick="toggleTheme()">
    <i class="fas fa-moon"></i>
  </div>
</header>
```

### Footer
```html
<!-- layouts/partials/footer.html -->
<footer class="site-footer">
  <div class="social-links">
    {{ if .Site.Params.github }}
    <a href="{{ .Site.Params.github }}" class="social-link">
      <i class="fab fa-github"></i>
    </a>
    {{ end }}
    {{ if .Site.Params.linkedin }}
    <a href="{{ .Site.Params.linkedin }}" class="social-link">
      <i class="fab fa-linkedin"></i>
    </a>
    {{ end }}
  </div>
  <div class="copyright">
    © {{ now.Format "2006" }} {{ .Site.Params.author }}
  </div>
</footer>
```

## 📝 Best Practices

1. **Template Organization**
   - Keep templates modular
   - Use partials for reusable components
   - Follow Hugo's template hierarchy

2. **Performance**
   - Minimize template complexity
   - Use efficient conditionals
   - Cache partial templates when possible

3. **Maintainability**
   - Document complex logic
   - Use consistent naming
   - Keep templates DRY

4. **Accessibility**
   - Use semantic HTML
   - Include ARIA labels
   - Ensure keyboard navigation

## 🔍 Debugging

1. **Template Debugging**
   ```html
   {{ printf "%#v" . }}
   ```

2. **Variable Inspection**
   ```html
   {{ with .Site.Params }}
   {{ printf "%#v" . }}
   {{ end }}
   ```

3. **Conditional Debugging**
   ```html
   {{ if .IsPage }}
   This is a page
   {{ else if .IsSection }}
   This is a section
   {{ end }}
   ``` 