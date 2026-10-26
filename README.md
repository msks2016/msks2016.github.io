# Personal website: Mohammad Shahinur Karim

An academic website built with [Jekyll](https://jekyllrb.com) for GitHub Pages. Every section of the site is a folder, and every item (a paper, a project, a job, a blog post) is one small text file. To add something, copy a file; to remove something, delete its file.

The layout follows the [academicpages](https://github.com/academicpages/academicpages.github.io) template (menu at the top, profile and contact links in a sidebar), rebuilt with a smaller, simpler set of files. It uses no outside fonts or scripts, so it loads quickly everywhere, including mainland China.

---

## 1. Put the site online (first time)

1. Sign in to GitHub as **msks2016** and create a new repository named exactly **`msks2016.github.io`**. Make it **Public** and leave "Add a README" unticked.
2. On the new repository's page, click **uploading an existing file**.
3. Unzip the download. Open the `msks2016.github.io` folder, select **everything inside it** (all files and folders), and drag them into the upload area. Upload the contents, not the folder itself, or the site will not build. Then click **Commit changes**.
4. Go to **Settings → Pages**. Under *Build and deployment*, set **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**, and click **Save**.
5. After 1–2 minutes the site is live at **https://msks2016.github.io**. You can watch progress under the **Actions** tab ("pages build and deployment").

Your file manager may hide `.gitignore` because its name starts with a dot. That is fine: the site works without it.

---

## 2. Where everything is

| What you see on the site | Where to edit it |
|---|---|
| Your name, bio, photo, email, ORCID, GitHub and other sidebar links | `_config.yml` (the `author:` block) |
| Menu tabs (names and order) | `_data/navigation.yml` |
| Front page: the large statement, introduction and contact sentence | `_pages/home.md` |
| **Projects** tab and the projects on the front page | `_projects/` (one file per project) |
| **Research** tab | `_research/` (one file per theme) |
| **Publications** tab | `_publications/` (one file per paper) |
| **Experience** tab | `_experience/` (one file per position) |
| **About** tab: introduction | `_pages/about.md` |
| **About** tab: education, internships, awards, skills, languages | `_about/` (one file per item) |
| **Blog** tab | `_posts/` (one file per post) |
| The short introduction under each tab title | the matching file in `_pages/` |
| Colours, fonts, spacing | `assets/css/main.css` (top of the file) |
| Profile photo and icons | `images/` |
| PDFs (CV, papers, posters) | `files/` |
| Blank starter files with every option explained | `_templates/` |

You do not need to touch `_layouts/` or `_includes/`. They hold the page design.

---

## 3. Everyday edits

**Edit a file on GitHub:** open the file, click the pencil icon, make the change, then click **Commit changes**. The site updates 1–2 minutes later.

**Add a new item:** open the folder (for example `_publications`), click **Add file → Create new file**, type a file name ending in `.md`, paste in the matching starter from `_templates/`, fill it in and commit.

**Remove an item:** open the file, click the **⋯** menu, choose **Delete file**, and commit.

### Add a publication
Copy `_templates/publication.md` into `_publications/`, for example as `2027-karim-new-paper.md`. Fill in the title, authors, date, journal and DOI. Your name is put in bold automatically (set the exact spelling in `highlight_author` in `_config.yml`). Papers are grouped by year, newest first.

### Add or update a project
Copy `_templates/project.md` into `_projects/`. The file name becomes the web address: `my-project.md` → `/projects/my-project/`. Set `featured: true` to show it on the front page, and `order` to choose its position. `status` controls the coloured line beside it: **Ongoing** (blue-violet), **In preparation** (pink), **Proposed** (grey, dashed) or **Completed** (dark).

When a project is published, update its text and add the paper and code links (see the commented-out `links:` lines at the top of `_projects/lncrna-signature-benchmark.md`).

### Write a blog post
Copy `_templates/blog-post.md` into `_posts/` and name it `YYYY-MM-DD-short-title.md`. Jekyll requires the date at the start of the name, and posts appear newest first. If the post is about one of your papers, set `publication:` to the paper's file name without `.md` (for example `"2025-myopia-screen-time"`). The paper's citation then appears at the end of the post, and a "Blog post" link appears next to the paper on the Publications tab.

### Experience, About and Research
- **Experience:** one file per position in `_experience/`. Set `category` to `research` or `professional`. Positions are sorted by `start` date, newest first.
- **About:** one file per item in `_about/`. Set `category` to `education`, `internship`, `award`, `skill` or `language`, and `order` (1 = first). To add a new section, add two lines under `sections:` in `_pages/about.md`.
- **Research:** one file per theme in `_research/`. Projects and papers whose `themes:` list includes the theme's file name (without `.md`) are listed under it automatically.

### Change the profile photo
Upload a square photo to `images/` (for example `images/photo.jpg`), then change `avatar: "/images/profile.png"` in `_config.yml` to `avatar: "/images/photo.jpg"`. The current image is a placeholder with your initials.

### Add your CV or Google Scholar to the sidebar
Upload the PDF to `files/` (for example `files/Karim_CV.pdf`) and set `cv: "/files/Karim_CV.pdf"` in `_config.yml`. Fill in `google_scholar`, `researchgate` or `linkedin` with the full web address in the same block. Empty values ("") are hidden. Remove your phone number and referees' contact details from any CV you upload, because files in this repository are public.

### Rename, reorder or hide a tab
Edit `_data/navigation.yml`. To hide a tab, delete its two lines. To rename one, change its `title`.

---

## 4. Rules that prevent most errors

- Keep the `---` lines at the top and bottom of the settings block of each file.
- Keep text values in double quotes: `title: "My title"`. If the text itself needs quotation marks, use curly ones (“ ” or ‘ ’).
- Keep the indentation (spaces) in `_config.yml`, `_data/navigation.yml` and the `sections:` lists.
- Dates are written `YYYY-MM-DD`, without quotes.

If the site stops updating, open the **Actions** tab. A red cross means the build failed; click it to see which file has the problem.

---

## 5. Change the look

All colours and fonts are set at the top of `assets/css/main.css`:

- `--hematoxylin` (blue-violet) and `--eosin` (pink) are the two accent colours, taken from H&E histology staining.
- `--font-serif` is used for headings and `--font-sans` for body text. Both use fonts already installed on the visitor's device.
- A dark version of the palette is used automatically when the visitor's device is in dark mode. Delete the `@media (prefers-color-scheme: dark)` block to turn this off.

---

## 6. Preview on your computer (optional)

You can skip this: editing on GitHub is enough. To preview locally, install Ruby and Bundler, then run these commands in this folder:

```
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

---

## 7. Credits

- Layout inspired by [academicpages](https://github.com/academicpages/academicpages.github.io), itself based on [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) by Michael Rose.
- Icons: [Font Awesome Free](https://fontawesome.com) 6.5.2, licensed CC BY 4.0.
