---
layout: post
title: "Getting Started with My Blog"
subtitle: "A guide to creating your first post"
date: 2024-01-15
category: Tutorial
---

Welcome to my blog! This is your first post, and I'm excited to share how easy it is to create content with this Jekyll-based blog.

## Creating a New Post

To create a new post, simply add a new Markdown file to the `_posts` directory. The file name should follow this format:

```
YYYY-MM-DD-title.md
```

For example: `2024-01-15-getting-started.md`

## Front Matter

At the top of each post, you need to add front matter (the YAML between the `---` markers):

```yaml
---
layout: post
title: "Your Post Title"
subtitle: "A brief subtitle"
date: 2024-01-15
category: Tutorial
---
```

## Writing Content

After the front matter, you can write your content using Markdown. Here are some common elements:

### Headings

Use `#` for headings:

```markdown
## Second Level Heading
### Third Level Heading
```

### Emphasis

- *Italic*: `*italic text*`
- **Bold**: `**bold text**`

### Links

Create links with `[text](url)`:

```markdown
[Visit Google](https://google.com)
```

### Code

Inline code uses backticks:

```markdown
Use `code` in a sentence.
```

Code blocks use triple backticks:

```markdown
```python
def hello():
    print("Hello, World!")
```
```

### Images

Add images with:

```markdown
![Alt text](image-url)
```

## Publishing Your Blog

With GitHub Pages, your blog will automatically publish when you push to your repository. Just run:

```bash
git add .
git commit -m "Add new post"
git push
```

Your blog will be live at `https://yourusername.github.io/repository-name/`

Happy blogging! 🚀
