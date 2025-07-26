# eSIM Myanmar

A cutting-edge, bilingual web application delivering Myanmar’s future of mobile connectivity through instant digital SIM activation. Built with Next.js 14 and React 18, featuring dynamic 3D animated backgrounds using GSAP 3 and Three.js for a fully immersive UI experience.

---

## Brand Identity

**Primary Colors:**  
- Dark Blue: `#1e2f3c`  
- Light Gray: `#c0c0c0`  
- Accent Cyan: `#00ffff`  
- Transparent: `transparent`

**Contact:**  
- Email: info@esim.com.mm  
- Website: esim.com.mm  
- Social: @eSIMMyanmar  
- Phone: 09650000172  

---

## Core Features

- **Dynamic 3D Animations:** Built with GSAP 3 and Three.js particle systems for interactive, animated backgrounds without static images.  
- **Bilingual Support:** Full i18n support using `next-intl` and locale-based routing for English and Myanmar languages.  
- **AI-Powered Chat Assistant:** Integrated with Google Vertex AI and OpenAI GPT-4 Turbo for context-aware conversational support.  
- **Payment Gateways:** Integrated local payment providers such as AYA PAY and WavePay, plus Stripe for international transactions, all with secure webhook processing.  
- **Responsive & Accessible UI:** Mobile-first design using Tailwind CSS and Shadcn UI components, optimized for accessibility and performance.  
- **Secure Authentication:** Firebase Authentication with JWT tokens for user security and session management.  
- **Cloud-Native Deployment:** Containerized with Docker and deployed via Google Cloud Run with CI/CD automation through Google Cloud Build.  
- **Testing & Quality Assurance:** End-to-end testing with Playwright, unit and integration tests with Jest and React Testing Library.  

---

## Technology Stack

| Category           | Technologies                                                  |
|--------------------|--------------------------------------------------------------|
| Frontend           | Next.js 14, React 18, TypeScript 5                           |
| Animation          | GSAP 3, Three.js, Framer Motion                              |
| Styling            | Tailwind CSS, Shadcn UI                                      |
| Internationalization| next-intl, Noto Sans Myanmar font                            |
| AI Integration     | Google Vertex AI, OpenAI GPT-4 Turbo                         |
| Backend            | Firebase Functions, Next.js API Routes                       |
| Payment Processing | AYA PAY API, WavePay SDK, Stripe                             |
| Testing            | Playwright, Jest, React Testing Library                      |
| Deployment         | Docker, Google Cloud Run, Google Cloud Build                 |

---

## Project Structure

```plaintext
esim-myanmar/
├── public/                           # Static assets (fonts, favicon, robots.txt)
│   ├── fonts/NotoSansMyanmar.woff2  # Burmese font for Myanmar text rendering
│   ├── favicon.ico
│   └── robots.txt
│
├── src/
│   ├── app/
│   │   ├── [lang]/                   # Language-specific routing (en, my)
│   │   │   ├── layout.tsx            # Localized layout with header/footer and AI agent modal
│   │   │   └── {page,about,contact,...}.tsx  # Localized pages
│   │   ├── providers.tsx             # React context providers for auth, theme, i18n, etc.
│   │   └── AnimatedBackground.tsx   # GSAP + Three.js 3D animated background component
│   │
│   ├── components/                   # Reusable UI components with GSAP animations
│   │   ├── ui/                      # Shadcn UI components
│   │   ├── payments/                # Payment gateway UI & integration components
│   │   ├── ai/                      # AI chat widget and assistant components
│   │   └── i18n/                    # Language toggle and localization helpers
│   │
│   ├── lib/
│   │   ├── i18n.ts                  # Localization config and helpers
│   │   ├── firebase/                # Firebase utils (auth, firestore, storage)
│   │   ├── payments/                # Payment processor helpers and API client
│   │   └── animation/               # GSAP and Three.js animation utilities and configs
│   │
│   ├── hooks/                       # Custom React hooks
│   ├── api/                        # Next.js API routes
│   │   ├── vertex-ai/route.ts       # AI agent API endpoint (chat)
│   │   └── payments/webhooks/       # Payment webhook handlers (AYA PAY, WavePay, Stripe)
│   │
│   ├── messages/                   # Translation JSON files
│   │   ├── en.json
│   │   └── my.json
│   │
│   ├── styles/                    # Global CSS, Tailwind config, PostCSS config
│   └── tests/                     # Unit & integration tests
│
├── docker/                        # Docker multi-stage build configs
├── playwright/                    # Playwright end-to-end tests
├── .env.example                   # Environment variables template
├── package.json                  # Dependencies & scripts
├── tsconfig.json                 # TypeScript config
├── next.config.js                # Next.js config
└── README.md                     # This file
