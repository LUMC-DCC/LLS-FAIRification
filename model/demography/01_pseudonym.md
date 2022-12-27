### Model participant and family ID

```mermaid
%%{init: {'theme':'base'}}%%
graph TD
   
    J{ID:<br> famID} --> |rdf:type| K[ncit:identifier]
    J -->|stato:has value| L((233))
    H{Family} --> |rdf:type| I[ncit:family]
    A{Person} -->|rdf:type| B[ncit:person]
    C{Role:<br> Study participant} -->|rdf:type| D[ncit:human study subject]
    C -->|rdf:type| E[ro:role]
    F{ID:<br> LLnr} --> |rdf:type| G[ncit:identifier]
    A -->|ro:has role| C
    J -->|iao:denotes| H
    A -->|ro:member of| H
    F -->|iao:denotes| C
    F -->|stato:has value| M((01-01-222))
    
    classDef literal fill:#dae8fc;
    classDef ontology fill:#d5e8d4;
    class L,M literal;
    class K,I,B,D,G,E ontology;
 ```

### Description
1. A person, defined by the NCIT-term for person, has a role as study participant in LLS. This person is also member of a family. It is explicitly defined that the role study participant is 1) a role; and human study subject.
2. There is an ID that refers to a study participant which is of type identifier and has a certain value. Family, defined by the NCIT-term for family, also has an ID of type identifier and a value.
3. The two ID's are unambigiously defined by the combination of two triples: the specific ID is of type identifier (triple 1), and it is specified what the ID denotes (triple 2)

### Abbreviations
* ncit = [National Cancer Institute Thesaurus OBO edition](https://ontobee.org/ontology/ncit)
* ro = [Relation Ontology](https://ontobee.org/ontology/RO)
* iao = [Information Artefact Ontology](https://ontobee.org/ontology/IAO)
* stato = [Statistical Methods Ontology](https://ontobee.org/ontology/STATO)

### Example RDF (turtle)
```ttl
@prefix obo: <http://purl.obolibrary.org/obo/> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

#Person is of type ncit:person, has a role as study participant and is member of a family
<http://lls_example_data.org/person/001-001-001> a obo:NCIT_C25190 ;
    obo:RO_0000087 <http://lls_example_data.org/study_participant/001-001-001> ;
    obo:RO_0002350 <http://lls_example_data.org/longevity_family/233> .

#Participant ID (LLnr) is of type ncit:identifier, denotes the study participant role and has a certain value
<http://lls_example_data.org/participant_identifier/001-001-001> a obo:NCIT_C25364 ;
    obo:IAO_0000219 <http://lls_example_data.org/study_participant/001-001-001> ;
    obo:STATO_0000129 "001-001-001"^^xsd:string .

#Role study participant is of type ro:role and of type ncit:human study subject
<http://lls_example_data.org/study_participant/001-001-001> a obo:BFO_0000023, obo:NCIT_C70665 .

#Family ID is of type ncit:identifier, denotes the family to which the person belongs to and has a certain value
<http://lls_example_data.org/family_identifier/233> a obo:NCIT_C25364 ;
    obo:IAO_0000219 <http://lls_example_data.org/longevity_family/233> ;
    obo:STATO_0000129 "233"^^xsd:string .

#Family is of type ncit:family
<http://lls_example_data.org/longevity_family/233> a obo:NCIT_C25173 .
```
