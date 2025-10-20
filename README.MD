# Yilmaz Kiymaz — Unity Expert Website

This repository contains the lightweight, static website for Yilmaz Kiymaz. It highlights Unity consulting services, projects such as Sandbox City, conference talks, and a simple developer blog.

## Structure

```
/
├── index.html                # Home page
├── assets/css/main.css       # Shared styling
├── data/articles.json        # Article metadata (feeds home & blog pages)
├── blog/
│   ├── index.html            # Blog listing page
│   ├── designing-sandbox-city.html
│   └── faster-prototyping-with-dots.html
└── README.MD
```

## Editing content

- **Profile & services**: Update the relevant sections directly in `index.html`.
- **Articles**: Add new entries to `data/articles.json` (title, slug, date, description, tags). Then create a new HTML file in `blog/` named after the slug (e.g. `blog/my-article.html`). Use the existing articles as templates.
- **Blog listing**: The home page and `blog/index.html` automatically pull the latest entries from `data/articles.json`.

## Local preview

Because the site uses `fetch` to load `articles.json`, serve the files over HTTP when previewing locally:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000> in your browser.

## Deployment

Upload the repository contents to any static hosting provider (GitHub Pages, Netlify, Vercel, etc.). No server-side runtime is required.
