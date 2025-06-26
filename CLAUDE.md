# NJ Wedding Photography Business Website

## Project Overview
A modern wedding photography business website featuring a portfolio gallery and content management system.

## Tech Stack
- **Frontend**: SvelteKit (SPA mode)
- **Backend**: Directus (Headless CMS + CRM)
- **Styling**: Tailwind CSS
- **Deployment**: Coolify on VPS

## Project Structure
```
├── frontend/          # SvelteKit SPA
│   ├── src/
│   │   ├── routes/    # Page routes
│   │   ├── lib/       # Utilities and stores
│   │   ├── components/# Reusable components
│   │   └── app.html   # App shell
│   ├── static/        # Static assets
│   └── package.json
├── directus/          # Directus CMS configuration
└── docker-compose.yml # Local development setup
```

## Key Features
- **Portfolio Gallery**: Wedding photo and video showcases
- **Content Management**: Easy content updates via Directus
- **Contact System**: Lead capture and CRM integration
- **Responsive Design**: Mobile-first approach
- **SEO Optimized**: Meta tags, structured data

## Development Workflow
- `npm run dev` - Start SvelteKit development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## Deployment
- **Platform**: Coolify on VPS
- **Frontend**: Static SPA build
- **Backend**: Directus container
- **Database**: PostgreSQL (via Coolify)

## Environment Variables
- `VITE_DIRECTUS_URL` - Directus API endpoint
- `DIRECTUS_KEY` - API access token
- `DIRECTUS_SECRET` - Admin secret

## Notes
- Images optimized for web delivery
- Directus handles all dynamic content
- SPA mode for fast client-side navigation