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