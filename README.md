# I-SceI barcoding
Nanopore sequencing enables a dramatic cost reduction in plasmid sequencing. Our foundry's price reduction will largely be because of more effective allocation of sequencing resources.

The most expensive part of plasmid sequencing on NGS platforms is indexing (ie, the step that allows you to distinguish between two different wells). Since Nanopore can sequence an entire plasmid in a single go, we can add barcodes prior to Nanopore preparation with simple ligation.

Barcodes can also be added with PCR, but we are looking to eliminate PCR from our workflows because it is relatively unreliable and cannot be used for large plasmids. We want a single method that can scale to plasmids of large size. 

### Why now
We need a cheap sequencing method (or else this will dominate all costs of our foundry). We will have to do this at some point. If we invest in I-SceI barcoding and it works, we can immediately begin using it in our process.

## Materials needed
This experiment should be self-contained other than 2 minipreps we will need of FreeGenes materials (I added I-SceI sites to most FreeGenes plasmids). These should be miniprepped and validated during synthesis of other materials.

- 2 phosophylated duplexes (($0.63 x (avg 50) x 2 + $20) x 2 = $166)
- 2 unphosophylated duplexes (($0.63 x (avg 50) x 2) x 2 = $126)

We are ordering both phosophylated and unphosophylated duplexes to test both out. End repair + ligation should theoretically repair the 5' and would greatly reduce our overall costs, so we will also be testing duplexes without phosophylation. Other optimizations, like not requiring end repair, could be made later, but this is the easiest viable method.

Assuming a 20bp barcode is sufficient, we can use unphosophylated duplexes, and we can get negotiate with IDT for good pricing, it should cost us about ~$850 for a set of 96 barcodes.

### Experimental workflow
1. Miniprep DNA is simultaneously cut with I-SceI and ligated with barcode
2. DNA is pooled and purified as a pool
3. Nanopore prep is executed
4. Sequencing data is analyzed / another round of opentrons optimization is done

### Lowering costs
The primary optimization to lower costs is testing unphosophylated duplexes, since chemical phosophylation is expensive. We could also enzymatically phosophylate and duplex ourselves, but these add complications to our workflow that I wish to avoid.

# Results
After this experiment is run, we should be able to tell:
1. If I-SceI barcoding will work for our sequencing reactions
2. If we can get away with unphosophylated duplexes
3. How much barcode is required for sorting

### Risks
This experiment is relatively low risk. However, we will be automating Nanopore sequencing prep during experimentation, so we will want time to iterate.
