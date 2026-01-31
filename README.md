# Footloose Entertainment Website - Netlify Setup Guide

## Project Overview
Modern, SEO-optimized website for Footloose Entertainment built for deployment on Netlify. Focus on Jacksonville & St. Augustine markets with emphasis on corporate events and photobooths.

## Folder Structure

```
footloose-site/
├── index.html              # Homepage
├── styles.css              # Main stylesheet
├── script.js               # JavaScript for interactivity
├── README.md              # This file
├── images/                # All images go here
│   ├── footloose-logo.png
│   ├── footloose-logo-white.png
│   ├── hero-event.jpg
│   ├── corporate-event.jpg
│   ├── wedding-event.jpg
│   ├── dj-setup.jpg
│   ├── 360-photobooth.jpg
│   ├── photography-service.jpg
│   ├── team-event.jpg
│   └── icons/
│       ├── dj-icon.svg
│       ├── photobooth-icon.svg
│       └── package-icon.svg
├── corporate-events.html   # Coming next
├── photobooths.html       # Coming next
├── dj-services.html       # Coming next
└── ... (other pages)
```

## Step 1: Get Your Images Ready

### Required Images for Homepage:

1. **Logo** (`footloose-logo.png`)
   - Your current logo
   - Recommended size: 400x160px (transparent background)
   - Also create white version for footer

2. **Hero Image** (`hero-event.jpg`)
   - Your best event photo - DJ setup with crowd dancing
   - Recommended size: 1920x1080px
   - Should show energy and professionalism

3. **Corporate Event** (`corporate-event.jpg`)
   - Professional corporate event photo
   - Size: 1200x800px
   - Show DJ or photobooth at business setting

4. **Wedding Event** (`wedding-event.jpg`)
   - Wedding reception photo
   - Size: 1200x800px
   - Show happy couple or guests having fun

5. **DJ Setup** (`dj-setup.jpg`)
   - Your DJ equipment/setup photo
   - Size: 800x600px
   - Professional lighting setup

6. **360 Photobooth** (`360-photobooth.jpg`)
   - 360 photo booth in action
   - Size: 800x600px
   - Guests using the booth

7. **Photography Service** (`photography-service.jpg`)
   - Photographer at work or photo example
   - Size: 800x600px

8. **Team/Event Photo** (`team-event.jpg`)
   - Your team at event or group enjoying event
   - Size: 1000x800px

### Image Optimization:
Before uploading, optimize all images:
- Use tools like TinyPNG.com or Squoosh.app
- Convert to WebP format if possible (but JPG is fine)
- Reduce file size without losing quality
- Target: Under 200KB per image

## Step 2: Set Up GitHub

### Create GitHub Account (if needed):
1. Go to https://github.com
2. Click "Sign up"
3. Choose free plan
4. Verify email

### Create Repository:
1. Click the "+" in top right corner
2. Select "New repository"
3. Name it: `footloose-entertainment`
4. Description: "Footloose Entertainment website"
5. Make it Public
6. Check "Add a README file"
7. Click "Create repository"

### Upload Your Files:
1. Click "Add file" → "Upload files"
2. Drag and drop all files from footloose-site folder
3. Add commit message: "Initial homepage commit"
4. Click "Commit changes"

## Step 3: Set Up Netlify

### Create Netlify Account:
1. Go to https://netlify.com
2. Click "Sign up"
3. Choose "Sign up with GitHub" (easiest)
4. Authorize Netlify to access your GitHub

### Deploy Your Site:
1. Click "Add new site" → "Import an existing project"
2. Choose "GitHub"
3. Select your `footloose-entertainment` repository
4. Build settings:
   - Build command: (leave blank)
   - Publish directory: `/` (root)
5. Click "Deploy site"

### Get Your Staging URL:
- Netlify will give you a URL like: `random-name-123.netlify.app`
- This is your staging site!

### Set Up Custom Subdomain:
1. In Netlify dashboard, go to "Site settings"
2. Click "Domain management"
3. Click "Add custom domain"
4. Enter: `new.footlooseentertainment.com`
5. Follow DNS instructions (we'll set this up next)

## Step 4: DNS Setup for Subdomain

You need to add a CNAME record in your domain DNS:

### If using GoDaddy:
1. Log into GoDaddy
2. Go to "My Products" → Domain
3. Click DNS for footlooseentertainment.com
4. Click "Add" → "CNAME"
5. Host: `new`
6. Points to: `[your-netlify-url].netlify.app`
7. TTL: 1 Hour
8. Save

### If using Cloudflare:
1. Log into Cloudflare
2. Select footlooseentertainment.com
3. Go to DNS
4. Click "Add record"
5. Type: CNAME
6. Name: `new`
7. Target: `[your-netlify-url].netlify.app`
8. Proxy status: DNS only (gray cloud)
9. Save

**Wait 10-60 minutes for DNS to propagate**

## Step 5: Update Content

### Update Phone Number:
Search for `(904) 555-1234` and replace with your real number in:
- index.html (appears 3 times)

### Update Social Media Links:
In footer section of index.html, update:
- Facebook URL
- Instagram URL

### Update Logo Paths:
Once you upload your actual logo:
- Replace `images/footloose-logo.png` paths
- Replace `images/footloose-logo-white.png` paths

## Step 6: Test Your Site

Visit `new.footlooseentertainment.com` and check:

✓ All images load
✓ Mobile menu works
✓ All buttons/links work
✓ Phone number is correct
✓ Forms work (when you add contact page)
✓ Site loads fast (under 3 seconds)

## Making Updates

### To update your site:
1. Edit files on your computer
2. Go to GitHub repository
3. Click "Upload files" or edit directly on GitHub
4. Commit changes
5. Netlify automatically rebuilds (takes 1-2 minutes)
6. Check `new.footlooseentertainment.com`

## SEO Checklist

Before launch, verify:
- [ ] All images have descriptive alt text
- [ ] Page title is accurate (60 characters or less)
- [ ] Meta description is compelling (155 characters or less)
- [ ] All internal links work
- [ ] Phone number clickable on mobile
- [ ] Site loads in under 3 seconds
- [ ] Mobile responsive on all devices
- [ ] Google Analytics installed (when ready)

## Next Pages to Build

1. **Corporate Events** (`corporate-events.html`)
2. **Photobooths** (`photobooths.html`)
3. **DJ Services** (`dj-services.html`)
4. **Contact/Quote** (`contact.html`)
5. **Jacksonville Corporate** (`jacksonville-corporate-event-dj.html`)
6. **St. Augustine Wedding** (`st-augustine-wedding-entertainment.html`)

## Color Scheme Reference

Primary Colors:
- Red: #E63946 (energy, excitement)
- Navy: #1D3557 (trust, professional)
- Gold: #FFB703 (celebration, premium)
- Cream: #F1FAEE (elegance)

## Font Reference

- Headlines: Bebas Neue (bold, impactful)
- Body Text: Barlow (clean, readable)

## Support

If you need help:
1. Check Netlify documentation: https://docs.netlify.com
2. GitHub guides: https://guides.github.com
3. I can help you troubleshoot any issues!

## Going Live

When you're ready to replace your old site:
1. Make sure all pages are built and tested
2. Back up your current site
3. In your domain DNS settings:
   - Change your main A record or CNAME to point to Netlify
   - Or update your existing DNS to point to Netlify
4. Test everything at www.footlooseentertainment.com
5. Keep the old site available for 24 hours just in case

---

## Questions?

Feel free to ask about:
- Image specifications
- Content updates
- Adding new pages
- SEO optimization
- Anything else!
