# Academic Archiving & Citation

This document describes how Project Phoenix is archived for academic citation and provides guidance for others who wish to archive similar work.

---

## Zenodo Archive

This repository will be archived on Zenodo for long-term preservation and academic citation.

**Status:** Archived

**Archive Details:**
- **Title:** Project Phoenix: The Agentic Greenfield Pipeline for Legacy Modernization
- **Version:** 1.0.0
- **Date:** 2026-03-07
- **License:** CC BY 4.0
- **DOI:** [10.5281/zenodo.18904231](https://doi.org/10.5281/zenodo.18904231)

---

## Why Archive on Zenodo?

1. **Permanent DOI** - Persistent identifier that won't break
2. **Long-term preservation** - CERN-backed infrastructure
3. **Academic credibility** - Citable in research papers
4. **Version tracking** - Each release gets its own DOI
5. **Discoverability** - Indexed by academic search engines
6. **Citation network** - Links to related works (Cormorant, 6D, PACE)

---

## Preparation Checklist

Repository preparation for archiving:

- [x] Repository structure is clean and logical
- [x] All essential files at appropriate levels
- [x] CITATION.cff file with complete metadata
- [x] LICENSE file clearly specifies terms (CC BY 4.0)
- [x] CHANGELOG.md documents version history
- [x] .gitignore excludes temporary/build files
- [x] Internal links verified and working
- [x] README.md includes abstract and overview
- [x] References to related works (Cormorant, 6D, PACE)
- [ ] GitHub repository created and pushed
- [ ] GitHub release v1.0.0 created
- [ ] Zenodo integration enabled
- [ ] DOI received from Zenodo

---

## Zenodo Submission Guide

When submitting to Zenodo, use these details:

### Required Fields

| Field | Value |
|-------|-------|
| **Upload type** | Software (framework/methodology) |
| **Title** | Project Phoenix: The Agentic Greenfield Pipeline for Legacy Modernization |
| **Creators** | Michael Shatny (ORCID: 0009-0006-2011-3258) |
| **Description** | Use abstract from README.md |
| **License** | Creative Commons Attribution 4.0 International |
| **Keywords** | legacy modernization, agentic pipeline, greenfield development, business logic extraction, software transformation, AI-native development, cormorant foraging, phoenix methodology |
| **Version** | 1.0.0 |

### Related Identifiers

Link to related works in the ecosystem:
- **Cormorant Foraging Framework:** 10.5281/zenodo.18210081 (relationship: "is part of")
- **6D Foraging Methodology:** 10.5281/zenodo.18209946 (relationship: "references")
- **PACE Pattern:** 10.5281/zenodo.18049371 (relationship: "references")
- **Semantic Intent SSOT:** 10.5281/zenodo.17114972 (relationship: "references")

### Related Documentation Sites

- **Phoenix (Framework):** https://phoenix.cormorantforaging.dev
- **Phoenix (Standalone):** https://semanticintent.dev/phoenix
- **Cormorant Foraging:** https://cormorantforaging.dev
- **6D Methodology:** https://6d.cormorantforaging.dev
- **Case Study UC-024:** https://uc-024.stratiqx.com

### Notes

Include trademark notice: "Project Phoenix" is a trademark of Michael Shatny.

---

## After Receiving DOI

Once Zenodo assigns a DOI, complete these tasks:

### 1. Update Repository

- [ ] Add DOI badge to README.md
- [ ] Update citation examples in README.md with actual DOI
- [ ] Update this file (ARCHIVING.md) status from Pending to Archived
- [ ] Add DOI to this file's archive details section
- [ ] Update CITATION.cff with DOI
- [ ] Update LICENSE with DOI in attribution section

### 2. Verify GitHub Release

- [ ] Tag: v1.0.0
- [ ] Title: "Project Phoenix v1.0.0"
- [ ] Description: Copy from CHANGELOG.md
- [ ] Attach DOI in release notes

### 3. Enable Auto-Archiving

For future versions:
- [ ] Connect GitHub repository to Zenodo
- [ ] Enable automatic DOI generation for new releases
- [ ] Each GitHub release will automatically create a new Zenodo version

### 4. Update External References

- [ ] Add DOI to phoenix.cormorantforaging.dev
- [ ] Update semanticintent.dev/phoenix with DOI
- [ ] Update Cormorant Foraging Framework references
- [ ] Update 6D Methodology references
- [ ] Add Phoenix DOI to semanticintent-ai site

---

## Ecosystem Integration

Project Phoenix is the transformation layer of the Semantic Intent ecosystem:

```
Semantic Intent (Philosophy) -- DOI: 10.5281/zenodo.17114972
  |
PACE Pattern (UX)           -- DOI: 10.5281/zenodo.18049371
  |
6D Methodology (Diagnostic) -- DOI: 10.5281/zenodo.18209946
  |
Cormorant Foraging (3D)     -- DOI: 10.5281/zenodo.18210081
  |
Project Phoenix (Transform) <-- This work
```

Once archived, this DOI will be referenced by:
- Future releases of Cormorant Foraging Framework
- Future releases of 6D Methodology
- Research papers on AI-native legacy modernization
- Case studies applying the Phoenix pipeline

---

## Archiving Timeline

1. Documentation complete
2. Push to GitHub -- create repository and push initial commit
3. Create release -- tag v1.0.0 and create GitHub release
4. Enable Zenodo -- connect repository to Zenodo
5. Receive DOI -- wait for Zenodo to assign DOI
6. Update references -- add DOI to all relevant files
7. Announce -- share with ecosystem and research community

---

*Last updated: 2026-03-07*
