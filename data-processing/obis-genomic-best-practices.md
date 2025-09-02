# OBIS/GBIF and your genomic datasets

DFO genomic (metabarcoding, eDNA, or qPCR) data should be made openly available through the normal DFO Enterprise Data Hub (EDH) pathway, however EDH is not the domain specific repository for this data and it should be included in larger national or international repositories to ensure the maximum usefulness of the data. There are a number of options for where this data can be published openly depending on the area of study, if the data concerns purely marine species, the [Ocean Biodiversity Information System (OBIS)](https://obis.org/) is the proper repository, however if the species include freshwater, terrestrial, or eukaryote occurrences, the [Global Biodiversity Information Facility (GBIF)](https://www.gbif.org/) is the proper repository.

A guiding document should be [Publishing DNA-derived data through biodiversity data platforms](https://doi.org/10.35035/doc-vf1a-nr22) which is published jointly by GBIF and OBIS.

## Best Practices

DwC is highly extensible and can accommodate just about any kind of information related to biological occurrence

### Data format - Darwin Core (DwC)

#### Required DwC fields

- [`occurenceID`](http://rs.tdwg.org/dwc/terms/occurrenceID): An identifier for the dwc:Occurrence (as opposed to a particular digital record of the dwc:Occurrence). In the absence of a persistent global unique identifier, construct one from a combination of identifiers in the record that will most closely make the dwc:occurrenceID globally unique. (e.g. `dfo_marsci_1234`)
- [`eventDate`](http://rs.tdwg.org/dwc/terms/eventDate): The date-time or interval during which a dwc:Event occurred. For occurrences, this is the date-time when the dwc:Event was recorded.
- [`decimalLongitude`](http://rs.tdwg.org/dwc/terms/decimalLongitude): The geographic longitude (in decimal degrees, using the spatial reference system given in dwc:geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive.
- [`decimalLatitude`](http://rs.tdwg.org/dwc/terms/decimalLatitude): The geographic latitude (in decimal degrees, using the spatial reference system given in dwc:geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive.
- [`scientificName`](http://rs.tdwg.org/dwc/terms/scientificName): The full scientific name, with authorship and date information if known. When forming part of a dwc:Identification, this should be the name in lowest level taxonomic rank that can be determined. This term should not contain identification qualifications, which should instead be supplied in the dwc:identificationQualifier term.
- [`occurenceStatus`](http://rs.tdwg.org/dwc/terms/occurrenceStatus):A statement about the presence or absence of a Taxon at a Location.
- `basisOfRecord`:
  - `PreservedSpecimen`: preserved in etOh, tissue, etc.
  - `FossilSpecimen`: a fossil
  - `LivingSpecimen`: an intentionally kept/cultivated living specimen (i.e. aquarium)
  - `HumanObservation`: an observation without a specimen being kept (e.g. bird siting, benthic sample with specimens discarded after counting)
  - `MachineObservation`:
  - <mark>`MaterialSample`: physical sample was taken, and may have been preserved or destroyed, Use for DNA-derived data extension</mark>
- [`scientificNameID`](http://rs.tdwg.org/dwc/terms/parentNameUsageID)[^1]: An identifier for the name usage (documented meaning of the name according to a source) of the direct, most proximate higher-rank parent taxon (in a classification) of the most specific element of the dwc:scientificName.

[^1]: Strongly recommended term

### Data format - Mismatch between World Online Register of Marine Species (WoRMS) and NCBI SRA

### Data Format - "Eukaryote"

`speciesID` = "BIOTA" when no more information is known.
