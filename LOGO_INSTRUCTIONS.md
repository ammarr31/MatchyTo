# Logo Setup Instructions

## Important: Copy Logo File

Before uploading to Hostinger, you need to copy your logo file to the `web` folder:

1. **Copy the logo file**:
   - From: `matchyto_flutter_app/assets/images/applogo.png`
   - To: `web/applogo.png`

2. **Or manually**:
   - Open the `web` folder
   - Copy `applogo.png` from your Flutter app's assets folder
   - Paste it into the `web` folder

## After Copying

All HTML files are already configured to use `applogo.png` from the same directory.

The logo will appear on:
- Homepage (index.html)
- Privacy Policy page
- Terms of Service page
- Support page

## File Structure

Your `web` folder should contain:
```
web/
├── index.html
├── privacy-policy.html
├── terms-of-service.html
├── support.html
├── applogo.png  ← Make sure this file is here!
└── README.md
```

## Testing

Before uploading to Hostinger, test locally:
1. Open any HTML file in a browser
2. The logo should appear in the header
3. If you see a broken image, the logo file is missing

