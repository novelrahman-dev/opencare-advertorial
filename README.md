# Opencare Advertorial - GitHub Pages Deployment

This package is optimized for GitHub Pages deployment with relative paths.

## Quick Deployment Steps

### Option 1: Direct Upload to GitHub Repo

1. **Create/Navigate to your GitHub repository**
   ```
   https://github.com/novelrahman-dev/opencare-advertorial
   ```

2. **Delete all existing files** in the repo (or create a new branch)

3. **Upload all files from this folder** to the root of your repo:
   - index.html
   - assets/ (folder with CSS and JS)
   - All image files (*.jpg, *.png)

4. **Commit the changes**

5. **Enable GitHub Pages**:
   - Go to Settings → Pages
   - Source: "Deploy from a branch"
   - Branch: main (or master)
   - Folder: / (root)
   - Click Save

6. **Wait 1-2 minutes** for GitHub to build and deploy

7. **Visit your site**:
   ```
   https://novelrahman-dev.github.io/opencare-advertorial/
   ```

### Option 2: Using Git Command Line

```bash
# Clone your repo (or navigate to it)
git clone https://github.com/novelrahman-dev/opencare-advertorial.git
cd opencare-advertorial

# Remove old files (optional, if updating)
git rm -rf .
git commit -m "Clear old files"

# Copy new files
cp -r /path/to/opencare-github-pages/* .

# Add and commit
git add .
git commit -m "Deploy advertorial site"

# Push to GitHub
git push origin main
```

## Troubleshooting

### Page shows blank or "404"
- Make sure all files are in the ROOT of your repo, not in a subfolder
- Check that GitHub Pages is enabled in Settings → Pages
- Wait 2-3 minutes after pushing for GitHub to rebuild

### CSS/JS not loading
- This build uses relative paths (./assets/) which works for GitHub Pages
- Make sure the `assets/` folder is uploaded correctly
- Check browser console (F12) for specific errors

### Images not showing
- Verify all .jpg and .png files are uploaded
- Check that filenames match exactly (case-sensitive)

## File Structure

Your repo should look like this:
```
opencare-advertorial/
├── index.html
├── assets/
│   ├── index-CWIhDKvv.css
│   └── index-Ctsl4Ut2.js
├── dental-checkup.jpg
├── hero-dental-benefits.jpg
├── insurance-paperwork.jpg
├── unused-benefits.jpg
└── insurance-logos.png
```

## Features Included

✅ Fully responsive design
✅ Exit-intent popup
✅ Testimonial slider
✅ FAQ accordion  
✅ Urgency countdown banner
✅ Google Ads tracking integration
✅ Optimized for native advertising

## Support

If you continue to have issues, check:
1. GitHub Actions tab for build errors
2. Browser console (F12 → Console) for JavaScript errors
3. Network tab (F12 → Network) to see which files are failing to load

Built: November 27, 2025
Version: GitHub Pages Compatible
