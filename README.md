Trying to write about possible projects to do about the coronavirus crisis is much harder than I thought, 
as I keep thinking of new google queries to try, getting down rabbit holes and then thinking of new possible things to do.
but here's an attempt at reviewing my thoughts this week.

1. I wanted to use NLP to read biomedical texts;

2. I wanted to deal with "clinical guidelines", as these are texts supposed to be written by doctors for laypeople 
(as well as medical people), so they ought to be very explicit and not depend on lots of extra background that doctors 
can expect other doctors to have, but not any joe in the streets;

3. My expectation is that many of these texts will still have quite a lot of "domain knowledge" in the shape of names of diseases 
or conditions, names of drugs or medications or procedures, etc.

4. I know of at least one taxonomy for these clinical terms, called SNOMED CT (CT is for clinical terms http://www.snomed.org/) 
(https://tools.wmflabs.org/freebase/m/08wb1y). 

Another is Unified Medical Language System (UMLS) https://lhncbc.nlm.nih.gov/system/files/pub2001027.pdf

5. these SNOMED CTs have been mapped to Wikidata see project description in 
https://www.wikidata.org/wiki/Wikidata:Property_proposal/SNOMED_CT_identifier

6. given a silly sentence such as "If the patient has a leg injury, paracetamol is not necessary." our GKR system 
(http://lap0973.sprachwiss.uni-konstanz.de:8080/sem.mapper/) will parse the sentence, but not know what to do with "paracetamol" as 
WordNet only has "acetaminophen" or  Tylenol, not paracetamol 
(Wikidata tells me that paracetamol and acetaminophen are the same, but with these resources automatically created one never knows)
02674482-n English (an analgesic for mild pain but not for inflammation; also used as an antipyretic; (Datril, Tylenol, Panadol, Phenaphen, 
Tempra, and Anacin III are trademarks of brands of acetaminophen tablets))Tylenol 

7. Now how to stop this from happening? how to make sure that if a term is not found in WordNet then Wikidata is searched and 
presumably (because it has links to SNOMED CT and MeSH https://www.wikidata.org/wiki/Property:P486) found?

8. So there was a workshop last year https://clinical-nlp.github.io/2019/ where they collected many resources.
there are by now several collections of resources on covid19 and the coronavirus and the question is what  one should we try to do.

9. if interested in ontologies and Wikidata we should look at https://www.wikidata.org/wiki/Wikidata:WikiProject_COVID-19

10. also interesting one of the resources on the website above is a database of drugs used that people have tried to repurpose and 
their medical trials.
https://clue.io/repurposing
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5568558/

11. my idea was to look at medical guidelines for flu-like symptoms in say
https://www.cdc.gov/flu/index.htm
https://www.cdc.gov/flu/professionals/diagnosis/clinician_guidance_ridt.htm
https://www.cdc.gov/flu/professionals/infectioncontrol/peri-post-settings.htm
https://www.cdc.gov/flu/professionals/antivirals/summary-clinicians.htm
try to construct a minitheory or at least a corpus of it and see what there is in Wikidata.

But I haven't done anything yet. a friend sent me some easy "sentences" (attached) so that I can at least try them in our GKR system
and check how bad we're doing. GKR can't deal with conditionals, yet.

12. Medical WordNet: a new methodology for the construction and validation of information resources for consumer health
Authors: Barry  Smith and Christiane  Fellbaum 
COLING '04: Proceedings of the 20th international conference on Computational Linguistics August 2004 Pages 371–es https://doi.org/10.3115/1220355.1220409
https://www.aclweb.org/anthology/C04-1054.pdf
http://verbs.colorado.edu/~mpalmer/Ling7800/WN-BioWN.pdf
http://compling.hss.ntu.edu.sg/events/2018-gwc/pdfs/GWC2018_paper_49.pdf Wordnet of Medical Events GWC2018

13. First International Workshop on Formal Biomedical Knowledge Representation (KR-MED 2004)
http://ceur-ws.org/Vol-102/
very clear presentation on UMLS
https://www.slideshare.net/roger961/the-unified-medical-language-system-what-is-it-and-how-to-use-it

14. https://github.com/stylerw/thymedata This is a repository for annotation data for the THYME Project, a clinical natural language processing project dedicated to extracting useful temporal relations from the clinical narrative. http://thyme.healthnlp.org (M. Palmer included)

15. Recent open source dataset from Roam Analytics (Potts)
Effective Feature Representation for Clinical Text Concept Extraction. Proceedings of the NAACL Workshop on Clinical Natural Language Processing (NAACL-ClinicalNLP), 2019.https://github.com/roamanalytics/roamresearch/tree/master/Papers/Feature4Healthcare or
https://github.com/roamanalytics/roamresearch/tree/master/Papers/PSL-drugs-diseases

16. There's plenty of text about the coronavirus and covid-19, mostly research papers, e.g. "Microsoft Research, the National Library of Medicine, and the Allen Institute for AI (AI2), gathered and prepared over 29,000 papers related to the new virus and the wider coronavirus family, 13,000 of them processed so that computers can read the underlying data, plus information about the authors and their affiliations. from https://www.wired.com/story/researchers-deploy-ai-better-understand-coronavirus/".
https://c3dti.ai/ is another consortium. They say:
An initial list of preloaded data sets include:

    Epidemiological Data: Johns Hopkins
    Clinical Data: Line Lists
    Genomic Data: NCBI Viral Sequences
    Journal Articles: CORD-19 Dataset
    Epidemiological Data: WHO Situational Reports
    Epidemiological Data: Atlantic COVID-19 Tracking Project
    Clinical Data: COVID-19 Chest X-Ray and CT Images
(can't find all of these data myself!)

17. Wikidata Imbalance Dashboard https://prowd.netlify.com/
infectious disease - Q18123741
disease caused by infection of pathogenic biological agents in a host organism
Number of entities: 493

18. AZ suggests checking https://www.statnews.com/
seems well-written news about COVID-19.

19.  Kaggle dataset also suggested by AZ
https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge

Description: In response to the COVID-19 pandemic, the White House and a coalition of leading research groups have prepared the COVID-19 Open Research Dataset (CORD-19). CORD-19 is a resource of over 51,000 scholarly articles, including over 40,000 with full text, about COVID-19, SARS-CoV-2, and related coronaviruses. This freely available dataset is provided to the global research community to apply recent advances in natural language processing and other AI techniques to generate new insights in support of the ongoing fight against this infectious disease. There is a growing urgency for these approaches because of the rapid acceleration in new coronavirus literature, making it difficult for the medical research community to keep up.

Call to Action
They are issuing a call to action to the world's artificial intelligence experts to develop text and data mining tools that can help the medical community develop answers to high priority scientific questions. The CORD-19 dataset represents the most extensive machine-readable coronavirus literature collection available for data mining to date. This allows the worldwide AI research community the opportunity to apply text and data mining approaches to find answers to questions within, and connect insights across, this content in support of the ongoing COVID-19 response efforts worldwide. There is a growing urgency for these approaches because of the rapid increase in coronavirus literature, making it difficult for the medical community to keep up.

A list of our initial key questions can be found under the Tasks section of this dataset. These key scientific questions are drawn from the NASEM’s SCIED (National Academies of Sciences, Engineering, and Medicine’s Standing Committee on Emerging Infectious Diseases and 21st Century Health Threats) research topics and the World Health Organization’s R&D Blueprint for COVID-19.
Many of these questions are suitable for text mining, and we encourage researchers to develop text mining tools to provide insights on these questions.

They are maintaining a summary of the community's contributions. For guidance on how to make your contributions useful, we're maintaining a forum thread with the feedback we're getting from the medical and health policy communities.
Prizes: Kaggle is sponsoring a $1,000 per task award to the winner whose submission is identified as best meeting the evaluation criteria. The winner may elect to receive this award as a charitable donation to COVID-19 relief/research efforts or as a monetary payment. More details on the prizes and timeline can be found on the discussion post.
Accessing the Dataset
We have made this dataset available on Kaggle. Watch out for periodic updates.The dataset is also hosted on AI2's Semantic Scholar. And you can search the dataset using AI2's new COVID-19 explorer. The licenses for each dataset can be found in the all _ sources _ metadata csv file.

20. Wikidata COVID-19 dashboard https://sites.google.com/view/covid19-dashboard/
