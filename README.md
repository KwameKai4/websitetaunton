# Taunton Somerset Local Business Directory

A modern, SEO-optimized business directory for Taunton, Somerset built with Astro.js and Tailwind CSS.

## 🚀 Features

- **SEO Optimized**: Comprehensive meta tags, structured data (JSON-LD), sitemap, and robots.txt
- **Mobile Responsive**: Fully responsive design that works on all devices
- **Easy to Manage**: Simple JSON file for adding/editing business listings
- **Fast Performance**: Static site generation with Astro for lightning-fast load times
- **Category Organization**: Businesses organized by service categories
- **Featured Listings**: Highlight premium businesses with featured badges
- **Local SEO**: Geo-targeting meta tags and LocalBusiness schema markup

## 📋 How to Add a New Business Listing

1. Open `src/data/businesses.json`
2. Add a new entry to the `businesses` array following this template:

```json
{
  "id": 9,
  "name": "Business Name Here",
  "category": "Category Name",
  "description": "Brief description of the business and services offered.",
  "phone": "01823 555009",
  "email": "contact@business.co.uk",
  "address": "Street Address, Taunton TA1 XXX",
  "website": "https://business.co.uk",
  "featured": false
}
```

3. Save the file
4. Rebuild the site with `npm run build`

### Field Descriptions:

- **id**: Unique number for each business (increment from the last ID)
- **name**: Business name
- **category**: Must match existing categories or create a new one (Plumbers, Cleaners, Electricians, Builders, Gardeners, Painters & Decorators)
- **description**: Brief description of services (1-2 sentences)
- **phone**: Contact phone number
- **email**: Contact email address
- **address**: Full address including postcode
- **website**: Full website URL (optional - use empty string "" if none)
- **featured**: Set to `true` for featured listings, `false` for standard listings

## 🛠️ Development Commands

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Project Structure

```
/
├── public/
│   ├── favicon.svg         # Site icon
│   └── robots.txt          # Search engine instructions
├── src/
│   ├── components/
│   │   ├── Hero.astro              # Header section
│   │   ├── BusinessCard.astro      # Individual business display
│   │   ├── CategorySection.astro   # Category grouping
│   │   └── Footer.astro            # Footer section
│   ├── data/
│   │   └── businesses.json         # ** EDIT THIS TO ADD BUSINESSES **
│   ├── layouts/
│   │   └── Layout.astro            # Main layout with SEO
│   ├── pages/
│   │   └── index.astro             # Homepage
│   └── styles/
│       └── global.css              # Tailwind CSS
└── astro.config.mjs        # Astro configuration
```

## 🎨 Adding New Categories

To add a new service category:

1. Simply add a business with a new category name in `businesses.json`
2. The category will automatically appear in the navigation and get its own section
3. Update the footer links in `src/components/Footer.astro` if desired

## 🔍 SEO Features

- **Meta Tags**: Title, description, keywords, author
- **Open Graph**: Social media sharing optimization
- **Structured Data**: LocalBusiness schema for each listing
- **Sitemap**: Auto-generated XML sitemap
- **Robots.txt**: Search engine crawling instructions
- **Geo Tags**: Location-specific meta tags for local SEO
- **Fast Loading**: Static HTML generation, minimal JavaScript

## 📱 Mobile Optimization

- Responsive grid layouts
- Touch-friendly click-to-call and click-to-email
- Mobile-optimized navigation
- Fast loading on all devices

## 🌐 Deployment

The site generates static HTML files. Deploy the `dist/` folder to any static hosting service:

- Netlify
- Vercel
- GitHub Pages
- Cloudflare Pages
- Any web server

## 📝 License

Built for TauntonSomerset.co.uk

## 🤝 Support

For questions or assistance, contact: info@tauntonsomerset.co.uk
