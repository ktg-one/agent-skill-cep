# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased] - v8.0

### Added
- **Expert Knowledge Bases** - Comprehensive documentation for all 4 permanent expert council members:
  - `EXPERTS-MEMORY_ARCHITECT.md` - Preservation gatekeeper expert knowledge base
  - `EXPERTS-COMPRESSION_SPECIALIST.md` - Density optimization expert knowledge base  
  - `EXPERTS-CROSS-DOMAIN-ANALYST.md` - Edge preservation specialist knowledge base
  - `EXPERTS-RESTORATION_ENGINEER.md` - Receiving model advocate knowledge base

- **Advanced Techniques Integration** - STRAWHATS cascade techniques:
  - **ARQ (Attentive Reasoning Queries)** - Quality gates for council experts (90.2% success rate, 29% token reduction, 40-60% error reduction)
  - **CoVE (Chain of Verification)** - Packet verification variants (CoVE_FACTUAL, CoVE_LOGICAL, CoVE_CONSISTENCY, CoVE_MULTI_EXPERT)
    - Single variant: +12% tokens, +25-35% accuracy
    - Multi-variant: +30% tokens, +45-65% accuracy
  - **USC (Universal Self-Consistency)** - Multi-candidate packet generation for high-stakes handoffs
    - USC=2: +80% tokens, +41% quality (sweet spot)
    - USC=3: +120% tokens, +45% quality
    - USC=5: +200% tokens, +50% quality
  - **Combined cascade techniques**: ~+450 tokens overhead, but effectiveness near 3x improvement
  - **CASCADE.md** - Full integration guide for cascade techniques
  - **MIRAS.md** - MIRAS/Titans complement positioning and future-proofing strategy
  - **INDEX.md** - Expert Council Knowledge Base Index with quick router

- **Naming Rubric Updates** - Updated to v8 format:
  - Reasoning levels: L1-L10 (maps directly to R score)
  - Format: `$MM$DD$YYYY-XXX-LN-domain-topic-context`
  - Benchmark domain requirement (first keyword)
  - Model codes (3 uppercase letters)

- `.gitignore` - Added gitignore file to exclude `.cursor/rules/openmemory.mdc` from version control
- `openmemory.md` - Added OpenMemory integration guide (currently empty, to be populated)
- **Buffer of Thought section** in README.md - Added section inviting community to share reasoning templates (not sensitive content) to build a dataset

### Changed
- **Version updated**: v7.0 → v8.0 throughout all files
- **Removed all KTG branding** - Changed to generic CEP references
- **SKILL.md** - Updated naming convention to v8 format (L1-L10, benchmark domains)
- **README.md** - Updated version references, removed branding, added Buffer of Thought section
- **anti-injection.md** - Updated version reference to v8

### Removed
- All KTG/ktg branding references
- Personal/branding links and attribution

---

## Notes

- Expert knowledge bases provide detailed guidance for each council member
- Cascade techniques (ARQ, CoVE, USC) enhance packet quality and validation
- MIRAS integration prepares for future Google architecture compatibility
- v8 naming rubric enforces stricter format for better indexing and retrieval
