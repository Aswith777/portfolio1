# CH. ASWITH — Personal Portfolio Website

[![Deployment](https://img.shields.io/badge/deployment-Vercel%20Ready-black?style=flat-square&logo=vercel)](https://vercel.com)
[![Status](https://img.shields.io/badge/status-Active%20Undergraduate-00f2fe?style=flat-square)](https://github.com)
[![Specialization](https://img.shields.io/badge/degree-B.Tech%20CIC%202027-10b981?style=flat-square)](https://mvgrce.com)

A modern, responsive, high-performance developer portfolio for **Chinthapalli Aswith (CH. ASWITH)**, a B.Tech student specializing in Computer and Information/Communication-related technologies (CIC) at MVGR College of Engineering (graduating in 2027).

Designed with a dark developer aesthetic, subtle gradients, glassmorphism cards, and an interactive presentation of full-stack skills, academic progress, and project work.

---

## 📁 Project Architecture

```
aswith-portfolio/
├── index.html                   # Semantic, accessible HTML5 entry point
├── favicon.svg                  # Dark-mode glowing developer favicon
├── vercel.json                  # Vercel deployment configuration & security headers
├── .gitignore                   # Standard Git ignore for frontend & backend
├── README.md                    # Complete documentation
├── start-preview.ps1            # 1-click local preview server script (PowerShell .NET)
│
├── css/
│   ├── variables.css            # Color tokens, glassmorphism, dark palette, spacing
│   ├── base.css                 # Reset, typography, accessibility, reduced-motion
│   ├── components.css           # Buttons, cards, badges, navbar, forms, modals, toasts
│   └── sections.css             # Section-specific layouts, responsive grids, hero terminal
│
├── js/
│   ├── config.js                # Centralized data store (links, contact, placeholders)
│   ├── main.js                  # App initialization, scroll reveal, dark tech particle effect
│   └── modules/
│       ├── icons.js             # Crisp inline SVG icons library
│       ├── navbar.js            # Sticky navigation, mobile menu, scroll spy
│       ├── skills.js            # Interactive category filtering, animated skill cards
│       ├── contact.js           # Form validation, copy-to-clipboard, feedback
│       └── modal.js             # Resume & project details dialogs
│
├── assets/
│   └── resume/                  # Dedicated folder for resume PDF
│       └── README.md            # Resume guide & instructions
│
├── api/                         # Vercel Serverless Function (optional serverless backend)
│   └── contact.js               # Secure serverless contact form handler with validation
│
└── backend/                     # Spring Boot Backend Project (Full-Stack Architecture)
    ├── pom.xml                  # Maven configuration with Spring Web, Validation, Lombok
    ├── .env.example             # Environment variable template
    └── src/
        └── main/
            ├── java/com/aswith/portfolio/
            │   ├── Application.java
            │   ├── controller/ContactController.java
            │   ├── service/ContactService.java
            │   ├── repository/ContactMessageRepository.java
            │   ├── model/ContactMessage.java
            │   └── dto/
            │       ├── ContactRequestDto.java
            │       └── ApiResponseDto.java
            └── resources/
                └── application.yml
```

---

## ⚡ Quick Start: Running Locally

### Option 1: One-Click Local Server (Recommended on Windows)
No Node.js, Python, or external packages required! Simply run the included PowerShell preview script:

1. Right-click `start-preview.ps1` and select **Run with PowerShell**  
   *(or run `./start-preview.ps1` inside PowerShell)*.
2. It will automatically start a local server at `http://localhost:3000` and open your default browser.

### Option 2: Open Directly in Browser
You can open `index.html` directly in Google Chrome, Microsoft Edge, or Firefox.  
*(Note: To use modern ES modules, running via Option 1 or any local server is recommended).*

---

## 🛠️ Personalization & Easy Editing (`js/config.js`)

All personal details, URLs, and project links are centralized in [`js/config.js`](file:///C:/Users/chmun/.gemini/antigravity/scratch/aswith-portfolio/js/config.js). You do **not** need to manually search through HTML files to update your details!

### 1. Adding your GitHub & LinkedIn Profile Links
In `js/config.js`, update the `social` object:
```javascript
social: {
  github: {
    url: "https://github.com/your-username", // Add your URL
    isPlaceholder: false
  },
  linkedin: {
    url: "https://linkedin.com/in/your-username", // Add your URL
    isPlaceholder: false
  }
}
```

### 2. Adding Your Resume PDF
1. Save your resume document as `Chinthapalli_Aswith_Resume.pdf` in `assets/resume/`.
2. In `js/config.js`, set:
```javascript
resume: {
  fileName: "Chinthapalli_Aswith_Resume.pdf",
  filePath: "assets/resume/Chinthapalli_Aswith_Resume.pdf",
  isAvailable: true, // change from false to true
}
```

### 3. Adding New Projects
Under `projects` in `js/config.js`:
```javascript
projects: [
  {
    id: "raise-your-voice",
    title: "Raise Your Voice — Digital Complaint Box",
    category: "Digital Complaint Management / Full-Stack Project",
    description: "...",
    tags: ["Full-Stack", "Digital Complaint Box", "Web Development", "Database"],
    demoUrl: "https://...",
    githubUrl: "https://github.com/...",
    isDemoAvailable: true,
    isGithubAvailable: true
  }
]
```

---

## 🚀 Deployment Guide

### Deploying to Vercel (Frontend & Serverless API)
1. Push your repository to GitHub.
2. Log in to [Vercel](https://vercel.com) and click **"Add New Project"**.
3. Select your `aswith-portfolio` repository.
4. Click **Deploy**. Vercel will automatically serve your static assets and route `/api/contact` to the serverless function in `api/contact.js`.

---

## ☕ Running the Spring Boot Backend (`backend/`)

For full-stack Java/Spring Boot development:

### Prerequisites:
- Java JDK 17 or higher
- Apache Maven 3.8+ (or your IDE's built-in Maven)

### Running the API:
```bash
cd backend
mvn clean spring-boot:run
```
The REST API will start at `http://localhost:8080` with endpoints:
- `GET  /api/health` — Service health check
- `POST /api/contact` — Validated contact message submission and database persistence

---

## ♿ Accessibility & Standards Compliance
- **WCAG 2.1 AA Compliant**: High contrast typography, clear focus states, semantic HTML landmarks (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- **Reduced-Motion Support**: Respects users with vestibular motion sensitivity via `@media (prefers-reduced-motion: reduce)`.
- **Keyboard Navigation**: Full skip link and accessible modal trapping.
- **Zero Fabricated Content**: Accurately reflects your genuine academic record, certifications, and technical proficiencies.

---

## 📄 License & Ownership
© 2026 **CH. ASWITH**. All rights reserved.
