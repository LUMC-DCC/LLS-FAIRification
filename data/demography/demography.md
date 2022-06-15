## Person pseudonym and family
### Model

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
A person, defined by the NCIT-term for person, has a role as study participant in LLS. This person is also member of a family. It is explicitly defined that the role study participant is 1) a role; and 2) a human study subject.
There is an ID that refers to a study participant which is of type identifier and has a certain value. Family, defined by the NCIT-term for family, also has an ID of type identifier and a value.

## Administrative gender
### Model

```mermaid
%%{init: {'theme':'base'}}%%
graph TD
   
    
    A{Person} -->|rdf:type| B[ncit:person]
    C{Role:<br> Study participant} -->|rdf:type| D[ncit:human study subject]
    F{Quality/Attribute<br> type: Female}
    G{Process:<br>Sex recording process} -->|ro:has output| H{Output type:<br>Female}
    C -->|rdf:type| E[ro:role]
    A -->|ro:has role| C
    A -->|??:has quality/attribute| F
    C -->|ro:realized in| G
    H -->|stato:has value| I((female))
    H -->|rdf:type| K[??:output]
    G -->|rdf:type| J[??:process]
    H -->|??:refers to| F
    F -->|rdf:type| L[??:attribute/quality]
    F -->|rdf:type| M[??:admin sex/gender]
    F -->|rdf:type| N[??:female/male/??]
    
    classDef literal fill:#dae8fc;
    classDef ontology fill:#d5e8d4;
    class I literal;
    class K,J,B,D,E,L,M,N ontology;
 ```
 
 ### Description
 To do.
 
 ## Ontology terms
 ### LLS variables
| Concept          | OPAL variable name | Description                               	  | Ontology                                                                       | Value     | Units |
| ---------------- | ------------------ | ----------------------------------------------- | ------------------------------------------------------------------------------ | --------- | ----- |
| LLnr                   | LLnr               | For the LLS generated number for the participant            | [ncit:identifier (C25364)](http://purl.obolibrary.org/obo/NCIT_C25364)         | UniqueID  |       |
| FID_GRR                | famID              | For the LLS generated number for the family the participant belongs to                                 | [ncit:identifier (C25364)](http://purl.obolibrary.org/obo/NCIT_C25364)         | UniqueID  |       |


### Relations

| Relation          | Ontology |
| ---------------- | ------------------ | 
| has role               | [ro:has role (0000087)](http://purl.obolibrary.org/obo/RO_0000087)             |
| member of              | [ro:member of (0002350)](http://purl.obolibrary.org/obo/RO_0002350)            |
| denotes                | [iao:denotes (0000219)](http://purl.obolibrary.org/obo/IAO_0000219)            |
| has value              | [stato:has value (0000129)](http://purl.obolibrary.org/obo/STATO_0000129)      |

### Other model constructs

 | Concept          | Ontology |
| ---------------- | ------------------ |
| Person                 | [ncit:person (C25190)](http://purl.obolibrary.org/obo/NCIT_C25190)             |
| Role:Study participant | [ncit:human study subject (C70665)](http://purl.obolibrary.org/obo/NCIT_C70665)|
|                        | [ro:role (0000023)](http://purl.obolibrary.org/obo/BFO_0000023)                |
| Family                 | [ncit:family (C25173)](http://purl.obolibrary.org/obo/NCIT_C25173)             |

## Abbreviations
* ncit = National Cancer Institute Thesaurus
* ro = Relation Ontology
* iao = Information Artefact Ontology
* stato = Statistical Methods Ontology