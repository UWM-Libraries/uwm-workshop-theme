# UWM Workshop Template

A reusable Jekyll template for building technology-focused workshop sites with University of Wisconsin–Milwaukee (UWM) branding standards.

---

## Features

- UWM-branded styling using official colors and fonts (with accessible fallbacks)
- Organized lesson structure using a Jekyll **collection**
- Automatically generated **Previous / Next** navigation for lesson pages
- Simple **home page layout** listing lessons in order
- Template-ready setup with example `_config.yml`

---

## Getting Started

### Prerequisites

- Ruby and Bundler installed (e.g., `ruby -v`, `bundle -v`)
- Basic familiarity with Jekyll: themes, layouts, and front matter

### Local Setup

1. **Clone the template repository**:

   ```bash
   git clone https://github.com/uwm-libraries/workshop-template.git
   cd workshop-template
   ```

2. **Install dependencies**:

   ```bash
   bundle install
   ```

3. **Run locally**:

   ```bash
   bundle exec jekyll serve
   ```

   Visit `http://localhost:4000` to preview.

---

## Customizing for Your Workshop

### 1. Update `_config.yml`

- Change the `title`, `description`, `author` to fit your workshop.
- Adjust `baseurl` to match the GitHub repo name (e.g., `/my-workshop`).
- Confirm the `url` field corresponds to the base GitHub Pages domain (like `https://yourusername.github.io`).

### 2. Add/Edit Lessons

- Create or update Markdown files in `_lessons/`:
  ```yaml
  ---
  layout: lesson
  title: "Lesson 1: Topic Name"
  position: 1
  permalink: /lessons/lesson-1/
  ---
  ```
- Make sure each lesson has a unique `position` and `permalink`.

### 3. Write Home Page Content

- Open `index.md` and edit the welcome message. It uses the `home` layout.
- You can extend the layout with objectives, images, or links if desired.

---

## Deployment via GitHub Pages

1. Commit all changes to your repository.
2. Enable GitHub Pages in **Settings → Pages**.
3. Make sure the build source is set to your branch (e.g., `main`) and the correct path (root or `/docs`).
4. Wait a moment — your site should go live at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

---

## Optional Enhancements

- Use **GitHub Actions** to build the site if you rely on plugins not supported by Pages' default build.
- Add front-matter variables like `duration`, `prerequisites`, or `resources` to lessons for richer templates.
- Enhance visual design with hero images or customized buttons using SCSS.

---
