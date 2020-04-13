Trying to write to you about stuff to do about the coronavirus crisis is much harder than I thought, 
as I keep thinking of new google queries to try, getting down rabbit holes and then thinking of new possible things to do.
but here's an attempt at reviewing my thoughts.

1. I wanted to use NLP to read biomedical texts;

2. I wanted to deal with "clinical guidelines", as these are texts supposed to be written by doctors for laypeople 
(as well as medical people), so they ought to be very explicit and not depend on lots of extra background that doctors 
can expect other doctors to have, but not any joe in the streets;

3. My expectation is that many of these texts will still have quite a lot of "domain knowledge" in the shape of names of diseases 
or conditions, names of drugs or medications or procedures, etc.

4. I know of at least one taxonomy for these clinical terms, called SNOMED CT (CT is for clinical terms) 
(https://tools.wmflabs.org/freebase/m/08wb1y). 

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