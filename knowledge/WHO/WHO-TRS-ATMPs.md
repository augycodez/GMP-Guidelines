# WHO Guidelines on Cell and Gene Therapy Products (2022)

**Source:** World Health Organization (WHO)  
**Document type:** Technical Report / Regulatory Guideline  
**Year:** 2022  
**Status:** ⏳ Content extraction in progress  
**Source URL:** https://www.who.int/publications/m/item/who-guidelines-on-cell-and-gene-therapy  
**Folder:** `WHO/WHO-TRS-ATMPs/`

---

## Scope

These WHO guidelines cover GMP and quality requirements for:

- Cell therapy products (including CAR-T, tumor-infiltrating lymphocytes, dendritic cells)
- Gene therapy products (viral and non-viral vectors)
- Combined cell and gene therapy (CAR-T and other genetically modified cell products)
- Tissue-engineered products
- Starting materials and raw materials for ATMP manufacture

Applicable to manufacturers seeking WHO prequalification and countries using WHO standards as the national GMP framework.

---

## Key Topics (Placeholder — to be completed on full text extraction)

### 1. Facility and Equipment Requirements
> _Extract from PDF: cleanroom classification requirements for CGT manufacturing, segregation requirements, closed vs. open processing, isolator use_

### 2. Starting Materials
> _Extract from PDF: donor eligibility, cell sourcing, viral vector starting materials, plasmid DNA requirements_

### 3. Process Controls
> _Extract from PDF: critical quality attributes, in-process controls, hold times, cell expansion monitoring_

### 4. Quality Control Testing
> _Extract from PDF: identity, purity, potency, sterility, mycoplasma, adventitious agents, replication-competent retrovirus/lentivirus_

### 5. Validation Requirements
> _Extract from PDF: process validation lifecycle, cleaning validation for multi-product facilities, aseptic process simulation_

### 6. Documentation and Traceability
> _Extract from PDF: batch records, chain of identity, patient traceability for autologous products_

### 7. Distribution and Cold Chain
> _Extract from PDF: cryopreservation, cold chain requirements, transport validation for ATMPs_

---

## Notable Requirements / Alerts

> _To be completed after full text extraction_

---

## Comparison Notes

| Aspect | WHO (this doc) | EMA/CAT | PIC/S Annex 2 | FDA |
|--------|---------------|---------|----------------|-----|
| Cleanroom grade for aseptic fill | TBD | Grade A/B | Grade A/B | ISO 5 |
| Autologous traceability | TBD | Required | Required | Required |
| Potency testing | TBD | Required pre-release | Required | Required |
| Viral safety testing | TBD | Extensive | Extensive | Extensive |

> Update this table after content extraction.

---

## How to Populate This File

1. Obtain WHO guideline PDF from official WHO website (link above)
2. Run `python gmp_engine.py md WHO-TRS-ATMPs` after placing PDF in `WHO/WHO-TRS-ATMPs/source/`
3. Replace placeholder sections above with extracted content
4. Update `knowledge/WHO/INDEX.md` routing table
5. Update `ROADMAP.md` status to ✅ Done
