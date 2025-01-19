# smallworld

_This is a template for the static site generator [Astro](https://astro.build/)._

I like Astro, but I don't like spending hours messing with customizations I don't need. This template is based on a few key principles for my own site:

- I wanted a basic website with a single-author blog.
- The website should incorporate accessible and usable elements.
- Complex systems should be avoided in favor of simpler ones.
- I should be able to easily understand what I see.

The result is an Astro template that heavily limits the use of CSS classes, and maximizes the use of semantic HTML.

## Quickstart

```shell
npm create astro@latest -- --template anaxite/astro-smallworld
cd astro-smallworld
npm run dev
npm run build
```

## Less quick start

### Install

1. Install Astro.

```shell
npm create astro@latest -- --template anaxite/astro-smallworld
```

2. Install this template's dependencies, if you didn't already.

```shell
cd <install-directory>
npm install
```

3. Run the template in preview mode, or build the final output.

```shell
npm run dev
npm run build
```

4. Optionally, format your source files with Prettier.

```shell
npm run format
```

If you use mise-en-place for your tooling, this project comes with a mise configuration file.

### Configure site settings

Site-wide settings are stored in `src/settings.ts`. This is also where you can set the favicon file name, and Open Graph image settings.

### Configure CSS

The file `src/styles/main.scss` controls which CSS elements Pico CSS includes in the final site. See [the Pico CSS website](https://picocss.com/docs/sass) for information about these elements. 

> Building your project may show deprecation warnings due to how Pico CSS writes its SASS files. These warnings are non-fatal and can be ignored for now.. 

### Add and edit pages

Create your static pages as `.astro` files under `src/pages`. The template includes an index page with the most recent blog posts, an About page, and a 404 page.

Use the Base layout to wrap your content in semantically-correct `<main>` tags. The Base layout also takes `title` and `description` attributes that supplement the main site title and description. If you want your content to have a nice border, I recommend you wrap it in `<article>` tags to benefit from Pico CSS styling.

To start with a basic page template, see the file in `src/templates`.

### Navigation

To add a page to the site navigation, edit the `PageHeader.astro` component directly.

### Blog

smallworld comes with a blog collection by default. To add a new post, create a Markdown file in the `src/content/blog` directory or one of its subdirectories. The path and file name becomes the post URL.

A post must have `title`, `description` and `pubDate` keywords in its frontmatter. `tags` are optional.

To see a post template, see the file in `src/templates`.


## About Astro

Want to learn more about Astro? Check out [their documentation](https://docs.astro.build) or jump into their [Discord server](https://astro.build/chat).
