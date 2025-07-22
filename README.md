# David Meagher's Blog

Welcome to the source code for my personal blog, hosted on GitHub Pages using Jekyll.

## About

This is a static blog built with Jekyll and hosted on GitHub Pages. It features:

- Clean, responsive design using the Minima theme
- Blog posts with categories and tags
- About page
- RSS feed
- SEO optimization
- Custom domain support (davidmeagher.net)

## Local Development

To run this blog locally:

1. Make sure you have Ruby and Bundler installed
2. Clone this repository
3. Run `bundle install` to install dependencies
4. Run `bundle exec jekyll serve` to start the development server
5. Visit `http://localhost:4000` to view your site

To preview draft posts, use: `bundle exec jekyll serve --drafts`

## Writing New Posts

1. Create a new file in the `_posts` directory
2. Name it using the format: `YYYY-MM-DD-title-of-post.md`
3. Add the required front matter at the top
4. Write your post in Markdown
5. Commit and push to publish

## Site Structure

- `_posts/` - Published blog posts
- `_drafts/` - Draft posts (not published)
- `_layouts/` - Page templates
- `_includes/` - Reusable components
- `_config.yml` - Site configuration
- `about.md` - About page
- `index.md` - Homepage

## Customization

You can customize the site by:
- Editing `_config.yml` for site settings
- Modifying files in `_layouts/` and `_includes/` for design changes
- Adding custom CSS in the `_sass/` directory
- Installing additional Jekyll plugins in the `Gemfile`

## Deployment

This site is automatically deployed to GitHub Pages whenever changes are pushed to the main branch.

Visit the live site at: [https://davidmeagher.net](https://davidmeagher.net)
