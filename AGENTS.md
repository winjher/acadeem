# AGENTS.md

## Project Overview
Single-page static HTML site (`index.html`) for "LepVision University & Park". No build step, no backend, no dependencies.

## Running
Served via nginx in `docker-compose.base44.yml` on host port 3000. The source directory is bind-mounted read-only into the nginx document root, so edits to `index.html` appear immediately.

## Verification
- `curl http://localhost:3000/` should return the HTML page.
- The page embeds a Google Apps Script portal in an iframe via the "Open Student Portal" button. The URL is a placeholder; a warning banner appears if the URL doesn't match the expected pattern. No external credentials are required for the static page itself.
