# PWA Study Hub — Setup & Status

## Current UI foundation
- Responsive mobile-first home screen.
- Botany, Zoology and Chemistry subject cards.
- Search, dark mode and bottom navigation shell.
- PWA manifest and service worker for installable app shell.
- GitHub Pages-compatible relative paths.

## Publish free with GitHub Pages
1. Open repository Settings.
2. Open Pages under Code and automation.
3. Select Deploy from a branch.
4. Select branch main and folder /(root), then Save.
5. Wait for GitHub Pages to publish. The public URL appears on the Pages settings screen.

## Install on Android
1. Open the published HTTPS Pages URL in Chrome.
2. Open browser menu and choose Install app or Add to Home screen.
3. Launch it from the home screen.

## Current limitations
- This is the first UI foundation, not the finished learning app.
- Chapter lists remain placeholders until the official 2026–27 degree-awarding university syllabus is confirmed.
- Markdown reader, diagrams gallery, MCQ engine, bookmarks and progress tracking are next.
- Service worker currently caches the app shell; complete offline notes need content caching.
- GitHub Pages hosts static files only. Login, cross-device sync and online ranking require a backend.

## Content workflow
Each chapter will be a Markdown file in its subject's CHAPTERS folder. A shared chapter index/loader will be added next so new notes can appear without building a separate screen for every chapter.
