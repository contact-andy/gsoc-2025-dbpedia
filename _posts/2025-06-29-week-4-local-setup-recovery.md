---
layout: post
title: "Week 4: Local Setup Recovery and Progress on Extraction"
short_title: "Week-4"
date: 2025-06-29
categories: [gsoc, dbpedia]
---

This report summarizes my work during the fourth official GSoC coding week (June 22–28). The week began with unexpected hardware issues, but significant progress was made through local setup recovery and continued development of the DBpedia extraction pipeline.

<!--more-->

## Tasks Completed

- Faced a major setback early in the week due to an **operating system crash** on my local laptop caused by a power failure. Recovering previous files proved difficult, and I ultimately had to **format the machine**. The experience reinforced the importance of regularly backing up project files to the cloud.
- Successfully **reinstalled the OS** and reconfigured the local development environment.
- Installed the **DBpedia Extraction Framework locally** and was able to **extract RDF data successfully**. Observed that system performance impacts extraction speed significantly—even single attribute extractions were time-consuming.
- Installed **Apache Jena Fuseki** and verified the extracted RDF data using **SPARQL queries**, confirming the setup is functional.
- On the main server, although it was operational this week, the workflow changed based on mentor recommendations. I was instructed to **create a personal storage directory** and clone the extraction framework there.
- Faced issues installing **Java 8** on the main server due to restricted permissions. Decided to pause work on the server-side until a solution is found. Mentors recommended creating a **virtual environment** for future extractions.
- Attempted to create a **SLURM script** to run background tasks on the server, but the script failed to execute as expected. Further debugging is planned.
- Had a productive conversation with a **2024 GSoC contributor**, who offered advice and shared helpful insights about overcoming similar technical challenges.
- Although my **DBpedia Mappings Wiki account** is active, I encountered **permission errors** when trying to create templates. After contacting the DBpedia team, they resolved the issue, and I confirmed that all permissions now work correctly.
- Continued communication with **AAU technical staff** regarding the backup server. Unfortunately, their server is currently down due to unknown issues, and my access will be granted once it’s restored.
- Published the **Week 3 report** on the GitHub Pages project blog.
- Continued reading and exploring DBpedia documentation on **infobox templates**, **mapping definitions**, and the **extraction framework**, building upon last week’s efforts.
- Attended the **Week 4 mentor meeting** on **June 27, 2025**, and shared the current status. Received feedback and recommendations for upcoming work.

## Challenges

- The **local OS crash** resulted in a temporary loss of progress and required a full reinstallation and environment rebuild.
- Encountered **permission issues** on the DBpedia Mappings Wiki, though these were eventually resolved.
- Inability to install **Java 8** on the main server stalled progress on server-based extraction work.
- **SLURM job submission script** did not function as intended, which blocked automation efforts on the server.
- The **AAU backup server** remains unavailable due to technical issues, preventing any redundancy setup this week.

## Next Steps

- Set up and manage a **virtual environment** on the main server for Java 8 and the extraction framework.
- Resume full extraction pipeline work, including:
  - Creating and updating **infobox templates**
  - Defining new **DBpedia mappings**
  - Developing **custom extractors** (e.g., for citations and disambiguation)
- Verify **mapping statistics** to evaluate and validate the quality of extracted data.
- Continue using **Apache Jena Fuseki** to test and query extracted RDF outputs.
- Create **mapping templates** for infoboxes that currently lack DBpedia mappings.
- **Read and review** advanced DBpedia documentation and case studies to deepen understanding of the live extraction process.
- **Implement a live DBpedia extraction run** using the configured framework and validate the output against expected RDF structure and mappings.


## Conclusion

While the week began with significant technical obstacles, including a local OS failure, key progress was made through successful local setup, RDF extraction, and SPARQL testing. The activation of mapping permissions and mentor support further accelerated development. In the coming week, focus will shift to virtual environment setup on the main server and continued work on the complete DBpedia extraction pipeline.
