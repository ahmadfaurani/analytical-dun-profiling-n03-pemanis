# SPR Electoral Roll Data Sources

**Constituency:** N03 Pemanis (P146 Muar)  
**Data As Of:** 2026-07-02  
**Access Date:** 2026-07-02

---

## Primary Source

**File:** `8_PEMANIS_as_of_190626.xlsx` (SPR Electoral Roll)  
**Source Type:** Official primary source (Suruhanjaya Pilihan Raya)  
**Access Method:** Direct file download  
**CVS Status:** ✅ Primary source — no cross-reference required for voter counts

### Data Fields Extracted

| Field | Description | CVS Tier |
|-------|-------------|----------|
| Polling District Code | 8-digit PD identifier | Tier 1 |
| Polling District Name | Official PD name (e.g., PEMANIS 1) | Tier 1 |
| Total Voters | Registered voters (PEMILIH BERDAFTAR) | Tier 1 |
| Malay Voters | Ethnic breakdown (MELAYU) | Tier 1 |
| Chinese Voters | Ethnic breakdown (CINA) | Tier 1 |
| Indian Voters | Ethnic breakdown (INDIA) | Tier 1 |
| Other Voters | Other ethnicities (LAIN-LAIN) | Tier 1 |
| Male Voters | Gender breakdown (LELAKI) | Tier 1 |
| Female Voters | Gender breakdown (PEREMPUAN) | Tier 1 |
| 18-29 Voters | Youth voters (UNDI18 cohort) | Tier 1 |

---

## Constituency Code Discrepancy (CVS NOTICE)

**Issue:** SPR file shows N02, official sources list as N03

| Source | Code | Notes |
|--------|------|-------|
| SPR Electoral Roll XLSX | N02 | File naming convention |
| Utusan Malaysia (2026-06) | N03 | Official nomination announcement |
| Berita Harian (2026-06) | N03 | Candidate nomination coverage |
| Wikipedia 2022 results | N03 | Historical reference |

**Resolution:** Used N03 for consistency with official announcements. Discrepancy documented in all briefs with CVS NOTICE.

**Confidence:** [HIGH] — SPR file is authoritative for voter counts; N03 code is authoritative for public reference

---

## Data Quality Notes

- **Completeness:** 100% (all 13 polling districts present)
- **Accuracy:** Verified against SPR official publication
- **Timeliness:** As of 19 June 2026 (latest available)
- **Format:** XLSX (Excel spreadsheet)

---

## Usage Notes

- SPR XLSX is the **official primary source** for voter counts
- No cross-reference required for Tier 1 claims (voter numbers, PD names)
- Derived analysis (PD tier classification, turnout modelling) tagged [MEDIUM]
- All numerical claims in Step 1 brief cite "SPR Electoral Roll 2026"

---

**Accessed:** 2026-07-02  
**Stored:** `/home/p62operator/memory/n02-pemanis-demographic-brief-20260702.md` (source brief)  
**Classification:** TLP:AMBER — Internal Campaign Use Only
