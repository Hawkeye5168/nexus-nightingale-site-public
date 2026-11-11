# Public dossier revalidation — 2026-11-07

Claim-level check of the fifteen public disease pages against UniProt, Orphanet, ClinicalTrials.gov, RCSB PDB and PubMed.
Only the claims marked **CURRENT** or **CROSS-REFERENCED** were re-checked in this pass. Prevalence and most drug-approval dates remain **UNVERIFIED** and are not presented as clinical validation.

## Summary

| Check | Result |
|---|---:|
| Pages | 15 |
| UniProt identity/gene/length current | 15/15 |
| ClinicalTrials.gov total current | 15/15 |
| ClinicalTrials.gov total stale | 0/15 |
| Orphanet entry current | 15/15 |
| OMIM id current | 15/15 |
| OMIM conflicts found and corrected | 1 |
| Orphanet blocked by bot check | 0/15 |
| PDB entries checked | 1 |
| Key PMID resolved | 15/15 |
| Hard identity conflicts | 0 |

## Per-page status

| Page | Gene | UniProt | Length | Orphanet | OMIM | CT.gov total | Overall |
|---|---|---|---:|---|---|---|---:|
| hutchinson-gilford-progeria | LMNA | P02545 | 664 | CURRENT | CROSS-REFERENCED | 11 (CURRENT) | CURRENT (checked claims) |
| friedreich-ataxia | FXN | Q16595 | 210 | CURRENT | CROSS-REFERENCED | 115 (CURRENT) | CURRENT (checked claims) |
| lesch-nyhan-syndrome | HPRT1 | P00492 | 218 | CURRENT | CROSS-REFERENCED | 7 (CURRENT) | CURRENT (checked claims) |
| huntington-disease | HTT | P42858 | 3142 | CURRENT | CROSS-REFERENCED | 302 (CURRENT) | CURRENT (checked claims) |
| duchenne-muscular-dystrophy | DMD | P11532 | 3685 | CURRENT | CROSS-REFERENCED | 503 (CURRENT) | CURRENT (checked claims) |
| gaucher-disease | GBA1 | P04062 | 536 | CURRENT | CROSS-REFERENCED | 183 (CURRENT) | CURRENT (checked claims) |
| fabry-disease | GLA | P06280 | 429 | CURRENT | CROSS-REFERENCED | 258 (CURRENT) | CURRENT (checked claims) |
| pompe-disease | GAA | P10253 | 952 | CURRENT | CROSS-REFERENCED | 180 (CURRENT) | CURRENT (checked claims) |
| ttr-amyloidosis | TTR | P02766 | 147 | CURRENT | CROSS-REFERENCED | 270 (CURRENT) | CURRENT (checked claims) |
| alpha-1-antitrypsin-deficiency | SERPINA1 | P01009 | 418 | CURRENT | CROSS-REFERENCED | 147 (CURRENT) | CURRENT (checked claims) |
| cystic-fibrosis | CFTR | P13569 | 1480 | CURRENT | CROSS-REFERENCED | 1784 (CURRENT) | CURRENT (checked claims) |
| angelman-syndrome | UBE3A | Q05086 | 875 | CURRENT | CROSS-REFERENCED | 56 (CURRENT) | CURRENT (checked claims) |
| myotonic-dystrophy-1 | DMPK | Q09013 | 629 | CURRENT | CROSS-REFERENCED | 180 (CURRENT) | CURRENT (checked claims) |
| neonatal-diabetes | KCNJ11 | Q14654 | 390 | CURRENT | CURRENT | 5 (CURRENT) | CURRENT (checked claims) |
| wilson-disease | ATP7B | P35670 | 1465 | CURRENT | CROSS-REFERENCED | 84 (CURRENT) | CURRENT (checked claims) |

## Prevalence comparison

Public prevalence text remains **UNVERIFIED**; the Orphanet range is shown for comparison only.

| Page | Public claim (UNVERIFIED) | Orphanet range |
|---|---|---|
| hutchinson-gilford-progeria | ~1 in 4 million (commonly cited; some sources state 1 in 8 million) — UNVERIFIED exact figure this session, requires con | <1 / 1 000 000 |
| friedreich-ataxia | 1–9 per 100,000 (Orphanet); ~1 in 20,000–1 in 50,000 in people of Caucasian descent | 1-9 / 100 000 |
| lesch-nyhan-syndrome | ~1 in 380,000 (commonly cited; X-linked, almost exclusively males) — UNVERIFIED exact figure this session | 1-9 / 1 000 000 |
| huntington-disease | ~1 in 10,000 (Caucasian); ~30,000 symptomatic in US — commonly cited; UNVERIFIED exact figure this session | 1-9 / 100 000 |
| duchenne-muscular-dystrophy | ~1 in 3,500-5,000 live male births (commonly cited) — UNVERIFIED exact figure this session | 1-9 / 100 000 |
| gaucher-disease | ~1 in 40,000-60,000 general population; ~1 in 850 in Ashkenazi Jewish population (commonly cited) — UNVERIFIED exact fig | 1-9 / 100 000 |
| fabry-disease | ~1 in 40,000-60,000 males (classic form); higher in some populations — commonly cited; UNVERIFIED exact figure this sess | 1-5 / 10 000 |
| pompe-disease | ~1 in 40,000 (all forms combined); infantile form ~1 in 138,000 — commonly cited; UNVERIFIED exact figure this session | Unknown |
| ttr-amyloidosis | ~1 in 100,000 (Val30Met endemic in Portugal/Sweden/Japan; higher there) — commonly cited; UNVERIFIED exact figure this s | 1-9 / 1 000 000 |
| alpha-1-antitrypsin-deficiency | ~1 in 2,500-5,000 (PI*ZZ, European descent) — commonly cited; UNVERIFIED exact figure this session | 1-5 / 10 000 |
| cystic-fibrosis | ~1 in 2,500-3,500 live births (Caucasian); carrier ~1 in 25 — commonly cited; UNVERIFIED exact figure this session | 1-5 / 10 000 |
| angelman-syndrome | ~1 in 12,000-20,000 — commonly cited; UNVERIFIED exact figure this session | 1-9 / 100 000 |
| myotonic-dystrophy-1 | ~1 in 8,000 (most common adult muscular dystrophy) — commonly cited; UNVERIFIED exact figure this session | 1-5 / 10 000 |
| neonatal-diabetes | ~1 in 100,000-260,000 live births — commonly cited; UNVERIFIED exact figure this session | Unknown |
| wilson-disease | ~1 in 30,000 — commonly cited; UNVERIFIED exact figure this session | 1-9 / 100 000 |

## OMIM correction

**Neonatal diabetes:** the public page and record used **OMIM 606176**, which is PNDM1 / GCK. The KCNJ11 entry is **OMIM 618856 (PNDM2)**. The public page, JSON record and this report were corrected on 7 Nov 2026.

## Structure cross-check

- **3T3K** — *1.24 A Structure of Friedreich's ataxia frataxin variant Q148R* (RCSB entry resolved).
- **1EKG** — *MATURE HUMAN FRATAXIN* (RCSB entry resolved).
- **3S4M** — *Crystal structure of wild-type human frataxin* (RCSB entry resolved).

These entries describe different constructs; the public FXN page names them separately.

## What this does not establish

- It does not validate prevalence, natural history, efficacy or safety.
- It does not turn a source-linked research dossier into clinical advice.
- OMIM entry text was not fetched; the Cloudflare human checkbox remains outstanding. OMIM ids were cross-referenced through Orphanet.
- Orphanet entries were opened in a browser; that verifies the code and page, not every claim or exact prevalence.
- Drug approval dates were not all re-fetched from regulators.
- A reachable Orphanet page is not proof that every claim on the page is correct.
