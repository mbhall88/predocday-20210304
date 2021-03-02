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

<img src="images/tree.png" height="700" style="border: none;">

---

## Ground truth pan-genome variants

<img src="images/pg-variants.png"  style="border: none;">

---

## Precision

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

## Recall

todo: define and add plots

{{% /section %}}
