# Loader Project

Simple page loader animation using GSAP and vanilla JS.

## What it is
- Fullscreen overlay with animated bars and a numeric counter.
- After the counter reaches 100 the overlay animates away revealing the page.
- Assets in this folder: `index.html`, `style.css`, `app.js`, `otter.jpg`, font file `Aquire-BW0ox.otf`.

## How to run (recommended)
1. Open a terminal in the project folder:
   cd c:\Users\vthak\htmlcodes\loader
2. Serve files with a local static server (required for fonts/images to load correctly):
   - With Python:
     python -m http.server 5500
     Open http://localhost:5500 in the browser
   - OR with npx:
     npx serve .
   - OR use VS Code Live Server extension.

3. `index.html` already loads GSAP from CDN:
   <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.13.0/gsap.min.js"></script>

## Development / Notes
- Counter logic is in `app.js`. Adjust increment/delay there to control speed/smoothness.
- To use a bundler/React/Next.js, install GSAP via npm:
  npm install gsap
  then import in client code: import gsap from 'gsap';
- Ensure `otter.jpg` and `Aquire-BW0ox.otf` exist in the same folder or update paths.

## Troubleshooting
- If fonts or images don't load when opening `index.html` directly, run a local server (file:// can block them).
- If the counter jumps to 100 immediately, reduce the random increment in `app.js` (e.g. Math.floor(Math.random()*5)+1).
- Check browser console for errors (missing elements, GSAP import errors).

## License
MIT