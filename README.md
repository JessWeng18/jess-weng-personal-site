# Jess Weng

My personal site. It is one self-contained page (`index.html`) with no build step, so it hosts anywhere for free.

Preview by opening `index.html` in your browser.

## Adding LinkedIn posts

On LinkedIn, open a post → `…` menu → **Embed this post** → copy the `<iframe>` code.
Each post is a parchment scroll (`<article class="scroll">`) in the "Above the Clouds" section. Paste the iframe
inside that scroll's `<div class="text">`, replacing the placeholder text, and change the title in its `<h3>`. Scrolls alternate left and right automatically and unroll on hover
(tap on phones). Embeds may only show on the hosted site, not in local previews.

## Adding photos to the Scrapbook

Put image files in a `photos` folder next to `index.html`. In the Scrapbook page, replace an empty polaroid
(`<figure class="polaroid empty">…</figure>`) with:

```html
<figure class="polaroid"><img src="photos/your-photo.jpg" alt="what's in the photo" loading="lazy"><figcaption>caption</figcaption></figure>
```

Each event is one `<section class="memory">` block with a title and date; copy one to start a new row.

## Adding to the beanstalk

The site has two pages in one file: the title page, and the climb (`#tale`), which opens at the seed
and is read by scrolling up. Each leaf is one `<article class="entry">` inside `<div class="stalk">`. Newest goes at the top
(the top of the stalk is the present), oldest at the bottom. The vine and leaves redraw themselves
automatically, so you only add or edit the HTML.

## Put it online

### Option A: GitHub Pages (free, yourname.github.io)
1. Create a GitHub account and a new **public** repository named `<your-username>.github.io`.
2. Push this folder to it:
   ```
   git init
   git add .
   git commit -m "First version of my site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
   git push -u origin main
   ```
3. In the repo: **Settings → Pages → Source: Deploy from a branch → main / root**.
4. Your site appears at `https://<your-username>.github.io` within a minute or two.

### Option B: Vercel (free, nicer for custom domains)
1. Push the folder to any GitHub repo (steps above, any repo name).
2. Sign in at vercel.com with GitHub → **Add New → Project** → import the repo.
3. Framework preset: **Other**. No build command. Click **Deploy**.
4. Every later `git push` redeploys automatically.

Either way you can later buy a domain (e.g. `jessweng.com`) and connect it in Pages or Vercel settings.
