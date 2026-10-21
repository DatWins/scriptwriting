# Scriptwriting - Notes & Journal

A blog that has the most interesting questions about how to write scripts or screenplays.
Built with [Hugo](https://gohugo.io/) (static and fast) and the [hugo-scroll](https://github.com/zjedi/hugo-scroll) theme.

Five sections: **Ideas, Formatting, Scene, Dialogue, Actions.**

## Add a write-up

1. Create a file in `content/en/<section>/`, for example `content/en/ideas/my-new-post.md`:

   ```
   ---
   title: "My New Post"
   description: "One line shown under the title in the section list."
   slug: "my-new-post"
   category: "Ideas"      # Ideas, Formatting, Scene, Dialogue or Actions
   weight: 3              # order inside the section
   ---
   Write the post in Markdown here.
   ```

2. List it in that section's page, `content/en/homepage/01-ideas.md` (or `02-formatting.md`, `03-scene.md`, `04-dialogue.md`, `05-actions.md`):

   ```
   - [My New Post]({{< relref "/ideas/my-new-post.md" >}})  
     One line describing it.
   ```

## Run locally

Needs Hugo **extended** 0.147 or newer. Clone with submodules (the theme is a submodule):

```
git clone --recurse-submodules https://github.com/DatWins/scriptwriting
cd scriptwriting
hugo server
```

## Deploy

Pushing to `main` publishes to GitHub Pages through `.github/workflows/hugo.yaml`.
In the repo's Settings → Pages, set the source to "GitHub Actions".

Colors: `layouts/partials/custom_head.html`. Cover text and picture: `content/en/_index.md` and `assets/images/cover-image.jpg`.
