# CORD19

CORD19 project is about Text Mining, Knowledge Discovery & Question Answer.
Our goal: efficiently extract information from 45,000 + papers to find cures for COVID-19.

### I opensource all my code for this project on Kaggle and keep a copy of my code here.

By Keyword Window search with keywords identified by domain knowledge, I found the following 
#### Potential drug candidates:
therapeutic peptides , antiviral nucleosides target rna polyermase; protease inhibitor; monoclonal antibody can be a target; macrocyclic peptides; gs5734; quercetin; pb2 subunit; xinjiaxiangruyin; iav usurps zbtb25; m2 inhibitors; nitazoxanide ntz; active small molecular inhibitors; NHC;… (Based on past researches on sars/mers,flu, hcv,herp, ebov – other diseases caused by rna viruses)

My method of identify similar papers based cosine similarity is tested to be effective.

Question Answering system based on the same method also seem to work, but need further validation.

More research can be done use the top words identified in text mining in combination with domain knowledge. I plan to come back after my final projects to dig deeper.

Also got pretty good document dlustering results. Worth trying to label the clusters. May find useful information.


Update: T5 (Text-To-Text Transfer Transformer) ‘s summarizer function helped me read the 20 abstracts output form my Question Answering system (see the last post about my Kaggle submission). The results are exciting! See Part 5 T5 validation of Question Answering Outputs.


### Submissions on Kaggle

### Part 1 data pre-processing and EDA 
(with all available data at the time the research was conducted -- 45230 papers. The notebook is 90M in size so I can only upload a version with only partial output on GitHub. Also the Kaggle website had some problem saving all output. )

https://www.kaggle.com/leijiang1/part-1-data-preprocessing-and-eda?scriptVersionId=31277199

### Part 2 TFIDF Clustering at Abstract level 
(with all available abstracts at the time the research was conducted -- 35177 papers)

https://www.kaggle.com/leijiang1/part-2-tfidf-clustering-at-abstract-level

### Part 3 What can we learn from the keyword window “polymerase + therapeut”?

https://www.kaggle.com/leijiang1/part-3-keyword-window-polymerase-therapeut-r

### Part 4 Identify similar papers and Question Answering based cosine similarity
https://www.kaggle.com/leijiang1/part-4-identify-similar-papers-based-on-cossim

### Part 5 T5 validation of Question Answering Outputs
https://www.kaggle.com/leijiang1/part-5-t5-validation-of-question-answering-outputs

### Part 6 Ask questions on Therapeut3775 subset
https://www.kaggle.com/leijiang1/part-6-ask-questions-on-therapeut3775-subset


---------------------------------------------------------

### UPDATE:

## Reuseable pipelines
### Reuse the pipeline built in Part 4 to answer more questions about therapeutics.


to validate the question answering system and also demo how to resuse the pipeline created.

#### Data:

Therapeut3775 subset generated on april 1 in part 3 notebook


### then validate the results use pipeline in Part 5



------------------------------------

I also compared using full abstract and keyword WINDOW generated for question answering. 

asked more questions:

Question1=['What are clinical effective therapeutics or drugs for COVID-19?']

Question2=['What are the therapeutic target genes for COVID-19 or coronavirus?']

Question3=['What are the therapeutic targets for COVID-19 or coronavirus ?']


from validation results, ask questions1,2 on WINDOW did not yield good results.



Like to use Question2 to evualate since it has reference answer from Benchsci dataset.

Question3 is the question I really want answer since therapeutic is not limited to gene related methods.


## Results

#### Question2=['What are the therapeutic target genes for COVID-19 or coronavirus?']

#### for WINDOW method (see code on my github) although answers are kind of related. but not detail enough.
#### so WINDOW is not very useful to dig deep, judging from Q2. did not mention many genes in benchsci data.


#### for Q1 
have not got the chance to validate. but i think
at least should mention hiv drug effective to be a good answer


code for using full abstract (go to the end for the question answring code):

https://github.com/lj89/CORD19/blob/master/Therapeut_Part_4_Identify_similar_papers_based_on_cosSim.ipynb
