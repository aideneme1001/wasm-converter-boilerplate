# FFmpeg.wasm Next.js Boilerplate

**This is a 100% client-side boilerplate.** All file conversion happens entirely in the browser using WebAssembly. No server uploads, no backend required.

A minimal, production-ready Next.js App Router boilerplate demonstrating browser-based video conversion using FFmpeg compiled to WebAssembly.

---

## Live Demo & Full Production Tool

For a complete file conversion experience with support for 50+ formats, visit:

**[EveryFileConvert.com](https://everyfileconvert.com)**

---

## Features

- **Fully client-side** - Files never leave the user's browser
- **Private by design** - No server uploads, no tracking
- **Fast** - Uses SharedArrayBuffer for multi-threaded WASM execution
- **Modern** - Built with Next.js App Router and TypeScript

---

## Quick Start

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd <project-name>
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run the development server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## How It Works

This boilerplate demonstrates MP4 to GIF conversion:

1. **Load FFmpeg WASM** - Fetches the FFmpeg core from unpkg CDN
2. **Select an MP4 file** - User picks a video from their device
3. **Convert in-browser** - FFmpeg processes the video entirely client-side
4. **Download the GIF** - Result is provided as a direct download

The key configuration is in `next.config.js`, which sets the required security headers for SharedArrayBuffer support:

```javascript
{
  key: "Cross-Origin-Opener-Policy",
  value: "same-origin",
},
{
  key: "Cross-Origin-Embedder-Policy",
  value: "require-corp",
}
```

---

## Tech Stack

- [Next.js](https://nextjs.org/) - React framework with App Router
- [FFmpeg.wasm](https://github.com/ffmpegwasm/ffmpeg.wasm) - FFmpeg compiled to WebAssembly
- [TypeScript](https://www.typescriptlang.org/) - Type safety

---

## Browser Support

FFmpeg.wasm requires browsers that support:

- WebAssembly
- SharedArrayBuffer (requires COOP/COEP headers)
- Blob URLs

Works in modern Chrome, Firefox, Safari, and Edge.

---

## License

MIT

---

## Credits

Built with [FFmpeg.wasm](https://github.com/ffmpegwasm/ffmpeg.wasm). For a full-featured online file converter, visit [EveryFileConvert.com](https://everyfileconvert.com).
