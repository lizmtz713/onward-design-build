# 🚀 Deployment Guide - Onward Design Build

Step-by-step guide to deploy the new website and replace the current one.

---

## Option 1: Netlify (Recommended - Free)

### Step 1: Create Netlify Account
1. Go to [netlify.com](https://netlify.com)
2. Sign up with email or GitHub

### Step 2: Deploy
1. Click **"Add new site"** → **"Deploy manually"**
2. Drag the entire `onward-design-build` folder into the upload area
3. Wait for deployment (30 seconds)
4. You'll get a URL like `random-name-123.netlify.app`

### Step 3: Test
- Visit the Netlify URL
- Check all pages work:
  - Homepage (index.html)
  - About (about.html)
  - Portfolio (portfolio.html)
  - Services (services.html)
  - Contact (contact.html)
- Test mobile view
- Test contact form (needs Formspree setup)

### Step 4: Connect Domain
1. In Netlify dashboard → **Domain settings**
2. Click **"Add custom domain"**
3. Enter `onwarddesignbuild.com`
4. Netlify will show DNS settings to update

### Step 5: Update DNS (in GoDaddy or wherever domain is)
```
Type: A
Name: @
Value: 75.2.60.5

Type: CNAME
Name: www
Value: [your-site-name].netlify.app
```

### Step 6: Wait for DNS
- Takes 5 minutes to 48 hours
- Check status in Netlify dashboard
- SSL certificate auto-generates

---

## Option 2: Vercel (Also Free)

### Step 1: Create Account
1. Go to [vercel.com](https://vercel.com)
2. Sign up

### Step 2: Deploy
1. Click **"Add New"** → **"Project"**
2. Select **"Import from folder"** or drag & drop
3. Upload the `onward-design-build` folder
4. Click **Deploy**

### Step 3: Connect Domain
1. Go to **Settings** → **Domains**
2. Add `onwarddesignbuild.com`
3. Update DNS as instructed

---

## Form Setup (Required)

### Formspree (Free - 50 submissions/month)
1. Go to [formspree.io](https://formspree.io)
2. Create account
3. Click **"New Form"**
4. Copy the form endpoint (looks like `https://formspree.io/f/xyzabc123`)
5. Update `contact.html`:

Find this line:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

Replace `YOUR_FORM_ID` with your actual form ID.

### Test Form
1. Submit a test message
2. Check your email for the submission

---

## Image Replacement

Replace Unsplash placeholders with real photos:

### Files to Update:
1. **index.html** - Hero image, project images, founder photo
2. **about.html** - Project photo, founder photo
3. **portfolio.html** - All project images
4. **services.html** - Service images

### How to Replace:
1. Find the `<img src="https://images.unsplash.com/...">` tags
2. Replace with real image URLs or upload images to Netlify

### Image Sizes:
- Hero: 1920x1080 minimum
- Project cards: 1000x750 minimum
- Founder: 800x1000 portrait
- Use WebP or optimized JPG (under 500KB each)

---

## Post-Launch Checklist

### Immediate
- [ ] Form working (test submission)
- [ ] All pages load correctly
- [ ] Mobile looks good
- [ ] Links work (no 404s)
- [ ] SSL certificate active (https)

### Within 24 Hours
- [ ] Submit sitemap to Google Search Console
- [ ] Update Google Business Profile with new website
- [ ] Test from multiple devices
- [ ] Share new URL with client

### Within 1 Week
- [ ] Set up Google Analytics
- [ ] Replace placeholder images
- [ ] Get client approval on all copy
- [ ] Update social media links

---

## Troubleshooting

### Site not loading?
- DNS propagation can take up to 48 hours
- Check Netlify/Vercel dashboard for errors
- Try clearing browser cache

### Form not working?
- Verify Formspree form ID is correct
- Check spam folder for test submissions
- Ensure method="POST" on form

### Images not loading?
- Check image URLs are correct
- Ensure images are public (not behind auth)
- Check file size (under 10MB)

### Mobile looks broken?
- All pages should be responsive
- Test in Chrome DevTools (F12 → mobile view)
- Clear cache and refresh

---

## Support

Having issues? Check:
- Netlify docs: docs.netlify.com
- Vercel docs: vercel.com/docs
- Formspree docs: formspree.io/help

---

## Files in This Project

```
onward-design-build/
├── index.html      ✅ Homepage
├── about.html      ✅ About page
├── portfolio.html  ✅ Portfolio page
├── services.html   ✅ Services page
├── contact.html    ✅ Contact page
├── README.md       ✅ Project documentation
└── DEPLOY.md       ✅ This file
```

**Total: 5 pages, fully designed, SEO optimized, ready to deploy** 🎉
