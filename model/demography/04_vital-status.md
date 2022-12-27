### Model vital status
```mermaid
%%{init: {'theme':'base'}}%%
graph TD
   
    A{Person} -->|rdf:type| B[ncit:person]
    C{Role:<br> Study participant} -->|rdf:type| D[ncit:human study subject]
    F{Quality: Vital status}
    G{Process:<br>Status recording process} -->|ro:has output| H{Output type:<br>Vital status}
    C -->|rdf:type| E[ro:role]
    A -->|ro:has role| C
    A -->|ro:has quality| F
    C -->|ro:realized in| G
    H -->|stato:has value| I((dead or <br> alive or <br> lost to follow up))
    H -->|rdf:type| K[ncit:output]
    G -->|rdf:type| J[iao:process]
    H -->|iao:is about| F
    F -->|rdf:type| L[iao:quality]
    F -->|rdf:type| M[ncit:dead or <br> ncit:alive or <br> ncit:unknown]
    F -->|rdf:type| N[ncit:vital status]
            
    classDef literal fill:#dae8fc;
    classDef ontology fill:#d5e8d4;
    class I literal;
    class K,J,B,D,E,L,M,N,O ontology;
 ```

### Model death information (if vital status is deceased)

```mermaid
%%{init: {'theme':'base'}}%%
graph TD
   
    A{Person} -->|rdf:type| B[ncit:person]
    C{Role:<br> Study participant} -->|rdf:type| D[ncit:human study subject]
    F{Quality: Date of death}
    G{Process:<br>Death information <br> recording} -->|ro:has output| H{Output type:<br>Date of death <br> information}
    C -->|rdf:type| E[ro:role]
    A -->|ro:has role| C
    A -->|ro:has quality| F
    C -->|ro:realized in| G
    H -->|stato:has value| I((2012-12-12))
    H -->|rdf:type| K[ncit:output]
    G -->|rdf:type| J[iao:process]
    H -->|iao:is about| F
    F -->|rdf:type| L[iao:quality]
    F -->|rdf:type| M[ncit:date of death]
            
    classDef literal fill:#dae8fc;
    classDef ontology fill:#d5e8d4;
    class I literal;
    class K,J,B,D,E,L,M,O ontology;
 ```

### Description
1. The model separates a couple of 'things'. First, there is the attribute or quality a person has (e.g., brown hair, female sex, age of 94, alive or deceased). Secondly, there is the process of how this was measured or determined plus the value of the output of that process. Of course, the value of the output of the recording process (e.g., it is determined that someone is alive) should correspond to the actual attribute or quality of the person (e.g., alive). Thirdly, when it turns out someone is deceased, some 'death information' is recorded, in this case date of death.
2. In the LSS-case a 'mortality check' was done at reference date 11-01-2021: via the ['Basisregistratie Personen'](https://www.rvig.nl/brp)(National identity registration) it was checked whether a participant was deceased or alive (and if deceased what was the date of death). This extra information about the process was not modeled.
3. Besides output values dead and alive, it could have been that at the date the vital status was checked the person was not a participant in the study anymore for a reason other than deceased. In LLS The value given to this output possibility was 'lost to follow up'. However, it would be strange to assign this value 'lost to follow up' to the quality 'vital status' of a person. The quality refers to the state or condition of being living or deceased. We have included the NCIT-possibility where vital status is unknown, but strictly speaking this seems incorrect (one is either dead or alive).

### Abbreviations
* ncit = [National Cancer Institute Thesaurus OBO edition](https://ontobee.org/ontology/ncit)
* ro = [Relation Ontology](https://ontobee.org/ontology/RO)
* iao = [Information Artefact Ontology](https://ontobee.org/ontology/IAO)
* stato = [Statistical Methods Ontology](https://ontobee.org/ontology/STATO)
* uo = [Units of measurement ontology](https://ontobee.org/ontology/UO)

### Example RDF (turtle)