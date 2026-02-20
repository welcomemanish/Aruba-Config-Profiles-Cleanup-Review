# Contributing to Aruba CPCR

Thank you for your interest in contributing to the **Aruba CPCR — Config Profiles Cleanup Review** project! Contributions of all kinds are welcome — bug reports, feature suggestions, keyword additions, UI improvements, and documentation fixes.

---

## Getting Started

1. **Fork** the repository on GitHub
2. **Clone** your fork locally
3. Make your changes to `Aruba CPCR - By Manish Sharma.html`
4. Test your changes by opening the HTML file in a browser and uploading a sample tech-support log
5. **Submit a Pull Request** with a clear description of your changes

---

## Ways to Contribute

### 🐛 Reporting Bugs

If you find a bug or unexpected behaviour:

- Open a [GitHub Issue](../../issues)
- Include the **browser and version** you are using
- Describe the **steps to reproduce** the issue
- If possible, describe what the expected behaviour should be
- Do **not** attach real customer log files — use sanitized/anonymized samples

### 💡 Suggesting Features or Enhancements

Have an idea for a new feature or improvement?

- Open a [GitHub Issue](../../issues) with the label `enhancement`
- Describe the use case and why it would be valuable
- If you have a proposed implementation, feel free to share it

### 🔑 Adding New Keywords / Profile Types

The keyword list is the core of the parser. If you notice a profile type that is not currently being scanned:

1. Identify the exact CLI keyword as it appears in `show running-config` output
2. Add it to the `KEYWORDS` array in the `<script>` section of the HTML file
3. Test it against a config that contains the keyword
4. Submit a Pull Request with a brief description of what the profile type represents

### 📝 Improving Documentation

Documentation improvements are always welcome:

- Fix typos or unclear wording in the README
- Add examples or screenshots
- Improve the usage instructions

---

## Code Style Guidelines

Since this is a single-file HTML/CSS/JS tool:

- Keep all code in the single HTML file — do not split into separate files
- Follow the existing code style and commenting conventions (use `// ═══` section headers for JS)
- Use CSS variables for all colours — do not hardcode colour values
- Ensure all three themes (dark, gray, light) are tested when making UI changes
- Keep the tool fully functional **without any internet connection** (no CDN dependencies for core functionality; Google Fonts is acceptable as a progressive enhancement)

---

## Testing Your Changes

Before submitting a Pull Request, please verify:

- [ ] The tool loads correctly in Chrome, Edge, and Firefox
- [ ] Drag-and-drop file upload works
- [ ] Auto-analysis triggers immediately on file selection
- [ ] The stats panel displays correct counts
- [ ] Search, filter, and sort functions work correctly
- [ ] CSV export downloads correctly
- [ ] All three themes (Dark, Gray, Light) render correctly
- [ ] The tool works on a reasonably large log file (10 MB+) without freezing

---

## Pull Request Process

1. Ensure your PR description clearly explains **what** was changed and **why**
2. Reference any related issues (e.g., `Closes #12`)
3. Keep PRs focused — one feature or fix per PR is preferred
4. Be responsive to review feedback

---

## Questions?

Feel free to open an issue or reach out via GitHub at [github.com/welcomemanish](https://github.com/welcomemanish).
