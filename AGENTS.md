# Repository Guidelines

## Project Structure & Module Organization

This repository is a small, static Chinese-language trip receipt mockup generator. The page, styles, and browser-side behavior are kept together in `index.html`. Image assets used by the page live in `assets/` (`didi-logo.png`, `header.png`, and `enterprise-banner.png`). There is no separate source, test, or build directory; keep additions proportionate to this single-page structure.

## Build, Test, and Development Commands

There is no package manager or build configuration in the repository. Open `index.html` directly in a browser for local use, or serve the current directory with a static server, for example:

- `python3 -m http.server 8000` — serve the page at `http://localhost:8000`.

No automated build or test command is configured. When changing behavior, exercise the affected controls in a browser and check the page at desktop and narrow viewport widths.

## Coding Style & Naming Conventions

Keep HTML semantic and accessible, preserve the document language (`zh-CN`), and use the existing two-space indentation. Keep CSS in the page’s `<style>` block and JavaScript in its existing page-level script unless the project grows enough to justify separate files. Use descriptive, lowercase kebab-case CSS class names (such as `.actions` and `.enterprise-banner`) and clear function and variable names. Reference images with paths under `assets/`; do not embed duplicate copies.

## Testing Guidelines

There is no test framework or coverage requirement at present. For UI changes, verify the relevant form actions, generated preview/output, and any print or download behavior affected by the change. Confirm that asset paths load and that the layout remains usable on a narrow screen. If automated tests are introduced, document their invocation here and keep test files clearly named (for example, `*.test.js`).

## Commit & Pull Request Guidelines

This directory has no Git metadata, so repository-specific commit conventions cannot be established. Use concise, imperative commit subjects that describe the change. Pull requests should explain the user-visible behavior changed, list manual verification performed, link related work when applicable, and include screenshots for visual changes.

## Security & Configuration

The page is static and has no repository-managed secrets or runtime configuration. Do not commit credentials, personal trip data, or generated receipts containing real identifying information. Keep sample content fictional.
