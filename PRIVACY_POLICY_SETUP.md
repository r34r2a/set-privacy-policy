# Privacy Policy Setup Instructions

## Overview
You need a public HTTPS URL for your privacy policy to publish on app stores (Google Play, Apple App Store, etc.). This guide walks you through hosting it for free on GitHub Pages and linking it from your app and store listing.

---

## Step 1: Create a GitHub Repository

1. Go to https://github.com and sign in (or create an account)
2. Click the **+** icon → **New repository**
3. Repository name: `privacy-policy` (or any name you prefer)
4. Set it to **Public** (GitHub Pages requires public repos on free plans)
5. **Do NOT** initialize with README (we'll upload our own files)
6. Click **Create repository**

---

## Step 2: Upload the Privacy Policy File

1. On your new repository page, click **uploading an existing file**
2. Drag and drop `privacy-policy.html` from this folder:
   ```
   /home/kal/ak47/ark/code/projects/startup/privacy-policy.html
   ```
3. Commit message: `Add privacy policy`
4. Click **Commit changes**

---

## Step 3: Enable GitHub Pages

1. Go to your repository's **Settings** tab
2. In the left sidebar, click **Pages**
3. Under **Build and deployment** → **Source**, select **Deploy from a branch**
4. Under **Branch**, select `main` (or `master`) and folder `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes, then refresh the page
7. GitHub will show your site URL, typically:
   ```
   https://<your-username>.github.io/privacy-policy/privacy-policy.html
   ```

---

## Step 4: Get Your Privacy Policy URL

Your final URL will look like:
```
https://<your-github-username>.github.io/<repo-name>/privacy-policy.html
```

**Verify it works:** Open the URL in your browser. It should display the privacy policy page with HTTPS (lock icon visible).

---

## Step 5: Add to App Stores

### Google Play Console
1. Go to [Google Play Console](https://play.google.com/console)
2. Select your app → **App content → Privacy policy**
3. Paste your public URL
4. Click **Save**
5. Repeat for each app (you can use the same URL for all apps)

### Apple App Store Connect
1. Go to [App Store Connect](https://appstoreconnect.apple.com)
2. Select your app → **App Information**
3. Add the privacy policy URL in the **Privacy Policy URL** field
4. Click **Save**

---

## Step 6: Link Privacy Policy From Within Your App

App stores require the privacy policy to be accessible from inside the app. Add a link in your **About**, **Settings**, or **Terms** screen.

Example link text:
```
Privacy Policy: https://<your-username>.github.io/<repo-name>/privacy-policy.html
```

Or make it clickable so it opens in a device browser.

---

## Verification Checklist

Before submitting your app:

- [ ] Privacy policy URL loads with `https://`
- [ ] Page displays correctly on mobile and desktop
- [ ] No login required to view
- [ ] Page is not a PDF or downloadable file
- [ ] URL works worldwide (no geo-restrictions)
- [ ] URL added to app store listing for each app
- [ ] Privacy policy link accessible from within the app

---

## Future Updates

If you need to update the privacy policy later:

1. Edit `privacy-policy.html`
2. Upload the updated file to your GitHub repo (replace the existing file)
3. GitHub Pages will automatically redeploy within 1-2 minutes
4. The same URL serves the updated content — no app store changes needed

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| 404 error on GitHub Pages URL | Make sure the file is at the root of the repo, not in a subfolder |
| Page not secure (no HTTPS) | GitHub Pages provides HTTPS automatically; wait a few minutes after enabling |
| App store rejects URL | Ensure the URL is publicly accessible and not behind a login |
| Changes not showing | GitHub Pages can take 1-2 minutes to deploy; check the Actions tab for deployment status |

