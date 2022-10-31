---
title: Environmental-Friendliness of Buildings in New York
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-10-31'
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
  <meta name="dc.date" content="2022-10-31" />
  <meta name="citation_publication_date" content="2022-10-31" />
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
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/995e0bca751813bf7d08769820737c3e54a7d0bc/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/995e0bca751813bf7d08769820737c3e54a7d0bc/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-cmyy/v/995e0bca751813bf7d08769820737c3e54a7d0bc/manuscript.pdf" />
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
Source: Kaggle/ Adoptable Dogs in the US

Data Format: CSV File

Content: The dataset contains information on over 3,000 adoptable dogs listed on PetFinder.com regarding to their origins, as well as the state they are currently listed for adoption in.


## Attributes:

contact_city: The city where the animal is located. (String)

contact_state: The state where the animal is located. (String)

description: A description of the animal. (String)

url: The URL of the animal's profile on PetFinder. (String)

type.x: The type of animal. (String)

species: The species of the animal. (String)

breed_primary: The primary breed of the animal. (String)

breed_secondary: The secondary breed of the animal. (String)

breed_mixed: Whether the animal is a mixed breed. (String)

breed_unknown: Whether the animal's breed is unknown. (String)

color_primary: The primary color of the animal. (String)

color_secondary: The secondary color of the animal. (String)

color_tertiary: The tertiary color of the animal. (String)

age: The age of the animal. (String)

sex: The animal's sex. (String)

size: The size of the animal. (String)

coat: The type of coat the animal has. (String)

fixed: Whether the animal is spayed or neutered. (String)

house_trained: Whether the animal is house trained. (String)

declawed: Whether the animal is declawed. (String)

special_needs: Whether the animal has any special needs. (String)

shots_current: Whether the animal is up to date on shots. (String)

env_children: Whether the animal is good with children. (String)


## Proposal:

We plan to develop a model that can predict the extent of children-friendliness of adoptable dogs based on the dog’s origin information, such as the dog’s breed, color, age and so on, so that families with children can take this model for reference when planning to adopt a dog. We will start by finding the correlation between the dog’s features and env_children in the dataset. We will then evaluate the indices to obtain the extent of the children-friendliness of a dog.



## References

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
[Energy Efficiency of buildings in New York]([https://manubot.org](https://www.kaggle.com/datasets/mikhailma/energy-efficiency-of-buildings-in-new-york))
