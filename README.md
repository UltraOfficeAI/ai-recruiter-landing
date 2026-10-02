# ai-recruiter-landing

Landing page for UltraOffice's two-sided AI recruiter business: companies pay a success-only placement fee, candidates drop a resume and get matched + applied for free.

Static site in `public/` (plain HTML/CSS, no build). Design: Lightfield token system + dovetail-style landing structure.

## Local preview

```bash
npx serve public
# or
python -m http.server 8000 -d public
```

## Deploy (Firebase Hosting)

```bash
npm install -g firebase-tools
firebase login
firebase projects:create ai-recruiter-landing   # once, if the project doesn't exist
firebase deploy --only hosting
```

Live URL after deploy: `https://ai-recruiter-landing.web.app` (and `https://ai-recruiter-landing.firebaseapp.com`).

If the project id is taken, pick another (`firebase projects:create <name>`) and update `projects.default` in `.firebaserc`.
