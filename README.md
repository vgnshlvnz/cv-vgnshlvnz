# CV site

Static CV page on Cloudflare (Workers Static Assets, free tier).

## Edit
Everything is in `public/index.html`. Search for `[` to find every placeholder.

## Preview locally
    npx wrangler dev        # http://localhost:8787

## Deploy
    npx wrangler login
    npx wrangler deploy     # gives you https://vignesh-cv.<subdomain>.workers.dev

For auto-deploy on every push: Cloudflare dashboard > Workers & Pages > Create >
Import a repository, pick this repo. No build command needed.

## The PDF button
- If `public/cv.pdf` exists, the button downloads it.
- If not, it opens the print dialog; choose "Save as PDF". The print stylesheet
  lays the CV out on A4 with selectable text.
- To make a fixed cv.pdf: open the site in Chrome, click the button, Save as PDF
  (Margins: None, Background graphics: on), save it as `public/cv.pdf`, redeploy.
