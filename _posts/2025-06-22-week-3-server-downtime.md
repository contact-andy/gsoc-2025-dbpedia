---
layout: post
title: "Week 3: Server Downtime and Mapping Wiki Access"
short_title: "Week-3"
date: 2025-06-22
categories: [gsoc, dbpedia]
---

This report summarizes my work during the third official GSoC coding week (June 15–21). While the week faced setbacks due to server downtime, some key progress was achieved in community engagement and project planning.

<!--more-->

## Tasks Completed

- Unfortunately, the **main server was down** for most of the week, which blocked progress on deploying or testing the extraction framework. The issue was promptly communicated to mentors.
- Continued attempts to access the [DBpedia Mappings Wiki](https://mappings.dbpedia.org), but the login issue from last week remained unresolved. The team was contacted again for support.
- **Towards the end of the week**, I received confirmation that my **account was activated**, and I now have access to the Mappings Wiki.
- Participated in the **Week 3 mentor meeting** on **June 20, 2025**, to present current status and discuss challenges and next steps.
- Published the **Week 2 report** on the GitHub Pages project blog.
- Read and explored DBpedia documentation on **infobox templates, mapping definitions**, and extraction framework structure to prepare for upcoming tasks.
- Communicated with **AAU technical staff** about configuring the local server as a backup environment. However, no concrete progress was made this week.
- Attempted to install **Virtuoso locally**, but due to the unavailability of a functional extraction output for testing, installation and usage were postponed.
- Successfully **completed Payoneer account registration** and received a status update following review.

## Challenges

- **Main server outage** prevented any extraction or deployment work for the week.
- Ongoing **DBpedia Mappings Wiki access issue** limited the ability to contribute to template and mapping definitions until account activation was completed.
- **No progress** was made on setting up the **AAU backup server**, despite efforts to engage the appropriate contacts.
- **Virtuoso setup** was stalled due to lack of new RDF data to test with, stemming from the blocked extraction process.

## Next Steps

- Install and configure the **DBpedia Extraction Framework** on the **AAU backup server**.
- Resume work on the **complete extraction pipeline**, including:
  - Creating new **infobox templates**
  - Defining **DBpedia mappings**
  - Developing new **extractors** such as citation and disambiguation modules
- Verify **mapping statistics** to evaluate coverage and correctness of extracted RDF data.
- Reattempt **local Virtuoso installation**, using valid output data from the extraction framework once available.

## Conclusion

Despite the disruption caused by the main server downtime, the successful activation of the Mappings Wiki account and continued research into DBpedia architecture helped keep momentum. Looking ahead, focus will return to technical implementation on the backup server and expanding the mapping and extraction capabilities of the project.
