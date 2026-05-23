# EMA Guideline on Medicinal Products Containing Genetically Modified Cells
## Quality, Non-Clinical and Clinical Aspects

**EMA Reference:** CAT/CPWP/557799/2012  
**Committee:** Committee for Advanced Therapies (CAT)  
**Document type:** EMA Regulatory Guideline  
**Year:** 2012 (active, check EMA website for latest revision)  
**Status:** ⏳ Content extraction in progress  
**Source URL:** https://www.ema.europa.eu/en/documents/scientific-guideline/guideline-quality-non-clinical-clinical-aspects-medicinal-products-containing-genetically-modified_en.pdf  
**Folder:** `EMA/EMA-CAT-Genetically-Modified-Cells/`

---

## Scope

Covers medicinal products where the active substance consists of or contains cells that have been genetically modified to express one or more therapeutic genes, including:

- **CAR-T cell products** (chimeric antigen receptor T-cells)
- **TCR-T cell products** (T-cell receptor-engineered T-cells)
- **NK cell products** (genetically modified natural killer cells)
- Gene-corrected stem cell therapies
- Oncolytic cell-virus combinations

Does **not** cover products solely constituted by naked nucleic acids or non-modified cells.

---

## Key Topics (Placeholder — to be completed on full text extraction)

### 1. Quality Section — Manufacturing

**1.1 Starting Materials**
> _Extract: autologous vs. allogeneic source material, donor eligibility, apheresis product requirements, viral vector starting material specifications_

**1.2 Manufacturing Process**
> _Extract: cell expansion, transduction/transfection conditions, purification, formulation, cryopreservation — critical process parameters_

**1.3 Critical Quality Attributes (CQAs)**
> _Extract: identity (CAR expression), viability, purity (T-cell subset distribution), potency, sterility, adventitious agents, residuals_

**1.4 Specification Setting**
> _Extract: release specifications, shelf-life specifications, justification for CQAs_

### 2. Vector Characterization

> _Extract: vector design, integration profile, RCR/RCL testing requirements, genotoxicity considerations_

### 3. Non-Clinical Requirements

> _Extract: in vitro/in vivo efficacy, safety pharmacology, biodistribution, genotoxicity studies_

### 4. Clinical Requirements

> _Extract: Phase I dose escalation, patient population, follow-up requirements (long-term safety), risk management_

---

## Notable Alerts / Augy's Annotations

> _Add your own annotations here as you review this document — deviations from PIC/S Annex 2, CAR-T-specific nuances, etc._

---

## Comparison: CAR-T Requirements Across Regulators

| Aspect | EMA/CAT (this doc) | FDA (CMC Gene Therapy) | PIC/S Annex 2 | WHO |
|--------|--------------------|------------------------|----------------|-----|
| Autologous chain of identity | Required | Required | Required | Required |
| CAR expression assay (identity) | Required | Required | Required | TBD |
| RCR/RCL testing | Required | Required | Required | Required |
| Potency assay (functional) | Required | Required | Recommended | TBD |
| Long-term follow-up | Required (15 yr) | Required (15 yr) | Recommended | TBD |

> Update this table after content extraction.

---

## How to Populate This File

1. Download from EMA website using source URL above
2. Run `python gmp_engine.py md EMA-CAT-Genetically-Modified-Cells` after placing PDF in folder
3. Replace placeholders with extracted content
4. Update `knowledge/EMA/INDEX.md`
5. Update `ROADMAP.md` status to ✅ Done
