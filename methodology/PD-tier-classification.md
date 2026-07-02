# PD Tier Classification Methodology

**Constituency:** N03 Pemanis (P146 Muar)  
**Version:** V1 (DUN Profiling Workflow)  
**Date:** 2026-07-02

---

## Classification Thresholds

Polling districts are classified into tiers based on ethnic composition (Malay % and Chinese %). This enables strategic resource allocation and targeted messaging.

### Tier Definitions

| Tier | Threshold | Description | Strategic Implication |
|------|-----------|-------------|----------------------|
| **Malay Super Safe** | Malay ≥80% | Overwhelming Malay majority | BN/PN stronghold; PH non-competitive |
| **Malay Safe** | Malay 60-79% | Clear Malay majority | BN-favored; PN competitive; PH underdog |
| **Malay-Leaning Mixed** | Malay 50-59% | Slight Malay majority | Competitive; turnout + persuasion both matter |
| **True Mixed** | Malay 45-49%, Chinese 45-49% | No clear ethnic majority | Tossup; highest volatility |
| **Chinese-Leaning Mixed** | Chinese 50-59%, Malay 35-49% | Slight Chinese majority | PH-favored; BN needs retention play |
| **Chinese Safe** | Chinese 60-74% | Clear Chinese majority | PH stronghold; BN damage limitation |
| **Chinese Super Safe** | Chinese ≥75% | Overwhelming Chinese majority | PH lock; BN/PN non-competitive |

---

## N03 Pemanis PD Classification (Applied)

### Malay Super Safe (≥80% Malay)

| PD | Total Voters | Malay % | Chinese % | Classification |
|----|-------------|---------|-----------|----------------|
| PEMANIS 1 | 2,992 | 98.6% | 0.5% | Malay Super Safe |
| PEMANIS 2 | 2,957 | 93.0% | 5.6% | Malay Super Safe |
| FELDA MEDOI | 2,006 | 99.3% | 0.1% | Malay Super Safe |
| BUMBUN | 1,432 | 95.0% | 2.2% | Malay Super Safe |

**Total Voters:** 9,387 (30.8% of electorate)  
**Strategic Note:** BN base; PN spoiler potential; PH symbolic presence only

---

### Malay Safe (60-79% Malay)

| PD | Total Voters | Malay % | Chinese % | Classification |
|----|-------------|---------|-----------|----------------|
| KAMPONG JAWA | 6,405 | 65.3% | 32.0% | Malay Safe |
| GUBAH | 1,820 | 65.7% | 20.4% | Malay Safe |
| SULIR | 1,584 | 75.5% | 11.2% | Malay Safe |

**Total Voters:** 9,809 (32.2% of electorate)  
**Strategic Note:** BN favored but contestable; PN competitive; PH needs Malay moderation

---

### Chinese-Leaning Mixed (50-59% Chinese, 35-49% Malay)

| PD | Total Voters | Malay % | Chinese % | Classification |
|----|-------------|---------|-----------|----------------|
| KAMPONG MENGKUDU | 1,007 | 48.8% | 48.5% | **True Mixed (Tossup)** |

**Total Voters:** 1,007 (3.3% of electorate)  
**Strategic Note:** **KEY BATTLEGROUND** — Only truly competitive PD; winner takes seat

---

### Chinese Safe (60-74% Chinese)

| PD | Total Voters | Malay % | Chinese % | Classification |
|----|-------------|---------|-----------|----------------|
| TAHANG RIMAU | 2,023 | 40.6% | 51.2% | Chinese Safe |
| JALAN BULOH KASAP | 577 | 44.9% | 53.4% | Chinese Safe |

**Total Voters:** 2,600 (8.5% of electorate)  
**Strategic Note:** PH favored; BN needs retention play; turnout critical

---

### Chinese Super Safe (≥75% Chinese)

| PD | Total Voters | Malay % | Chinese % | Classification |
|----|-------------|---------|-----------|----------------|
| PEKAN JABI | 3,736 | 28.7% | 66.4% | Chinese Safe (not Super Safe) |
| KAMPONG TENGAH | 3,152 | 28.6% | 68.1% | Chinese Safe |
| KAMPONG ABDULLAH SELATAN | 767 | 6.8% | 92.5% | Chinese Super Safe |

**Total Voters:** 7,655 (25.1% of electorate)  
**Strategic Note:** PH stronghold; GOTV priority; BN/PN non-competitive

---

## Classification Logic (Pseudocode)

```python
def classify_pd(malay_pct, chinese_pct):
    if malay_pct >= 80:
        return "Malay Super Safe"
    elif malay_pct >= 60:
        return "Malay Safe"
    elif malay_pct >= 50:
        return "Malay-Leaning Mixed"
    elif chinese_pct >= 75:
        return "Chinese Super Safe"
    elif chinese_pct >= 60:
        return "Chinese Safe"
    elif chinese_pct >= 50:
        return "Chinese-Leaning Mixed"
    elif 45 <= malay_pct <= 49 and 45 <= chinese_pct <= 49:
        return "True Mixed (Tossup)"
    else:
        return "Other Mixed"
```

---

## Strategic Application

### BN Resource Allocation

| Tier | Priority | Resource % | Rationale |
|------|----------|------------|-----------|
| Malay Super Safe | HIGH | 40% | Base mobilization; prevent PN inroads |
| Malay Safe | HIGH | 30% | Hold 60%+ vote share |
| True Mixed | MEDIUM | 15% | Persuasion play (moderate Malay + Chinese) |
| Chinese PDs | LOW | 15% | Damage control; retain 30-40% via MCA |

### PH Resource Allocation

| Tier | Priority | Resource % | Rationale |
|------|----------|------------|-----------|
| Chinese Super Safe | HIGH | 40% | GOTV maximization (80%+ turnout target) |
| Chinese Safe | HIGH | 25% | GOTV + retention (75%+ turnout target) |
| True Mixed | HIGH | 20% | Persuasion play (win PD) |
| Malay PDs | LOW | 15% | Symbolic presence; moderate Malay outreach |

### PN-MIPP Resource Allocation

| Tier | Priority | Resource % | Rationale |
|------|----------|------------|-----------|
| Malay Super Safe | HIGH | 50% | Protest vote mobilization (25%+ target) |
| Malay Safe | MEDIUM | 30% | Spoiler role (15-20% target) |
| True Mixed | LOW | 10% | Indian + protest Malay consolidation |
| Chinese PDs | LOW | 10% | Symbolic presence; Indian voters |

---

## Confidence Tags

| Classification | Confidence | Justification |
|----------------|------------|---------------|
| All PD tier assignments | [HIGH] | Derived from SPR XLSX (official primary source) |
| Strategic implications | [MEDIUM] | Based on historical patterns + demographic math |
| Resource allocation recommendations | [LOW] | SPECULATION: actual optimal allocation depends on ground intelligence |

---

**Methodology Owner:** DUN Profiling V1 Workflow  
**Last Updated:** 2026-07-02  
**Classification:** TLP:AMBER — Internal Campaign Use Only
