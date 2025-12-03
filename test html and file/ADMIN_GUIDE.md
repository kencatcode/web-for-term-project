# 📝 Matcha Lala Admin Guide - Content Management

## 🎯 Overview
This guide explains how to add new articles, manage images, and update content on your Matcha Lala website.

---

## 📸 Adding Pictures/Banners to Articles

### Option 1: Simple File Management (Current Setup)
**Best for: Small websites, occasional updates**

#### Steps to add images:
1. **Upload images** to the `images/` folder:
   ```
   matcha-website/
   ├── images/
   │   ├── articles/          ← Create this folder
   │   │   ├── story-banner.jpg
   │   │   ├── matcha-guide.jpg
   │   │   └── health-tips.jpg
   │   ├── logo.png
   │   └── hero-logo.png
   ```

2. **Update article HTML** in `article.html`:
   ```html
   <!-- Change this line -->
   <img src="./images/hero-logo.png" alt="Article Banner">
   
   <!-- To your new image -->
   <img src="./images/articles/story-banner.jpg" alt="Matcha Story">
   ```

3. **Image requirements**:
   - Format: JPG, PNG, WebP
   - Size: 1200x400px (3:1 ratio) for banners
   - File size: Under 500KB for fast loading

### Option 2: Advanced Content Management
**Best for: Frequent updates, multiple admins**

#### A. Use a Simple CMS (Recommended)
- **Forestry.io** (Free): Connects to your files, easy drag-drop images
- **NetlifyCMS**: Free, works with static sites
- **Strapi**: Self-hosted, more features

#### B. JSON-based Content Management
Create a `content.json` file to manage articles:
```json
{
  "articles": [
    {
      "id": 1,
      "title": "ที่มาที่ไปของมัทฉะลาล่า 🍵",
      "banner": "./images/articles/story-banner.jpg",
      "date": "2025-11-06",
      "category": "Our Story",
      "preview": "มัทฉะลาล่าเกิดขึ้นในปี 2024...",
      "content": "Full article content here...",
      "featured": true
    }
  ]
}
```

---

## 📝 Adding New Articles

### Method 1: Direct HTML Editing

1. **Duplicate existing article structure** in `article.html`
2. **Update content**:
   ```html
   <article class="card border-0 shadow-sm h-100">
     <div class="position-relative overflow-hidden" style="height: 250px;">
       <img src="./images/articles/new-article-banner.jpg" 
            alt="New Article" 
            class="w-100 h-100" 
            style="object-fit: cover; filter: brightness(0.7);">
     </div>
     
     <div class="card-body p-4">
       <h2 class="h4 fw-bold mb-2">Your New Article Title</h2>
       <!-- Rest of article content -->
     </div>
   </article>
   ```

### Method 2: Template System (Advanced)

Create reusable article templates:

1. **Create article template** (`templates/article-template.html`):
   ```html
   <article class="card border-0 shadow-sm h-100" data-article-id="{{id}}">
     <div class="position-relative overflow-hidden" style="height: 250px;">
       <img src="{{banner}}" alt="{{title}}" class="w-100 h-100" 
            style="object-fit: cover; filter: brightness(0.7);">
     </div>
     <div class="card-body p-4">
       <h2 class="h4 fw-bold mb-2">{{title}}</h2>
       <div class="text-muted small">{{date}} • {{readTime}}</div>
       <div class="article-preview">{{preview}}</div>
       <div class="article-full d-none">{{content}}</div>
     </div>
   </article>
   ```

2. **Use JavaScript** to populate templates from JSON data

---

## 🛠️ Technical Recommendations

### For Small Business (Your Current Situation):
✅ **Keep it simple** - Direct file editing
✅ **Use cloud storage** - Google Drive, Dropbox for image backup
✅ **Image optimization** - Use online tools like TinyPNG
✅ **Version control** - Keep backup of your files

### For Growth/Multiple Admins:
📈 **Headless CMS** - Strapi, Forestry, or Contentful
📈 **Build process** - Use tools like 11ty or Jekyll
📈 **Image CDN** - Cloudinary or ImageKit for automatic optimization
📈 **Git workflow** - Version control for team collaboration

---

## 📋 Content Management Workflow

### Current Simple Workflow:
1. **Write content** in text editor
2. **Prepare images** (resize, optimize)
3. **Upload images** to `images/articles/` folder
4. **Edit HTML** in `article.html`
5. **Test locally** before publishing
6. **Upload to web server**

### Recommended Improved Workflow:
1. **Content planning** - Use Notion or Trello
2. **Draft articles** - Write in Markdown
3. **Image preparation** - Batch resize with tools
4. **Use CMS** - Add content through admin interface
5. **Preview & publish** - Automatic deployment

---

## 🎨 Design Guidelines

### Article Banner Images:
- **Dimensions**: 1200x400px (3:1 ratio)
- **Style**: Bright, food-focused, matches matcha theme
- **Text overlay**: Ensure good contrast
- **File naming**: `article-slug-banner.jpg`

### Content Images:
- **Max width**: 800px
- **Format**: WebP preferred, JPG fallback
- **Alt text**: Always include for accessibility
- **Compression**: 80% quality for web

### Brand Colors (for image editing):
- **Matcha Green**: #4a7c59
- **Light Green**: #8fbc8f
- **Background**: #f8f9fa
- **Text**: #333333

---

## 🚀 Next Steps

### Phase 1 (Immediate):
- [ ] Create `images/articles/` folder
- [ ] Optimize existing images
- [ ] Create 2-3 placeholder articles

### Phase 2 (1-2 months):
- [ ] Implement simple JSON content system
- [ ] Add image upload form
- [ ] Create admin login area

### Phase 3 (Future):
- [ ] Full CMS integration
- [ ] Automatic image optimization
- [ ] SEO enhancements
- [ ] Analytics integration

---

## 📞 Support

For technical help:
- **HTML/CSS editing**: Use VS Code with Live Server extension
- **Image editing**: Canva, GIMP, or online tools
- **File management**: FileZilla for FTP uploads
- **Backup**: Google Drive or GitHub for version control

**Remember**: Always backup your files before making changes! 🔒