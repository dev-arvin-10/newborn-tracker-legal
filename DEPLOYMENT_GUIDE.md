# Deployment Guide for Legal Documents

This guide explains how to host the Newborn Tracker legal documents and update the app with the correct URLs.

## Option 1: GitHub Pages (Recommended - Free)

### Step 1: Create Repository
1. Go to GitHub and create a new repository
2. Name it `newborn-tracker-legal` (or any name you prefer)
3. Make it public (required for free GitHub Pages)

### Step 2: Upload Files
1. Upload all files from the `docs/` folder to your repository
2. Commit the changes

### Step 3: Enable GitHub Pages
1. Go to repository Settings
2. Scroll to "Pages" section
3. Under "Source", select "Deploy from a branch"
4. Select "main" branch and "/ (root)" folder
5. Click Save

### Step 4: Get Your URLs
Your documents will be available at:
- Privacy Policy: `https://yourusername.github.io/newborn-tracker-legal/privacy-policy.html`
- Terms of Service: `https://yourusername.github.io/newborn-tracker-legal/terms-of-service.html`
- Support: `https://yourusername.github.io/newborn-tracker-legal/support.html`

## Option 2: Netlify (Free)

### Step 1: Create Account
1. Go to netlify.com and create a free account

### Step 2: Deploy
1. Drag and drop the entire `docs/` folder to Netlify
2. Netlify will provide you with a random URL like `https://amazing-name-123456.netlify.app`

### Step 3: Custom Domain (Optional)
1. You can change the site name in Netlify settings
2. Or connect a custom domain if you have one

## Option 3: Vercel (Free)

### Step 1: Create Account
1. Go to vercel.com and create a free account

### Step 2: Deploy
1. Connect your GitHub repository or upload files directly
2. Vercel will provide you with a URL

## Updating the App

After hosting your documents, update the URLs in your app:

### Step 1: Edit Constants File
Open `NewbornTracker/src/utils/subscriptionConstants.ts` and replace the placeholder URLs:

```typescript
export const APP_URLS = {
  PRIVACY_POLICY: 'https://your-actual-domain.com/privacy-policy.html',
  TERMS_OF_SERVICE: 'https://your-actual-domain.com/terms-of-service.html',
  SUPPORT: 'https://your-actual-domain.com/support.html',
} as const;
```

### Step 2: Test the URLs
1. Build and run your app
2. Go to Settings and tap on the legal document links
3. Verify they open correctly in the browser

## Important Notes

1. **Test Before App Store Submission**: Make sure all URLs work before submitting to the App Store
2. **HTTPS Required**: Apple requires HTTPS URLs for legal documents
3. **Keep Documents Updated**: Update the "Last updated" date when you make changes
4. **Backup**: Keep a backup of your documents in case you need to update them

## Troubleshooting

### GitHub Pages Not Working
- Make sure the repository is public
- Check that GitHub Pages is enabled in settings
- Wait a few minutes for deployment to complete

### Links Not Opening in App
- Verify URLs are correct in constants file
- Make sure URLs use HTTPS
- Test URLs in a web browser first

### Need to Update Documents
1. Edit the HTML files in your repository
2. Commit the changes
3. GitHub Pages will automatically update (may take a few minutes)

## Contact

If you need help with deployment, contact: devarvin10@gmail.com