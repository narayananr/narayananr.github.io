---
layout: page
title: <font color="DodgerBlue">Research</font>
---

The central theme of my recent research has been around developing computational/statistical methods for analyzing RNA-seq data and use the methods extensively. 

### <font color="DarkCyan">Seqnature: Embracing genetic diversity </font>
Large number of sequencing efforts have characterized genetic variations in detail and catalogued millions of Single Nucleotide Polymorphisms and short insertions and deletions. However, we are still lagging behind in using the SNPs and indels in a standard sequencing analyses, like RNA-seq and ChIP-seq analysis pipelines. 

![Seqnature](/public/images/seqnature-personalized-genome.png)

To address this challenge, We developed, Seqnature, a software tool that can take known genetiic variations like SNPs and Indels and construct individualized or personalized genome. 

In case of model organisms, Seqnature can be used to construct strain-specific genomes utilizing strain-specific variations and reference genomes. In the case of multi-parental population like Diversity Outbred Mice, Seqnature can build hybrid diploid genomes using haplotypes inferred from array genotypes. In the case of humans, Seqnature can build diploid genomes using phased genetic variations.
 

### <font color="DarkCyan">Allele-specific expression </font>
Diploid organisms like humans have two copies (or alleles) of every autosomal gene. When there is one or more genetic variation between the two alleles, we can identify which allele is expressed and how much it is expressed. RNA-seq technology allows us to measure the allele-level expression. 
![ASE](/public/images/ASE-cartoon.jpg)

### <font color="DarkCyan">EMASE: Expectation Maximization for Allele Specific Expression</font>
Although RNA-seq is great to study allele-specific expression, short sequence reads and un-accounted genetic variations are known to cause alignment bias and inaccurate estimation of allele-specific expression. Current approaches to quantify allele-specific expression, relying only on the reference genome for alignment, need to go through an elaborate steps to avoid the alignment bias. 

![EMASE](/public/images/EMASE-illustration.png)

We have developed an EM algorithm that can utilize diploid alignments with multi-mapping reads and estimate allele-level and gene-level expression simultaneously. Accounting for the genetic variations in a diploid model and utilizing unique and multi-mapping reads in the EM framework greatly help in reducing the bias and accurate quantitation. The EM algorithm is implemented in Python as software EMASE and it is freely available. Download it from Github page for [EMASE](https://github.com/narayananr/emase). 

