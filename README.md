# Midas
Project repo for the JPMC Advanced Software Engineering Forage program

## Automatic Vercel deployment from GitHub

This repository includes a GitHub Actions workflow that deploys to Vercel on every push to `main` or `master`.

### 1) Add required GitHub repository secrets

In GitHub, open **Settings → Secrets and variables → Actions** and add:

- `VERCEL_TOKEN` (from your Vercel account token)
- `VERCEL_ORG_ID` (your Vercel team/org ID)
- `VERCEL_PROJECT_ID` (your Vercel project ID)

You can get the org/project IDs from Vercel project settings, or by running `vercel link` locally and checking `.vercel/project.json`.

### 2) Connect the repo to your Vercel project

Create/import the project in Vercel once so the IDs above match the correct project.

### 3) Push changes

After secrets are set, every push to `main`/`master` triggers `.github/workflows/vercel-deploy.yml` and updates the Vercel deployment automatically.
