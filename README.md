# Happy Trails Travel — Website

A simple, responsive marketing website for **Happy Trails Travel** — a travel
agent with 20+ years of experience helping clients plan stress-free vacations,
romantic getaways, destination weddings, and group & cruise travel.

- **Phone:** (515) 554-2798
- **Location:** Stuart, IA

Built with plain HTML + CSS (and a tiny bit of vanilla JavaScript for the mobile
menu). No build step required — perfect for GitHub Pages.

## Structure

```
.
├── index.html        # Home
├── about.html        # About
├── services.html     # Services (Vacations, Romantic, Weddings, Group & Cruise)
├── testimonials.html # Client reviews + trip photos (curated; see comment in file)
├── contact.html      # Contact form + details
├── css/style.css     # All styles (responsive, mobile + desktop)
├── js/main.js        # Mobile nav toggle + footer year
├── images/           # Placeholder images (see images/README.md)
└── .nojekyll         # Tells GitHub Pages to serve files as-is
```

## Before you go live — two quick edits

### 1. Connect the contact form (Formspree)

The contact form currently points at a placeholder.

1. Sign up at <https://formspree.io> (free tier is fine).
2. Create a form and copy its endpoint, e.g. `https://formspree.io/f/abcdwxyz`.
3. Open `contact.html` and replace `YOUR_FORM_ID` in this line:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   with your real form ID. (Submissions will go to the email on your Formspree
   account. The first submission triggers a one-time confirmation email.)

### 2. Swap in real photos (optional)

Replace the placeholder images in `images/` — see `images/README.md` for the
list of files and tips.

## Publishing on GitHub Pages

1. Create a new repository on GitHub and upload these files (keep the folder
   structure).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to *Deploy from a branch*.
4. Choose the `main` branch and the `/ (root)` folder, then **Save**.
5. After a minute or two your site will be live at
   `https://<your-username>.github.io/<repo-name>/`.

> Want a custom domain (e.g. `happytrailstravel.com`)? Add a `CNAME` file with
> your domain and configure DNS — GitHub's Pages docs walk through this.

## Local preview

Just open `index.html` in a browser. (Or run any static server, e.g.
`python -m http.server`, from this folder.)
