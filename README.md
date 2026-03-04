# 2007 Okanagan Camper Van - For Sale Website

A Hugo static site for listing a 2007 Ford E-350 Okanagan Camper Van for sale.

## Quick Start

### Prerequisites
- [Hugo](https://gohugo.io/installation/) (v0.112+ recommended)

### Build & Preview Locally

```bash
# Clone or navigate to this directory
cd okanagan-sale

# Start local dev server
hugo server -D

# Open http://localhost:1313 in your browser
```

### Build for Production

```bash
hugo --minify
```

The built site will be in the `public/` directory.

## Deploy to Free Hosting

### Option 1: Netlify (Easiest)
1. Create a free account at [netlify.com](https://netlify.com)
2. Drag and drop the `public/` folder onto the Netlify dashboard
3. Your site will be live at `something.netlify.app`
4. You can customize the subdomain in site settings

### Option 2: GitHub Pages
1. Create a new GitHub repo (e.g., `okanagan-sale`)
2. Push this project to the repo
3. Go to Settings > Pages > Source: GitHub Actions
4. Add a `.github/workflows/hugo.yml` workflow (see Hugo docs)
5. Your site will be live at `yourusername.github.io/okanagan-sale`

### Option 3: Cloudflare Pages
1. Create a free account at [pages.cloudflare.com](https://pages.cloudflare.com)
2. Connect your GitHub repo or direct upload
3. Build command: `hugo --minify`
4. Publish directory: `public`

## Customization

### Update Price or Details
Edit `hugo.toml` — all vehicle params are in the `[params]` section.

### Add/Replace Photos
Drop images into `static/images/` and update the `<img>` tags in
`layouts/_default/index.html`.

### Add Contact Info
Edit the CTA section at the bottom of `layouts/_default/index.html`.
You may want to add your phone number or email once you're ready to receive inquiries.

## Project Structure

```
okanagan-sale/
├── hugo.toml              # Site config & vehicle params
├── content/
│   └── _index.md          # Home page content
├── layouts/
│   └── _default/
│       └── index.html     # Main page template
├── static/
│   ├── css/
│   │   └── style.css      # Stylesheet
│   └── images/
│       ├── driver-side.jpg
│       ├── passenger-side.jpg
│       ├── front-view.jpg
│       ├── rear-view.jpg
│       ├── interior-cab.jpg
│       ├── interior-kitchen.jpg
│       └── odometer.jpg
└── archetypes/
    └── default.md
```

## Taking Down the Site

Once the van sells, simply delete the deployment (Netlify/GitHub Pages/Cloudflare)
or set the site to private. No ongoing costs to worry about.
