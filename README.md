# NeuroNet Atlas

An interactive atlas of **network neuroscience in psychiatric conditions**, plus two cellular-scale explainers.

| File | Contents |
|------|----------|
| `index.html` | Main atlas — 6 conditions × 4 network models, methods explainer, transdiagnostic comparison |
| `cortical-column.html` | Six-layer cortical column and canonical microcircuit, animated signal flow |
| `pyramidal-neuron.html` | Pyramidal neuron + interneurons, and a receptor-level zoom on schizophrenia |

**Conditions:** depression · bipolar · schizophrenia · PTSD · OCD · anxiety
**Models:** static functional · dynamic · maximum-entropy landscape · network control theory

## Deploying to GitHub Pages

### Option A — web UI
1. Create a new public repository on GitHub.
2. **Add file → Upload files**, drag in all four files *including the hidden `.nojekyll`*
   (in the macOS file dialog press `Cmd + Shift + .` to reveal hidden files). Commit.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, Folder: `/ (root)`. Save.
4. After ~1 minute the site is live at `https://<username>.github.io/<repo>/`

### Option B — command line
```bash
cd neuronet-atlas-site
git init && git add -A && git commit -m "NeuroNet Atlas"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```
Then enable Pages as in step 3 above.

### Notes
- Keep `.nojekyll` — it stops GitHub mangling the files.
- `index.html` must stay at the repo root.
- The 3D energy landscape loads Three.js from a CDN, so it needs internet on first view. Everything else works offline.
- **Keep all three HTML files in the same folder** — the navigation links between them are relative.

## Disclaimer
Group-level neuroimaging findings for research and education. Schematic illustrations, not diagnostic tools. Not medical advice.
