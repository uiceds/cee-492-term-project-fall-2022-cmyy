---
title: Environmental-Friendliness of Buildings in New York
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-09-26'
author-meta:
- Yu-Sian Lin
- Yueh-Ti Lee
- Minjiang Zhu
- Chengyou Yue
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Environmental-Friendliness of Buildings in New York" />
  <meta name="citation_title" content="Environmental-Friendliness of Buildings in New York" />
  <meta property="og:title" content="Environmental-Friendliness of Buildings in New York" />
  <meta property="twitter:title" content="Environmental-Friendliness of Buildings in New York" />
  <meta name="dc.date" content="2022-09-26" />
  <meta name="citation_publication_date" content="2022-09-26" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Yu-Sian Lin" />
  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />
  <meta name="citation_author" content="Yueh-Ti Lee" />
  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />
  <meta name="citation_author" content="Minjiang Zhu" />
  <meta name="citation_author_institution" content="Department of Something, University of Illinois" />
  <meta name="citation_author" content="Chengyou Yue" />
  <meta name="citation_author_institution" content="Department of Civil Engineering, University of Illinois" />
  <link rel="canonical" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta property="og:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta property="twitter:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta name="citation_fulltext_html_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/" />
  <meta name="citation_pdf_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/3babd3bb485cb4fa572b1b61634ca281fcc84004/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/3babd3bb485cb4fa572b1b61634ca281fcc84004/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/3babd3bb485cb4fa572b1b61634ca281fcc84004/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...

## Authors



+ **Yu-Sian Lin**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [yslin0114](https://github.com/yslin0114)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>

+ **Yueh-Ti Lee**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Yueh-Ti](https://github.com/Yueh-Ti)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>

+ **Minjiang Zhu**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Minjiang-Zhu](https://github.com/Minjiang-Zhu)<br>
  <small>
     Department of Something, University of Illinois
  </small>

+ **Chengyou Yue**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [TensorYue](https://github.com/TensorYue)<br>
  <small>
     Department of Civil Engineering, University of Illinois
  </small>









## Description:
Source: Kaggle / NYC Mayor's Office of Climate & Environmental Justice

Data Format: CSV File

Content: The dataset contains information on properties regarding its basic information, indices used for evaluating energy efficiency, types of energy used in the property, and greenhouse gas (GHG) emissions.

## Attributes:

Property name: name of the property.

Borough: borough for the property.

Primary property use type: main property usage (ex: office, housing, hotel).

Gross floor area (GFA) for primary use type: property area for main use in square ft.

Secondary property use type: secondary property usage (ex: office, housing, hotel).

Gross floor area (GFA) for secondary use type: property area for secondary use in square ft.

Year built: the year the property is built. If it has gone through a complete renovation, the renovation year can be the built year.

Occupancy: percentage of the property GFA that is occupied and operational.

Energy metered areas: areas within the property that is covered by energy meters.

Water metered areas: areas within the property that is covered by water meters.

ENERGY STAR Score: a score based on energy usage.

Source energy use intensity(EUI): EUI calculated from the energy source, in kBtu/ft^2, where kBtu is thousand British thermal units.

Weather normalized source EUI:  EUI normalized for weather.

Weather normalized site electricity intensity: weather normalized site electricity intensity per GFA.

Weather normalized site natural gas intensity: weather normalized site natural gas intensity per GFA.

Fuel oil: annual fuel oil used, in kBtu.

Diesel: annual diesel used, in kBtu.

Natural gas: annual natural gas used, in kBtu.

Electricity: annual electricity used, in kBtu.

Water: annual water use, in kGal.

Direct GHG emission: annual direct GHG emission emitted from the property, in tons of carbon dioxide equivalent.

Indirect GHG emission: annual indirect GHG emission emitted from the property, in tons of carbon dioxide equivalent.

Total GHG emission: sum of direct and indirect GHG emissions in tons of carbon dioxide equivalent.


## Proposal:

We plan to develop a model that can predict a property's environmental friendliness based on its GHG emission and energy efficiency. Types of energy used can affect the GHG emission of a property. Weather, property age, floor area, and so on can affect energy efficiency. We will start by finding the correlation between energy sources and GHG emissions. We will then evaluate both GHG emission and energy efficiency indices to obtain the extent of the environmental friendliness of a property.



## References

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
[Energy Efficiency of buildings in New York]([https://manubot.org](https://www.kaggle.com/datasets/mikhailma/energy-efficiency-of-buildings-in-new-york))
