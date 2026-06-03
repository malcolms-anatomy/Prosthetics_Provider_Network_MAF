# 📌 Prosthetics Provider Network Directory (MAF)

## 🏥 Overview

The Prosthetics Provider Network Directory is a structured database system built for the Malcolm's Anatomy Foundation (MAF) to catalogue verified prosthetic providers across Africa and partner regions.

The system is designed to:

- Maintain a centralized provider database
- Standardize service classification
- Enable public filtering and search via the website
- Support scalability for future expansion and campaigns

The directory is powered by:

- GitHub (data storage)
- JSON files (structured database)
- Sitejet (frontend website interface)
- JavaScript (filtering and rendering logic)

---

## 📁 Repository Structure

```
Prosthetics_Provider_Network_MAF/
│
├── providers.json
├── service-taxonomy.json
└── README.md
```

---

## 📊 Data Files Explanation

### 1. providers.json (Main Database)

This file contains all prosthetic providers.

Each entry includes:

- `provider_name`
- `country`
- `region`
- `provider_type`
- `services_offered`
- `contact_person`
- `phone_number`
- `email`
- `website`
- `physical_address`
- `social_media`

#### ⚠️ Important Rules

- `services_offered` MUST be an array
- Services must match values in `service-taxonomy.json`
- Do NOT create new service names without approval from Tech Lead
- Keep naming consistent and clean

### 2. service-taxonomy.json (Controlled Service List)

This file defines all allowed services in the system.

It is used to:

- Populate the service filter dropdown
- Standardize provider service entries
- Prevent inconsistent or duplicate service naming

**Example services:**

- Lower Limb Prosthetics
- Upper Limb Prosthetics
- Prosthetic Fitting
- Rehabilitation Therapy

#### ⚠️ Rules

- Only services in this file can be used in `providers.json`
- Any new service must be reviewed before being added

---

## 🌐 Website Integration (Sitejet)

The website:

- Fetches `providers.json` directly from GitHub (raw link)
- Fetches `service-taxonomy.json` for filter generation
- Uses JavaScript to:
  - Render provider cards
  - Apply filters (country, type, service, search)
  - Display results dynamically

---

## 🔍 Filtering System

The directory supports:

### Filters

- Country
- Provider Type
- Services (controlled list)
- Search (provider name + services)

### Behavior

- Users select filters
- Click "Search"
- Matching providers are displayed dynamically

---

## 🔄 Update Workflow

### Adding a new provider

1. Open `providers.json`
2. Add a new provider object
3. Ensure:
   - Service names match `service-taxonomy.json`
   - Structure is correct
4. Commit changes to GitHub

### Updating services

1. Edit `service-taxonomy.json`
2. Add or remove services (only if approved)
3. Commit changes
4. Website updates automatically

---

## 👥 Team Roles

### Tech Team

- Maintains GitHub repository
- Ensures data structure consistency
- Updates frontend integration if needed

### Prosthetic Provider Network Team

- Sources and verifies providers
- Updates provider records in GitHub
- Ensures accuracy of service classification

---

## ⚠️ Data Governance Rules

- No duplicate provider entries
- No free-text service variations
- All updates must be committed with clear messages
- Maintain consistency across country names
- Use official spelling of organizations

---

## 🚀 System Design Philosophy

This system is designed as a lightweight, scalable, no-backend directory system.

Instead of a traditional database:

- GitHub acts as the database
- JSON acts as structured data storage
- JavaScript acts as the query engine
- Sitejet acts as the UI layer

---

## 📈 Future Improvements (Roadmap)

Planned upgrades include:

- Featured providers system
- Pagination for large datasets
- Provider detail modal pages
- Admin upload interface (Power Apps / backend system)
- Integration with Google Ads landing pages
- Multi-language support

---

## 📬 Contact / Ownership

**Managed by:**
- Malcolms Anatomy Foundation (MAF)
- Technology & Digital Systems Department
