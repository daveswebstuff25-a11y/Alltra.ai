# Alltra Website with Netlify CMS

A modern, fast website for Alltra with an integrated content management system.

## Features

✅ **Lightning fast** - Static HTML/CSS/JS
✅ **Easy content editing** - Netlify CMS admin panel
✅ **No database required** - Content stored in files
✅ **Free hosting** - Deploy on Netlify for $0/month
✅ **Secure** - No WordPress vulnerabilities
✅ **SEO optimized** - Clean, semantic HTML

## What You Can Edit in the CMS

Once deployed, you can edit all of these through the admin panel at `yoursite.com/admin`:

- **Hero Section** - Headline, subheadline, CTA buttons, background image
- **Featured Solutions** - Add/edit/delete solution cards
- **Case Studies** - Add/edit/delete case studies for the carousel
- **Insights/Blog Posts** - Create and publish articles
- **Statistics** - Update the stats section numbers
- **Footer** - Edit footer links and social media
- **Navigation** - Change menu items

## How to Deploy (Option 1: Netlify - Recommended)

### Step 1: Push to GitHub

1. Go to https://github.com and create a new repository called "alltra-website"
2. In your terminal, run:
   ```bash
   cd "/Users/davidwright/Desktop/Alltra/Alltra Website"
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/alltra-website.git
   git push -u origin main
   ```

### Step 2: Deploy to Netlify

1. Go to https://netlify.com and sign up (free)
2. Click "Add new site" → "Import an existing project"
3. Choose "GitHub" and select your `alltra-website` repository
4. Build settings (leave as default):
   - Build command: (leave empty)
   - Publish directory: /
5. Click "Deploy site"

### Step 3: Enable Netlify CMS

1. In Netlify dashboard, go to "Site settings" → "Identity"
2. Click "Enable Identity"
3. Under "Registration preferences", select "Invite only"
4. Under "Services" → "Git Gateway", click "Enable Git Gateway"
5. Go to "Identity" tab and click "Invite users"
6. Enter your email address

### Step 4: Access Your CMS

1. Check your email for the invitation
2. Click the link and set your password
3. Go to `your-site-name.netlify.app/admin`
4. Login with your credentials
5. Start editing!

## How to Deploy (Option 2: Traditional Hosting)

For traditional hosting (Bluehost, HostGator, etc.):

1. Upload all files via FTP to your hosting's `public_html` folder
2. For the CMS to work, you'll need to use Netlify or set up a custom backend

**Note:** Netlify is recommended because it's free and has built-in CMS support.

## Local Development (Optional)

To test the CMS locally:

1. Install Netlify CLI:
   ```bash
   npm install -g netlify-cli
   ```

2. Run the dev server:
   ```bash
   cd "/Users/davidwright/Desktop/Alltra/Alltra Website"
   netlify dev
   ```

3. Access the CMS at `http://localhost:8888/admin`

## File Structure

```
alltra-website/
├── admin/                  # Netlify CMS admin interface
│   ├── config.yml         # CMS configuration
│   └── index.html         # Admin login page
├── content/               # Editable content (managed by CMS)
│   ├── case-studies/     # Case study markdown files
│   ├── insights/         # Blog posts/articles
│   ├── solutions/        # Solution cards
│   ├── settings/         # Site settings
│   ├── hero.json         # Hero section content
│   ├── stats.json        # Statistics section
│   └── footer.json       # Footer content
├── images/
│   └── uploads/          # Images uploaded through CMS
├── index.html            # Main website file
├── styles.css            # All styles
├── script.js             # JavaScript functionality
└── logo.png              # Your logo

```

## Editing Content

### Option 1: Through the CMS (Easy)
1. Go to `yoursite.com/admin`
2. Login
3. Click on the section you want to edit
4. Make changes
5. Click "Publish"

### Option 2: Manually Edit Files (Advanced)
You can also edit the files in the `content/` folder directly:
- Hero: `content/hero.json`
- Stats: `content/stats.json`
- Solutions: `content/solutions/*.md`
- Case Studies: `content/case-studies/*.md`
- Insights: `content/insights/*.md`

## Support

If you need help:
1. Check Netlify documentation: https://docs.netlify.com
2. Netlify CMS docs: https://www.netlifycms.org/docs/
3. Contact me for custom development needs

## Cost Breakdown

- **Hosting on Netlify**: FREE (up to 100GB bandwidth)
- **Domain name**: ~$12/year (optional, Netlify provides free subdomain)
- **SSL Certificate**: FREE (included with Netlify)
- **CMS**: FREE (Netlify CMS is open source)
- **Total**: $0-12/year

Compare to WordPress:
- Hosting: $10-50/month
- Premium theme: $60
- Plugins: $50-200/year
- Total: $180-800/year

## Next Steps

After deployment, you might want to:
- [ ] Add a custom domain
- [ ] Set up contact form (use Netlify Forms - free)
- [ ] Add Google Analytics
- [ ] Configure SEO meta tags
- [ ] Set up email notifications for form submissions

## Future Enhancements (Let me know if you want these)

- Contact form with email notifications
- Blog with pagination
- Search functionality
- Newsletter signup integration
- A/B testing capabilities
- Advanced analytics dashboard
