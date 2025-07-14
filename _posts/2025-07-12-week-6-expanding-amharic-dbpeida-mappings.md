---
layout: post
title: "Week 6: Expanding Mappings and Infobox Coverage in Amharic Wikipedia"
short_title: "Week-6"
date: 2025-07-12
categories: [gsoc, dbpedia]
---

This post summarizes the progress made during the sixth GSoC coding week (June 28 – July 5). The main focus this week was identifying existing infobox templates in Amharic Wikipedia, expanding DBpedia mappings, aligning templates with real Wikipedia content, and continuing the live extraction efforts.

<!--more-->

## Tasks Completed

- Based on mentor recommendations, I **searched Amharic Wikipedia** for existing infobox templates (`መረጃሳጥን`).  
  - Identified **67 total templates**. Among these:
    - ✅ **17 templates** were already mapped in Amharic DBpedia.
    - ✅ **12 templates** had existing content and infobox structure in Wikipedia.
    - ⚠️ **3 templates** had minimal attributes and require further exploration for mapping.
    - ❌ The rest were placeholder pages with no useful template data.

- Added **17 new template mappings** to [mapping.dbpedia.org](https://mapping.dbpedia.org) including:
  - `Flag`, `EthnicGroup`, `MilitaryConflict`, `WorldHeritageSite`, `MusicalWork`
  - `SoccerPlayer`, `Weapon`, `SportsEvent`, `SoccerMatch`, `Colour`
  - `ReligiousBuilding`, `Academic`, `Chef`  
  - These additions doubled the number of Amharic mappings from 17 to **34**.

- For previously mapped templates like `Book`, `Airline`, and `Olympic`, I:
  - Noticed there were **no Wikipedia pages using those infoboxes**, so I **created templates in Amharic Wikipedia** and aligned them with the mappings.
  - Updated or created articles that include the corresponding infoboxes to enable RDF extraction in future dumps.

- Attended the **Week 6 mentor meeting** on **July 11, 2025**, presented updates, and received feedback.
- The DBpedia team assigned a contact person to assist with **generating Amharic mapping statistics locally**. The assigned contributor provided detailed steps for the process.
   - I followed the recommended steps and executed the script, but it returned empty results. I plan to continue troubleshooting in the coming week.
   - My mentors advised me to keep working on generating local statistics, stay in close contact with the assigned person, and also reach out to other GSoC contributors who might have faced similar issues for further guidance and collaboration.

- Published the **Week 5 blog post** to the GitHub Pages project blog.

## Challenges

- Some Amharic Wikipedia templates lack proper properties, making them difficult to map.
- Generating local **mapping statistics** resulted in no output; requires further debugging.
- Ensuring Wikipedia content actually uses the mapped templates remains a bottleneck for extraction.

## Next Steps

- Continue the **end-to-end pipeline**: from template creation, mapping, and content editing to RDF extraction and SPARQL querying.
- Add more templates and complete mappings for those with basic attributes.
- Follow up on **local statistics generation** and collaborate on improving tools for Amharic mapping evaluation.
- Proceed with **live DBpedia extraction**, including RDF validation and alignment with mappings.
- Document the mapping/statistics generation process to support future contributors.

## Conclusion

This week marked significant progress in expanding Amharic DBpedia mappings and aligning them with Wikipedia content. The number of mapped templates has doubled, and the groundwork has been laid for more reliable RDF generation in future dumps. Despite challenges in statistics generation and template coverage, the pipeline is shaping up well and will be further refined in the coming weeks.
