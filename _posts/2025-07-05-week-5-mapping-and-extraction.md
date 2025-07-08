---
layout: post
title: "Week 5: Mapping Creation and Successful End-to-End Extraction"
short_title: "Week-5"
date: 2025-07-05
categories: [gsoc, dbpedia]
---

This post summarizes my work during the fifth official GSoC coding week (June 28 – July 5). The focus this week was on template mapping, end-to-end extraction testing, and validating RDF outputs with SPARQL queries.

<!--more-->

## Tasks Completed

- Attempted to set up a **virtual environment** for Java 8 and configure the **DBpedia Extraction Framework** using a batch script. However, the environment setup was unsuccessful and will require further troubleshooting.
- Published the **Week 4 blog post** on the GitHub Pages project blog.
- Created and added new **template mappings** on [mapping.dbpedia.org](https://mapping.dbpedia.org) for the following:
  - `Book`
  - `Airline`
  - `Olympic`
  - Additional templates such as `Continent`, `Color`, and `WorldHeritageSite` are in progress and will be added soon.
- Learned that mappings from the Mappings Wiki **cannot be directly extracted**. Instead, I retrieved the updated templates using the extraction framework programmatically.
- Updated the `mapping_am.xml` file and successfully **ran the extraction process**, generating valid **RDF output**.
- Tested the RDF output with **SPARQL queries** using **Apache Jena Fuseki**. While the setup worked as expected, no results were returned due to a **lack of Wikipedia articles using the new templates**.
- Contacted the **DBpedia team** regarding **Amharic mapping statistics**, which are currently unavailable. Tracking mapping statistics is important for measuring progress, and the team is now working on restoring this functionality.
- Attended the **Week 5 mentor meeting** on **July 4, 2025**, presented the current status, and received valuable feedback. Mentors recommended:
  - First identifying existing **Wikipedia templates and infoboxes** that are actively used
  - Mapping those in DBpedia before creating entirely new ones

- Overall, this week was productive, as I completed the full pipeline from **template creation to RDF extraction and SPARQL query testing**.

## Challenges

- The **virtual environment setup for Java 8** failed and will need further debugging.
- **No RDF output** was returned from SPARQL queries due to the absence of Amharic articles using the newly mapped templates.
- **Mapping statistics** remain inaccessible, limiting the ability to track quantitative progress.

## Next Steps

- Continue refining the full pipeline from template creation to RDF querying.
- Add new templates and complete mappings for partially mapped ones.
- Follow up on the mapping statistics dashboard with the DBpedia team.
- Begin preparations for **DBpedia Live extraction** using verified templates and mappings.

## Conclusion

This week marked an important milestone as I successfully completed the entire DBpedia extraction workflow: from creating new templates and mappings to extracting RDF data and verifying it through SPARQL. Though challenges remain, particularly with article coverage and statistics tracking, the progress so far provides a strong foundation for the coming phases.

