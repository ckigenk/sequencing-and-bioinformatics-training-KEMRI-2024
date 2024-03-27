## Prerequisite
* Create a conda environment called `parsnp`, install the `parsnp` tool and activate the environment

```
conda create -n parsnp -c bioconda parsnp -y && conda activate parsnp

```
## Download reference sequence
```
wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/005/845/GCF_000005845.2_ASM584v2/GCF_000005845.2_ASM584v2_genomic.fna.gz -O reference.fasta.gz && gunzip reference.fasta.gz
``` 
## Download dataset

```
wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/376/405/GCA_030376405.1_ASM3037640v1/GCA_030376405.1_ASM3037640v1_genomic.fna.gz -O sample1.fasta.gz && gunzip sample1.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/375/825/GCA_030375825.1_ASM3037582v1/GCA_030375825.1_ASM3037582v1_genomic.fna.gz -O sample2.fasta.gz && gunzip sample2.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/375/495/GCA_030375495.1_ASM3037549v1/GCA_030375495.1_ASM3037549v1_genomic.fna.gz -O sample3.fasta.gz && gunzip sample3.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/376/075/GCA_030376075.1_ASM3037607v1/GCA_030376075.1_ASM3037607v1_genomic.fna.gz -O sample4.fasta.gz && gunzip sample4.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/032/207/185/GCA_032207185.1_ASM3220718v1/GCA_032207185.1_ASM3220718v1_genomic.fna.gz -O sample5.fasta.gz && gunzip sample5.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/032/207/045/GCA_032207045.1_ASM3220704v1/GCA_032207045.1_ASM3220704v1_genomic.fna.gz -O sample6.fasta.gz && gunzip sample6.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/376/275/GCA_030376275.1_ASM3037627v1/GCA_030376275.1_ASM3037627v1_genomic.fna.gz -O sample7.fasta.gz && gunzip sample7.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/375/125/GCA_030375125.1_ASM3037512v1/GCA_030375125.1_ASM3037512v1_genomic.fna.gz -O sample8.fasta.gz && gunzip sample8.fasta.gz &&  wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/032/207/205/GCA_032207205.1_ASM3220720v1/GCA_032207205.1_ASM3220720v1_genomic.fna.gz -O sample9.fasta.gz && gunzip sample9.fasta.gz && wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/030/374/825/GCA_030374825.1_ASM3037482v1/GCA_030374825.1_ASM3037482v1_genomic.fna.gz -O sample10.fasta.gz && gunzip sample10.fasta.gz
```

## Run parsnp
```
parsnp -r reference.fasta -d genomes/ -p 12 -o E-coli-tree
```
## Convert the ggr output to multi fasta alignment file
```
harvesttools -i E-coli-tree/parsnp.ggr -S E-coli-tree/parsnp.fasta
````
## Activate iqtree
```
conda activate iqtree
```
## Run iqtree
```
iqtree -s E-coli-tree/parsnp.fasta -bb 1000 --redo -t 8 --prefix E-coli-tree
```
## Visualization
* navigate to https://itol.embl.de/
* upload the `E-coli-tree.contree` file
