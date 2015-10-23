#My favorite gene
---
##Hsp70
This page was created by **Laura L. López**

**Is the Hsp70 gene of the White shrimp match with other species?** 

![Litopenaeus vannamei](http://4.bp.blogspot.com/-MJDZVDXjc10/VWKr4-V85tI/AAAAAAACHkc/ovh3IzXv7sw/s1600/Litopenaeus%2Bvannamei%2B01.jpg)

********


###First step

**-** Primarily, I get a sequence from Genbank.

**-** I obtain this screenshot of the NCBI page:

![NCBI search](Imagen1.png)

**-** Then I downloaded the sequence in **fasta** format. The screenshot is below.

![Fasta Sequence](Image2.png)


###Second step

**-** I opened the jupyter page to make the blast of this sequence.

**-** I checked that my fasta file was in the correct folder.

	`ls query`

**-** I checked the number of sequences in the fasta file of the database of uniprot_sprot.
	
	`ls -s db\`

**-** I head the fasta sequence of Hsp70 gene.

	`head query/L-vannamei-Hsp70.fasta`

**-** I make a blast of my uniprot_sprot database.

`makeblastdb \`

`-dbtype prot \`

`-in db/uniprot_sprot.fasta \`

`-out db/uniprot_sprot` 

**-** Then I blasted my Hsp70 sequence with the database that I chose.

`blastx \`

`-query query\L-vannamei-Hsp70.fasta \`

`-db db\uniprot_sprot \`

`-out out\Lvannamei_Hsp70_blastx_uniprot.out`

**-** I observed the blast results and I obtain a lof of matches.

`cat out\Lvannamei_Hsp70_blastx_uniprot.out`

![Matches](Imagen3.png)


**-** I blasted my sequence again with more specific settings and I obtain the more close match to the gene of my specie.

`blastx \`

`-outfmt 6 \`

`-max_target_seqs 1 \`

`-evalue 1e-20 \`

`-query query\L-vannamei-Hsp70.fasta \`

`-db db\uniprot_sprot \`

`-out out\Lvannamei_Hsp70_blastx_uniprot-fmt6.out`

**-** To see the match I used this command:

`!cat out\Lvannamei_Hsp70_blastx_uniprot-fmt6.out`

![Match](Imagen4.png)


And that's all!!!
---


###Today was a very succesful day, cause I can apply the adquire Knowledge.
**----------------------------------------------------------------------------------------**



 















