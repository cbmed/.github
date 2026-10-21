---
name: Study DTS configuration
about: Create or update a study configuration
title: "[DTS Config] <study ID>"
---

## Review checklist

- [ ] **Study and file identification**
  - [ ] Study ID is correct.
  - [ ] Configuration filename is correct.
  - [ ] Expected data filename pattern is correct.

- [ ] **Table structure and format**
  - [ ] Column names and order match the DTS.
  - [ ] File format and encoding are correct.
  - [ ] Duplicate handling is correct.

- [ ] **Column constraints**
  - [ ] Data types and `nullable` settings are correct.
  - [ ] `allowed_values` lists are correct and complete.
  - [ ] `allowed_pattern` expressions match the required formats.
  - [ ] Maximum lengths and numeric ranges are correct.

- [ ] **Conditional rules**
  - [ ] All required dependencies are covered.
  - [ ] Conditions and resulting constraints are correct.

## Notes

<!-- Open questions or deviations, if any. -->
