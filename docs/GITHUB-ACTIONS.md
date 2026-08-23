# GitHub Actions — Automation Setup

：2026-04-09

> **Note:** The three GitHub Actions workflows described below (, , ) were removed during migration to  to allow clean publishing without a  token scope. They can be re-added from the original  repo if needed.


---

## 

 repo  3  GitHub Actions workflow，， Claude Code session  HTML 。

```
 push PDF → Actions  MD →  Claude  HTML sections → Actions merge + deploy
```

---

## Workflow 

|  |  |  |
|---|---|---|
| `validate-json.yml` | Validate JSON | push `reports.json`  `tag-classes.json` |
| `auto-md.yml` | Generate Knowledge MD | push `Raw pdfs/`、push `gmp_engine.py`、 07:00 TWN |
| `auto-merge-deploy.yml` | Merge HTML and Deploy | push `**/sections/`、 07:00 TWN、 |

---

##  Workflow 

### 1. Validate JSON（`validate-json.yml`）

****： push `reports.json`  `tag-classes.json`

****：
-  `python -m json.tool`  JSON 
- （、） GitHub 

****：`reports.json` （dashboard、merge engine ），。

---

### 2. Generate Knowledge MD（`auto-md.yml`）

****：
- Push  PDF  `Raw pdfs/`
- Push  `gmp_engine.py`
-  7 （cron: `0 23 * * *` UTC）

****：
1.  `pymupdf4llm`
2.  `python gmp_engine.py md --all`
   -  `PDF_FILES` dict  report， PDF  →  MD
   -  PDF mapping  report， `source/*.txt` fallback
3.  PDF  `Raw pdfs/processed/`
   - ：PDF  `Raw pdfs/` ****  `knowledge/*.md` 
   - ：MD  PDF ， cron 
4. Commit `knowledge/`  `Raw pdfs/`  repo

****： Claude API， Python + pymupdf4llm。

---

### 3. Merge HTML and Deploy（`auto-merge-deploy.yml`）

****：
- Push `**/sections/**`（Claude  HTML sections ）
-  7 （cron: `0 23 * * *` UTC）
- （ report ID）

****：

|  | merge  |
|---|---|
| Push sections/ |  report  sections ， merge  |
| cron  |  `merge --all`， sections  report |
|  |  `merge <report_id>` |

：
- Commit  repo（`output/*-Complete.html`、`knowledge/` ）
- Deploy  GitHub Pages（`gh-pages` branch）

**GitHub Pages **：`https://augycodez.github.io/GMP-Guidelines/`

---

## 

```
[] push PDF  Raw pdfs/
        ↓
[Actions] gmp_engine.py md --all
→  knowledge/*/XXX-Complete.md
→  PDF  Raw pdfs/processed/
→ commit  repo
        ↓
[] git pull，Claude Code session
→ Claude  MD， HTML sections
→ push sections/*.html
        ↓
[Actions]  sections/ 
→ gmp_engine.py merge <report_id>
→  output/*-Complete.html
→ Deploy  GitHub Pages
→ commit  repo
```

---

## 

， Claude Code session ：

1. ** HTML sections ** — Claude  MD →  `sections/*.html`
2. **reports.json ** —  report  metadata、section_map
3. **knowledge/INDEX.md ** —  report 
4. **** —  index.html、Complete.html 

---

## 

-  repo ** repo**，GitHub Actions **、**
-  Anthropic API， token 

---

## 

**Q：cron  merge --all， sections，？**
A：。workflow  `git diff --staged --quiet || git commit`， commit。

**Q：PDF  processed/ ， md --all ？**
A：。`generate_md_from_pdf()`  `Raw pdfs/`，processed/  PDF 。

**Q： report  PDF  `PDF_FILES` dict，？**
A：engine fallback  `source/*.txt`。 txt， WARNING 。PDF （ MD ）。
