# NOAA 'Omics Metabarcoding Assays

Metabarcoding assays used for DNA metabarcoding by NOAA 'Omics researchers, using terms from the [FAIRe](https://fair-edna.github.io) standard.

## Assays

An assay is defined by the unique combination of forward and reverse PCR primers, which have fixed data associated with them (taxonomic target, gene, subfragment, amplicon size, primer sequences, primer names, and primer references).

The fields of [assays.tsv](https://github.com/NOAA-Omics/noaa-omics-metabarcoding-assays/blob/main/assays.tsv) are described here:

- `assay_name`: A brief, concise identifier for the assay with no spaces or special characters, ensuring machine readability. Must be unique. Suggest including the targeted taxonomic group, gene, subfragment (if applicable), and author or commonly used name of assay.
- `targetTaxonomicAssay`: Taxa or species name targeted by the primers.
- `targetTaxonomicScope`: The taxonomic group(s) targeted in the study. This can differ from the targetTaxonomicAssay. For example, the targetTaxonomicAssay may be "Chordata" while the targetTaxonomicScope is "Chondrichthyes" (bony fish, sharks and rays).
- `target_gene`: Targeted gene or locus name for marker gene studies.
- `target_subfragment`: Name of subfragment of a gene or locus. Used to identify specific regions on marker genes like V6 of 16S rRNA.
- `pcr_primer_[forward|reverse]`: Primer sequence (5'->3'). The primer sequence should NOT contain MIDs and adapter sequences and should be reported in uppercase letters. In primers containing an "N" (any base), the published sequence may contain an "I" (inosine, pairs with any base).
- `pcr_primer_name_[forward|reverse]`: Standardized primer name, using original name but adding the name of the target gene, target subfragment (if applicable), and in some cases author information.
- `pcr_primer_reference_[forward|reverse]`: Link to original publication (DOI if available) of primer.

## Assay Preps

An assay prep contains additional fields whose values can vary from lab to lab. This metadata should be contained in a protocol available online, with the DOI in the field `nucl_acid_amp`. This DOI should be a Zenodo DOI of a BeBOP-formatted protocol, a protocols.io DOI, or some other stable DOI or URL of the protocol.

- `nucl_acid_amp`: Link to assay protocol. Example: https://doi.org/10.5281/zenodo.15636182
- `ampliconSize`: The length of the amplicon in basepairs *excluding* the primers, adapters, and MIDs. A range can be entered separated by a bar "|" (e.g., "140 | 160"). Units in basepairs.
- `thermocycler`
- `commercial_mm`
- `custom_mm`
- `pcr_cond`
- `barcoding_pcr_appr`
- `pcr2_commercial_mm`
- `pcr2_cond`
- `sequencing_location`
- `platform`
- `instrument`
- `seq_kit`
- `adapter_forward`
- `adapter_reverse`
- `lib_screen`
- `checksum_method`
- `seq_method_additional`
