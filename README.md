# Mortgage Calculator Site — Hugo

A fast, SEO-optimized mortgage calculator website built with Hugo.
Includes 4 calculators, clean responsive design, and Google AdSense ad slots.

## Calculators Included
- **Monthly Mortgage Payment** with PITI breakdown + pie chart
- **Amortization Schedule** — yearly and monthly views
- **Home Affordability** — 28/36 rule with DTI feedback
- **Refinance Calculator** — monthly savings, break-even, lifetime savings

## Quick Start

### 1. Install Hugo
```bash
# macOS
brew install hugo

# Linux (snap)
snap install hugo

# Windows
winget install Hugo.Hugo.Extended
```

### 2. Run locally
```bash
cd mortgage-site
hugo server -D
# Open http://localhost:1313
```

### 3. Build for production
```bash
hugo --minify
# Output goes to the public/ folder — deploy this to any static host
```

## Before Deploying

1. **Set your domain** — update `baseURL` in `hugo.toml`
2. **Add AdSense ID** — replace `ca-pub-XXXXXXXXXXXXXXXXX` in `hugo.toml` with your publisher ID
3. **Update ad slot IDs** — replace `1111111111`, `2222222222`, etc. in:
   - `layouts/partials/header.html` (top banner)
   - `layouts/partials/ad-sidebar.html` (sidebar — 2 slots)
   - `layouts/partials/ad-inline.html` (in-content)

## Ad Slots

| Slot | Location | Format |
|------|----------|--------|
| Header banner | Below nav, every page | Responsive leaderboard |
| Sidebar top | Right rail, desktop only | Medium rectangle |
| Sidebar bottom | Right rail, desktop only | Medium rectangle |
| Inline | Homepage, below calculator cards | Responsive |

## Hosting Options (Free or Cheap)
- **Netlify** — free tier, drag & drop `public/` folder or connect GitHub
- **Cloudflare Pages** — free, fast CDN worldwide
- **GitHub Pages** — free with GitHub Actions for auto-deploy
- **Vercel** — free tier, great performance

## SEO Notes
- Each calculator is its own URL (`/mortgage-calculator/`, `/amortization-calculator/`, etc.)
- Each page has unique `<title>` and `<meta description>` tags
- Substantial SEO content below each calculator for organic search
- Fast load — no JavaScript frameworks, no external fonts
