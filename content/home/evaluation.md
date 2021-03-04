+++
weight = 4
+++
{{% section %}}

# Aims

- Benchmark precision and recall of SNP calls against single-reference tools
- Quantify the amount of SNPs recovered using our genome graph approach

---

# Evaluation


20 diverse *E. coli* samples with both Illumina and Nanopore sequencing data and reference assemblies  

A reference genome graph of 578 *E. coli* genomes (genes and intergenic regions)

---

##### Constructing an evaluation set of diverse genomes

<img src="images/tree.png" height="600" style="border: none;">

---

### Precision

> What proportion of the VCF calls made are correct?

<p class="fragment fade-in-then-semi-out">
Construct probe of called allele
</p>

<p class="fragment fade-in-then-semi-out">
Map probe to sample's reference
</p>

<p class="fragment fade-in-then-semi-out">
Filter multi-mappings and masked regions
</p>

<p class="fragment">
number of matches / alignment length
</p>

---

### Precision

<img src="images/precision.png"  height="550" width="1100" style="border: none;">

---

### Recall

Ground truth pan-genome variants

<img src="images/pg-variants.png" style="border: none;">

---

### Recall

> What proportion of true variants do we find?

<p class="fragment fade-in-then-semi-out">
Apply VCF calls to the reference the calls were made against
</p>

<p class="fragment fade-in-then-semi-out">
Make probes for each pan-genome (truth) variant
</p>

<p class="fragment fade-in-then-semi-out">
Map probes to the mutated reference (Step 1)
</p>

<p class="fragment">
Considered TP if all bases in allele mapping agree
</p>

---

### Recall

<img src="images/recall.png"  height="550" width="1100" style="border: none;">




{{% /section %}}
