# MiTA 2026 Conference Website

This is the Jekyll-based website for the **International Conference on Machine Intelligence Theory and Applications (MiTA 2026)**, built with the [jekyll-theme-conference](https://github.com/DigitaleGesellschaft/jekyll-theme-conference) theme.

## Site Structure

```
├── _config.yml          # Site configuration
├── index.md             # Home page
├── sponsors.md          # Sponsors page
├── committees.md        # Committees page
├── deadline.md          # Important dates page
├── submission.md        # Paper submission page
├── registration.md      # Registration page
├── program.md           # Program schedule page
├── venue.md             # Venue & location page
├── contact.md           # Contact page
├── _data/               # Data files
│   ├── program.yml      # Schedule data
│   └── lang.yml         # i18n translations
├── _layouts/            # Page layout templates
├── _includes/           # Reusable HTML components
├── _sass/               # SCSS source files
├── _css/                # SCSS source (dev, built by Vite)
├── _js/                 # JS source (dev, built by Vite)
└── assets/              # Built CSS, JS, fonts, images
```

## Local Development

### Prerequisites

- Ruby 3.x + Bundler
- Node.js 20.x + npm
- Jekyll 4.x

### Setup

```bash
# 1. Install Node.js dependencies and build frontend assets
npm install
npm run build

# 2. Install Ruby dependencies
bundle install

# 3. Start local development server
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

### Development Workflow

- Edit page content: modify `.md` files in the root directory
- Edit layouts: modify files in `_layouts/`
- Edit components: modify files in `_includes/`
- Edit styles: modify files in `_css/` then run `npm run build`
- Edit scripts: modify files in `_js/` then run `npm run build`
- Quick style overrides: edit `assets/css/main.css` (no build needed)

## Deployment

This site is deployed to GitHub Pages using GitHub Actions.

1. Push changes to the `main` branch
2. GitHub Actions workflow (`.github/workflows/deploy.yml`) automatically:
   - Installs Node.js and Ruby dependencies
   - Builds frontend assets with Vite
   - Builds the Jekyll site
   - Deploys to GitHub Pages

## Customization

| What to change | Where to edit |
|---------------|---------------|
| Navigation links | `_config.yml` → `conference.navigation.links` |
| Conference tracks/colors | `_config.yml` → `conference.talks.tracks` |
| Page content | Corresponding `.md` file |
| Layout structure | `_layouts/*.html` |
| Reusable components | `_includes/*.html` |
| Theme styles | `_css/theme.scss` → `npm run build` |
| Quick style overrides | `assets/css/main.css` |
| Language translations | `_data/lang.yml` |

## License

This project uses the [jekyll-theme-conference](https://github.com/DigitaleGesellschaft/jekyll-theme-conference) theme (MIT License).