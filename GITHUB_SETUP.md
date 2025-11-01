# GitHub Setup Instructions

Your local Git repository has been initialized and your first commits have been made!

## Next Steps to Push to GitHub

1. **Create a new repository on GitHub:**
   - Go to https://github.com/new
   - Choose a repository name (e.g., "korumat-website" or "korumat.com")
   - Choose whether it should be public or private
   - **DO NOT** initialize it with a README, .gitignore, or license (we already have these)
   - Click "Create repository"

2. **Push your local repository to GitHub:**

   Run these commands in your terminal (replacing `YOUR_USERNAME` and `REPO_NAME` with your actual GitHub username and the repository name you chose):

   ```bash
   cd /Users/rocketbench/Downloads/korumat.com
   git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
   git branch -M main
   git push -u origin main
   ```

   You'll be prompted to enter your GitHub username and a personal access token (or password).

   **Note:** If you haven't set up authentication yet, GitHub will guide you through creating a personal access token.

3. **Verify the push:**

   Visit your repository URL on GitHub and you should see all your files!

## Example Commands

Assuming your GitHub username is `rocketbench` and you named the repo `korumat-website`:

```bash
git remote add origin https://github.com/rocketbench/korumat-website.git
git branch -M main
git push -u origin main
```

## Future Updates

After making changes to the website, commit and push them with:

```bash
git add .
git commit -m "Description of changes"
git push
```

## Troubleshooting

If you get authentication errors:
- Make sure you have a GitHub personal access token (not your password)
- Create one at: https://github.com/settings/tokens
- Use "repo" scope permissions

