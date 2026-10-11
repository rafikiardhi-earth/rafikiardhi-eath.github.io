# RafikiArdhi website

A Quarto website, published free on GitHub Pages at rafikiardhi.earth.

## Edit

- Pages are the `.qmd` files: `index.qmd` (home), `services.qmd`, `about.qmd`, `publications.qmd`, `contact.qmd`.
- Fill in every `[BRACKETED]` placeholder (ORCID, Scholar, LinkedIn, papers).
- Colours and fonts are in `styles.scss`; navigation is in `_quarto.yml`.
- Preview locally in RStudio (open the folder as a project, then Build → Render Website) or run `quarto preview`.

## Publish (one time)

1. Create a GitHub repository, e.g. `rafikiardhi-site`, and push this folder to its `main` branch.
2. In the repository: Settings → Actions → General → Workflow permissions → select **Read and write permissions**.
3. Push any change to `main`. The workflow in `.github/workflows/publish.yml` builds the site and pushes it to a `gh-pages` branch.
4. Settings → Pages → Source: **Deploy from a branch**, branch `gh-pages`, folder `/ (root)`.
5. The site is live at `https://<your-username>.github.io/rafikiardhi-site/` within a few minutes.

## Connect rafikiardhi.earth

1. At your registrar's DNS settings, add:
   - Four `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record for `www` pointing to `<your-username>.github.io`
2. In GitHub: Settings → Pages → Custom domain → `rafikiardhi.earth`, then tick **Enforce HTTPS** once it becomes available (can take up to an hour).

The `CNAME` file in this folder keeps the custom domain set after every publish.
