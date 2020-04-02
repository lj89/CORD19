# CORD19

CORD19 project is about Text Mining, Knowledge Discovery & Question Answer.
Our goal: efficiently extract information from 45,000 + papers to find cures for COVID-19.

By Keyword Window search with keywords identified by domain knowledge, I found the following 
#### Potential drug candidates:
therapeutic peptides , antiviral nucleosides target rna polyermase; protease inhibitor; monoclonal antibody can be a target; macrocyclic peptides; gs5734; quercetin; pb2 subunit; xinjiaxiangruyin; iav usurps zbtb25; m2 inhibitors; nitazoxanide ntz; active small molecular inhibitors; NHC;… (Based on past researches on sars/mers,flu, hcv,herp, ebov – other diseases caused by rna viruses)

My method of identify similar papers based cosine similarity is tested to be effective.

Question Answering system based on the same method also seem to work, but need further validation.

More research can be done use the top words identified in text mining in combination with domain knowledge. I plan to come back after my final projects to dig deeper.

Also got pretty good document dlustering results. Worth trying to label the clusters. May find useful information.


### Submissions on Kaggle

### Part 1 data preprocessing and EDA 
(with all avilable data at the time the research was conducted -- 45230 papers. The notebook is 90M in size so I can only upload a version with only partial output on GitHub. Also the Kaggle website had some problem saving all output. )

https://www.kaggle.com/leijiang1/part-1-data-preprocessing-and-eda?scriptVersionId=31277199

### Part 2 TFIDF Clustering at Abstract level 
(with all available abstracts at the time the research was conducted -- 35177 papers)

https://www.kaggle.com/leijiang1/part-2-tfidf-clustering-at-abstract-level

### Part 3 What can we learn from the keyword window “polymerase + therapeut”?

https://www.kaggle.com/leijiang1/part-3-keyword-window-polymerase-therapeut-r

### Part 4 Identify similar papers and Question Answering based cosine similarity

hthttps://www.kaggle.com/leijiang1/part-4-identify-similar-papers-based-on-cossim?scriptVersionId=31293853

### Part 5 T5 validation of Question Answering Outputs
https://www.kaggle.com/leijiang1/part-5-t5-validation-of-question-answering-outputs?scriptVersionId=31327890#Code
