# Contributing to NueWave-CSS

Thank you for considering contributing to **NueWave-CSS**, a lightweight, semantic CSS framework for [Nue](https://nuejs.org/). We welcome contributions from the community to improve the framework, add features, or fix bugs. This guide explains how to get started.

## Getting Started

1. **Fork the Repository**:

   - Fork [nuewave-css](https://github.com/your-username/nuewave-css) on GitHub.
   - Clone your fork:
     ```bash
     git clone https://github.com/your-username/nuewave-css.git
     cd nuewave-css
     ```

2. **Install Dependencies**:

   - Ensure [Bun](https://bun.sh/) is installed, as NueWave uses Bun for development and testing.
   - Install Nue globally (if not already):
     ```bash
     bun add -g nue
     ```

3. **Set Up the Demo**:
   - The `demo/` folder contains a sample Nue project to test changes.
   - Link the `dist/` folder for testing:
     ```bash
     cd demo
     ln -s ../dist ../node_modules/nuewave-css/dist
     ```
   - Run the demo:
     ```bash
     nue dev
     ```
   - Open `http://localhost:8080` (or Bun’s default port) to preview.

## Making Changes

1. **Create a Branch**:

   - Use a descriptive branch name:
     ```bash
     git checkout -b feature/add-nw-modal
     ```

2. **Edit Files**:

   - **CSS Files**: Modify `src/reset.css`, `src/base.css`, or `src/components.css` (then run `bun run build` to copy to `dist/`).
     - Keep styles semantic (no utility classes).
     - Use existing CSS variables (e.g., `--primary`, `--space-md`) for consistency.
     - Ensure components are lightweight and responsive.
   - **Demo**: Update `demo/` files to test new features (e.g., add a new component to `pages/index.html`).
   - **Docs**: Update `README.md` or this file if adding features.

3. **Test Your Changes**:

   - Run the demo (`cd demo && nue dev`) and check:
     - New styles render correctly in `pages/index.html` and `components/form.html`.
     - Responsive behavior works (e.g., `.nw-grid--2` collapses on mobile).
     - Island components (e.g., form) maintain interactivity.
   - Build the demo:
     ```bash
     cd demo && nue build
     ```
     - Verify `dist/` output includes updated `nuewave.css` and layers.

4. **Commit Changes**:
   - Write clear commit messages:
     ```bash
     git commit -m "Add .nw-modal component with responsive styles"
     ```

## Submitting a Pull Request

1. **Push to Your Fork**:

   ```bash
   git push origin feature/add-nw-modal
   ```

2. **Open a Pull Request**:

   - Go to the [nuewave-css repo](https://github.com/your-username/nuewave-css).
   - Click "New Pull Request" and select your branch.
   - Provide a clear title and description:
     - What you changed (e.g., "Added `.nw-modal` component").
     - Why it’s needed (e.g., "Supports modal dialogs in Nue islands").
     - Screenshots or demo updates, if applicable.
   - Reference any related issues (e.g., "Fixes #12").

3. **Code Review**:
   - Respond to feedback promptly.
   - Ensure changes align with NueWave’s goals:
     - Lightweight (~8KB total).
     - Semantic, no utilities.
     - Compatible with Nue’s islands and templates.

## Contribution Ideas

- **New Components**: Add classes like `.nw-nav`, `.nw-modal`, `.nw-alert`.
- **Theming**: Expand CSS variables (e.g., `--success`, `--danger`).
- **Bug Fixes**: Address rendering issues or browser inconsistencies.
- **Docs**: Improve `README.md` examples or add tutorials.
- **Tests**: Propose lightweight CSS testing tools (e.g., stylelint).

## Code Style

- **CSS**:
  - Use kebab-case for classes (e.g., `.nw-button--sm`).
  - Leverage `@layer` for organization.
  - Keep selectors simple (low specificity).
  - Follow Nue’s CSS-first philosophy (semantic over utility).
- **Commits**: Follow [Conventional Commits](https://www.conventionalcommits.org/) (e.g., `feat: add .nw-modal`, `fix: correct grid spacing`).

## Questions?

- Open an [issue](https://github.com/your-username/nuewave-css/issues) for discussion.
- Reach out via GitHub for clarification.

Thank you for helping make NueWave-CSS better for the Nue community!
