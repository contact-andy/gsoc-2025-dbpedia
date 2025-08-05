---
layout: post
title: "Week 9: Analyzing and Improving Template Mapping Quality"
short_title: "Week-9"
date: 2025-08-02
categories: [gsoc, dbpedia]
---

This post summarizes the progress made during the ninth GSoC coding week (July 27 – August 02). The week focused on auditing mapping statistics, identifying key issues in template mappings, implementing fixes, and exploring partial automation of the mapping process.

<!--more-->

## Tasks Completed

- Prepared a detailed **analytical report** based on the generated mapping statistics. This analysis uncovered several recurring issues:
  - Templates mapped to the **wrong ontology class**
  - **Template name mismatches** between DBpedia and Wikipedia
  - Templates that are **mapped in DBpedia but not reflected in statistics**
  - Templates without any **mapped properties**
  - Presence of **non-Amharic or empty templates**
  - Templates written in **English without proper Amharic translation**
  - **Broken template detail pages** in Wikipedia
  - **Duplicate templates** across different languages
  - Templates with **only one or no usable attributes**
  - Templates that are **not yet mapped** but require property correction
  - Templates with **Amharic names but invalid or unusable properties**

- Based on these findings, I proposed and documented the following **recommendations**:
  - Fix template mismatches and validate ontology class usage
  - Normalize and align template naming conventions
  - Translate or replace English-based templates
  - Consolidate duplicates across languages
  - Remove or repair broken template pages
  - Fix poor property labels or non-Amharic property usage
  - Review and clean up empty templates

- I then worked on **applying these fixes**, focusing on name corrections, property cleanup, and ontology alignment.
  - The impact was **immediately visible**: the **mapping statistics improved**, confirming that these changes help produce a cleaner and more accurate report.

- Initiated early work on **automating template creation and mapping** using custom scripts.
  - The foundation is set, but more time is needed to complete and fully test the automation process.

- Participated in the **Week 9 mentor meeting** on **August 01, 2025**.
  - Shared my findings, received valuable feedback, and aligned on priorities for the upcoming week.

- Published the **Week 8 blog post** to the GitHub Pages project blog.

## Challenges

- Automating template generation requires handling diverse edge cases and ensuring semantic alignment with the DBpedia ontology.
- Some templates are difficult to fix due to incomplete content or outdated structure in Wikipedia.

## Next Steps

- Continue improving **mapping statistics** and validate changes with fresh data dumps.
- Proceed with **DBpedia Live extraction** and review RDF output alignment.
- **Complete and test the automation script** for creating and mapping templates more efficiently.

## Conclusion

This week was a major milestone in improving the quality and accuracy of Amharic DBpedia mappings. The analytical report provided a clear roadmap for fixes, and the resulting improvements to statistics demonstrate the value of this work. With automation on the horizon, the workflow is set to become more scalable and sustainable in the weeks ahead.
