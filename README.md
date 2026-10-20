# 🌿 ASMS — Enterprise Healthcare Platform & Credential Engine

> **Production-grade Next.js 15 digital healthcare platform & programmatic clinical verification engine built for AYUSH Shubham Institute of Medical Sciences (Accredited Section-8 Non-Profit Medical Research Trust).**

[![Live Production](https://img.shields.io/badge/Live_Production-asms--iota.vercel.app-2E7D32?style=for-the-badge&logo=vercel&logoColor=white)](https://asms-iota.vercel.app/)
[![Case Study](https://img.shields.io/badge/Engineering-Case_Study-007ACC?style=for-the-badge&logo=github&logoColor=white)](#-system-architecture)
[![Next.js 15](https://img.shields.io/badge/Next.js_15-black?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript_5+-007ACC?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Vercel Edge](https://img.shields.io/badge/Vercel-Edge_Network-black?style=flat-square&logo=vercel&logoColor=white)](https://vercel.com/)
[![Section-8 Trust](https://img.shields.io/badge/Section--8_Trust-Govt_Accredited-2E7D32?style=flat-square)](https://asms-iota.vercel.app/)

---

## 🧭 Executive Summary & Commercial Impact

AYUSH Shubham Institute of Medical Sciences required a nationwide digital ecosystem to serve citizens, patients, students, and health authorities across **36 Indian States and Union Territories**.

This platform delivers:
1. **Automated Roll Number Verification:** Instant, tamper-evident credential verification for institutional candidates and alumni.
2. **National Healthcare Discovery:** Zero-dependency interactive GIS vector mapping enabling rural citizens to locate clinics and specialists.
3. **Programmatic Content at Scale:** 148 automated clinical SEO articles generating massive organic patient acquisition without server strain.
4. **Transparent Patient Welfare:** Full integration of Ayushman Bharat cashless TPA coverage, government welfare schemes, and a 0% interest EMI hospital desk.

---

## 🏛️ System Architecture

```mermaid
graph TD
    User([Citizen / Patient / Candidate]) -->|HTTPS / Edge Request| CDN[Vercel Global Edge Network]
    CDN --> AppRouter[Next.js 15 App Router]
    
    subgraph Frontend Applications
        AppRouter --> Home[Dynamic Homepage & Emergency Ribbon]
        AppRouter --> GISMap[36-State Vector GIS Exploration Map]
        AppRouter --> RollEngine[Roll Number Credential Search Engine]
        AppRouter --> SEOArticles[148 Programmatic SEO Health Articles]
        AppRouter --> OPDWizard[Telemedicine OPD & Financial Welfare Wizard]
    end
    
    subgraph Data & Verification Tier
        RollEngine --> MemoryIndex[High-Speed In-Memory Candidate Lookup]
        MemoryIndex --> CandidateStore[(Encrypted Verification Store)]
        SEOArticles --> EdgeCache[Edge Incremental Static Regeneration (ISR)]
    end
```

---

## ⚡ The Hard Engineering Challenges Conquered

### 1. The Relume vs. Tailwind CSS Cascade Specificity Clash
- **The Challenge:** Pre-built Relume layout elements introduced conflicting `r-2` CSS utility cascades that collided violently with Tailwind classes. This caused mobile navigation drawers and verification popovers to render completely transparent or off-screen.
- **The Solution:** Conducted a comprehensive CSS cascade audit, isolated CSS module scopes, purged conflicting overrides, and implemented strict Tailwind layout semantics with explicit z-index stacking and hardware-accelerated drawer transitions.

### 2. Zero-Dependency 36-State & UT Interactive Vector GIS Map
- **The Challenge:** Standard web GIS libraries (Mapbox, Leaflet) added over 450 KB of JavaScript overhead, crippling Core Web Vitals on budget Android devices across rural India.
- **The Solution:** Hand-extracted and optimized 177 KB of standalone SVG vector path coordinates for every state and union territory. Built a reactive React selection engine that delivers instant regional clinic availability with zero third-party GIS dependencies.

### 3. 148 Programmatic Dynamic SEO Health Articles
- **The Challenge:** Generating hundreds of specialized Ayurvedic and clinical guides manually would take months, while static page bloat threatened edge deployment build limits.
- **The Solution:** Architected a programmatic content pipeline combining structured JSON-LD medical schema markup with automated dynamic SVG header generation, achieving sub-second edge TTFB across all 148 routes.

### 4. Automated Headless CDP Regression Testing
- **The Challenge:** Frequent design iterations threatened regressions in high-stakes credential verification and appointment booking flows.
- **The Solution:** Engineered automated test suites leveraging the Edge Chrome DevTools Protocol (CDP) to programmatically validate interactive state transitions, drawer animations, and query inputs in headless CI environments.

---

## 📈 Developer Transformation & Growth

| Dimension | Before ASMS Project | After Delivering ASMS |
| :--- | :--- | :--- |
| **Architectural Scope** | Single-page apps, portfolio projects | Multi-page, 33-route enterprise healthcare portal |
| **Bundle & Performance Control** | Heavy reliance on external GIS libraries | Hand-crafted 177 KB SVG vector mapping engine |
| **CSS Mastery** | Surface-level utility styling | Deep CSS cascade resolution & specificity isolation |
| **Domain Logic** | Generic contact forms | Ayushman Bharat TPA compliance & verification engines |
| **Automated Testing** | Manual browser clicking | Headless Chrome DevTools Protocol (CDP) test suites |

---

## 🔒 Confidentiality & Intellectual Property Notice
*Proprietary candidate database records (`data/asms_database.json`), legal trust agreements, and internal administrative credentials remain strictly protected under non-disclosure agreements with the client. This repository serves as an open architectural case study and technical showcase.*
