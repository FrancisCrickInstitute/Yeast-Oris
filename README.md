
# OOR & ORC analysis in Yeast

This analysis supports the research presented in [Cell Cycle
Regulation has Shaped Budding Yeast Replication Origin Structure and
Function](https://www.biorxiv.org/content/10.1101/2024.01.10.575016v1)

In short we characterised the position and orientation of ORC binding
motifs relative to annotated origins of replication (OOR) in the yeast genome.

Please see the [analysis report](results/analysis.html) and the paper
for the analysis details.

## Instructions

1. Clone this repo

	`git clone https//github.com/FrancisCrickInstitute/Yeast-Oris`

2. Save the OOR [bed
file](http://cerevisiae.oridb.org/data_output.php?main=sc_ori&table=sc_ori&ext_format=BED;FASTA;&format=tab)
to `data/OOR_data.txt`
and download the [fasta](http://cerevisiae.oridb.org/cerevisiae_fasta.tgz) sequence
files. Both are available from [oridb](http://cerevisiae.oridb.org/)

	```
	cd data
	wget http://cerevisiae.oridb.org/cerevisiae_fasta.tgz
	tar -zxf cerevisiae_fasta.tgz
	```

3. Initiate the R environment. Select option `1: Restore the project
   from the lockfile.` if promted by renv. We used `R-4.0.3`
   for the analysis so this binary needs to be available on `$PATH`
   
   ```
   R
   renv::init()
   ```
   
   
4. Run the analysis script to generate the Rmd report and figures. All
   anaysis results are written to `results`

	`sh render.R`
