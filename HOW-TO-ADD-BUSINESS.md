# Quick Guide: Adding a New Business

## Step-by-Step Instructions

### 1. Open the businesses file
- Navigate to: `src/data/businesses.json`
- Open it in any text editor

### 2. Find the last business entry
- Scroll to the bottom of the file
- Look for the last business entry (currently ID 8)

### 3. Add your new business
Copy this template and add it BEFORE the closing `]`:

```json
    ,
    {
      "id": 9,
      "name": "Your Business Name",
      "category": "Choose One: Plumbers / Cleaners / Electricians / Builders / Gardeners / Painters & Decorators",
      "description": "Write a short description of your business (1-2 sentences max)",
      "phone": "01823 555009",
      "email": "contact@yourbusiness.co.uk",
      "address": "123 Street Name, Taunton TA1 XXX",
      "website": "https://yourbusiness.co.uk",
      "featured": false
    }
```

### 4. Important Notes

- **ID Number**: Always increment by 1 from the last business
- **Comma**: Don't forget the comma at the start if it's not the first entry
- **Category**: Must match one of the existing categories exactly (case-sensitive)
- **Featured**: Set to `true` for premium/highlighted listings, `false` for standard
- **Website**: Use empty string `""` if the business has no website

### 5. Example of Adding a Business

If the last entry is ID 8, your addition should look like:

```json
    },
    {
      "id": 9,
      "name": "Quick Fix Locksmiths",
      "category": "Locksmiths",
      "description": "24/7 emergency locksmith service. Lock repairs, replacements, and security upgrades.",
      "phone": "01823 555009",
      "email": "help@quickfixlocks.co.uk",
      "address": "89 High Street, Taunton TA1 1AA",
      "website": "https://quickfixlocks.co.uk",
      "featured": false
    }
  ]
}
```

### 6. Rebuild the Site

After saving your changes:

```bash
npm run build
```

### 7. Creating a New Category

Want to add a new service category (e.g., "Locksmiths", "Taxi Services")?

1. Simply use the new category name in the `"category"` field
2. The site will automatically:
   - Create a new section for that category
   - Add it to the navigation
   - Sort it alphabetically

Example:
```json
{
  "id": 9,
  "name": "Taunton Taxis",
  "category": "Taxi Services",
  "description": "Local taxi service available 24/7...",
  ...
}
```

### Common Mistakes to Avoid

❌ **Missing comma** between entries
❌ **Duplicate ID numbers**
❌ **Category name typos** (creates separate sections)
❌ **Invalid JSON** (use a JSON validator if unsure)
❌ **Forgetting to rebuild** after changes

### Need Help?

Contact: info@tauntonsomerset.co.uk
