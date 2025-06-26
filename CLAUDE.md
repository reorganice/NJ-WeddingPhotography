# NJ Wedding Photography Business Website

## Project Overview
A modern wedding photography business website featuring a portfolio gallery and content management system, built with AI-assisted development workflow using Claude Code.

## Tech Stack
- **Frontend**: SvelteKit (SPA mode)
- **Backend**: Directus (Headless CMS + CRM)
- **Styling**: Tailwind CSS
- **Deployment**: Coolify on VPS
- **Development**: Docker, MCP Servers, AI-assisted workflow

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
├── docker-compose.yml # Local development setup
├── PROJECT_LOG.md     # Development session logs
└── .claude/           # Claude Code configuration
    ├── settings.local.json
    └── commands/      # Custom slash commands
```

## AI Development Workflow

### Core Principles
1. **Research-Plan-Code**: Always research and plan before implementation
2. **Test-Driven Development**: Write tests first where applicable
3. **Continuous Documentation**: Update PROJECT_LOG.md with each session
4. **MCP Integration**: Leverage Docker MCP Toolkit and Context-7 for enhanced capabilities

### Development Commands
```bash
# Local development
npm run dev              # Start SvelteKit development server
npm run build           # Build for production  
npm run preview         # Preview production build
docker compose up       # Start full stack locally
docker compose down     # Stop all services

# Testing & Quality
npm run test           # Run test suite
npm run lint           # Lint codebase
npm run typecheck      # TypeScript validation

# Deployment
docker build -t wedding-frontend .  # Build frontend image
# Coolify handles deployment from Git
```

### Code Style & Standards
- **TypeScript**: Strict mode enabled
- **Formatting**: Prettier with 2-space indentation
- **Linting**: ESLint with SvelteKit config
- **Components**: Composition API pattern
- **Naming**: kebab-case for files, PascalCase for components
- **Imports**: Absolute imports from `$lib/`

### Testing Strategy
- **Unit Tests**: Vitest for utilities and logic
- **Component Tests**: Testing Library for Svelte components
- **E2E Tests**: Playwright for critical user flows
- **API Tests**: Test Directus endpoints and data flow

## Key Features
- **Portfolio Gallery**: Wedding photo and video showcases with lazy loading
- **Content Management**: Easy content updates via Directus admin
- **Contact System**: Lead capture with CRM integration
- **Responsive Design**: Mobile-first with Tailwind CSS
- **SEO Optimized**: Meta tags, structured data, sitemap
- **Performance**: Image optimization, code splitting

## Deployment Architecture

### Coolify Configuration
- **Frontend**: Static build served via Nginx
- **Backend**: Directus container with PostgreSQL
- **Database**: Managed PostgreSQL instance
- **Storage**: S3-compatible for media files
- **SSL**: Automatic Let's Encrypt certificates

### Environment Variables
```env
# Frontend (.env)
VITE_DIRECTUS_URL=https://cms.njwedding.com
VITE_SITE_URL=https://njwedding.com

# Backend (Directus)
DB_HOST=postgres
DB_PORT=5432
DB_DATABASE=directus
DB_USERNAME=directus
DB_PASSWORD=secure_password
KEY=random_key_here
SECRET=random_secret_here
ADMIN_EMAIL=admin@njwedding.com
ADMIN_PASSWORD=secure_admin_password
```

## Session Management
- Always update PROJECT_LOG.md with session progress
- **COMMIT CHECK**: Before major changes, always check if current work should be committed
- Commit frequently with descriptive messages
- Use Todo tracking for complex multi-step tasks
- Document decisions and architectural choices

## Development Rules (ALWAYS FOLLOW)
1. **Before adding dependencies**: Check if current changes should be committed first
2. **Before major features**: Commit current progress as a checkpoint
3. **After configuration changes**: Always commit configuration updates
4. **Before switching contexts**: Commit current work to avoid mixing concerns

## MCP Server Integration
- **Docker MCP Toolkit**: Container management and deployment
- **Context-7**: Enhanced context management
- Custom commands in `.claude/commands/` for repeated workflows

## Git Workflow
- **Main Branch**: `master` (production-ready)
- **Feature Branches**: `feature/description`
- **Commit Messages**: Conventional commits format
- **Auto-deployment**: Coolify watches main branch

## Notes
- Images optimized for web delivery with Sharp
- Directus handles all dynamic content and CRM
- SPA mode for fast client-side navigation
- Progressive enhancement for accessibility
- Regular security updates via Dependabot