# HousePoint - CIC House Points Leaderboard

A real-time house points leaderboard application built with React, Vite, TanStack Router, and Supabase.

## Features

- 🏠 Real-time point tracking for multiple houses
- 📊 Live leaderboard with instant updates
- 🔐 Admin authentication for point management
- 📝 Complete history log of all point changes
- 🎉 Celebration animations on winner announcements
- 📱 Responsive design for all devices

## Prerequisites

- Node.js 18+ or Bun
- Supabase account with a project set up

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd HousePoint
```

2. Install dependencies:
```bash
npm install
# or
bun install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

Then edit `.env.local` with your Supabase credentials:
- `VITE_SUPABASE_URL` - Your Supabase project URL
- `VITE_SUPABASE_PUBLISHABLE_KEY` - Your Supabase publishable API key

## Development

Start the development server:

```bash
npm run dev
# or
bun dev
```

The app will be available at `http://localhost:5173`

## Building

Build for production:

```bash
npm run build
# or
bun build
```

The output will be in the `dist` directory.

## Deployment

### GitHub Pages

1. Update `vite.config.ts` if deploying to a subdirectory:
```typescript
export default defineConfig({
  base: '/repository-name/',
  // ... rest of config
});
```

2. Create `.github/workflows/deploy.yml` (see below for full config)

3. Push to main and GitHub Actions will automatically build and deploy

### Firebase Hosting

1. Install Firebase CLI:
```bash
npm install -g firebase-tools
```

2. Initialize Firebase:
```bash
firebase init hosting
```

3. Build and deploy:
```bash
npm run build
firebase deploy
```

### AWS Amplify

1. Connect your GitHub repository to AWS Amplify Console
2. Amplify will auto-detect the build settings
3. Configure environment variables in Amplify console
4. Deploy automatically on push

### Netlify

1. Connect your GitHub repository via Netlify dashboard
2. Set build command: `npm run build`
3. Set publish directory: `dist`
4. Add environment variables in Netlify UI
5. Deploy

### Vercel

1. Import project from GitHub to Vercel dashboard
2. Vercel auto-detects Vite configuration
3. Add environment variables in project settings
4. Deploy automatically

## Project Structure

```
├── src/
│   ├── routes/              # TanStack Router pages
│   ├── integrations/        # Supabase integration
│   ├── lib/                 # Utilities and helpers
│   ├── components/          # Reusable components
│   ├── router.tsx           # Router configuration
│   ├── start.ts             # App initialization
│   └── styles.css           # Global styles
├── public/                  # Static assets
├── vite.config.ts           # Vite configuration
├── tsconfig.json            # TypeScript configuration
└── package.json
```

## Environment Variables

All environment variables are prefixed with `VITE_` to be accessible in the browser:

- `VITE_SUPABASE_URL` - Supabase project URL
- `VITE_SUPABASE_PUBLISHABLE_KEY` - Supabase publishable key

## Technologies

- **React 19** - UI framework
- **Vite** - Build tool
- **TypeScript** - Type safety
- **TanStack Router** - Routing
- **TanStack Query** - Data fetching
- **Supabase** - Backend & real-time
- **Tailwind CSS** - Styling
- **Radix UI** - Component library

## License

MIT
