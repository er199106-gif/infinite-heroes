# Infinite Heroes

A React + Vite comic generator that uses free Pollinations text and image endpoints instead of a paid Gemini API key.

## What changed

- No Gemini API key is required.
- No `.env.local` setup is required.
- Text generation uses `https://text.pollinations.ai`.
- Image generation uses `https://image.pollinations.ai`.
- Generated images are converted to Data URLs so PDF download continues to work.

## Run locally

Prerequisite: install Node.js.

```bash
npm install
npm run dev
```

Open:

```text
http://localhost:3000
```

## Build

```bash
npm run build
```

The production files will be created in `dist/`.

## Free hosting options

### GitHub Pages

1. Push this project to a GitHub repository.
2. Run `npm run build`.
3. Deploy the `dist/` folder with GitHub Pages, or use a GitHub Actions workflow for Vite.

If the site is hosted under a repository path, set `base` in `vite.config.ts`, for example:

```ts
base: '/your-repo-name/',
```

### Netlify

1. Create a free Netlify account.
2. Import the GitHub repository.
3. Build command: `npm run build`
4. Publish directory: `dist`

### Vercel

1. Create a free Vercel account.
2. Import the GitHub repository.
3. Framework preset: Vite
4. Build command: `npm run build`
5. Output directory: `dist`

### Google Colab

Colab can run a temporary dev server for testing, but it is not a good permanent website host. Use it only for experiments.

## Notes

Pollinations' free endpoints are useful for demos and prototypes. They may have rate limits, slower responses, or availability changes. For a production app, use a backend provider with a proper key and server-side protection.
