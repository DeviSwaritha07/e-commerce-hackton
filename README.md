# ReviewIQ — Customer Review Intelligence

A frontend-only customer review analytics application built from the supplied Women's Clothing E-Commerce Reviews dataset and `dataquest.ipynb`.

## What is included

- Dashboard with KPIs, rating distribution, sentiment snapshot and department review volume
- Reviews Explorer with search, department and rating filters
- AI Predictor using the notebook's TF-IDF + balanced Logistic Regression model directly in the browser
- Issue Intelligence using the notebook's issue dictionary and Level-3 priority workflow
- Product Watchlist
- Model & Method page with evaluation information
- `data/app-data.json` containing precomputed dataset analytics and review records
- `data/model.json` containing exported TF-IDF IDF values and Logistic Regression coefficients
- Original CSV and notebook in `source/`

## No backend / MongoDB

This version does not need Flask, FastAPI, Node/Express, MongoDB, or another server-side API. The browser loads the local JSON files and performs text prediction in JavaScript.

## Run locally

Do not double-click `index.html`. Use VS Code Live Server:

1. Open the `review-intelligence-app` folder in VS Code.
2. Install the **Live Server** extension.
3. Right-click `index.html`.
4. Select **Open with Live Server**.
5. The app opens in your browser.

## Deploy

### GitHub Pages
1. Create a GitHub repository.
2. Upload all files/folders from this project.
3. Go to **Settings → Pages**.
4. Select **Deploy from a branch**.
5. Select `main` and `/root`.
6. Save.
7. GitHub will provide your public website link.

### Netlify
Drag the whole project folder into Netlify's deploy area, or connect the GitHub repository.

### Vercel
Import the GitHub repository. Use the project root as the site root. No build command is required.

## Important

Keep these paths unchanged:
- `data/app-data.json`
- `data/model.json`
- `app.js`
- `styles.css`

The app uses relative paths, so it works on GitHub Pages, Netlify and Vercel.

## Model result

The notebook-aligned TF-IDF + Logistic Regression model was retrained using the supplied CSV with an 80/20 stratified split and achieved approximately **80.86% test accuracy** in this build.

## Source alignment

The app follows the supplied notebook's terminology and workflow:
- rating sentiment
- TF-IDF + Logistic Regression
- issue dictionary
- issue frequency
- business priority
- product/department analysis
- actionable recommendations
