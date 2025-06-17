---
layout: post
title: "Week 2: Server Deployment and Amharic Wikipedia Extraction"
short_title: "Week-2"
date: 2025-06-15
categories: [gsoc, dbpedia]
---

This report summarizes my work during the second official GSoC coding week (June 8–14). The primary focus was deploying the DBpedia Extraction Framework on the main server, configuring the extraction process, and successfully completing the extraction for Amharic Wikipedia.

<!--more-->

## Tasks Completed

- Installed and tested the DBpedia Extraction Framework on the **main server**.
- Installation proceeded smoothly due to familiarity with the requirements from the local setup completed in Week 1.
- Configured the Extraction Framework. Initially encountered errors due to missing `.properties` files, which were expected by the system. This was resolved by referring to the official [DBpedia Extraction Framework Quickstart Guide](https://github.com/dbpedia/extraction-framework/blob/master/documentation/quickstart.md), allowing me to tailor the configuration to meet the project's needs.
- Successfully extracted data from **Amharic Wikipedia**, generating RDF triples across multiple categories.
- Created a dedicated **GitHub Pages blog** for the project and shared the link with mentors and the DBpedia team.
- Attempted to install **Virtuoso** for triple store management but encountered permission issues. Later, I received confirmation that installing new software on the server is not permitted.
- Created an account on the [DBpedia Mappings Wiki](https://mappings.dbpedia.org) and sent an email requesting Create/Edit access. The team responded advising to follow up via the forum, but login attempts return a **"waiting for activation"** message. This issue has been communicated for further support.
- Attended the **Week 2 mentor meeting** on **June 13, 2025**, presented progress, and received feedback and suggestions.

## Challenges

- The extraction framework initially failed due to missing custom configuration files. This was resolved by researching and adapting example files.
- Installation of Virtuoso was blocked due to system-level restrictions, which limits testing of RDF storage and SPARQL querying locally.
- Difficulty gaining access to the **DBpedia Mappings Wiki**: despite registering and contacting the team, the account remains inactive and cannot log in due to "waiting for activation" status. The issue has been reported but is still unresolved.

## Next Steps

- Install and configure the DBpedia Extraction Framework on the **backup server** (AAU server).
- Work through the **entire extraction pipeline**, including:
  - Creating new **templates**
  - Defining **mappings**
  - Developing new **extractors** (e.g., citation, disambiguation)
- Verify and analyze **mapping statistics** to evaluate the quality and completeness of extractions.

## Conclusion

Week 2 marked a major milestone with the successful extraction of Amharic Wikipedia. Despite some system limitations and delays in wiki access, the overall deployment and data generation went well. With the groundwork in place, the focus will now shift to refining the extraction process, contributing to DBpedia mappings, and preparing the pipeline for expanded coverage and querying.
