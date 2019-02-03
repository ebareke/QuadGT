# quadGT
Joint Genotyping of Parental, Normal and Tumor Genomes
<p />
<b>QuadGT</b> is a software package for calling single-nucleotide variants in four sequenced genomes comprising a normal-tumor pair and the two parents. Genotypes are inferred using a joint model of parental variant frequencies, de novo germline mutations, and somatic mutations. <br >The model quantifies the descent-by-modification relationships between the unknown genotypes by using a set of parameters in a Bayesian inference setting.
<p/ >
Note that you can use QuadGT on any subset of the four related genomes, including parent-offspring trios, and normal-tumor pairs without parental samples.
<p/ >
The software package assumes a thorough probabilistic model of single-nucleotide variants with the following notable features.
<br/ >
<b>Multiple alleles.</b> Every locus has four possible alleles (A,C,G,T). Diploid genotypes combine multi-allele frequencies with adjusted heterozygous/homozygous SNP ratios.
<br/ >
<b>DNA mutation models.</b> Point mutations between related genomes follow standard DNA evolution models. The implemented models include the basic Jukes-Cantor model and a version of the Hasegawa-Kishino-Yano (a.k.a. Felsenstein's F84) model with purine-pyrimidine balance %(A+G)=%(C+T)=50%	and four parameters that adjust sequence divergence, transition/transversion ratio and nucleotide composition (GC-content and amino/keto %(A+C)/%(T+G) content).
<br/ >
<b>Known variants.</b> QuadGT integrates prior information on minor allele frequencies from a chosen variant database such as the NHLBI Exome Sequencing Project's Exome Variant Server.
<br/ >
<b>Inheritance.</b> Inheritance models span autosomes, sex chromosomes, and mitochondrial DNA. De novo mutations follow a DNA substitution model.
<br/ >
<b>Basecall qualities.</b> QuadGT's model incorporates alignment quality scores, uses them in inference, and automatically recalibrates score→probability mappings during model training.
<br/ >
<b>Tumor purity.</b> QuadGT infers tumor purity (normal-tumor sample mixture coefficient) from basecall statistics at somatic mutations, and takes it into account during variant calls.
