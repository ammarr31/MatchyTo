# MatchyTo Website

Static website for MatchyTo app, containing Privacy Policy, Terms of Service, Support/FAQ, and homepage.

## 📁 Files

- `index.html` - Homepage with app features and description
- `privacy-policy.html` - Privacy Policy (required for app stores)
- `terms-of-service.html` - Terms of Service (required for app stores)
- `support.html` - Support page with FAQs

## 🚀 Deployment

### Option 1: Firebase Hosting (Recommended)

1. **Initialize Firebase Hosting** (if not already done):
   ```bash
   cd /path/to/MatchyTo\ Backend
   firebase init hosting
   ```

2. **Configuration**:
   - Public directory: `web`
   - Single-page app: No
   - Auto-deploy: Yes (optional)

3. **Deploy**:
   ```bash
   firebase deploy --only hosting
   ```

4. **Your site will be available at**:
   - `https://YOUR_PROJECT_ID.web.app`
   - `https://YOUR_PROJECT_ID.firebaseapp.com`
   - Or custom domain if configured

### Option 2: Netlify

1. **Drag and drop** the `web` folder to [Netlify Drop](https://app.netlify.com/drop)
2. Or connect via Git and deploy automatically

### Option 3: Vercel

1. **Install Vercel CLI**:
   ```bash
   npm i -g vercel
   ```

2. **Deploy**:
   ```bash
   cd web
   vercel
   ```

### Option 4: GitHub Pages

1. Create a new repository
2. Upload the `web` folder contents
3. Enable GitHub Pages in repository settings
4. Select `main` branch and `/root` folder

### Option 5: Any Static Hosting

The website is pure HTML/CSS with no dependencies. You can upload to any static hosting service:
- AWS S3 + CloudFront
- Google Cloud Storage
- Azure Static Web Apps
- Any web hosting provider

## 🔗 Update URLs in App

After deploying, update the URLs in the Flutter app:

**File**: `matchyto_flutter_app/lib/screens/profile/settings_screen.dart`

```dart
// Replace with your actual deployed URLs
static const String _websiteUrl = 'https://YOUR_DOMAIN.com';
static const String _privacyPolicyUrl = 'https://YOUR_DOMAIN.com/privacy-policy.html';
static const String _termsUrl = 'https://YOUR_DOMAIN.com/terms-of-service.html';
static const String _supportUrl = 'https://YOUR_DOMAIN.com/support.html';
```

## 🎨 Customization

### Update Logo

Currently using emoji (📅). To use a custom logo:

1. **Add logo image** to `web` folder (e.g., `logo.png`)
2. **Update HTML** in all files:
   ```html
   <!-- Replace this -->
   <div class="logo">📅</div>
   
   <!-- With this -->
   <div class="logo">
     <img src="logo.png" alt="MatchyTo" style="width: 100px; height: 100px;">
   </div>
   ```

### Update Colors

The website uses the same color scheme as the app:
- Primary: `#667eea` (purple)
- Secondary: `#764ba2` (darker purple)

Update in `<style>` section of each HTML file.

### Update Contact Email

Search for `support@matchyto.com` in all HTML files and replace with your actual support email.

### Update App Store Links

In `index.html`, update the download badges:
```html
<a href="YOUR_APP_STORE_LINK" class="badge">📱 Download on App Store</a>
<a href="YOUR_GOOGLE_PLAY_LINK" class="badge">🤖 Get it on Google Play</a>
```

## ✅ Testing

Before deploying, test locally:

1. **Open in browser**:
   ```bash
   cd web
   python -m http.server 8000
   ```
   Or use any local web server.

2. **Visit**:
   - `http://localhost:8000/index.html`
   - `http://localhost:8000/privacy-policy.html`
   - `http://localhost:8000/terms-of-service.html`
   - `http://localhost:8000/support.html`

3. **Check**:
   - All links work
   - Pages are responsive (try different screen sizes)
   - No broken images
   - Contact email is correct

## 📱 Mobile Responsiveness

The website is fully responsive and works on:
- Desktop browsers
- Tablets
- Mobile phones

Test on different devices before deploying.

## 🔒 HTTPS Required

**Important**: App stores require HTTPS for Privacy Policy and Terms URLs. Ensure your hosting provides SSL certificates (most modern hosting services do this automatically).

## 📝 Content Updates

### Privacy Policy
- Update date when making changes
- Review data collection practices
- Ensure GDPR compliance if serving EU users

### Terms of Service
- Update date when making changes
- Review subscription terms
- Ensure compliance with app store policies

### Support Page
- Keep FAQs updated based on user questions
- Add new common issues as they arise

## 🚨 Important Notes

1. **Never delete Privacy Policy or Terms of Service** - App stores require these to be accessible at all times
2. **Keep URLs consistent** - Don't change URLs after app is published (or update in app store listings)
3. **Test on mobile** - Most users will view these pages on mobile devices
4. **Monitor accessibility** - Use tools like Google Lighthouse to ensure good performance

---

**Ready to deploy? Choose a hosting option above and get your site live! 🚀**

