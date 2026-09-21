# East Africa CoP on Mountain Monitoring website

Starter website for an **East Africa Community of Practice (CoP) on Mountain Monitoring**, initially focused on the Mount Kenya area, climate, and atmospheric composition.

The site is deliberately built with a small amount of Jekyll/Liquid on top of plain Markdown, YAML and CSS so that most routine maintenance can be done directly in the GitHub web interface.

## Repository structure

```text
.
├── _config.yml                  # Site title, repository/wiki URLs, form links
├── _data/
│   ├── navigation.yml           # Main navigation
│   ├── organizations.yml        # Participating organizations and logos
│   └── program.yml              # Symposium programme
├── _includes/
│   ├── footer.html
│   ├── header.html
│   └── org-logos.html
├── _layouts/
│   ├── default.html
│   └── home.html
├── _posts/                      # News posts (YYYY-MM-DD-title.md)
├── assets/
│   ├── css/style.css
│   └── images/
│       ├── hero/                # Main/hero photographs
│       ├── logos/               # Participating-organization logos
│       └── content/             # Other website images
├── documents/                   # PDFs and other files linked from pages/wiki
├── symposium/
│   ├── index.md
│   ├── program.md
│   ├── registration.md
│   └── abstracts.md
├── about.md
├── news.md
└── index.md
```

## First setup after creating the GitHub repository

1. Copy these files into the repository and push them to the default branch.
2. Edit `_config.yml` and replace `OWNER/REPOSITORY` in `repository_url` and `wiki_url`.
3. In GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the default branch (normally `main`) and `/ (root)`, then save.
6. Enable the repository **Wiki** under **Settings → General → Features** if it is not already enabled.
7. Once Pages is enabled, GitHub will show the public site URL in **Settings → Pages**.

For GitHub Free / free organizations, the Pages repository should be public.

## Routine editing through github.com

Almost all content can be maintained without a local development environment.

### Edit ordinary pages

Open the Markdown file, click the pencil/edit icon, change the text and commit the change.

Common files:

- `index.md` — introductory text on the home page
- `about.md` — CoP description
- `symposium/index.md` — symposium overview
- `symposium/registration.md` — registration instructions
- `symposium/abstracts.md` — abstract instructions

### Add a news item

Create a file under `_posts/` named:

```text
YYYY-MM-DD-short-title.md
```

Example:

```markdown
---
layout: default
title: First planning meeting
---

A short news item goes here.
```

The newest three posts appear automatically on the home page, and all posts appear under **News**.

### Use the wiki

The website is best for stable public information. The GitHub wiki can hold evolving material such as:

- meeting notes;
- technical working documents;
- inventories of monitoring activities;
- background information;
- shared resources;
- draft recommendations.

The News page already contains a link to the wiki. Update `wiki_url` in `_config.yml` after the repository has been created.

### Add the main photograph

1. Upload a photograph into `assets/images/hero/`, for example:
   `assets/images/hero/mount-kenya.jpg`
2. Edit `_config.yml`:

```yaml
hero_image: "/assets/images/hero/mount-kenya.jpg"
```

If `hero_image` is empty, the site uses a simple CSS mountain-style background instead.

### Add participating organizations

1. Upload each logo to `assets/images/logos/`.
2. Edit `_data/organizations.yml`:

```yaml
- name: Organization name
  logo: /assets/images/logos/organization-logo.svg
  url: https://example.org
```

Add one block per organization. SVG or PNG is preferred; use reasonably sized files.

### Add documents

Upload PDFs or other public documents to `documents/`. Link them from Markdown like this:

```markdown
[Download the concept note]({{ '/documents/concept-note.pdf' | relative_url }})
```

Use simple lower-case file names with hyphens and avoid spaces where practical.

### Edit the symposium programme

Edit `_data/program.yml`. An example structure is included as comments in that file.

Programme updates then propagate automatically to the programme page.

### Add registration and abstract forms

Create the forms separately (for example with Google Forms) and put their public URLs in `_config.yml`:

```yaml
symposium_registration_url: "https://..."
symposium_abstract_url: "https://..."
```

Until URLs are set, the corresponding pages display a neutral "not open yet" message.

## Adding future activities

The top level belongs to the Community of Practice, not to the symposium. A future workshop or meeting can therefore simply be added beside `symposium/`, for example:

```text
workshop-2027/
├── index.md
├── programme.md
└── registration.md
```

Add its link to `_data/navigation.yml` when it should appear in the main navigation.

## Local editing is optional

You do not need Jekyll installed simply to maintain the site through github.com. GitHub Pages will build the committed site.

For larger layout or CSS changes, local previewing can be useful, but it is not required for routine content updates.
