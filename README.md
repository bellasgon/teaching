# Virtual Syllabus Template (Jekyll + GitHub Pages)

A lightweight template to build a **virtual syllabus** with sidebar navigation, weekly pages, and reading pages, ready to publish with GitHub Pages.

## ✨ What this template includes

- Sidebar + main-content layout.
- Configuration-driven navigation via `_config.yml`.
- Modular Jekyll structure (`_layouts`, `_includes`).
- Optional course logo on the Home page.
- Responsive styling for desktop and mobile.

## 📁 Project structure

```text
.
├── _config.yml
├── _includes/
│   └── sidebar.html
├── _layouts/
│   └── default.html
├── assets/
│   ├── style.css
│   └── img/
│       └── jgu-logo.png (optional)
├── index.md
├── schedule.md
├── instructions.md
├── seminars/
│   ├── week01.md
│   └── week02.md
└── readings/
    └── core.md
```

## ⚙️ Main configuration (`_config.yml`)

Update these fields:

- `title`: course name.
- `description`: short subtitle.
- `baseurl`: for project GitHub Pages (example: `/teaching`).
- `course_logo`: logo path shown on Home.
- `course_navigation`: links displayed in the sidebar.

Example:

```yml
title: Seminar Course
description: Academic Seminar
baseurl: "/teaching"
course_logo: "/assets/img/jgu-logo.png"

course_navigation:
  main:
    - title: Home
      path: /
    - title: Schedule
      path: /schedule
```

## 🧭 How navigation works

The sidebar is automatically rendered from `course_navigation`.

- `main`: primary links (Home, Schedule, etc.)
- `weeks`: weekly pages (`/seminars/week01`, ...)
- `readings`: reading pages (`/readings/core`, ...)

To add a new week:

1. Create `seminars/week03.md`
2. Add it to `_config.yml`:

```yml
weeks:
  - title: Week 3
    path: /seminars/week03
```

## 🖼️ Home logo

The Home page shows a logo next to the title using `site.course_logo`.

1. Put your file in `assets/img/`.
2. Set `course_logo` in `_config.yml`.

If you want to remove the logo, leave it empty:

```yml
course_logo: ""
```

## 🚀 Deploy on GitHub Pages

1. Push this repository to GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select your branch (for example `main`) and root folder.
4. Save and wait for deployment.

If internal links break, check:

- `baseurl` in `_config.yml`
- `relative_url` usage in links

## 🛠️ Quick customization map

- Colors and spacing: `assets/style.css`
- Global HTML structure: `_layouts/default.html`
- Sidebar rendering: `_includes/sidebar.html`
- Home content: `index.md`

## 🤝 Reusing this template

To create a new syllabus with this structure:

1. Fork/clone this repository.
2. Update `_config.yml` (title, description, navigation).
3. Replace page content (`schedule.md`, `seminars/*`, `readings/*`).
4. Deploy with GitHub Pages.


