# <M. m. castaneus> recombination maps

This repo contains the recombination maps constructed for M. m. castnaeus using LDhelmet. 

I have compressed the maps from the LDhelmet output to make them smaller and more easily worked upon. I removed consecutive pairs of SNPs with the same recombination rate to save space and to format the rates into a kind-of GFF/GTF format. Here is an example couple of lines:
```
chr1	recom_rate	LDhelmet	3157499	3157499	.	9.4346e-03	104.27522436
chr1	recom_rate	LDhelmet	3157507	3157507	.	5.6209e-03	104.32019156
```
The fields of the file are, in order:

```
CHROM - The chromosome 
VALUE - The statistic the file stores
SOURCE - The program the values come from
POS - The position
POS - The position (repeated)
BLANK - A blank field that can be substituted for something else if you like
RHO - Mean recombination rate from the posterior distirubion from LDhelmet's rjMCMC
CUMULATIVE_RHO - The cumulative recombination rate, RHO*DISTANCE. Where DISTANCE iis the distance bertween the current and the previous SNP.
```

Maps constructed using block penalties of 10 and 100 are included.
