# Causal Biological Network database: BEL-scripted biological networks representing causal signaling pathways

Biological events integrated in the database: cell response to stress, cell proliferation, cell fate (including DNA damage response, autophagy, senescence, apoptosis and necroptosis), tissue repair and angiogenesis, pulmonary inflammatory processes, vascular inflammatory processes and chronic obstructive pulmonary disease (COPD)-specific networks.

## Publication
[Causal biological network database: a comprehensive platform of causal biological network models focused on the pulmonary and vascular systems. Boué et al. (2015), Database(Oxford)](http://dx.doi.org/10.1093/database/bav030)

## Species supported
 * H. sapiens
 * M. musculus
 * R. norvegicus

## Controlled Vocabulary / Ontology
 * PubMed ID
 * GO
 * HGNC
 * BEL terms


## Implementation
MongoDB with BEL statements (use of triplets)

## Export file formats
 * JSON
 * SIF

## Representation of causality statements
Causal relations in CBN are defined as BEL statements. A BEL statement represents the data as triplets: a **relationship** between a **subject** (abundance or process) and an **object** (abundance, process or second BEL statements).
The following terms are used to express the type of causal relation:
* decreases -|
* directlyDecreases =|
* increases ->
* directlyIncreases =>
* causesNoChange

## External links
[http://causalbionet.com/](http://causalbionet.com/)

