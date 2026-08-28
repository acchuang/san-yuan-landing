# San Yuan 三元

A single-page landing site for **San Yuan** — a multi-system astrology platform combining Chinese BaZi (八字), Western astrology, and Vedic astrology into one unified experience.

Live at: **https://9eaeb39b.san-yuan-landing.pages.dev**

---

## Features

### Interactive Demo Widget
Enter your birth date, time, and location to get real-time calculations:

| System | Calculations |
|--------|-------------|
| **Chinese BaZi** 八字 | Day Master (日主), Five Elements (五行), Ten Gods (十神), Personality Analysis |
| **Western Astrology** | Sun sign, Moon sign, Ascendant, House placements, Element distribution |
| **Vedic Astrology** | Nakshatra, Dasha periods, Rashi, Yoga |

### Landing Sections
- **Hero** — Immersive intro with animated background
- **Trust Signals** — Expert credentials & platform stats
- **Testimonials** — User reviews carousel
- **Interactive Demo** — Real calculation engine (not mock data)
- **Knowledge Hub** — Blog/article previews
- **Pricing** — Tiered plans
- **Footer** — Links, social, newsletter

---

## Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Single-file HTML + Tailwind CSS + vanilla JS |
| Icons | FontAwesome |
| Animation | Custom CSS + GSAP-ready structure |
| Hosting | Cloudflare Pages |
| CI/CD | Wrangler CLI |

---

## Calculation Engine

The demo widget includes a real calculation engine (not static mock data):

- **BaZi**: Day stem/branch from 1900 reference date using 天干地支 lookup tables
- **Five Elements**: Stem element + yin/yang polarity mapping
- **Ten Gods**: Simplified mapping from day stem
- **Western**: Sun sign via tropical zodiac date ranges, Moon sign approximation
- **Vedic**: Nakshatra from lunar longitude calculation

> ⚠️ This is a **frontend demo** for landing page engagement. Production-grade astrological calculations require ephemeris libraries (e.g., Swiss Ephemeris) and timezone-aware geocoding.

---

## Deploy

```bash
# Install Wrangler
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Deploy
wrangler pages deploy . --project-name=san-yuan-landing
```

Or push to `master` → Cloudflare Pages auto-deploys if connected.

---

## Project Structure

```
san-yuan-landing/
├── index.html          # Single-file app (HTML + CSS + JS)
├── wrangler.toml       # Cloudflare Pages config
└── README.md           # This file
```

---

## License

MIT — Alan Huang (acchuang)
