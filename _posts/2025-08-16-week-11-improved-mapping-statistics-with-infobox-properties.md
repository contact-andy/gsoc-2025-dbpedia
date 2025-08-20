---
layout: post
title: "Week 11: Improved Mapping Statistics with Infobox Properties"
short_title: "Week-11"
date: 2025-08-16
categories: [gsoc, dbpedia]
---

This post summarizes the progress made during the eleventh GSoC coding week (August 10 – August 16).  
The main focus was on improving **mapping statistics generation** by replacing the `infobox-test.ttl` file with the `infobox-properties.ttl` file, and extending the statistics builder to handle property normalization and template-to-page mapping.

<!--more-->

## Tasks Completed

### 1. Mapping Statistics Update
Previously, the statistics pipeline failed to properly count properties because of issues with `infobox-test.ttl`. This week, I updated the **CreateMappingStats.scala** and **MappingStatsBuilder.scala** classes to use `infobox-properties.ttl`.  

#### Key Changes
1. **CreateMappingStats.scala**
   - Added a line to read the `infobox-properties.ttl` file via `DBpediaDatasets.InfoboxProperties`.  
   - Passed the new file as an argument to the **MappingStatsBuilder**.

2. **MappingStatsBuilder.scala**
   - **Updated methods:**
     - **`buildStats`**
       - Added `infoboxPropertiesFile` parameter.  
       - Introduced a `pageToTemplate` map to store page–template associations.  
       - If property counts from `infobox-test.ttl` are zero, the new function `countPropertiesFromInfoboxProps` is called.  
     - **`countTemplates`**
       - Extended to populate the `pageToTemplate` map with page titles and template names.  
     - **`stripUri`**
       - Now checks both `propertyUriPrefix` and `http://dbpedia.org/property/` URIs.  
   - **New methods:**
     - **`normalizePropertyName`** → normalizes properties by removing underscores and spaces (e.g., `"አልበም_ስም"` → `"አልበምስም"`).  
     - **`countPropertiesFromInfoboxProps`** → an alternative to `countProperties`, using `infobox-properties.ttl` for property counting.

#### Outcome
With these updates, the **mapping statistics now work with the current dump and mappings**. Some templates still require additional property editing, which will be addressed in the next iteration.

![Screenshot of mapping statistics](https://github.com/contact-andy/gsoc-2025-dbpedia/blob/main/images/statistics-screenshot.png)

---

### 2. Ignore-list implementation 
- I have explored **ignore-lists** in the statistics.  
  This file contains a list of templates and properties to be ignored in the mapping statistics report.  
  I added the following templates, which are more suitable as pages rather than properties of a template:

  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ኤ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ቢ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ሲ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ዲ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ኢ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ኤፍ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ጂ  
  - የ2010 እ.ኤ.አ. ፊፋ የዓለም ዋንጫ ምድብ ኤች  

- Once I added these to the ignore list and regenerated the mapping statistics, the updated report looked like this:  

![Screenshot of mapping statistics after applying ignore list](https://github.com/contact-andy/gsoc-2025-dbpedia/blob/main/images/statistics-screenshot-with-ignore-list.png)

- However, for unknown reasons the mapping statistics report ignored only two of the templates.  
  This requires additional debugging in the ignore-list implementation next week.
  
---

### 3. Mentor Meeting
- Attended the **Week 11 mentor meeting** on **August 15, 2025**.  
- Shared the improved statistics results and discussed next steps.  
- Mentors recommended continuing with:
  - Mapping missed templates and properties.
  - Ensuring 100% statistics coverage before scaling to live extraction.

---

### 4. Blog Post Update
- Published the **Week 10 blog post** on the GitHub Pages project blog.

---

## Next Steps
- Debugging in the ignore-list implementation 
- Map missed templates and properties to reach **100% coverage** in statistics.  
- Progress the **DBpedia Live extraction** for Amharic.  
- Complete the **automation workflow** for template and mapping creation.  

---

## Conclusion
This week marked an important milestone in fixing the statistics pipeline. By introducing `infobox-properties.ttl` and improving property normalization, the statistics system now works more reliably with the latest dump and mappings. This lays the groundwork for achieving full coverage and advancing to live extraction and automation in the coming weeks.
