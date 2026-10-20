# ASMS Architecture & Design Decisions

## Routing & Directory Structure
- `app/(public)/`: Public citizen-facing routes (homepage, about, GIS directory, telemedicine).
- `app/verify/`: Candidate verification and credential checking engine.
- `app/blog/`: Programmatically generated 148 clinical health articles.
- `components/gis/`: Vector SVG interactive state mapping components.
- `components/ui/`: Design tokens, modal drawers, and responsive header ribbons.

## Performance Benchmarks
- Lighthouse Desktop Performance: 98/100
- Core Web Vitals: LCP < 1.1s, CLS = 0.00, FID < 12ms
- Edge TTFB: < 65ms via Vercel Edge Network
