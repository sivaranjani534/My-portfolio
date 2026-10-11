# Sivaranjani R — Portfolio (Static Version)

A single-page portfolio website built with plain **HTML, CSS, and JavaScript** — no build tools, no frameworks, no dependencies.

## 📁 Folder Structure

```
portfolio/
├── assets/
│   ├── profile.jpg                  # Profile photo
│   └── Sivaranjani_R_Resume.pdf     # Downloadable resume
├── index.html                       # HTML + CSS + JS all in one file
└── README.md                        # This file
```

## 🚀 How to Use

1. Unzip the folder.
2. Double-click `index.html` to open it directly in any browser — no server or installation needed.
3. To publish it online, upload the whole `portfolio` folder (keeping `assets/` alongside `index.html`) to any static host:
   - **GitHub Pages** — push the folder to a repo and enable Pages
   - **Netlify / Vercel** — drag and drop the folder to deploy
   - **Any web hosting** — upload via FTP/cPanel

## ✏️ How to Edit

Everything lives in `index.html`:
- **Styling** — inside the `<style>` block in the `<head>`
- **Content/Markup** — inside the `<body>` (Hero, About, Skills, Projects, Education, Certificates, Soft Skills, Languages, Contact)
- **Behavior** — inside the `<script>` block at the bottom (mobile menu, scroll effects, skill bar animation, contact form)

To update your photo or resume, simply replace the files inside `assets/` with new ones **using the same filenames** (`profile.jpg` and `Sivaranjani_R_Resume.pdf`), or update the file paths in `index.html` if you rename them.

## ✉️ Contact Form

The contact form works without any backend or third-party service — on submit, it opens the visitor's default email app with a pre-filled message addressed to `ranjanirajendiran1@gmail.com`.

## 🖌️ Sections Included

- Hero (name, role, location, CTAs, social links)
- About
- Skills (animated progress bars)
- Projects (Steganography, Bus Booking, Portfolio)
- Education
- Certifications & Publication
- Soft Skills
- Languages
- Contact
