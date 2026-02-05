# marcelgast-homepage

Personal site for Marcel, built with Jekyll + GitHub Pages.

## Recommended setup

- Theme base: `minima` with custom one-page overrides
- Style/theme controls: `assets/main.scss`
- Main content: `index.md`
- Build/deploy: GitHub Actions to GitHub Pages

## Project structure

- `_config.yml` site config
- `index.md` one-page content sections
- `_includes/header.html` top navigation
- `_includes/footer.html` footer + legal modals
- `assets/images/` static image folders
- `assets/main.scss` styling

## Add images

1. Put image files in `assets/images/` subfolders:
   - `assets/images/about/`
   - `assets/images/music/`
   - `assets/images/projects/`
   - `assets/images/practicetab/`
   - `assets/images/logos/`
2. Reference with absolute paths so they always resolve:

```md
![Me](/assets/images/about/me.jpg)
```

3. For responsive images in HTML sections, use:

```html
<img class="img-fluid" src="/assets/images/projects/xerador-cover.jpg" alt="Xerador cover">
```

## Run locally

1. Install Ruby (Homebrew):

```bash
brew install ruby@3.3
echo 'export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

2. Install project gems:

```bash
bundle install
```

3. Start local server:

```bash
bundle exec jekyll serve --livereload
```

4. Open <http://127.0.0.1:4000>

## Publish on GitHub Pages

1. Push this repository to GitHub
2. Open **Settings -> Pages**
3. Set source to **GitHub Actions**
4. Push to `main` to trigger deployment (`.github/workflows/pages.yml`)

GitHub Actions will build the site and deploy it to Pages automatically.
