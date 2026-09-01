# blog

My personal blog

## Local development

Clone with submodules (the PaperMod theme is a git submodule):

```sh
git clone --recurse-submodules git@tew.github.com:The-East-Wind/blog.git
```

If you already cloned without `--recurse-submodules`:

```sh
git submodule update --init --recursive
```

Run the dev server with drafts included, serving from the `/blog/` base path to match production:

```sh
hugo server -D --baseURL "http://localhost:1313/blog/"
```

Then open http://localhost:1313/blog/.

## New posts

```sh
hugo new content posts/<slug>.md
```

Set `draft = false` in the post's front matter when it's ready to publish.

## Build

```sh
hugo --gc --minify
```

Output goes to `public/`. Pushing to `main` triggers the GitHub Actions workflow (`.github/workflows/hugo.yml`), which builds and deploys automatically — a manual build is only needed to preview the production output locally.
