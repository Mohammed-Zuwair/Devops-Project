# Automated CI/CD Pipeline Showcase

A small static website for demonstrating the project locally and through GitHub Actions.

## Run locally
1. Extract this ZIP.
2. Open `index.html` in Chrome or Edge.
3. Explain the four pipeline stages shown on the page.

## GitHub Actions workflow
The workflow in `.github/workflows/deploy.yml` runs when code is pushed to `main`:
- Checks that `index.html` and `style.css` exist.
- Uploads the website as a Pages artifact.
- Deploys it to GitHub Pages.

## Enable GitHub Pages
1. Create a GitHub repository and push these project files to the `main` branch.
2. Open repository **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **GitHub Actions**.
4. Open the **Actions** tab to view the workflow run.
5. When deployment completes, open the Pages URL shown in the workflow summary.

Note: GitHub Pages deployment requires a GitHub repository and internet access. Opening `index.html` locally only demonstrates the website, not a completed cloud deployment.
