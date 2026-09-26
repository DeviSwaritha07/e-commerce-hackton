# Deployment guide

## Recommended for this project: GitHub Pages

Because the app is 100% frontend/static, GitHub Pages is enough. You do not need MongoDB.

### Step 1 — Create repository
Create a new GitHub repository, for example:
`review-intelligence-app`

### Step 2 — Upload project
Upload the contents of this folder, keeping the folder structure:

review-intelligence-app/
- index.html
- styles.css
- app.js
- data/
  - app-data.json
  - model.json
- source/
  - Womens Clothing E-Commerce Reviews.csv
  - dataquest.ipynb

### Step 3 — Enable Pages
GitHub:
Settings → Pages → Build and deployment → Deploy from a branch → `main` → `/ (root)` → Save.

### Step 4 — Open your site
GitHub will show the generated Pages URL under the Pages settings.

## Local testing
Use VS Code Live Server. Opening `index.html` directly as a `file://` URL can block the JSON fetch.

## Other static hosting
Netlify and Vercel also work. No build command is needed.
