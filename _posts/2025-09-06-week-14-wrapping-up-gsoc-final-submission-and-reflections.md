---
layout: post
title: "Week 14: Wrapping Up GSoC - Final Submission and Reflections"
short_title: "Week-14"
date: 2025-09-06
categories: [gsoc, dbpedia]
---

This post summarizes the progress made during the fourteenth and final GSoC coding week (August 31 – September 06).  
The main focus was on completing the **final GSoC submission**, finalizing documentation, polishing the website, and reflecting on the overall journey.  

<!--more-->

## Tasks Completed

### 1. Final Website Update
- The updated project website was pushed to GitHub for mentor review, successfully reviewed and merged, and is now publicly accessible at [am.dbpedia.org](http://am.dbpedia.org).  
- Updates included:  
  - **Semi-dynamic website** design for easier updates.  
  - **Multilingual support**: Amharic, English, and German (with Google Translate used for initial translations).  
  - **Menu reorganization** for improved navigation.  
  - **Updated look & feel** for a more polished experience.  

---

### 2. Documentation
- Documentation prepared and pushed to GitHub:  
  [Project Documentation](https://github.com/AmharicDBpedia/AmharicDBpedia/tree/GSOC2025/documentation)  
- Converted the full documentation into a **GitHub Wiki** for easier access and collaboration:  
  [AmharicDBpedia Wiki](https://github.com/AmharicDBpedia/AmharicDBpedia/wiki)  

---

### 3. Mappings and Statistics
- Updated **Amharic mappings**, the **mapping statistics report**, and the **Amharic ignore list**.  
- Submitted all updates as a **Pull Request** to the main repository. [View Pull Request #781](https://github.com/dbpedia/extraction-framework/pull/781)

---

### 4. Project Report Page
- Updated the project report page with all the latest work:  
  [GSoC 2025 DBpedia Amharic Chapter Report](https://github.com/contact-andy/GSoC-25_DBpedia_Amharic_Chapter)  

---

### 5. GSoC Final Submission
- Completed and submitted the **official GSoC final submission form** on **September 01, 2025**.  
- Sent a brief **achievement summary report** to mentors, as requested.  

---

### 6. Unit Test Progress
- Unit test development was already started last week, and I continued working on it this week.  
- Current result: no tests executed. More debugging and refinement are required, and this will be continued after GSoC.  

---

### 7. Blog Updates
- Published the **Week 13 and Week 14 blog posts** on the GitHub Pages project blog.  

---

## Reflections on the GSoC Journey

### Experience
Participating in GSoC with **DBpedia** was an invaluable experience. It provided me the opportunity to contribute to an international open-source project, collaborate with mentors, and improve structured knowledge representation for the Amharic language.  

### Knowledge
I gained deeper insights into:  
- The **DBpedia Extraction Framework** and its internal components.  
- Mapping Wikipedia templates and properties to the **DBpedia Ontology**.  
- Handling multilingual challenges, Unicode issues, and ignore-list debugging.  
- Managing open-source workflows using GitHub, PRs, and collaborative reviews.  

### Skills
Over the past three months, I strengthened my skills in:  
- **Scala programming** (modifying `MappingStatsBuilder.scala`, `CreateMappingStats.scala`, and `Language.scala`).  
- **Data extraction and analysis** using RDF dumps and statistics generation.  
- **Automation workflows** for template and property mappings.  
- **Technical writing** through project documentation, blog posts, and reports.  
- **Collaboration** and communication with mentors and the DBpedia community.  

### Challenges
- Finding appropriate **DBpedia ontology properties** for Amharic templates was time-consuming and required careful validation.  
- Unicode mismatches in templates caused unexpected bugs in statistics generation.  
- The **automation process** for mapping could not be fully completed within the GSoC timeframe.  
- Debugging issues in the extraction framework (e.g., the **user-agent bug in `Language.scala`**) required extensive investigation.  

### Acknowledgements
I would like to express my sincere gratitude to my mentors ([Ricardo Usbeck](https://www.linkedin.com/in/ricardo-usbeck/?originalSubdomain=de), [Tilahun Abedissa Taffa](https://www.linkedin.com/in/tilahun-abedissa-47372a9a/?originalSubdomain=et), [Hizkiel Alemayehu](https://www.linkedin.com/in/hizkiel-mitiku-alemayehu-97306010b/), [Meti Bayissa](https://www.linkedin.com/in/metiadanebayissa/)) for their **guidance, encouragement, and constructive feedback** throughout the project .
Their support was crucial in overcoming technical challenges, prioritizing tasks, and ensuring steady progress.  
Special thanks also go to the **DBpedia community**, who welcomed contributions and provided valuable insights along the way.  

---

## Conclusion
This week marked the official **completion of the GSoC 2025 project**. While some tasks such as automation and unit test refinement will continue beyond the program, the key objectives were successfully delivered:  
- **Comprehensive Amharic mappings**,  
- **Improved statistics pipeline**,  
- **Updated documentation and website**, and  
- **Final project reporting**.  

The project lays a strong foundation for expanding **Amharic DBpedia** in the future, with opportunities for further automation, refinement, and integration into the DBpedia ecosystem.  

