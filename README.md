# Michelle's Svelte Site ✨

A beautiful, modern website built with Svelte and SvelteKit.

## Features

- 🚀 Fast and responsive
- 🎨 Beautiful modern design with glassmorphism effects
- ⚡ Built with Svelte 4 and SvelteKit
- 📱 Mobile-friendly and responsive
- 🎯 Interactive counter component
- 🌈 Beautiful gradient backgrounds

## Getting Started

### Prerequisites

- Node.js (version 18 or higher)
- npm or yarn

### Installation

1. Install dependencies:
```bash
npm install
```

2. Start the development server:
```bash
npm run dev
```

3. Open your browser and navigate to `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run check` - Type check and lint
- `npm run format` - Format code with Prettier

## Project Structure

```
src/
├── app.css          # Global styles
├── app.html         # HTML template
├── app.d.ts         # TypeScript declarations
├── routes/          # SvelteKit routes
│   ├── +layout.svelte
│   └── +page.svelte
```

## Technologies Used

- **Svelte 4** - Frontend framework
- **SvelteKit** - Full-stack web framework
- **TypeScript** - Type safety
- **Vite** - Build tool and dev server
- **CSS3** - Modern styling with gradients and animations

## Customization

Feel free to customize the colors, layout, and components to match your needs. The main page component is located in `src/routes/+page.svelte`.

## Deployment

This project can be deployed to various platforms:

- **Vercel**: Automatic deployment from Git
- **Netlify**: Drag and drop deployment
- **GitHub Pages**: Static site hosting
- **Any static hosting service**: After running `npm run build`

## License

MIT License - feel free to use this project as a starting point for your own websites!
