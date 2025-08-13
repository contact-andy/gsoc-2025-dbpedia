---
layout: post
title: "Week 10: Mapping Statistics Debugging and Automation Progress"
short_title: "Week-10"
date: 2025-08-09
categories: [gsoc, dbpedia]
---

This post summarizes the progress made during the tenth GSoC coding week (August 03 – August 09). The main focus this week was debugging the mapping statistics generation process, documenting its workflow in detail, and advancing the automation of Amharic Wikipedia template creation and DBpedia mappings.

<!--more-->

## Tasks Completed

### 1. Mapping Statistics Debugging
Following the recent mapping statistics report, I worked on corrective actions to address previously identified issues in Amharic DBpedia mappings.  
The latest updates showed **an increase in both template and property mappings**, indicating that the fixes are improving the statistics output.

To better understand the statistics pipeline, I reviewed all scripts involved in **gathering statistics** for templates and properties, documenting the process. The statistics scripts provide:
- **Which templates exist** in Wikipedia.
- **Which properties** each template contains.
- **Template usage frequency** (number of pages using each template).
- **Property usage frequency** (how often each property appears).

**Required RDF files:**
- `xxwiki-yyyymmdd-transitive-redirects.ttl`
- `xxwiki-yyyymmdd-article-templates.ttl`
- `xxwiki-yyyymmdd-template-parameters.ttl`
- `xxwiki-yyyymmdd-infobox-test.ttl`

**Extractors used during configuration:**
- `org.dbpedia.extraction.mappings.RedirectExtractor`
- `org.dbpedia.extraction.mappings.ArticleTemplatesExtractor`
- `org.dbpedia.extraction.mappings.TemplateParameterExtractor`
- `org.dbpedia.extraction.mappings.InfoboxExtractor`

**Execution flow:**
1. **CreateMappingStats.scala** loads the above RDF files and passes them into **MappingStatsBuilder.scala**.
2. Key methods in `MappingStatsBuilder`:
   - `loadTemplateRedirects` → reads `transitive-redirects.ttl` and generates template redirects.
   - `countTemplates` → counts templates from `article-templates.ttl`.
   - `propertyDefinitions` → lists properties from `template-parameters.ttl` and initializes property counts.
   - `countProperties` → reads `infobox-test.ttl` to update property usage counts.
3. **WikipediaStats.scala** takes the processed redirects and statistics, formats them, and writes output for the statistics UI.

**Key Findings:**
- The first three RDF files were processed successfully.
- The **`infobox-test.ttl`** file failed in several scenarios:
  1. File was **empty**.
  2. File contained **invalid RDF triples**.
  3. File contained **valid triples but in an incompatible format** for property counting.
- When I manually generated the file in the expected format, **property counting worked**.
- This indicates the need for **further work on file generation** and possibly testing with `infobox_properties.ttl` in the coming week.

---

### 2. Automation of Template and Mapping Creation
I also continued developing a script to automate Amharic Wikipedia template creation and DBpedia mapping.  
The major steps are:
1. **Fetch English template text** using the Wikipedia API ✅
2. **Extract attributes** via a parser ✅
3. **Translate attributes** using an LLM (in progress — evaluating free LLMs for translation)
4. **Generate Amharic Wikipedia template**
5. **Generate Amharic DBpedia mapping**

Currently, the first two steps are complete, and translation work is in progress.

---

### 3. Meetings and Updates
- Attended the **Week 10 mentor meeting** on **August 08, 2025**.
  - Presented the current debugging results.
  - Mentors recommended:
    - Continuing mapping statistics work with updated templates and properties.
    - Testing translation tools for automation.
- Published the **Week 9 blog post** to the GitHub Pages project blog.

---

## Challenges
- The `infobox-test.ttl` file remains a bottleneck for accurate property counting.
- Automation requires a reliable translation tool for property names and descriptions.

---

## Next Steps
- Continue **mapping statistics generation** with updated templates.
- Progress **DBpedia Live extraction** for Amharic.
- Complete the **automation workflow** for template and mapping creation.

---

## Conclusion
This week’s work clarified the inner workings of the mapping statistics process and identified why property counts were failing. Manual testing confirmed that the method works when the input file is correct, guiding future fixes. Alongside this, progress on automation sets the stage for a faster and more scalable template-to-mapping pipeline in the coming weeks.
