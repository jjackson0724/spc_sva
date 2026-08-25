# SVA SPC Website Setup Instructions

Everything editable through the CMS — no code required after initial setup.

---

## Step 1 — Connect to GitHub first

The CMS needs a GitHub repo to save changes.

1. Go to github.com and create a free account (or use existing)
2. Create a new repository named: sva-spc
3. Upload all files from this folder to that repo
4. Make sure the repo is Public

---

## Step 2 — Deploy to Netlify

1. Go to netlify.com and create a free account
2. Click "Add new site" > "Import an existing project"
3. Connect your GitHub account
4. Select the sva-spc repository
5. Click Deploy
6. When asked for a site name type: spcsva
7. Site goes live at spcsva.netlify.app

---

## Step 3 — Enable the CMS Editor

1. In Netlify dashboard go to: Site Settings > Identity
2. Click "Enable Identity"
3. Under Registration: set to "Invite Only"
4. Under Services: click "Enable Git Gateway"
5. Go to: Site Settings > Identity > Invite Users
6. Invite yourself (your email)
7. Check your email and accept the invite
8. Now go to: spcsva.netlify.app/admin
9. Log in — you are now in the CMS editor

---

## What You Can Edit Without Code

### Alert Banner
- Go to admin > Site Settings > Alerts & Integrations
- Toggle alert on or off
- Change alert text
- Change alert link URL and link text
- Save — updates live immediately

### Leadership Names & Photos
- Go to admin > Officers & Advisors
- Click on any officer
- Change their name
- Upload their photo (headshot)
- Save — updates live immediately

### Google Calendar
- Create a Google Calendar named "SVA SPC Chapter Events"
- Settings > Share > Make available to public
- Settings > Integrate Calendar > copy the Embed Code (the iframe src line)
- In admin > Site Settings > paste the embed code in "Google Calendar Embed Code"
- Save — calendar appears on the site

### Google Photos Gallery Link
- Create a Google Photos album
- Share it publicly
- Copy the share URL
- In admin > Site Settings > paste in "Google Photos Album URL"
- Save — the View Photo Album button now links to your album

### Photo Gallery (upload individual photos)
- Go to admin > Photo Gallery
- Click "New Photo"
- Upload a photo, add a caption and date
- Save — photo appears on the site

---

## Step 4 — Connect the Contact Form

1. Go to formspree.io and create a free account
2. Create a new form
3. Set the notification email to: veteranservices@spcollege.edu
4. Copy your Form ID (looks like: xpzgkjvw)
5. Open index.html, find YOUR_FORM_ID, replace with your actual ID
6. Commit the change to GitHub — Netlify auto-deploys

---

## Updating Officer Names When Leadership Changes

1. Go to spcsva.netlify.app/admin
2. Click Officers & Advisors
3. Find the officer whose name changed
4. Update their name and photo
5. Save
6. Done — no code, no files, no uploads needed

---

## Files Overview

- index.html            Main website (reads from _data/ files dynamically)
- _data/settings.json   Alert, calendar, photos URL (editable via CMS)
- _data/officers.json   Leadership roster (editable via CMS)
- admin/index.html      CMS login page
- admin/config.yml      CMS field configuration
- photos/               Upload photos here or via CMS
- netlify.toml          Netlify build settings
