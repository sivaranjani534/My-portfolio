# Sivaranjani R — Portfolio

A personal portfolio site built with React, Vite, and Tailwind CSS, generated
from your resume. The contact form sends messages straight to your inbox
using EmailJS (no backend server needed).

## 1. Open in VS Code

1. Unzip this folder.
2. Open it in VS Code: `File > Open Folder…`
3. Open a terminal in VS Code: `Terminal > New Terminal`

## 2. Install dependencies

```bash
npm install
```

## 3. Set up the contact form to email you (EmailJS)

Right now the form is wired up but needs your own free EmailJS credentials
so messages arrive in **ranjanirajendiran1@gmail.com** (or any inbox you
choose).

1. Go to https://www.emailjs.com and sign up (free tier is enough).
2. **Email Services** -> **Add New Service** -> choose Gmail -> connect
   `ranjanirajendiran1@gmail.com` -> copy the **Service ID**.
3. **Email Templates** -> **Create New Template**. Use these variables in the
   template body, they match what the site sends:
   - `{{from_name}}`
   - `{{from_email}}`
   - `{{message}}`
   - `{{to_email}}`

   Example template body:
   ```
   New portfolio message from {{from_name}} ({{from_email}})

   {{message}}
   ```
   Copy the **Template ID**.
4. **Account** -> **General** -> copy your **Public Key**.
5. In this project, duplicate `.env.example` as a new file named `.env`,
   and fill in the three values:
   ```
   VITE_EMAILJS_SERVICE_ID=service_xxxxxxx
   VITE_EMAILJS_TEMPLATE_ID=template_xxxxxxx
   VITE_EMAILJS_PUBLIC_KEY=xxxxxxxxxxxxxxx
   ```
6. Restart the dev server after saving `.env`.

Until `.env` is filled in, the form will show a friendly error message
telling visitors to email you directly, it won't crash the site.

## 4. Run it locally

```bash
npm run dev
```

Open the printed local URL (usually http://localhost:5173).

## 5. Edit your content

All resume content lives in one file, so you can update it without touching
any component:

```
src/data/resume.js
```

Update your name, skills, projects, education, certifications, or contact
details there.

## 6. Build for deployment

```bash
npm run build
```

This outputs a production-ready `dist/` folder. You can deploy it for free
on Vercel, Netlify, or GitHub Pages. When deploying, add the same three
`VITE_EMAILJS_*` values as environment variables in your hosting provider's
dashboard (most hosts don't read `.env` automatically at deploy time).

## Project structure

```
src/
  components/    Nav, Hero, About, Skills, Projects, Education, Contact, Footer
  data/resume.js Your resume content -- edit this to update the site
  index.css      Tailwind + global styles
  App.jsx        Page layout
```

## Design notes

The theme plays on your flagship project (AES + image steganography):
two accent colors, amber ("cipher") and teal ("plain"), stand in for
"encrypted" and "decrypted" states throughout the UI, and the hero name
animates in from scrambled characters, like text resolving out of a cipher.
