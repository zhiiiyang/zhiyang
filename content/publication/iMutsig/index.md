---
abstract: There are two frameworks for characterizing mutational signatures which are commonly used to describe the nucleotide patterns that arise from mutational processes. Estimated mutational signatures from fitting these two methods in human cancer can be found online, in the Catalogue Of Somatic Mutations In Cancer (COSMIC) website or a GitHub repository. The two frameworks make differing assumptions regarding independence of base pairs and for that reason may produce different results. Consequently, there is a need to compare and contrast the results of the two methods, but no such tool currently exists. In this paper, we provide a simple and intuitive interface that allows such comparisons to be easily performed. When using our software, the user may download published mutational signatures of either type. Mutational signatures from the pmsignature data source are expanded to probabilistic vectors of 96-possible mutation types, the same model specification used by COSMIC, and then compared to COSMIC signatures. Cosine similarity measures the extent of signature similarity. iMutSig provides a simple and user-friendly web application allowing researchers to compare signatures from COSMIC to those from pmsignature, and vice versa. Furthermore, iMutSig allows users to input a self-defined mutational signature and examine its similarity to published signatures from both data sources. 
authors:
- Zhi Yang
- Priyatama Pandey
- Paul Marjoram
- Kimberly D. Siegmund

date: "2020-06-10T00:00:00-07:00"
doi: "10.12688/f1000research.24435.1"
featured: true
image:
  focal_point: ""
math: true
projects:
- cancer
publication: In  *F1000Research*
publication_short: In *F1000Research*
publication_types:
- "2"
summary:  
tags: 
- R
- Shiny
title: iMutSig - a web application to identify the most similar mutational signature using shiny
url_code: "https://github.com/USCbiostats/iMutSig"
url_dataset: ""
url_pdf: ""
url_poster: ""
url_preprint: "https://f1000research.com/articles/9-586"
url_project: ""
url_slides: ""
url_source: ""
url_video: ""
---