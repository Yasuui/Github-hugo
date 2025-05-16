# Troubleshooting Guide

This document contains solutions to common issues encountered while developing and maintaining the portfolio website.

## 🚨 Common Issues

### Hugo Server Issues

#### "command not found: hugo"
- **Cause**: Hugo is not properly installed or not in PATH
- **Solution**: 
  ```bash
  # Install Hugo using Homebrew
  brew install hugo
  # Verify installation
  hugo version
  ```

#### "Error: failed to load config: ..."
- **Cause**: Invalid configuration in config.toml
- **Solution**: Check config.toml syntax and required fields

### Theme Issues

#### Theme not found
- **Cause**: Theme not properly installed or configured
- **Solution**:
  ```bash
  # Install theme
  git submodule add https://github.com/MeiK2333/github-style.git themes/github-style
  # Update config.toml
  echo 'theme = "github-style"' >> config.toml
  ```

#### Missing theme assets
- **Cause**: Theme not properly initialized
- **Solution**:
  ```bash
  # Initialize and update submodules
  git submodule init
  git submodule update
  ```

### Content Issues

#### Content not showing up
- **Cause**: Draft status or incorrect front matter
- **Solution**: 
  - Check `draft: false` in front matter
  - Verify content is in correct directory
  - Check file extension (.md)

#### Images not displaying
- **Cause**: Incorrect path or missing images
- **Solution**:
  - Use relative paths: `![alt text](../images/image.jpg)`
  - Place images in `static/images/`
  - Check file permissions

### Git Issues

#### Submodule problems
- **Cause**: Theme submodule not properly initialized
- **Solution**:
  ```bash
  # Remove and re-add submodule
  git submodule deinit -f themes/github-style
  git rm -f themes/github-style
  git submodule add https://github.com/MeiK2333/github-style.git themes/github-style
  ```

#### Branch conflicts
- **Cause**: Multiple developers working on same files
- **Solution**:
  ```bash
  # Update your branch
  git fetch origin
  git rebase origin/develop
  # Resolve conflicts
  git add .
  git rebase --continue
  ```

## 🔧 Development Environment

### Local Development
- Use `hugo server -D` for development
- Access site at `http://localhost:1313`
- Changes auto-reload

### Production Build
- Use `hugo` to generate static files
- Check `public/` directory for output
- Verify all assets are included

## 📝 Best Practices

1. **Content Organization**
   - Use clear, descriptive filenames
   - Organize content in appropriate directories
   - Use consistent front matter

2. **Theme Customization**
   - Create custom layouts in `layouts/`
   - Add custom CSS in `assets/css/`
   - Document all customizations

3. **Version Control**
   - Use meaningful commit messages
   - Keep branches up to date
   - Review changes before merging

## 🔍 Debugging Tips

1. **Enable Debug Mode**
   ```bash
   hugo server -D --debug
   ```

2. **Check Hugo Logs**
   - Look for warnings and errors
   - Verify template rendering
   - Check content processing

3. **Validate Content**
   - Use Hugo's built-in validation
   - Check markdown syntax
   - Verify front matter

## 📚 Additional Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [GitHub-style Theme Issues](https://github.com/MeiK2333/github-style/issues)
- [Hugo Forums](https://discourse.gohugo.io/) 