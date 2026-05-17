# Deploying to GitHub Pages (under VinMoeMac)

Your global git is set to your work email (`vincent@bodhiumlabs.com`). We'll override it for **this repo only** so commits go to your personal **VinMoeMac** account.

## Step 1 — Add your photos

Drop your images into the `images/` folder. See `images/README.txt` for filenames.

## Step 2 — Preview locally

Double-click `index.html`. Make sure it looks how you want before deploying.

## Step 3 — Create the GitHub repo (browser)

1. Sign in to https://github.com as **VinMoeMac** (sign out of any work account first!).
2. Click **+** (top right) → **New repository**.
3. Name it something like `mothers-day` or `for-mom`.
4. Set it **Public** (required for free GitHub Pages).
5. **Do NOT** check "Add a README" — we already have one.
6. Click **Create repository**.
7. Copy the URL it shows, e.g. `https://github.com/VinMoeMac/mothers-day.git`

## Step 4 — Push from your computer

Open PowerShell, then run these commands (replace the URL with yours):

```powershell
cd C:\Users\vinmo\Documents\mothers-day-site

git init
git branch -M main

# Override identity for THIS repo only (keeps your global work identity intact)
git config user.name "VinMoeMac"
git config user.email "vinmoemac15@gmail.com"

git add .
git commit -m "Happy Mother's Day site"

git remote add origin https://github.com/VinMoeMac/mothers-day.git
git push -u origin main
```

When git prompts for credentials, sign in as **VinMoeMac** (use a Personal Access Token if asked for a password — github.com → Settings → Developer settings → Personal access tokens).

## Step 5 — Turn on GitHub Pages

1. On the repo page, click **Settings** (top right of repo).
2. In the left sidebar click **Pages**.
3. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
4. Set **Branch** to `main` and folder to `/ (root)`.
5. Click **Save**.
6. Wait ~1 minute. The page will refresh and show your live URL:
   `https://VinMoeMac.github.io/mothers-day/`

## Step 6 — Share with Mom 💐

Send her the link!

---

## To update the site later

```powershell
cd C:\Users\vinmo\Documents\mothers-day-site
git add .
git commit -m "what you changed"
git push
```

Changes go live in about a minute.
