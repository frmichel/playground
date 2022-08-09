layout: page
title: "PAGE FILE2"

# This is the title

- [Other doc](file2.md)
- [Back](index.md)

## Section 1

fksdjfdlkfj lsdj sldkj sfdklj sfdlkj sfdlkjsfdmgklf glkgkld g.

## Section 2
Configuration method | Argument-passing method
------------ | -------------
`config.ini` property file | HTTP query string parameters
`ServiceDescription.ttl` RDF document | Terms of the SPARQL query graph pattern

A piece of code:

```sparql
prefix dwc:    <http://rs.tdwg.org/dwc/terms/>
prefix owl:    <http://www.w3.org/2002/07/owl#>
prefix rdfs:   <http://www.w3.org/2000/01/rdf-schema#>
prefix schema: <http://schema.org/>

CONSTRUCT {

    ?species
      schema:subjectOf ?photo; schema:image ?img; schema:thumbnailUrl ?thumbnail;
      schema:contentUrl ?audioUrl.
      
} WHERE {

    # Query a regular SPARQL endpoint of the LOD cloud
    SERVICE <http://taxref.mnhn.fr/sparql> {
      ?species 
        a                       owl:Class;
        rdfs:label              "Delphinus delphis". 
    }
    ...
}
```
