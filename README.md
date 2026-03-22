# Muhammed Razi — Portfolio Website
## Deploy Guide (Netlify + Decap CMS)

---

### STEP 1 — Push to GitHub

1. Go to https://github.com/new
2. Create a repo called: `my-portfolio` (set to Public)
3. Upload ALL these files keeping the folder structure:
   ```
   index.html
   netlify.toml
   admin/
     index.html
     config.yml
   posts/
     2026-03-22-iec-60079-basics.md
     2026-03-20-ncr-management-guide.md
   ```

---

### STEP 2 — Deploy on Netlify (Free)

1. Go to https://netlify.com → Sign up (use your GitHub account)
2. Click **"Add new site" → "Import an existing project"**
3. Choose **GitHub** → select your `my-portfolio` repo
4. Build settings: leave everything blank (no build command needed)
5. Click **Deploy site** — it goes live in ~30 seconds!
6. Your site URL will be something like `https://random-name.netlify.app`
   - You can rename it in: Site Settings → Domain Management → Custom subdomain

---

### STEP 3 — Enable Netlify Identity (for CMS login)

1. In Netlify dashboard → go to **Site Settings → Identity**
2. Click **"Enable Identity"**
3. Scroll down to **"Git Gateway"** → click **"Enable Git Gateway"**
4. Go to **Identity tab** at the top → click **"Invite users"**
5. Enter YOUR email address → you'll get an invite link

---

### STEP 4 — Log into your CMS Admin Panel

1. Visit: `https://your-site.netlify.app/admin`
2. Accept the invite from your email
3. Set your password
4. You're in! You'll see the Decap CMS panel.

---

### STEP 5 — Write Your First Article

1. In the admin panel, click **"Articles & Insights"**
2. Click **"New Articles & Insights"**
3. Fill in:
   - **Title** — name of your article
   - **Category** — Study Notes / Tips / Project Experience
   - **Summary** — one line shown on the card
   - **Body** — write in the rich text editor (like Word!)
   - **Tags** — keywords like "IEC 60079", "NCR", etc.
4. Click **"Publish"** → it automatically creates a markdown file in `/posts`
   and your site updates within seconds!

---

### Adding New Articles Later

Just repeat Step 5 — go to `/admin`, click New, write, publish.
No coding. No touching any files. Done!

---

### Optional: Custom Domain

If you have a domain (e.g. muhammedrazi.com):
- Netlify → Site Settings → Domain Management → Add custom domain
- Netlify gives you free HTTPS automatically.

---

### File Structure Explained

```
index.html          ← Your main portfolio website
netlify.toml        ← Tells Netlify how to serve the site
admin/
  index.html        ← The CMS admin login page
  config.yml        ← Defines your article fields & categories
posts/
  *.md              ← Your articles (auto-created by CMS when you publish)
assets/
  images/           ← Images you upload via CMS go here
```
