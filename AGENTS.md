# AGENTS.md

## Sadr

### Build and test
- The repo has no build step and no tests. It is a static site (index.html, style.css, logo.jpg) that .github/workflows/static.yml uploads from the repo root to GitHub Pages.
- To check a change, serve the root with `python3 -m http.server 8765 --bind 127.0.0.1`, then request `/`, `/style.css` and `/logo.jpg`. Each request answers HTTP 200.

### Toolchain
- The repo has no package manager, runtime or lockfile. CI installs only SHA-pinned GitHub Actions and the digest-pinned `semgrep/semgrep` image.
