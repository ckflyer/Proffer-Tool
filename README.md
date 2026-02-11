# ✈️ Airline Reserve Shift Navigator

A Progressive Web App (PWA) designed for airline employees on reserve to easily navigate phone menu systems when proffering for shifts. Generate dialable phone numbers with automated menu selections and pauses.

## 🚀 Features

- **Phone Number Generation**: Automatically creates dialable numbers with commas for IVR pauses
- **Menu Tree Navigation**: Add multiple menu steps to navigate complex phone systems
- **Save Configurations**: Store frequently used shift proffer configurations
- **One-Tap Calling**: Instantly dial generated numbers
- **Progressive Web App**: Install on iOS and Android home screens
- **Offline Support**: Works without internet connection once installed
- **Ad Support**: Ready for Google AdSense integration
- **Cross-Platform**: Single codebase works on iOS and Android

## 📱 Installation

### For Users

#### iOS (iPhone/iPad)
1. Open Safari and go to the app URL
2. Tap the Share button (square with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Tap "Add" in the top right
5. The app icon will appear on your home screen

#### Android
1. Open Chrome and go to the app URL
2. Tap the menu (three dots)
3. Tap "Add to Home screen" or "Install app"
4. Confirm by tapping "Add"
5. The app icon will appear on your home screen

### For Developers

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/shift-navigator.git
   cd shift-navigator
   ```

2. **No build process needed!** This is a pure HTML/CSS/JavaScript app
   
3. **Test locally**
   - Open `index.html` in your browser, or
   - Use a local server:
     ```bash
     python -m http.server 8000
     # or
     npx serve
     ```
   - Visit `http://localhost:8000`

## 🌐 Deployment

### Option 1: GitHub Pages (Free & Easy)

1. **Push code to GitHub**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/shift-navigator.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click Settings → Pages
   - Under "Source", select "main" branch
   - Click Save
   - Your app will be live at: `https://yourusername.github.io/shift-navigator/`

3. **Update manifest.json**
   - Change the `start_url` in `manifest.json` to your GitHub Pages URL

### Option 2: Netlify (Free with Custom Domain)

1. Sign up at [netlify.com](https://netlify.com)
2. Drag and drop your project folder
3. Your app is live instantly with HTTPS
4. Optional: Add custom domain in settings

### Option 3: Vercel (Free)

1. Install Vercel CLI: `npm i -g vercel`
2. Run: `vercel`
3. Follow prompts
4. Your app is deployed!

## 💰 Adding Google AdSense

1. **Sign up for Google AdSense**
   - Visit [google.com/adsense](https://www.google.com/adsense)
   - Apply for an account
   - Wait for approval (usually 1-2 weeks)

2. **Get Ad Code**
   - Once approved, create a new ad unit
   - Recommended: 320x50 banner for mobile
   - Copy the ad code provided

3. **Replace Placeholder**
   - Open `index.html`
   - Find this section:
     ```html
     <div class="ad-placeholder">
         Ad Space (320x50)
         <br><small>Add your AdSense code here</small>
     </div>
     ```
   - Replace with your AdSense code:
     ```html
     <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXX"
          crossorigin="anonymous"></script>
     <ins class="adsbygoogle"
          style="display:inline-block;width:320px;height:50px"
          data-ad-client="ca-pub-XXXXXX"
          data-ad-slot="XXXXXXXXXX"></ins>
     <script>
          (adsbygoogle = window.adsbygoogle || []).push({});
     </script>
     ```

## 🎯 How to Use

1. **Enter Base Number**: Input the main phone number (e.g., 1-800-555-1234)
2. **Add Menu Steps**: Click "+ Add Menu Step" for each IVR menu level
3. **Enter Options**: Type the number to press at each menu (1, 2, 3, etc.)
4. **Generate**: The app automatically creates the dialable number with pauses
5. **Call**: Tap "Call Now" to dial automatically
6. **Save**: Give it a name and save for future use

### Example Scenario

**Scenario**: Proffering for a morning shift
- Base Number: 1-800-555-CREW (1-800-555-2739)
- Press 1 for "Reserve Line"
- Press 2 for "Shift Proffering"
- Press 3 for "Morning Shifts"
- Enter Employee ID: 12345

**Generated Number**: `1-800-555-2739,,1,,2,,3,,12345`

The commas create 2-second pauses between each menu selection.

## 🛠️ Technical Details

### Technologies Used
- Pure HTML5, CSS3, JavaScript (No frameworks!)
- Progressive Web App (PWA) standards
- Service Worker for offline functionality
- LocalStorage for saved configurations
- Web App Manifest for installation

### Browser Compatibility
- ✅ iOS Safari 11.3+
- ✅ Android Chrome 40+
- ✅ Desktop browsers (Chrome, Firefox, Safari, Edge)

### File Structure
```
shift-navigator/
├── index.html          # Main app file
├── manifest.json       # PWA manifest
├── sw.js              # Service worker
├── icon-192.png       # App icon (192x192)
├── icon-512.png       # App icon (512x512)
├── README.md          # This file
└── .gitignore         # Git ignore file
```

## 🎨 Customization

### Change Colors
Edit the CSS in `index.html`:
- Primary gradient: `.background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);`
- Button colors: `.btn-primary`, `.btn-success`, etc.
- Theme color: `<meta name="theme-color" content="#1e40af">`

### Change App Name
1. Update `manifest.json`: `"name"` and `"short_name"`
2. Update `index.html`: `<title>` tag and header

### Add More Features
The code is well-commented and easy to modify. Common additions:
- Multiple saved configuration folders
- Share configurations with coworkers
- Statistics/usage tracking
- Voice input for menu options

## 📝 License

MIT License - Feel free to modify and distribute

## 🤝 Contributing

Contributions welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## ⚠️ Disclaimer

This is an unofficial tool created to assist airline employees. It is not affiliated with or endorsed by any airline company. Use at your own discretion and ensure compliance with your company's policies.

## 📧 Support

For issues or questions, please open an issue on GitHub.

---

**Made for airline crew members, by airline crew members** ✈️
