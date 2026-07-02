# CVS Compliance Statement

**Constituency:** N03 Pemanis (P146 Muar)  
**Analysis Date:** 2026-07-02  
**Workflow:** DUN Profiling V1

---

## Core Truth Validation System (CVS) Application

This analysis follows the mandatory CVS protocol for all electoral intelligence outputs. All briefs have passed the validation gate (`./tools/truth-validator/validate.sh`).

---

## Step-by-Step CVS Compliance

### Step 1: Demographics (SPR XLSX)

**Source:** SPR Electoral Roll 2026 (official primary source)  
**CVS Status:** ✅ Compliant

- **Tier 1 Claims:** All voter counts, ethnic breakdowns, PD names sourced directly from SPR XLSX
- **Multi-Source Verification:** Not required (SPR = official primary source)
- **Confidence Tags:** [HIGH] for all SPR data, [MEDIUM] for derived analysis (PD tier classification)
- **Speculation:** None (factual data only)

### Step 2: Candidate Profiling

**Sources:** Utusan Malaysia, Berita Harian, Wikipedia, party announcements  
**CVS Status:** ✅ Compliant

- **Tier 1 Claims:** Candidate names, parties, ages verified via ≥2 independent sources
- **Multi-Source Verification:** Applied to all candidate nominations
- **Confidence Tags:** [HIGH] for verified claims, [MEDIUM/LOW] for single-source or analytical claims
- **Speculation:** Strategic assessments tagged [MEDIUM/LOW] with assumptions stated

### Step 3: Historical Performance

**Sources:** Wikipedia 2022 results, ElectionData.MY, news archives, SPR historical data  
**CVS Status:** ✅ Compliant

- **Tier 1 Claims:** Vote counts, turnout %, majorities cross-referenced across ≥2 sources
- **Multi-Source Verification:** 2018/2022 results verified via Wikipedia + ElectionData.MY + news
- **Confidence Tags:** [HIGH] for verified results, [MEDIUM] for turnout modelling, [LOW] for projections
- **Speculation:** All scenario projections prefixed with `SPECULATION:` or `SCENARIO:`

### Step 4: Master Operational Brief

**Sources:** Synthesis of Steps 1-3 briefs  
**CVS Status:** ✅ Compliant

- **Tier 1 Claims:** All numerical claims reference source documents (Steps 1-3)
- **Multi-Source Verification:** Inherited from input briefs
- **Confidence Tags:** All analytical claims tagged [HIGH/MEDIUM/LOW] with justification
- **Speculation:** Victory probability models prefixed with `SPECULATION:`; assumptions explicitly listed

---

## Confidence Tag Legend

| Tag | Meaning | Application |
|-----|---------|-------------|
| **[HIGH]** | Verified via ≥2 independent sources or official primary source | SPR voter counts, election results, candidate names |
| **[MEDIUM]** | Reasonable inference from multiple data points or single-source verified | Turnout modelling, demographic alignment, strategic assessments |
| **[LOW]** | Speculative, depends on unverified assumptions | Vote projections, victory scenarios, candidate vulnerabilities |

---

## Speculation Demarcation

All predictive claims are explicitly flagged:

- `SPECULATION:` — Forward-looking claims without empirical basis
- `SCENARIO:` — Conditional projections (if-then modelling)

**Example:**  
> SPECULATION: Turnout elasticity assumes youth skew pro-PH (60%+ youth turnout → PH gains), older voters skew pro-BN. Actual elasticity unknown.

---

## Conflict Resolution

No major conflicts detected. Minor discrepancy noted:

- **Constituency Code:** SPR file shows N02, official sources (Utusan Malaysia, BH) list as N03
- **Resolution:** Documented in brief with CVS NOTICE; used N03 for consistency with official announcements

---

## Validation Gate Confirmation

All 4 brief documents passed the truth validator:

```bash
./tools/truth-validator/validate.sh briefs/n03-pemanis-demographic-brief-20260702.md    ✅ PASS
./tools/truth-validator/validate.sh briefs/n03-pemanis-candidate-demographic-brief-20260702.md  ✅ PASS
./tools/truth-validator/validate.sh briefs/n03-pemanis-historical-performance-brief-20260702.md ✅ PASS
./tools/truth-validator/validate.sh briefs/n03-pemanis-master-operational-brief-20260702.md     ✅ PASS
```

**Validation Requirements Met:**
- [x] All Tier 1 numbers verified against source
- [x] All names double-checked (spelling, position, party)
- [x] All citations include file#line or URL
- [x] Confidence tags applied to Tier 2 claims
- [x] Tier 3 speculation clearly demarcated
- [x] Math shown explicitly for analytical claims

---

## Source Verification Summary

| Step | Primary Sources | Verification Method | Status |
|------|-----------------|---------------------|--------|
| Step 1 | SPR Electoral Roll 2026 | Official primary source | ✅ |
| Step 2 | Utusan Malaysia, BH, Wikipedia | Multi-source cross-reference | ✅ |
| Step 3 | Wikipedia, ElectionData.MY, news | Multi-source cross-reference | ✅ |
| Step 4 | Steps 1-3 briefs | Inherited verification | ✅ |

---

**Validated By:** DUN Profiling V1 Workflow  
**Validation Date:** 2026-07-02  
**Classification:** TLP:AMBER — Internal Campaign Use Only
