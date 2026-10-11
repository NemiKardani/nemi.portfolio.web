# Workspace Guidelines - Deployment Target (nemi.portfolio.web)

This repository is the **production static hosting target** for Nemi Kardani's Portfolio (hosted via GitHub Pages).

---

## 1. Important Role & Constraint

> **CRITICAL RULE**: Do not edit HTML, CSS, or JS files directly in this repository.
- **Source of Truth**: All source code, React components, Three.js scenes, and styling reside in the sibling project:
  [nemi-portfulio-next](file:///Users/nemi_s_mac/Documents/Development/Flutter_Devlopment/My%20Portfulio/nemi-portfulio-next)
- **Deployment Flow**:
  1. Make edits in `nemi-portfulio-next`.
  2. Run `npm run build` in `nemi-portfulio-next` to produce `out/`.
  3. Synchronize `nemi-portfulio-next/out` to this directory (`nemi.portfolio.web`).
  4. Or run the automated script:
     ```bash
     bash "../nemi-portfulio-next/.agents/skills/portfolio-build-and-sync/scripts/sync.sh"
     ```
  5. Review `git status` here and commit to `main`.

---

## 2. Post-Implementation Update Rule

> **"Update context, rules, skills, and MCP according to changes after implementation if need to update."**
- Any architectural changes, domain changes, or workflow modifications must be mirrored back into `nemi-portfulio-next/GEMINI.md` and `.agents/`.
