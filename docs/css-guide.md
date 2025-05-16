# CSS Customization Guide

This document outlines the custom CSS modifications made to the GitHub-style theme.

## 🎨 Color Scheme

```css
:root {
  /* Primary Colors */
  --primary-color: #0366d6;
  --secondary-color: #24292e;
  
  /* Text Colors */
  --text-primary: #24292e;
  --text-secondary: #586069;
  
  /* Background Colors */
  --bg-primary: #ffffff;
  --bg-secondary: #f6f8fa;
  
  /* Accent Colors */
  --accent-1: #0366d6;
  --accent-2: #28a745;
  --accent-3: #d73a49;
}
```

## 📱 Responsive Design

### Breakpoints
```css
/* Mobile First Approach */
@media (min-width: 640px) { /* sm */ }
@media (min-width: 768px) { /* md */ }
@media (min-width: 1024px) { /* lg */ }
@media (min-width: 1280px) { /* xl */ }
```

### Layout Adjustments
```css
/* Container */
.container {
  width: 100%;
  padding-right: 1rem;
  padding-left: 1rem;
  margin-right: auto;
  margin-left: auto;
}

/* Responsive Grid */
.grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
}
```

## 🖋️ Typography

```css
/* Font Stack */
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
  line-height: 1.6;
}

/* Headings */
h1, h2, h3, h4, h5, h6 {
  font-weight: 600;
  line-height: 1.25;
  margin-bottom: 1rem;
}

/* Code Blocks */
pre, code {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
}
```

## 🌓 Dark Mode

```css
/* Dark Mode Variables */
[data-theme="dark"] {
  --bg-primary: #0d1117;
  --bg-secondary: #161b22;
  --text-primary: #c9d1d9;
  --text-secondary: #8b949e;
}

/* Dark Mode Toggle */
.theme-toggle {
  cursor: pointer;
  padding: 0.5rem;
  border-radius: 0.25rem;
  transition: background-color 0.2s;
}
```

## 🎯 Custom Components

### Project Cards
```css
.project-card {
  border: 1px solid var(--border-color);
  border-radius: 6px;
  padding: 1rem;
  transition: transform 0.2s;
}

.project-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

### Navigation
```css
.nav-link {
  color: var(--text-primary);
  text-decoration: none;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  transition: background-color 0.2s;
}

.nav-link:hover {
  background-color: var(--bg-secondary);
}
```

## 🔧 Utility Classes

```css
/* Spacing */
.m-1 { margin: 0.25rem; }
.m-2 { margin: 0.5rem; }
.m-3 { margin: 1rem; }
.m-4 { margin: 1.5rem; }
.m-5 { margin: 2rem; }

/* Text Alignment */
.text-center { text-align: center; }
.text-right { text-align: right; }
.text-left { text-align: left; }

/* Display */
.d-flex { display: flex; }
.d-grid { display: grid; }
.d-none { display: none; }
```

## 📝 Best Practices

1. **Use CSS Variables**
   - Maintain consistency
   - Easy theme switching
   - Centralized configuration

2. **Mobile First**
   - Start with mobile styles
   - Use media queries for larger screens
   - Test on multiple devices

3. **Performance**
   - Minimize CSS
   - Use efficient selectors
   - Optimize animations

4. **Maintainability**
   - Use BEM naming convention
   - Comment complex sections
   - Organize by component 