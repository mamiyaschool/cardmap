# AGENTS.md

## Cursor Cloud specific instructions

### Overview

CardMap（カードマップ）is a zero-dependency, single-file web application (`index.html`) for card-based memo organization. No build system, no package manager, no backend.

### Running the application

Serve files with any static HTTP server. The simplest approach:

```bash
python3 -m http.server 8000 --directory /workspace
```

Then open `http://localhost:8000/index.html` in a browser.

### Key caveats

- **CDN dependencies**: The app loads Tailwind CSS, html2canvas, and pptxgenjs from CDNs at runtime. Internet connectivity is required for full functionality (styling and export features).
- **No lint/test/build**: There is no linter, no automated test suite, and no build step. The entire application is a single `index.html` file with inline CSS and JavaScript.
- **Data persistence**: Uses browser `localStorage` — data does not persist across different browser profiles or after clearing browser data.
- **Manual testing only**: To verify changes, serve the file and test in a browser.
