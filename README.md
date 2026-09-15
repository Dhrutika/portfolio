# Dhrutika Rathod — Portfolio

A static portfolio site with a home page, blog, and contact page. No build step, no framework — plain HTML/CSS, ready for GitHub Pages.

## Structure

```
index.html          Home page (your existing portfolio)
blog.html            Blog listing page
blog/
  hello-world.html   Sample first post — use as a template for new posts
contact.html         Contact page with a working form (via Formspree)
assets/
  style.css          Shared styles used by all pages
```

## Deploying to GitHub Pages

1. Create a new repo on GitHub (or reuse your existing portfolio repo).
2. Push these files to the repo root:
   ```
   git init
   git add .
   git commit -m "Add blog and contact pages"
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git branch -M main
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages**, set the source branch to `main` and folder to `/ (root)`.
4. Your site will be live at `https://<your-username>.github.io/<your-repo>/` within a minute or two.

## Setting up the contact form

The contact form uses [Formspree](https://formspree.io), a free service that emails form submissions to you — no backend or database required, which is why it works on GitHub Pages.

1. Sign up at formspree.io (free tier is enough).
2. Create a new form and copy the endpoint it gives you, e.g. `https://formspree.io/f/abcd1234`.
3. Open `contact.html` and replace `YOUR_FORM_ID` in the `<form action="...">` line with your real ID.
4. Commit and push — the form is live.

Alternatives if you'd rather not use Formspree: [Getform](https://getform.io), [Web3Forms](https://web3forms.com), or a `mailto:` link (lowest effort, opens the visitor's email client instead of submitting in-page).

## Adding a new blog post

1. Copy `blog/hello-world.html` to `blog/your-post-slug.html`.
2. Edit the title, date, and body content inside the `<article class="post-body">` section.
3. Open `blog.html` and copy one `<a class="post-card">...</a>` block, update its `href`, date, title, excerpt and tags, and paste it above the previous newest post (so posts stay newest-first).
4. Commit and push.

No build tools, no CMS — just copy, edit, link, push.

## Editing content

Everything is plain HTML with a handful of CSS classes defined in `assets/style.css`. To change colors or fonts, edit the `:root` variables at the top of that file — they cascade through every page.
