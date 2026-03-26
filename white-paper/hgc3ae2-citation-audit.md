# Citation Audit Addendum

**Paper Title:** Mitigating Confident Misalignment in Agentic Systems: The HGC³AE² Framework  
**Parent Log:** `white-paper/Mitigating Confident Misalignment in Agentic Systems - The HGC3AE2 Framework.md`  
**Artifact Type:** white-paper  
**Audit Scope:** bibliography, footnotes, source verification, Chicago compliance, source-to-claim alignment  
**Status:** citation QA complete / remediation pending

## Citation audit summary
The citation audit found a mix of valid sources, incomplete entries, placeholder entries, and entries that point to real topics but are not currently citable as written. The paper’s conceptual source domains are strong, but the scholarly apparatus is not yet reliable enough for submission.

## Logged citation issues

### WP-011 — Remove placeholder bibliography entries
**Priority:** Critical  
**Problem:** Several bibliography items are not actual citations. They function as topic labels or research placeholders rather than verifiable sources. Examples include lines such as "AI and Ethics governance ecosystem literature," "FAA human factors guidance," and similar pseudo-entries.  
**Action:** Remove all placeholder-style lines and replace them with real sources, each with a full author/title/publication trail and stable link or DOI.  
**Done when:** Every bibliography entry resolves to a real source that can be independently verified.

### WP-012 — Repair misattributed authorship entries
**Priority:** Critical  
**Problem:** At least one entry is attached to a real paper but credits the wrong authors. The de Sousa / Janssen line is one example where the current draft does not match the verified authorship of the cited work.  
**Action:** Recheck author names for every entry against the publisher page, DOI record, or Google Scholar result.  
**Done when:** No bibliography entry attributes a source to the wrong authors.

### WP-013 — Convert topic-level references into exact source citations
**Priority:** High  
**Problem:** Some entries refer to a body of literature instead of a specific work, making them impossible to verify or footnote properly.  
**Action:** For each such entry, identify the exact article, book, chapter, standard, or regulation that supports the claim and cite that item specifically.  
**Done when:** Every entry names a precise source rather than a topic bucket.

### WP-014 — Normalize all bibliography entries to full Chicago style
**Priority:** High  
**Problem:** Several entries are incomplete, inconsistent, or missing Chicago-required metadata such as editors, publisher, edition, journal details, dates, URLs, or DOI strings.  
**Action:** Rebuild the bibliography in one standard format and include all required metadata for books, chapters, articles, regulations, and organizational publications.  
**Done when:** The bibliography is internally consistent and fully Chicago-compliant.

### WP-015 — Replace or fully specify CAP theorem citation
**Priority:** High  
**Problem:** The current Brewer / CAP line is too thin to function as a scholarly citation. It currently names a concept and year rather than a fully specified source.  
**Action:** Either cite Brewer’s original talk/conjecture in full form if appropriate, or replace it with a more stable formal source such as the later proof/discussion literature.  
**Done when:** The CAP citation identifies a specific, defensible source.

### WP-016 — Complete and verify regulatory / institutional citations
**Priority:** High  
**Problem:** Institutional sources such as the European Commission AI Act and OECD AI Principles are real but not consistently cited with enough detail or current publication framing.  
**Action:** Verify the controlling official publication pages and cite the final or authoritative version, including year, institution, formal title, and link.  
**Done when:** All institutional and regulatory sources are traced to official primary documents.

### WP-017 — Complete book chapter and handbook citations
**Priority:** High  
**Problem:** Edited-volume and handbook citations are especially vulnerable because they currently lack enough metadata to be verified cleanly.  
**Action:** Rebuild each chapter citation with chapter title, book title, editor(s), edition if applicable, publisher, year, and page span.  
**Done when:** Every book-chapter citation can be independently located without ambiguity.

### WP-018 — Audit every footnote against a verified bibliography entry
**Priority:** Critical  
**Problem:** A source can appear plausible in a footnote even when the bibliography entry is incomplete or wrong.  
**Action:** Map every footnote to a verified bibliography item and remove orphan notes, placeholder notes, or notes that shorten invalid bibliography entries.  
**Done when:** Every note points to a valid, verified bibliography source.

### WP-019 — Verify claim-to-source alignment
**Priority:** Critical  
**Problem:** Some sources may be real but still not support the specific proposition they are attached to in the paper.  
**Action:** For each citation, confirm that the cited source actually supports the sentence or paragraph where it appears. Replace weak fit sources with better ones where necessary.  
**Done when:** Every citation supports its attached claim directly or by clearly stated inference.

### WP-020 — Separate primary, secondary, and analogical support
**Priority:** Medium  
**Problem:** The paper mixes governance, neuroscience, human-factors, and distributed-systems material. Some sources are direct support, while others are analogical or framing support.  
**Action:** Tag citations internally by function: primary empirical support, conceptual support, regulatory support, analogical support, or background context.  
**Done when:** The evidentiary structure is easier to defend and overclaim risk is reduced.

### WP-021 — Remove pseudo-current dates and stale publication assumptions
**Priority:** Medium  
**Problem:** Some entries appear to use years that are convenient anchors rather than the most authoritative publication date/version.  
**Action:** Verify the correct edition, update year, adoption year, or publication year for every source.  
**Done when:** All years in the bibliography match the authoritative source record.

### WP-022 — Build a verified master source table
**Priority:** High  
**Problem:** The paper now needs a source-of-truth layer so the bibliography does not drift again during revision.  
**Action:** Maintain a master table with columns for current citation text, verified source title, authors, publication venue, year, DOI/link, citation status, and replacement text.  
**Done when:** Every bibliography item can be tracked and regenerated from a verified source table.

### WP-023 — Regenerate short-form notes after bibliography cleanup
**Priority:** High  
**Problem:** Once bibliography entries change, the short-form notes may become inconsistent or invalid.  
**Action:** After the bibliography is rebuilt, regenerate all short-form note forms so they match the corrected entries exactly.  
**Done when:** Notes and bibliography are fully synchronized.

### WP-024 — Produce a submission-safe bibliography pass
**Priority:** Critical  
**Problem:** The current citation layer is the single biggest blocker to submission readiness.  
**Action:** Execute a final pass that produces:
- a verified bibliography,
- corrected footnotes,
- link-backed audit records,
- and source-to-claim validation.
**Done when:** The paper’s citation apparatus is defensible under close academic scrutiny.

## Recommended remediation order
1. Remove placeholders and pseudo-citations.
2. Repair misattributions and wrong years.
3. Verify institutional / regulatory sources against official pages.
4. Rebuild book chapter and handbook citations.
5. Map every footnote to a verified entry.
6. Recheck claim-to-source alignment.
7. Regenerate notes and final bibliography.

## Companion artifacts
- `full_citation_audit_hgc3ae2.xlsx` — full audit workbook

## Owner notes
This addendum captures the citation-specific defects identified during the full citation audit. It should be treated as a blocking QA layer before any submission-oriented rewrite or formatting pass.