
# Nest Land Bank & Realty — Website Package
Files included:
- index.html — single-page website.
- deploy_instructions.txt — how to deploy on GitHub Pages quickly.

## What you need to do (3 quick steps)
1. **Edit index.html (optional)**:
   - Replace the placeholder Google Form URL in the script:
     Find the line: `const formUrl = 'https://forms.gle/YOUR_GOOGLE_FORM_URL_PLACEHOLDER';`
     Replace with your actual Google Form share link (Forms → Send → Link).
   - If you want the site to show live listings from your Google Sheet, publish the sheet to the web (CSV) and replace the `sampleListings` with a fetch parser (instructions below).

2. **Connect Google Sheet as CSV (optional, no code server)**:
   - In your Google Sheet (Form Responses tab): `File → Publish to the web` → choose the tab → format: `Comma-separated values (.csv)` → Publish.
   - Copy the CSV export URL: `https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID/export?format=csv&gid=GID`
   - In `index.html`, find the comment that shows CSV fetch pseudo-code and replace `sampleListings` or add a fetch call to load and parse the CSV then call `renderListings(parsedData)`.
   - If you want, I can provide the exact CSV parsing snippet for your sheet structure — tell me when you're ready.

3. **Host the site (simple free option)**:
   - Use GitHub Pages:
     - Create a new GitHub repo (e.g., `nest-land-bank-site`) and upload `index.html`.
     - In the repo settings → Pages → Source: main branch → / (root) → Save.
     - Your site will be live at `https://USERNAME.github.io/REPO_NAME/` within a minute.
   - Alternatively, upload `index.html` to Netlify or Vercel (drag-and-drop) for also free hosting with HTTPS.

## Need help?
Tell me:
- Your Google Form link and I’ll paste it into `index.html` for you.
- Or, tell me your Google Sheet ID and I’ll give you the exact small JavaScript snippet to fetch and parse the CSV and show live listings.
