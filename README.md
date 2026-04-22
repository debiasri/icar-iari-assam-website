# ICAR-IARI Assam — Official Website
### GitHub Pages + Decap CMS · Completely Free · No Credit Card · Never Goes Down

## GOOD NEWS — No OAuth Server Needed!
The CMS now uses GitHub PKCE login — colleagues log in directly with GitHub.
No Render, no Heroku, no credit card. Just GitHub (free).

---

## PART A — ONE-TIME SETUP (~15 minutes)

### Step 1 — Create GitHub accounts
Every person who will update the website needs a free GitHub account.
Go to github.com → Sign up → use ICAR email. Repeat for each colleague.

### Step 2 — Create the repository (admin does this once)
1. GitHub → click + → New repository
2. Name: icar-iari-assam-website
3. Visibility: PUBLIC (required for free GitHub Pages)
4. Click Create repository

### Step 3 — Upload website files
1. Unzip icar-iari-assam-ghpages.zip
2. On GitHub repo page → click "uploading an existing file"
3. Drag everything from the unzipped folder into the browser
4. Type commit message: "First upload" → Commit changes
NOTE: Make sure the .github folder is included in the upload.

### Step 4 — Edit ONE line in config.yml
1. In repo: go to public → admin → config.yml → click pencil icon (Edit)
2. Find: repo: YOUR-GITHUB-USERNAME/icar-iari-assam-website
3. Replace YOUR-GITHUB-USERNAME with your actual GitHub username
4. Commit changes

### Step 5 — Enable GitHub Pages
1. Repo → Settings → Pages
2. Source → select "GitHub Actions"
3. Save
4. Wait 2-3 minutes → your site is live at:
   https://YOUR-USERNAME.github.io/icar-iari-assam-website/

### Step 6 — Create GitHub OAuth App (for Admin Panel login)
1. GitHub → profile picture → Settings → Developer settings → OAuth Apps → New OAuth App
2. Fill in:
   - Application name: ICAR-IARI Assam CMS
   - Homepage URL: https://YOUR-USERNAME.github.io/icar-iari-assam-website
   - Authorization callback URL: https://YOUR-USERNAME.github.io/icar-iari-assam-website/admin/
     (trailing slash is important)
3. Click Register application
4. Copy the Client ID shown
5. Click "Generate a new client secret" → copy the secret

6. Go back to public/admin/config.yml (pencil icon to edit)
7. Change: app_id: icar-iari-assam
   To:     app_id: YOUR-CLIENT-ID  (paste the Client ID)
8. Commit changes

### Step 7 — Give colleagues access
Repo → Settings → Collaborators → Add people → search their GitHub username → Add collaborator
They accept the email invitation → they can now log into Admin Panel.

---

## PART B — UPDATING THE WEBSITE (for all colleagues)

Admin Panel URL: https://YOUR-USERNAME.github.io/icar-iari-assam-website/admin/
Click "Login with GitHub" → approve → start editing.

Add News:       Left sidebar → Home Page → News & Highlights → Add news → Save → Publish
Add Notice:     Notice Board → New → fill in → Save → Publish
Add Team Member:Scientists & Staff → New → fill in + upload photo → Save → Publish
Add Publication:Publications → New → fill in → Save → Publish
Upload Photo:   Photo Gallery → New → upload → Save → Publish
Update Contact: Site Settings → edit → Save → Publish

Changes appear on the live website within 2 minutes of publishing.

---

## CUSTOM DOMAIN

For any domain, add these DNS records at your registrar:
  A record: @ → 185.199.108.153
  A record: @ → 185.199.109.153
  A record: @ → 185.199.110.153
  A record: @ → 185.199.111.153
  CNAME:    www → YOUR-USERNAME.github.io

For gov.in domain: send the 4 IP addresses above to NIC helpdesk.
Then: GitHub repo → Settings → Pages → Custom domain → enter your domain → Enforce HTTPS.

---

## TROUBLESHOOTING

Admin login fails        → Check OAuth App callback URL ends with /admin/ (trailing slash required)
Website not loading      → Settings → Pages → Source must be "GitHub Actions"
Changes not visible      → Wait 2-3 min, then Ctrl+Shift+R (hard refresh)
Photo not uploading      → Rename file with no spaces or special characters
Want to remove a member  → Admin → Scientists & Staff → click person → Delete

---

## TOTAL COST: Rs. 0 per month (GitHub is free, OAuth App is free, hosting is free)

ICAR-IARI Assam · Design by AKMU · 2025
