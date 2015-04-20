---
layout: page
title: <font color="DodgerBlue">Research</font>
---

The central theme of my recent research has been around developing computational/statistical methods for analyzing RNA-seq data and use the methods extensively. 

### <font color="DarkCyan">Seqnature: Embracing genetic diversity </font>
Large number of sequencing efforts have characterized genetic variations in detail and catalogued millions of Single Nucleotide Polymorphisms (SNP) and short insertions and deletions (indel). However, we are still lagging behind in using the SNPs and indels in a standard sequencing analyses, like RNA-seq and ChIP-seq analysis pipelines. 

![Seqnature](/public/images/seqnature-personalized-genome.png)

To address this challenge, We developed, Seqnature, a software tool that can take known genetiic variations like SNPs and Indels and construct individualized or personalized genome. 

In case of model organisms, Seqnature can be used to construct strain-specific genomes utilizing strain-specific variations and reference genomes. In the case of multi-parental population like Diversity Outbred Mice, Seqnature can build hybrid diploid genomes using haplotypes inferred from array genotypes. In the case of humans, Seqnature can build diploid genomes using phased genetic variations.
 

### <font color="DarkCyan">Allele-specific expression </font>
Diploid organisms like humans have two copies (or alleles) of every autosomal gene. When there is one or more genetic variation between the two alleles, we can identify which allele is expressed and how much it is expressed. RNA-seq technology allows us to measure the allele-level expression. 
![ASE](/public/images/ASE-cartoon.jpg)

### <font color="DarkCyan">EMASE: Expectation Maximization for Allele Specific Expression</font>
Although RNA-seq is great to study allele-specific expression, short sequence reads and un-accounted genetic variations are known to cause alignment bias and inaccurate estimation of allele-specific expression. Current approaches to quantify allele-specific expression, relying only on the reference genome for alignment, need to go through an elaborate steps to avoid the alignment bias. These approaches also do not use any multimapping reads.

![EMASE](/public/images/EMASE-illustration.png)
We use diploid transcriptome, where each transcript has two copies adjusted for both SNP and indels and align RNA-seq reads to the diploid transcriptome. The diploid model helps remove any alignment bias, but it also gives rise to different types of multi-mapping reads. We have developed an EM algorithm that can utilize the multi-mapping reads and estimate allele-level and gene-level expression simultaneously. 

Accounting for the genetic variations in a diploid model and utilizing multi-mapping reads in the EM framework greatly help in reducing the bias and accurate quantitation. The EM algorithm is implemented in Python as software EMASE and it is freely available. Download it from Github page for [EMASE](https://github.com/narayananr/emase). 


### <font color="DarkCyan"> Cause and Extent of Allele-specific expression reciprocal F1 mice </font>
To understand the cause and extent of allele-specific gene expression, We are using liver RNA-seq data from F1 mice crossed reciprocally. The F1 reciprocal cross from two divergent mouse inbred strains NOD and PWK allowed to find that allele-specific expression prevalent and most of allele-specific expression is caused by local genetic effect and only a handful of known genes show parent-of-origin effect.


### <font color="DarkCyan">Genetic Architecture of Gene Expression in Hippocampus and Liver </font>
coming soon

### <font color="DarkCyan">Classifying and quantifying human and mouse RNA-seq data from PDX models </font>
coming soon


