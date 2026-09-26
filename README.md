# RoStats

Analytics dashboard for Roblox game developers: player analytics, server health, monetization, market trends, user journeys, and AI tools for thumbnails, assets and in-game chatbots.

Live preview: https://matetheakhaladze.github.io/RoStats/

## Stack

- React 19 + TypeScript, Vite
- Tailwind CSS 4
- Recharts for charts, lucide-react for icons
- React Router (hash routing so GitHub Pages never 404s on refresh)

All data on the preview is mock data generated in `src/data/mock.ts`. Backend (Django + DRF) comes next.

## Pages

| Route | Page |
| --- | --- |
| `/` | Landing page |
| `/#/app` | Overview |
| `/#/app/players` | Players (from uploaded CSVs) |
| `/#/app/monetization` | Monetization (from uploaded CSVs) |
| `/#/app/market` | Market Trends (live Roblox charts) |
| `/#/app/data` | Import Creator Dashboard CSVs |
| `/#/app/art` | Art Generator + home menu test |
| `/#/app/chatbot` | Chatbot |
| `/#/app/billing` | Subscription and credits |
| `/#/app/settings` | Games and account |

## Development

```bash
npm install
npm run dev
```

## Deployment

This app is configured for Vercel. Import the repo into Vercel and use the default Vite settings:

- Build command: `npm run build`
- Output directory: `dist`
- Framework preset: Vite

The frontend is served from the root URL, so `vite.config.ts` uses `base: '/'` instead of the GitHub Pages subpath.
