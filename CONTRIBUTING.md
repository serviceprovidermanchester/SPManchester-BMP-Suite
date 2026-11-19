# Contributing to PixelForge BMP Conversion Suite

Thank you for your interest in contributing to **PixelForge BMP Conversion Suite**, an open-source project maintained by **SPManchester Private Limited**. We welcome contributions from developers of all skill levels and backgrounds. By participating in this project, you help make a better tool for everyone.

---

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [Development Setup](#development-setup)
4. [How to Contribute](#how-to-contribute)
   - [Reporting Bugs](#reporting-bugs)
   - [Requesting Features](#requesting-features)
   - [Submitting Pull Requests](#submitting-pull-requests)
5. [Branch Naming Conventions](#branch-naming-conventions)
6. [Commit Message Conventions](#commit-message-conventions)
7. [Pull Request Checklist](#pull-request-checklist)
8. [Code Style Guide](#code-style-guide)
9. [Contact](#contact)

---

## Code of Conduct

This project adheres to our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [info@spmanchester.com](mailto:info@spmanchester.com).

---

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- A text editor or IDE (VS Code recommended)
- Git installed on your machine
- A GitHub account

### Fork and Clone

1. **Fork** the repository by clicking the "Fork" button on the GitHub repository page.
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/bmp.git
   cd bmp
   ```
3. **Add the upstream remote** to keep your fork in sync:
   ```bash
   git remote add upstream https://github.com/spmanchester/bmp.git
   ```
4. **Verify your remotes**:
   ```bash
   git remote -v
   ```

### Keeping Your Fork Up to Date

Before starting new work, always sync your fork with the upstream repository:

```bash
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```

---

## Development Setup

PixelForge BMP Conversion Suite is a **pure client-side application** — there is no build step, no package manager, and no server required.

**To run the project locally:**

1. Navigate to the project directory.
2. Open `index.html` directly in your browser:
   - Double-click `index.html` in your file explorer, **or**
   - Use a simple local server for a more authentic experience:
     ```bash
     # Using Python 3
     python -m http.server 8080

     # Using Node.js (npx)
     npx serve .
     ```
   - Then visit `http://localhost:8080` in your browser.

That's it. No `npm install`, no build pipeline, no environment variables.

---

## How to Contribute

### Reporting Bugs

Before filing a bug report, please:

- Search [existing issues](https://github.com/spmanchester/bmp/issues) to avoid duplicates.
- Reproduce the issue in the latest version.

When filing a bug report, include:

- **Summary**: A clear, concise description of the bug.
- **Steps to Reproduce**: Numbered steps to consistently reproduce the issue.
- **Expected Behaviour**: What you expected to happen.
- **Actual Behaviour**: What actually happened.
- **Screenshots / Console Logs**: Attach if applicable.
- **Environment**: Browser name + version, OS, screen resolution.
- **Tool Affected**: Which of the 7 BMP tools is affected (e.g., BMP to PNG, BMP to JPEG, etc.).

Use the **Bug Report** issue template on GitHub.

---

### Requesting Features

We love hearing ideas! Before submitting a feature request:

- Check [existing issues](https://github.com/spmanchester/bmp/issues) and [discussions](https://github.com/spmanchester/bmp/discussions) to see if it has already been suggested.
- Consider whether the feature aligns with the project's scope (client-side BMP image conversion).

When filing a feature request, include:

- **Problem Statement**: What problem does this feature solve?
- **Proposed Solution**: Describe your ideal solution.
- **Alternatives Considered**: Any alternative approaches you thought of.
- **Additional Context**: Mockups, examples, or references.

Use the **Feature Request** issue template on GitHub.

---

### Submitting Pull Requests

1. **Create a branch** from `main` using the naming conventions below.
2. **Make your changes** — keep them focused and atomic. One PR per logical change.
3. **Test thoroughly** across browsers (see [PR Checklist](#pull-request-checklist)).
4. **Commit** using [Conventional Commits](#commit-message-conventions).
5. **Push** your branch to your fork:
   ```bash
   git push origin feature/your-feature-name
   ```
6. **Open a Pull Request** against the `main` branch of the upstream repository.
7. Fill in the PR template completely.
8. **Link any related issues** using GitHub keywords (e.g., `Closes #42`).

A maintainer from SPManchester Private Limited will review your PR. Please be responsive to feedback and requested changes.

---

## Branch Naming Conventions

Use the following prefixes to categorise your branch:

| Prefix     | Use Case                                         | Example                          |
|------------|--------------------------------------------------|----------------------------------|
| `feature/` | New features or enhancements                     | `feature/add-webp-preview`       |
| `fix/`     | Bug fixes                                        | `fix/canvas-resize-glitch`       |
| `docs/`    | Documentation updates only                      | `docs/update-contributing-guide` |
| `chore/`   | Maintenance, dependency updates, config changes  | `chore/update-meta-tags`         |
| `style/`   | CSS or visual/UI-only changes                   | `style/improve-dark-mode`        |
| `refactor/`| Code restructuring without changing behaviour    | `refactor/extract-converter-util`|
| `test/`    | Adding or fixing tests                           | `test/add-bmp-parser-tests`      |

Branch names should be **lowercase** and use **hyphens** (not underscores or spaces).

---

## Commit Message Conventions

This project follows the **[Conventional Commits](https://www.conventionalcommits.org/)** specification. Well-formed commit messages make the project history readable and enable automated changelogs.

### Format

```
<type>(<optional scope>): <short description>

[optional body]

[optional footer(s)]
```

### Types

| Type       | When to Use                                                   |
|------------|---------------------------------------------------------------|
| `feat`     | A new feature visible to users                                |
| `fix`      | A bug fix                                                     |
| `docs`     | Documentation changes only                                    |
| `style`    | Formatting, whitespace, semicolons — no logic changes         |
| `refactor` | Code restructuring, no feature or bug change                  |
| `test`     | Adding or updating tests                                      |
| `chore`    | Build process, tooling, maintenance tasks                     |
| `perf`     | Performance improvements                                      |
| `ci`       | CI/CD configuration changes                                   |

### Examples

```
feat(bmp-to-png): add transparency preservation option

fix(canvas): resolve off-by-one error in BMP header parsing

docs: add FAQ section to README

chore: update GitHub Actions workflow to Node 20

style(ui): align toolbar buttons consistently across breakpoints

refactor(converter): extract BMP reader into reusable module
```

### Rules

- Use the **imperative mood** in the description ("add" not "added" or "adds").
- Keep the first line under **72 characters**.
- Reference issues in the footer: `Closes #42` or `Fixes #17`.
- Breaking changes must include `BREAKING CHANGE:` in the footer.

---

## Pull Request Checklist

Before marking your PR as ready for review, confirm the following:

### Functionality
- [ ] The feature or fix works as described in the linked issue.
- [ ] No existing functionality has been broken.
- [ ] Edge cases have been considered and handled.

### Browser Testing
- [ ] Tested in **Google Chrome** (latest stable).
- [ ] Tested in **Mozilla Firefox** (latest stable).
- [ ] Tested in **Apple Safari** (latest stable, if on macOS).
- [ ] Tested in **Microsoft Edge** (latest stable).
- [ ] No unhandled errors or warnings in the browser console.

### Code Quality
- [ ] Code follows the [Code Style Guide](#code-style-guide).
- [ ] No `console.log` statements left in production code (use `console.warn` / `console.error` where appropriate).
- [ ] No commented-out dead code.
- [ ] Variable and function names are descriptive and meaningful.

### Accessibility
- [ ] All interactive elements are keyboard-navigable.
- [ ] Images and icons have appropriate `alt` attributes.
- [ ] Colour contrast meets WCAG 2.1 AA standards (minimum 4.5:1 for normal text).
- [ ] Checked with a screen reader or accessibility audit tool (e.g., Lighthouse, axe DevTools).

### Documentation
- [ ] Inline comments added for complex logic.
- [ ] `README.md` updated if the change affects usage or feature list.
- [ ] Any new configuration or option is documented.

### PR Hygiene
- [ ] Branch is up to date with `main`.
- [ ] Commits follow the Conventional Commits convention.
- [ ] PR title is clear and follows `type: description` format.
- [ ] Related issues are linked (`Closes #XX`).

---

## Code Style Guide

PixelForge BMP Conversion Suite is built with **vanilla HTML, CSS, and JavaScript** — no frameworks, no transpilers, no build tools. Please respect this architecture.

### JavaScript

- **ES6+ only** — use `const`/`let` (never `var`), arrow functions, template literals, destructuring, `async`/`await`, and other modern syntax freely.
- **No external libraries or frameworks** — no jQuery, React, Vue, Lodash, etc.
- **No TypeScript** — the project is intentionally dependency-free.
- Use **camelCase** for variables and functions, **PascalCase** for constructor functions / classes.
- Use **descriptive names** — avoid single-letter variables except in short loop indices.
- Prefer **pure functions** where possible; minimise side effects.
- Handle errors with `try/catch` and provide meaningful user feedback.
- Use **`const`** by default; only use `let` when reassignment is necessary.
- Keep functions **small and focused** — aim for single responsibility.
- Use **JSDoc comments** for public functions:
  ```js
  /**
   * Converts a BMP file to PNG format using the Canvas API.
   * @param {File} file - The source BMP file object.
   * @returns {Promise<Blob>} A promise that resolves to a PNG Blob.
   */
  async function convertBmpToPng(file) { ... }
  ```

### HTML

- Use **semantic HTML5** elements (`<main>`, `<section>`, `<article>`, `<nav>`, `<button>`, etc.).
- All form inputs must have associated `<label>` elements.
- Include appropriate **ARIA attributes** where native semantics are insufficient.
- Validate your HTML using the [W3C Validator](https://validator.w3.org/).

### CSS

- Write **plain CSS** — no SCSS, LESS, or PostCSS.
- Use **CSS custom properties** (variables) for colours, spacing, and typography.
- Follow a **mobile-first** approach with `min-width` media queries.
- Class names use **kebab-case** (e.g., `.converter-panel`, `.upload-btn`).
- Avoid `!important` except as a last resort.
- Group properties logically: positioning → box model → typography → visual → animation.

### File Organisation

- Keep all tools' logic in clearly named, separate JS files or clearly delimited sections.
- Do not minify source files — the source should be human-readable at all times.

---

## Contact

For questions, suggestions, or anything not covered by GitHub Issues, reach out to:

**SPManchester Private Limited**
- 🌐 Website: [www.spmanchester.com](https://www.spmanchester.com)
- 📧 Email: [info@spmanchester.com](mailto:info@spmanchester.com)

We aim to respond to all enquiries within **3 business days**.

---

*Thank you for contributing to PixelForge BMP Conversion Suite. Every contribution — no matter how small — makes a difference. We appreciate your time and effort.*

— **The SPManchester Private Limited Team**
