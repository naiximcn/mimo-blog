# MiMo Blog

A modern, dark-themed blog built with Jekyll, inspired by the [MiMo website](https://mimo.xiaomi.com/).

## Features

- Dark theme with accent colors
- Responsive design for all devices
- Animated hero section with scrolling text
- Blog posts with categories
- About page
- Mobile-friendly navigation

## Quick Start

### Prerequisites

- Ruby (2.7 or higher)
- Bundler
- Jekyll

### Installation

1. Clone this repository:
```bash
git clone https://github.com/your-username/mimo-blog.git
cd mimo-blog
```

2. Install dependencies:
```bash
bundle install
```

3. Start the development server:
```bash
bundle exec jekyll serve
```

4. Open your browser and visit:
```
http://localhost:4000
```

## Creating Posts

1. Create a new file in the `_posts` directory
2. Name it using the format: `YYYY-MM-DD-title.md`
3. Add front matter at the top:
```yaml
---
layout: post
title: "Your Post Title"
subtitle: "A brief subtitle"
date: 2024-01-15
category: Tutorial
---
```

4. Write your content using Markdown
5. Save and see it live!

## Deployment to GitHub Pages

1. Push your code to GitHub
2. Go to your repository settings
3. Navigate to "Pages"
4. Select "GitHub Actions" as the source
5. Create `.github/workflows/jekyll.yml`:

```yaml
name: Deploy Jekyll site to Pages

on:
  push:
    branches: ["main"]

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        uses: actions/configure-pages@v4
      - name: Build with Jekyll
        uses: actions/jekyll-build-pages@v1
        with:
          source: ./
          destination: ./_site
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

6. Push and your site will be live at:
```
https://yourusername.github.io/repository-name/
```

## Customization

### Colors

Edit the CSS variables in `assets/css/style.css`:

```css
:root {
  --bg-primary: #0a0a0a;
  --bg-secondary: #111111;
  --bg-card: #1a1a1a;
  --text-primary: #ffffff;
  --text-secondary: #a0a0a0;
  --accent: #00d4aa;
  --gradient-start: #00d4aa;
  --gradient-end: #0099ff;
}
```

### Content

- Edit `_config.yml` to change site title and description
- Edit `index.md` for the homepage
- Edit `about.md` for the about page
- Edit `_includes/header.html` and `_includes/footer.html` for navigation

## License

MIT License
