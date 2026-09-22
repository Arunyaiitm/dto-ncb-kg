# NCB Drug Trafficking Knowledge Graph

Model documentation and visualisation for a knowledge graph extracted from the
**NCB News Bulletin** corpus (Narcotics Control Bureau, Ministry of Home Affairs, India),
built against the **Drug Trafficking Ontology (DTO)**.

## Pages

- **[Knowledge graph documentation](ncb_kg_documentation.html)** — model, term cross-reference, instance counts
- **[Interactive visualisation](knowledge_graph_visualization.html)** — schema graph, extracted incidents, country × drug

## Files

| File | Contents |
|---|---|
| `dto_ext.ttl` | `dtox:` — additive extension to DTO (datatype properties, Place, provenance classes) |
| `dto_vocab.ttl` | Controlled vocabularies generated from UNODC IDS data (116 drug classes, 14 seizure-location types, 8 transport modes) |

## Base ontology

> Tiwari, S., Kejriwal, M., & Mihindukulasooriya, N. (2025).
> *Ontological Modeling of Drug Trafficking in the Global South Using Newspaper Data.*
> https://doi.org/10.1007/978-3-031-99554-5_14 · Ontology: https://w3id.org/def/DTO/

DTO is used unmodified under CC-BY 4.0. The `dtox:` extension is additive: it introduces
new terms only, because published DTO v2.0 declares no datatype properties and therefore
cannot express quantity, date, monetary value or place.

## What is deliberately NOT published here

The knowledge graph instance data (`kg_ncb.ttl`) and the article corpus are **not** in this
repository. The NCB bulletins reproduce third-party newspaper articles whose copyright
remains with the original publishers. Extraction and analysis are appropriate; public
redistribution of the article text is not.

A publishable form of the graph would carry **annotations plus source URLs** rather than
article text — every record already holds its `dtox:sourceURL`.

## Namespace caveat

`https://w3id.org/def/DTO/ext#` is **not yet registered or resolvable**. It was chosen to sit
naturally beneath the published DTO namespace and must be replaced before formal publication.
