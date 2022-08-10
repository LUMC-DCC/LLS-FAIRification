### Model age

```mermaid
%%{init: {'theme':'base'}}%%
graph TD
   
    A{Person} -->|rdf:type| B[ncit:person]
    C{Role:<br> Study participant} -->|rdf:type| D[ncit:human study subject]
    F{Quality: Age}
    G{Process:<br>Age recording process} -->|ro:has output| H{Output type:<br>Age}
    C -->|rdf:type| E[ro:role]
    A -->|ro:has role| C
    A -->|ro:has quality| F
    C -->|ro:realized in| G
    H -->|stato:has value| I((94))
    H -->|iao:has measurement unit label| N{Year}
    H -->|rdf:type| K[ncit:output]
    G -->|rdf:type| J[iao:process]
    H -->|iao:is about| F
    F -->|rdf:type| L[iao:quality]
    F -->|rdf:type| M[ncit:age]
    N -->|rdf:type| O[uo:year]
        
    classDef literal fill:#dae8fc;
    classDef ontology fill:#d5e8d4;
    class I literal;
    class K,J,B,D,E,L,M,O ontology;
 ```

### Description
1. The model separates two 'things'. On the hand, there is the attribute or quality a person has (e.g., brown hair, female sex, age of 94). On the other hand, there is the process of how this was measured or determined plus the value of the output of that process.
2. Because age in years is less identifying than birth date and specific enough for the analyses needed, LLS stored age in OPAL. 
3. Age is relative to a specific point in time. For example, at the time of inclusion to LLS a person is 94. MISSING: this information - i.e, that we are talking about the age of a person at the first round of inclusion (called 'IOP1') - is still missing in the model.


### Abbreviations
* ncit = [National Cancer Institute Thesaurus OBO edition](https://ontobee.org/ontology/ncit)
* ro = [Relation Ontology](https://ontobee.org/ontology/RO)
* iao = [Information Artefact Ontology](https://ontobee.org/ontology/IAO)
* stato = [Statistical Methods Ontology](https://ontobee.org/ontology/STATO)
* uo = [Units of measurement ontology](https://ontobee.org/ontology/UO)

### Example RDF (turtle)