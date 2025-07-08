---
layout: post
title: "Week 5: Mapping Creation and Successful End-to-End Extraction"
short_title: "Week-5"
date: 2025-07-05
categories: [gsoc, dbpedia]
---

This post summarizes my work during the fifth official GSoC coding week (June 28 – July 5). The focus this week was on template mapping, end-to-end extraction testing, and initiating the live DBpedia extraction process.

<!--more-->

## Tasks Completed

- Attempted to set up a **virtual environment** for Java 8 and configure the **DBpedia Extraction Framework** using a batch script. However, the environment setup was unsuccessful and will require further troubleshooting.
- Published the **Week 4 blog post** on the GitHub Pages project blog.
- Created and added new **template mappings** on [mapping.dbpedia.org](https://mapping.dbpedia.org) for the following:
  - ✅ `Book`
  - ✅ `Airline`
  - ✅ `Olympic`
  - ℹ️ Additional templates such as `Continent`, `Color`, and `WorldHeritageSite` are in progress and will be added soon.
- Learned that mappings from the Mappings Wiki **cannot be directly extracted**. Instead, I retrieved the updated templates using the extraction framework programmatically.
- Updated the `mapping_am.xml` file and successfully **ran the extraction process**, generating valid **RDF output**.
- Tested the RDF output with **SPARQL queries** using **Apache Jena Fuseki**. While the setup worked as expected, no results were returned due to a **lack of Wikipedia articles using the new templates**.
- Contacted the **DBpedia team** regarding **Amharic mapping statistics**, which are currently unavailable. Tracking mapping statistics is important for measuring progress, and the team is now working on restoring this functionality.
- Attended the **Week 5 mentor meeting** on **July 4, 2025**, presented the current status, and received valuable feedback. Mentors recommended:
  - First identifying existing **Wikipedia templates and infoboxes** that are actively used
  - Mapping those in DBpedia before creating entirely new ones
- **Started implementing a live DBpedia extraction run** using the configured framework. This work is ongoing and will be continued in the upcoming week.
- Continued to **read and review advanced DBpedia documentation and case studies** to strengthen understanding of the live extraction process.

## Challenges

- The **virtual environment setup for Java 8** failed and will need further debugging.
- **No RDF output** was returned from SPARQL queries due to the absence of Amharic articles using the newly mapped templates.
- **Mapping statistics** remain inaccessible, limiting the ability to track quantitative progress.

## Next Steps

- Continue work on the full pipeline, from template creation to RDF extraction and SPARQL querying  
- Add new templates and complete mappings for partially mapped ones  
- Follow up with the DBpedia team on restoring mapping statistics  
- **Continue live DBpedia extraction**, including RDF output validation and alignment with mapping definitions  
- Read and review **advanced DBpedia documentation and case studies** to deepen understanding of live extraction

## Conclusion

This week marked an important milestone as I successfully completed the entire DBpedia extraction workflow—from creating new templates and mappings to extracting RDF data and verifying it through SPARQL. I also began exploring and implementing a **live DBpedia extraction run** using the configured framework. While the process has started, further work is needed to validate the output against the expected RDF structure and mappings. This will continue into the next week. Despite some ongoing challenges with article coverage and statistics tracking, progress remains steady and on track.
