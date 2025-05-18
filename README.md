# Gurusparsh Resort Website

A modern redesign of the Gurusparsh Resort website that preserves its agricultural theme while enhancing user experience with contemporary design elements and animations.

## Features

- Responsive design for all device sizes (mobile, tablet, desktop)
- Interactive booking modal for room reservations
- Detailed room pages for all accommodation types
- Photo gallery with lightbox feature
- Comprehensive amenities and activities section
- Contact form with validation

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm (v7 or higher)

### Local Development

1. Clone the repository
   ```
   git clone [repository-url]
   cd gurusparsh-resort
   ```

2. Install dependencies
   ```
   npm install
   ```

3. Run the development server

   **Windows:**
   ```
   run-local.bat
   ```
   
   **macOS/Linux:**
   ```
   chmod +x run-local.sh
   ./run-local.sh
   ```
   
   Or manually set environment:
   ```
   # Windows (CMD)
   set NODE_ENV=development
   npx tsx server/index.ts
   
   # Windows (PowerShell)
   $env:NODE_ENV="development"
   npx tsx server/index.ts
   
   # macOS/Linux
   NODE_ENV=development npx tsx server/index.ts
   ```

4. Open [http://localhost:5000](http://localhost:5000) in your browser

### Building for Production

To create a production-ready build:

```
npm run build
```

This will generate optimized assets in the `dist` directory.

### Deployment

This project can be deployed on various platforms:

#### Netlify

The repository includes a `netlify.toml` file for easy deployment on Netlify.

1. Connect your GitHub repository to Netlify
2. Netlify will automatically detect the configuration in `netlify.toml`
3. The build settings are already configured:
   - Build command: `cd client && npx vite build && cd .. && esbuild server/index.ts --platform=node --packages=external --bundle --format=esm --outdir=dist`
   - Publish directory: `dist/public`

#### Vercel

The repository includes a `vercel.json` file for Vercel deployment.

1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect the configuration in `vercel.json`
3. The build settings are already configured to build the client-side application

#### Manual Deployment

If you prefer to deploy manually:

1. Build the application:
   ```
   cd client && npx vite build && cd ..
   esbuild server/index.ts --platform=node --packages=external --bundle --format=esm --outdir=dist
   ```

2. Deploy the `dist/public` directory to your hosting provider of choice

## Project Structure

- `client/src/` - React frontend code
  - `components/` - Reusable UI components
  - `pages/` - Page components for each route
  - `hooks/` - Custom React hooks
  - `lib/` - Utility functions and shared code
- `server/` - Express backend code
- `shared/` - Code shared between frontend and backend
- `public/` - Static assets

## Tech Stack

- React
- TypeScript
- Express
- Tailwind CSS
- shadcn/ui Components
- Framer Motion
- Wouter (for routing)
- React Query
- Zod (for validation)

## License

This project is licensed under the MIT License