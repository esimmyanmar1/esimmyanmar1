# eSIM Myanmar

Welcome to **eSIM Myanmar** — Myanmar’s next-generation digital SIM platform, enabling instant mobile connectivity with seamless eSIM activation. This bilingual web app delivers a rich, immersive user experience powered by cutting-edge web technologies.

---

## 🎨 Brand Identity

| Color           | Hex Code     |
|-----------------|--------------|
| Dark Blue       | `#1e2f3c`    |
| Light Gray      | `#c0c0c0`    |
| Accent Cyan     | `#00ffff`    |
| Transparent     | `transparent`|

**Contact Us:**  
✉️ Email: [info@esim.com.mm](mailto:info@esim.com.mm)  
🌐 Website: [esim.com.mm](https://esim.com.mm)  
🐦 Twitter: [@eSIMMyanmar](https://twitter.com/eSIMMyanmar)  
📞 Phone: 09650000172  

---

## 🚀 Core Features

- **Dynamic 3D Animations:** Engaging particle system backgrounds built with GSAP 3 and Three.js — no static images, purely interactive and animated.
- **Bilingual Support:** Full localization with `next-intl` for seamless English and Myanmar language switching.
- **AI-Powered Chat Assistant:** Context-aware conversational AI powered by Google Vertex AI and OpenAI GPT-4 Turbo.
- **Integrated Payment Gateways:** Local providers AYA PAY, WavePay, plus Stripe for international payments, complete with secure webhook handling.
- **Mobile-First Responsive UI:** Built with Tailwind CSS and Shadcn UI components for a smooth experience across all devices.
- **Robust Security:** Firebase Authentication with JWT ensures user data protection and session security.
- **Cloud-Native Deployment:** Dockerized architecture deployed on Google Cloud Run for scalability and reliability.
- **Quality Assurance:** Comprehensive testing suite including Playwright for end-to-end tests and Jest for unit/integration tests.

---

## 🛠️ Technology Stack

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

## 📁 Project Structure

```plaintext
esim-myanmar/
├── public/                           # Static assets (fonts, favicon, robots.txt)
│   ├── fonts/NotoSansMyanmar.woff2  # Burmese font for Myanmar localization
│   ├── favicon.ico
│   └── robots.txt
│
├── src/
│   ├── app/
│   │   ├── [lang]/                   # Localized routing (en/my)
│   │   │   ├── layout.tsx            # Localized layout with header, footer, AI chat modal
│   │   │   └── {page,about,contact,...}.tsx  # Localized pages
│   │   ├── providers.tsx             # React context providers for auth, i18n, theme
│   │   └── AnimatedBackground.tsx   # GSAP + Three.js 3D animated background component
│   │
│   ├── components/                   # Reusable UI components with GSAP animation effects
│   │   ├── ui/                      # Shadcn UI library components
│   │   ├── payments/                # Payment gateway UI & logic components
│   │   ├── ai/                      # AI chat widgets and assistants
│   │   └── i18n/                    # Language switcher components
│   │
│   ├── lib/                         # Utility helpers (i18n, firebase, payments, animation)
│   ├── hooks/                       # Custom React hooks
│   ├── api/                         # Next.js API routes
│   │   ├── vertex-ai/route.ts       # AI chat API endpoint
│   │   └── payments/webhooks/       # Payment webhook handlers
│   │
│   ├── messages/                    # Translation JSON files
│   │   ├── en.json
│   │   └── my.json
│   │
│   ├── styles/                     # Global styles, TailwindCSS config
│   ├── tests/                      # Unit and integration tests
│
├── docker/                        # Docker build and config files
├── playwright/                    # End-to-end test suites
├── .env.example                   # Sample environment variables
├── package.json                  # Dependencies and scripts
├── tsconfig.json                 # TypeScript configuration
├── next.config.js                # Next.js config
└── README.md                     # This file
