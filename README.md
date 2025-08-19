
# Auto-built Resume (LaTeX → PDF via GitHub Actions)

This repository compiles `resume.tex` to `resume.pdf` on every push to `main`.
The built PDF is committed back to the repo and also uploaded as a workflow artifact.

## Quick Start

1. **Create a new GitHub repo** (e.g., `resume`), set default branch to `main`.
2. Push these files:
   ```bash
   git init
   git add .
   git commit -m "init: LaTeX resume with auto-build"
   git branch -M main
   git remote add origin https://github.com/<USERNAME>/<REPO>.git
   git push -u origin main
   ```

3. **Enable GitHub Pages (optional, for a clean URL):**
   - Go to *Settings → Pages*.
   - Set *Branch* to `main` and *Folder* to `/ (root)`.
   - The PDF will then be available at:
     `https://<USERNAME>.github.io/<REPO>/resume.pdf`

4. **Edit `resume.tex`** and push. The workflow will:
   - Compile to `resume.pdf`
   - Commit `resume.pdf` to the repo
   - Upload an artifact named `resume-pdf`

## Badge (optional)

Add this to your README to show build status:

```
![Build LaTeX](https://github.com/<USERNAME>/<REPO>/actions/workflows/build-resume.yml/badge.svg)
```

## Notes

- The workflow uses [`xu-cheng/latex-action`](https://github.com/xu-cheng/latex-action) and `latexmk`.
- Keep your LaTeX minimal or add packages as needed.
- We purposely **track** `resume.pdf` to serve via GitHub Pages and for easy sharing.

