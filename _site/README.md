# iPaul Media and Creations - Jekyll Site

A simple placeholder template for your kickass app/product/startup/whatever until it launches. Includes an email signup form and a cool slideshow background.

## Building and Serving the Site

To set up and run this Jekyll site locally:

```bash
# Install dependencies
bundle install

# Serve the site locally with auto-regeneration
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000/opensoon` (note the baseurl from `_config.yml`).

### Additional Jekyll Commands

```bash
# Build the site for production
bundle exec jekyll build

# Serve with drafts included
bundle exec jekyll serve --drafts

# Serve on a different port
bundle exec jekyll serve --port 4001
```

## Project Structure

### Adding New Content

#### Pages
- Add new pages as `.md` or `.html` files in the root directory
- Pages will automatically use the default layout unless specified
- Example: `about.md`, `contact.html`

#### Posts
- Create a `_posts/` directory if you want to add blog posts
- Posts should follow the naming convention: `YYYY-MM-DD-title.md`
- Example: `_posts/2024-01-15-my-first-post.md`

#### Drafts
- Create a `_drafts/` directory for unpublished posts
- Drafts don't need a date in the filename
- View drafts locally with `bundle exec jekyll serve --drafts`

### Customizing Styles

The site uses Sass for styling. To update styles:

1. **Main Sass entry point**: `assets/sass/main.scss`
2. **Sass directory structure**:
   - `assets/sass/base/` - Base styles (reset, typography, page, background)
   - `assets/sass/components/` - Component styles (buttons, forms, icons, etc.)
   - `assets/sass/layout/` - Layout styles (header, footer, signup form)
   - `assets/sass/libs/` - Libraries and utilities (variables, mixins, functions)

3. **To modify styles**:
   - Edit existing `.scss` files in the appropriate directory
   - Add new `.scss` files and import them in `main.scss`
   - Variables are defined in `assets/sass/libs/_vars.scss`

4. **Sass configuration**: Controlled in `_config.yml` under the `sass:` section

### Configuration

- **Site settings**: Edit `_config.yml` for site-wide configuration
- **Layouts**: Located in `_layouts/` directory
- **Includes**: Reusable components in `_includes/` directory

## Features

### Signup Form
The signup form won't actually do anything (other than report back with a "thank you" message) until you tie it to either a third party service (eg. MailChimp) or your own hosted solution.

There are two ways to set it up:

1. **Conventional (non-AJAX) way**: Point the form's "action" attribute to your service/script URL. Remove the "Signup Form" code block from `assets/js/main.js`.

2. **AJAX way**: Consult your service's documentation. Basic interaction code is included under "Signup Form" in `assets/js/main.js`.

### Slideshow Background
Configure the slideshow in `assets/js/main.js` under "Slideshow Background":

- **images**: List of images to cycle through in format `'url': 'alignment'`
- **delay**: Time between transitions (in ms, must be at least twice the transition speed)

## Credits

- **Demo Images**: [Unsplash](https://unsplash.com) (not included)
- **Icons**: [Font Awesome](https://fontawesome.io)
- **Other**: [Responsive Tools](https://github.com/ajlkn/responsive-tools)
