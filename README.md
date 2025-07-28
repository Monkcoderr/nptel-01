# 🎓 Certificate Download Portal

A simple, static HTML/CSS/JavaScript website for distributing certificates via QR codes. No backend or database required - perfect for GitHub Pages or basic web hosting.

## 📁 Project Structure

```
nptel-01/
├── index.html                    # Optional landing page
├── download_abhishek.html        # Example download page
├── styles.css                    # Main stylesheet
├── documents/                    # Folder for PDF certificates
│   └── abhishek_certificate.pdf  # (You need to add this)
└── README.md                     # This file
```

## 🚀 Quick Start

1. **Add your PDF certificates** to the `documents/` folder
2. **Create download pages** by copying `download_abhishek.html`
3. **Update the file paths** in each HTML page
4. **Generate QR codes** linking to your download pages
5. **Deploy** to GitHub Pages or any static hosting

## 📋 Setup Instructions

### Step 1: Add Certificate Files
Place your PDF certificates in the `documents/` folder:
```
documents/
├── abhishek_certificate.pdf
├── rahul_certificate.pdf
├── priya_certificate.pdf
└── john_certificate.pdf
```

### Step 2: Create Download Pages
For each certificate, create a new HTML page:

1. Copy `download_abhishek.html` to `download_[username].html`
2. Update these lines in the new file:

```html
<!-- Update the title -->
<title>Download Certificate - [Name]</title>

<!-- Update the greeting -->
<h1 class="greeting">Hello [Name]!</h1>

<!-- Update the file path in JavaScript -->
link.href = 'documents/[username]_certificate.pdf';
link.download = '[Name]_Certificate.pdf';
```

**Example for user "Rahul":**
```html
<title>Download Certificate - Rahul</title>
<h1 class="greeting">Hello Rahul!</h1>
<!-- In JavaScript -->
link.href = 'documents/rahul_certificate.pdf';
link.download = 'Rahul_Certificate.pdf';
```

### Step 3: Generate QR Codes
Create QR codes that link to your download pages:

- **Abhishek:** `https://yourdomain.com/download_abhishek.html`
- **Rahul:** `https://yourdomain.com/download_rahul.html`
- **Priya:** `https://yourdomain.com/download_priya.html`

**Recommended QR Code Generators:**
- [QR Code Generator](https://www.qr-code-generator.com/)
- [QRStuff](https://www.qrstuff.com/)
- [Google Charts QR API](https://developers.google.com/chart/infographics/docs/qr_codes)

### Step 4: Deploy Your Website

#### Option A: GitHub Pages
1. Push your code to a GitHub repository
2. Go to Settings → Pages
3. Select source branch (usually `main`)
4. Your site will be available at `https://[username].github.io/[repository-name]/`

#### Option B: Hostinger/cPanel
1. Upload all files to your hosting public folder
2. Ensure the folder structure is maintained
3. Test the download links

## 🎨 Customization

### Colors and Styling
Edit `styles.css` to change:
- Background gradient colors
- Button colors
- Font styles
- Spacing and layout

### Messages and Text
Update the following in each HTML file:
- Greeting messages
- Success messages
- Footer text
- Contact information

### Adding Your Logo
Replace the emoji icon with your logo:
```html
<!-- Replace this line -->
<div class="certificate-icon" aria-hidden="true">🎓</div>

<!-- With this -->
<img src="logo.png" alt="Organization Logo" class="certificate-icon">
```

## 🔧 Features

- ✅ **Mobile-friendly** responsive design
- ✅ **Accessibility** features (keyboard navigation, screen readers)
- ✅ **Modern UI** with gradients and animations
- ✅ **Success feedback** after download
- ✅ **Error handling** for missing files
- ✅ **SEO optimized** with proper meta tags
- ✅ **No dependencies** - works offline

## 📱 QR Code Best Practices

1. **Test QR codes** before printing/distributing
2. **Use high contrast** for better scanning
3. **Include backup URL** as text below QR code
4. **Size appropriately** - minimum 2cm x 2cm for print
5. **Test on multiple devices** and QR code readers

## 🐛 Troubleshooting

### Download Not Working
- Check PDF file exists in `documents/` folder
- Verify file path spelling in HTML
- Ensure proper file permissions on server

### QR Code Not Scanning
- Increase QR code size
- Improve print quality
- Check for typos in the URL
- Test with different QR code readers

### Mobile Display Issues
- Clear browser cache
- Check viewport meta tag is present
- Test on different screen sizes

## 📈 Analytics (Optional)

Add Google Analytics to track downloads:

```html
<!-- Add to <head> section -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔒 Security Notes

- PDFs are publicly accessible via direct URL
- No password protection on files
- Consider adding basic auth for sensitive certificates
- Use HTTPS for secure transmission

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to submit issues and pull requests to improve this template!

---

**Need help?** Create an issue in this repository or contact support. 