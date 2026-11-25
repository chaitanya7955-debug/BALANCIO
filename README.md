<p align="left">
  <img src="public/balancio-mark.svg" alt="Balancio brand mark" width="48" height="48" />
</p>

# balancio

**Every trip. Every expense. Every balance.**

Balancio is a smart group travel expense management and debt settlement platform built to make shared trips transparent, accurate across currencies, and effortless to settle.

---

## Key Capabilities

- **Multi-Currency Expense Ledger**: Log expenses in `USD`, `EUR`, `GBP`, `CAD`, or `JPY` and normalize totals into each trip's base currency with transparent conversion previews.
- **Equal & Exact Splits**: Split receipts evenly across selected travelers (with deterministic remainder-cent distribution) or assign exact base-currency shares per participant.
- **Minimum-Cash-Flow Debt Settlement**: Automatically reduces tangled group debts into the fewest direct repayments required to bring every traveler to zero balance.
- **One-Click Settlement Recording**: Record transfers directly from the settlement plan, update net balances immediately, and track settled history.
- **Real-Time Balancio Notifications**: In-app notification center, unread badge tracking, and toast alerts for expenses, settlements, and trip milestones.
- **Traveler Authentication & Branded Experience**: Dedicated sign-in and registration flow, branded loading transitions, and persistent browser session state.

---

## Brand Identity

- **Product Name**: Balancio
- **Wordmark**: `balancio` (lowercase geometric sans-serif)
- **Tagline**: *Every trip. Every expense. Every balance.*
- **Category**: Smart group travel expense management and debt settlement platform
- **Brand Mark**: Two connected traveler nodes linked by a leveled equilibrium bar beneath a travel horizon arc ([`public/balancio-mark.svg`](public/balancio-mark.svg)).

For complete typography, color tokens, and usage rules, see [Brand Guidelines](docs/BRAND_GUIDELINES.md).

---

## Quick Start

```bash
# Install dependencies
npm install

# Start the Balancio development server
npm run dev

# Run unit tests (settlement engine & precision invariants)
npm test

# Type-check and build production bundle
npm run typecheck
npm run build
```

---

## Project Structure

```text
balancio/
├── index.html                        # Browser tab title, metadata, and favicon
├── public/
│   └── balancio-mark.svg             # Official Balancio vector mark
├── docs/
│   ├── BRAND_GUIDELINES.md           # Balancio visual identity & brand rules
│   └── TECHNICAL_DOCUMENTATION.md    # Architecture, data models, and algorithms
├── src/
│   ├── components/
│   │   ├── AuthPage.tsx              # Sign-in, registration, and demo workspace entry
│   │   ├── BrandMark.tsx             # Balancio SVG mark and lowercase wordmark lockup
│   │   ├── Dashboard.tsx             # Trip KPIs, expense ledger, settlement plan, balances
│   │   ├── ExpenseModal.tsx          # Multi-currency expense & split builder
│   │   ├── LoadingScreen.tsx         # Branded loading state with tagline
│   │   ├── Navbar.tsx                # Top navigation, notifications dropdown, user controls
│   │   └── TripModal.tsx             # New group trip creation modal
│   ├── data/
│   │   └── seedTrips.ts              # Pre-populated sample trips and notifications
│   ├── lib/
│   │   ├── settlement.ts             # Integer-cent balance & minimum-cash-flow engine
│   │   ├── settlement.test.ts        # Vitest suite for settlement accuracy
│   │   └── storage.ts                # LocalStorage persistence layer
│   ├── styles/
│   │   ├── tokens.css                # Balancio color, typography, and spacing tokens
│   │   └── app.css                   # Responsive layout and component styles
│   ├── types/
│   │   └── balancio.ts               # Core TypeScript domain interfaces
│   ├── App.tsx                       # Root orchestration, tab titles, and toast pipeline
│   └── main.tsx                      # Application entry point
├── package.json
├── tsconfig.json
└── vite.config.ts
```

---

## Technical Documentation

See [docs/TECHNICAL_DOCUMENTATION.md](docs/TECHNICAL_DOCUMENTATION.md) for architecture details, integer-cent accounting invariants, and the minimum-cash-flow settlement algorithm.
