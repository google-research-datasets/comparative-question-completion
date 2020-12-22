Dataset name: XComp


What’s in the dataset?


The dataset includes short questions in natural language that make comparisons between entity pairs, for example, “is a cockroach or beetle more dangerous?” 

The questions are in three subject domains: animals, cities and NBA players. 

In each sentence, one of the compared entities in the sentence has been 'masked' (replaced with a [MASK] symbol). For example, for the question above the masked sentence is: “is a [MASK] or beetle more dangerous?”
The dataset presents the task of automatically recovering the masked entity name, and provides the original entity for evaluation purposes. In addition to the original masked entity text (e.g., 'cockroach'), it details the respective Wikidata entity ID, (e.g., 'Q18123008').



Structure of the data:

Text files of tab-separated columns. There are three files of identical structure, per subject domain.

Data elements:

1. A sentence-long question, in which an entity name has been replaced with a genetic '[MASK]' token. The text has been pre-processed using BERT, and the beginning and end of the sentence are denoted by [CLS] and [SEP] tokens.
Example: “[CLS] is a [MASK] or beetle more dangerous ? [SEP]”


2. The masked text span
Example: 'cockroach' 


3. The Wikidata entity identifier, which maps to the masked text. This mapping was obtained automatically using an entity linking system. 
Example: 'Q18123008' (The Wikidata entity page is located at https://www.wikidata.org/wiki/Q18123008)

4. The conjectured property along which the comparison is made. This property was identified heuristically, based on the sentence’s text.
Example: 'dangerous'



