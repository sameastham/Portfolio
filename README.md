# Sam Eastham Portfolio Website

A modern, responsive portfolio website with full-screen scrollable sections featuring your UX design work.

## Features

- ✨ Full-screen sections with smooth scrolling
- 🎨 Beautiful gradient backgrounds matching your Figma design
- 📱 Fully responsive (mobile, tablet, desktop)
- 🎯 Smooth navigation with active section highlighting
- 💼 Portfolio showcase with hover effects
- 📧 Contact form that sends emails
- ⚡ Fast loading with optimized animations

## Setup Instructions

### 1. Basic Setup

Simply open `index.html` in your web browser. The site will work immediately for viewing.

### 2. Contact Form Setup (Required for email functionality)

The contact form uses **Web3Forms** - a free service that sends form submissions to your email.

**Steps to enable the contact form:**

1. Go to [https://web3forms.com](https://web3forms.com)
2. Sign up for a free account (no credit card required)
3. Get your Access Key from the dashboard
4. Open `script.js` and find this line (around line 100):
   ```javascript
   access_key: 'YOUR_WEB3FORMS_ACCESS_KEY_HERE',
   ```
5. Replace `YOUR_WEB3FORMS_ACCESS_KEY_HERE` with your actual access key
6. Save the file

**Example:**
```javascript
access_key: 'a1b2c3d4-e5f6-7890-abcd-ef1234567890',
```

### 3. Resume Download Setup

To enable the "Download Resume" button:

1. Open `script.js`
2. Find the `downloadBtn` event listener (around line 70)
3. Replace the alert with your resume URL:
   ```javascript
   window.open('path/to/your/resume.pdf', '_blank');
   ```

**Example:**
```javascript
window.open('https://yourwebsite.com/resume.pdf', '_blank');
// or use a relative path:
window.open('./files/resume.pdf', '_blank');
```

### 4. Customization

#### Update Personal Information
- Edit the text in `index.html`
- Update the LinkedIn URL in the contact section
- Replace portfolio project details

#### Change Colors
- Open `styles.css`
- Modify CSS variables at the top:
  ```css
  :root {
      --primary-pink: #ff00ff;
      --primary-cyan: #00d4ff;
      /* etc... */
  }
  ```

#### Add Your Photo
Replace the SVG placeholder in the About section with your actual photo:
```html
<div class="about-image">
    <img src="path/to/your/photo.jpg" alt="Sam Eastham">
</div>
```

### 5. Hosting

To make your site live on the internet:

#### Option 1: Netlify (Recommended - Free)
1. Create account at [netlify.com](https://netlify.com)
2. Drag and drop your website folder
3. Your site will be live in seconds!
4. Free custom domain available

#### Option 2: GitHub Pages (Free)
1. Create a GitHub repository
2. Upload your files
3. Enable GitHub Pages in settings
4. Access at `yourusername.github.io/repository-name`

#### Option 3: Vercel (Free)
1. Create account at [vercel.com](https://vercel.com)
2. Import your project
3. Instant deployment with custom domain

## File Structure

```
portfolio/
├── index.html          # Main HTML file
├── styles.css          # All styling and responsive design
├── script.js           # JavaScript for interactivity
└── README.md          # This file
```

## Browser Support

- ✅ Chrome (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile browsers

## Troubleshooting

### Contact form not working
- Make sure you've added your Web3Forms access key
- Check browser console for errors (F12)
- Verify you're connected to the internet

### Resume download not working
- Verify the resume file path is correct
- Check that the resume file exists in the specified location
- Make sure the file is accessible (not blocked by permissions)

### Navigation not working on mobile
- Clear browser cache
- Make sure JavaScript is enabled
- Try a different browser

## Need Help?

If you encounter any issues:
1. Check the browser console for errors (Press F12)
2. Verify all file paths are correct
3. Make sure JavaScript is enabled in your browser

## Credits

Design: Sam Eastham
Development: Built with HTML, CSS, and JavaScript
Fonts: Google Fonts (Poppins, Space Mono)

---

**Enjoy your new portfolio website! 🎉**
