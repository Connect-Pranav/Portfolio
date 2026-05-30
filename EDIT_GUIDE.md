# 🛠️ Pranav Portfolio — Full Editing Guide
**Portfolio Builder Skill · Maintained by Claude**

---

## 🚀 How to Host on GitHub Pages (Free)

### Step 1 — Create GitHub Account
1. Go to https://github.com and sign up (free)
2. Verify your email

### Step 2 — Create a New Repository
1. Click the **"+"** icon → **New repository**
2. Repository name: `pranav-portfolio` (or anything you like)
3. Set to **Public**
4. Check ✅ **Add a README file**
5. Click **Create repository**

### Step 3 — Upload Your Files
1. Open your new repository
2. Click **Add file** → **Upload files**
3. Drag and drop `index.html` from this folder
4. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to repository **Settings** (top menu)
2. Click **Pages** in the left sidebar
3. Under **Source** → select **Deploy from a branch**
4. Branch: **main** → Folder: **/ (root)**
5. Click **Save**
6. Wait 2–3 minutes → your site will be live at:
   **https://YOUR-USERNAME.github.io/pranav-portfolio/**

---

## ✏️ How to Edit Content

### Change Your Name / Title
Open `index.html` and search (`Ctrl+F`) for:
```
Pranav Kumar
```
Replace with your updated name anywhere it appears.

### Change Description Text
Search for:
```
9+ years building revenue systems
```
Edit that paragraph directly.

### Change Quote
Search for:
```
Revenue doesn't grow by accident
```
Replace with any quote you prefer.

### Update Contact Details
Search for `connect_pranav@outlook.com` → replace with new email
Search for `9990974701` → replace with new phone
Search for `connect-pranav` → replace with new LinkedIn username

### Change Stats (9+, 114%, ₹80L, 30+)
Search for `data-count="9"` → change the number
Search for `114%` → change the value
Search for `₹80L` → change the value
Search for `data-count="30"` → change the number

---

## 🃏 Edit Service Cards (What I Bring)

Search for `SVC_DATA` in the file. You'll find:

```javascript
const SVC_DATA = {
  pl: {
    title: 'P&L & Revenue Operations',
    stats: [...],
    what: [...bullet points...],
    cases: [...],
    tools: [...]
  },
  gtm: { ... },
  leadership: { ... },
  data: { ... }
};
```

Edit any field directly. Each card has:
- `title` — card heading
- `tag` — subtitle line
- `stats` — 4 numbers (num + lbl)
- `overview` — paragraph summary
- `what` — bullet point array
- `cases` — 2 company case cards
- `tools` — skill chips

---

## 📊 Edit Impact Cards

Search for `data-cat="indiamart"` to find IndiaMART cards.
Search for `data-cat="justdial"` for Justdial.
Search for `data-cat="magicbricks"` for Magicbricks.

Each card looks like:
```html
<div class="icard rv d1" data-cat="indiamart">
  <div class="icard-img">📊</div>
  <div class="icard-body">
    <div class="icard-tag">TAG TEXT</div>
    <div class="icard-title">TITLE</div>
    <div class="icard-desc">DESCRIPTION</div>
    <div class="icard-mets">
      <div><div class="imet-num">114%</div><div class="imet-lbl">Label</div></div>
    </div>
  </div>
</div>
```

---

## 🏆 Edit Awards

Search for `id="awards"` to find the awards section.
Each award card:
```html
<div class="aw-card rv d1">
  <div class="aw-img"><img src="..." /></div>
  <div class="aw-body">
    <div class="aw-org im">◆ IndiaMART</div>
    <div class="aw-title">AWARD NAME</div>
    <div class="aw-desc">DESCRIPTION</div>
  </div>
</div>
```

To change an award photo: replace the `src="..."` with a new image URL or base64.

---

## 📜 Edit Certifications

Search for `id="certifications"` — each cert card:
```html
<div class="cert-card rv d1">
  <div class="cert-img"><img src="..." /></div>
  <div class="cert-body">
    <div class="cert-provider linkedin">◆ LinkedIn Learning</div>
    <div class="cert-title">CERT NAME</div>
    <div class="cert-date">DATE INFO</div>
  </div>
</div>
```

---

## 🎨 Change Colors

All colors are CSS variables at the top of the `<style>` tag:
```css
:root {
  --bg: #071a2e;          /* main background */
  --green: #39e600;       /* accent color */
  --green2: #50ff00;      /* hover green */
  --text: #ffffff;        /* main text */
  --text2: #b8d0e8;       /* secondary text */
  --card: #0d1e30;        /* card background */
}
```

Change `--green` to any color (e.g. `#ff6b00` for orange) to re-theme the whole site.

---

## 🖼️ Change Hero Photo

**Option A — Use the in-page editor:**
Click **"Edit Hero Photo"** button (bottom-right of page) and upload a new image.

**Option B — Directly in HTML:**
The hero photo is embedded as a base64 image. To replace:
1. Go to https://www.base64-image.de/
2. Upload your photo
3. Copy the `data:image/png;base64,...` string
4. In `index.html`, search for `hero-photo-wrap`
5. Replace the `src="data:image/png..."` with your new base64 string

---

## 📐 Edit Layout (Edit Mode)

Click **"Edit Layout"** button on the page to:
- **Click any box** to select it
- **Drag boxes** to reorder them
- **Use sliders** to resize width, font size, padding
- **Move Up/Down** buttons to rearrange
- All changes **auto-save** in your browser

---

## 🔄 Re-generate with Claude

If you want Claude to make further changes, just share the `index.html` file and say:
> "Use the Portfolio Builder skill and update [section]"

Claude will load the file and apply your changes.

---

*Portfolio Builder Skill · Last updated: May 2026*
