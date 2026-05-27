# Sosa's 64bit Fix

A modular computer repair business website — statically hosted on GitHub Pages.

**Site:** https://alsosram.github.io/sosa-64bit-fix/

## Features

- **Repairs Showcase** — Post repairs with full details: issue, diagnosis, process, parts used, and customer reviews
- **Device Asset Tracking** — Register devices with serial numbers, customer info, specs, and more
- **Customer Reviews** — Customers can submit reviews using their device serial number as verification
- **Admin Panel** — Full CRUD for repairs, devices, reviews, and site content
- **GitHub-based Storage** — All data stored as JSON files in the repo via GitHub API
- **Modular Design** — Update content through the admin panel without touching code

## Setup

### 1. Fork / Clone this repo

```bash
git clone https://github.com/YOUR_USERNAME/sosa-64bit-fix.git
```

### 2. Enable GitHub Pages

Go to **Settings > Pages** and set the source to `main` branch, root folder.

### 3. Create a GitHub Token

Go to [GitHub Tokens](https://github.com/settings/tokens) and create a classic token with `repo` scope.

### 4. Access Admin Panel

Navigate to `https://YOUR_USERNAME.github.io/sosa-64bit-fix/admin.html`

- **Default Password:** `admin123`
- **Repo Owner:** Your GitHub username
- **Repo Name:** `sosa-64bit-fix`
- **GitHub Token:** The token you created

### 5. Change the Default Password

Go to **Account** tab in the admin panel and change the password immediately.

## Admin Sections

### Repair
- Add/Edit/Delete repair entries
- Each repair includes: title, device type/model, issue, diagnosis process, parts used, status, and optional customer review

### Devices (Asset Tracking)
- Register devices with serial numbers
- Store customer name, device type, brand, model, year, and specs/notes
- Serial numbers are used to verify customer reviews

### Reviews
- Customer-submitted reviews appear as "Pending"
- Reviews must contain a valid serial number from the Devices list to be accepted
- Approve or reject reviews from the admin panel

### Settings
- Edit all site content (hero, services, about, contact, footer)

### Account
- Change password
- Enable/disable MFA with authenticator app

## File Structure

```
├── index.html           # Main website
├── admin.html           # Admin panel
├── site-config.json     # Site content configuration
├── admin-config.json    # Admin authentication config
├── css/
│   ├── style.css        # Main site styles
│   └── admin.css        # Admin panel styles
├── js/
│   ├── main.js          # Public site JavaScript
│   └── admin.js         # Admin panel JavaScript
├── repairs/
│   ├── repairs.json     # Repairs index (metadata)
│   ├── example-repair.json   # Example repair entry
│   └── example-repair-2.json
├── devices/
│   └── devices.json     # Device asset database
└── reviews/
    └── reviews.json     # Customer reviews
```
