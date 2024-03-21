# Bacterial Genomics

## Retrieval of genomes from GenBank
## Strain typing
### Step 1: Strain Typing (MLST v 2.23.0)

Multilocus sequence typing is a useful system for phylogenetic and epidemiological studies of multidrug-reistant _E.coli_. Strain typing can characterize and confirm epidemiological linkage in and outbreak setting and provide insights into bacterial population dynamics

Multilocus sequence typing (MLST) is an unambiguous procedure for characterising isolates of bacterial species using the sequences of internal fragments of (usually) seven house-keeping genes. Approximately 450-500 bp internal fragments of each gene are used, as these can be accurately sequenced on both strands using an automated DNA sequencer. For each house-keeping gene, the different sequences present within a bacterial species are assigned as distinct alleles and, for each isolate, the alleles at each of the seven loci define the allelic profile or sequence type (ST).

Each isolate of a species is therefore unambiguously characterised by a series of seven integers which correspond to the alleles at the sven house-keeping loci.Most bacterial species have sufficent varriation within house-keeping genes to provide many alleles per locus allowing billions of distinct allelic profiles to be distinguished using seven house-keeping loci. 

The advantage of MLST is:-
- Sequence data are unambigious and allelic profiles of isolates can be easily be compared to those in a large central database via the internet in contrast to most strain typing methods that usually involve comparing DNA fragments sizes on gels.
- Allelic profiles can also be obtained from clinical materials by PCR of the seven house keeping loci directly, thus samples can be precisely characterised even when they cannot be cultured from clinical material.
#### _E. coli_ MLST scheme
| gene | full name | 
|------|-----------|
| adk  | adenylate kinase |
| fumC  | fumarate hydratase |
| gyrB | DNA gyrase |
|icd |isocitrate/isopropylmalate dehydrogenase|
|mdh |malate dehydrogenase|
|purA |adenylosuccinate dehydrogenase|
|recA |ATP/GTP binding motif|




### Step 2: Phylogroup classification (ezclermont v 0.7.0)
E. coli phylogroup refers to the classification of E. coli bacteria into different phylogenetic groups based on their genetic characteristics. Classical phenotypic tests fail to identify non-sensu stricto _E.coli_ as well as phylogroups. Clermmont and collegues developed a PCR assay that allows the identification of most of these species based on the presence or absence of marker genes. The ezclermont tool is based on the Clermont PCR typing method. This method targets specific genes that are associated with different _E.coli_ phylogentic groups

There are currently eight recognized phylogroups, labeled as A, B1, B2, C, D, E, F, and Escherichia cryptic clade I (ECCI). These phylogroups are based on variations in certain genes, such as chuA and yjaA, and provide insights into the pathogenic potential and ecological niches of different E. coli strains.
#### Phylogroups 
| Phylogroup | site | Effect |
|----------| -------|---------|
| A | Commensal strains | These strains are generally harmless and live as part of the normal gut microbiota in humans and animals. They do not typically cause infections.|
| B1 | Commensal strains | Like Phylogroup A, these strains are usually harmless and are found in the intestines of humans and animals.|
| B2 | Extraintensinal pathogenic strain | These strains are associated with urinary tract infections (UTIs), sepsis, and other infections outside the intestine. They often possess virulence factors that enable them to cause diseases.|
| D | Diffusely adherent | Some strains within this phylogroup are associated with diarrhea, especially in young children.|
| E | Enteropathogenic strains | These strains are known for causing gastroenteritis, particularly in infants and young children.|
| F | Enteroinvasive strains | These strains can cause a condition similar to shigellosis, with symptoms such as bloody diarrhea.|
| N | Neonatal meningitis strains | This phylogroup is associated with infections such as neonatal meningitis. |

### Step 3: AntiMicrobial Resistance genes and Virulence factors (abricate v 1.0.14)


### Step 4: Plasmid replicon screening (abricate v 1.0.0)
Plasmids are extrachromosomal mobile genetic elements capable of self-replication. Many bacteria and archaea carry plasmids, which are generally small and circular. They contain genes encoding plasmid core functions, such as conjugation transfer, replication, and partitioning. They also carry accessory genes that can help hosts adapt faster to unfavorable environments, such as genes for antimicrobial resistance (AMR) as well as virulence genes. These accessory genes can be transferred horizontally to other hosts (5) and thus can spread AMR genes among pathogens

Mass screening of contigs for antimicrobial resistance or virulence genes is made possible by Abricate. It comes bundled with multiple databases: NCBI, CARD, ARG-ANNOT, Resfinder, MEGARES, EcOH, PlasmidFinder, Ecoli_VF and VFDB. For plasmid screening, abricate utilizes the plasmidfinder database hosted at [CGE](http://www.genomicepidemiology.org/). PlasmidFinder uses replicon genes, which control plasmid replication, as the reference database.



## Annotation of plasmids and visualization
## Genotyping
