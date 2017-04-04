---
layout: page
title: " Prediction of regulatory elements in mammalian genomes using chromatin signatures."
breadcrumb: true
categories:
    - publication
## publication related information
pub:
    authors: " Kyoung-Jae Won, Iouri Chepelev, Bing Ren,  Wei Wang"
    journal: " BMC bioinformatics"
    date: 2008-12-18
    doi:  10.1186/1471-2105-9-547
    volume:  9
    pages:  547
    abstract: " BACKGROUND: Recent genomic scale survey of epigenetic states in the mammalian genomes has shown that promoters and enhancers are correlated with distinct chromatin signatures, providing a pragmatic way for systematic mapping of these regulatory elements in the genome. With rapid accumulation of chromatin modification profiles in the genome of various organisms and cell types, this chromatin based approach promises to uncover many new regulatory elements, but computational methods to effectively extract information from these datasets are  still limited. RESULTS: We present here a supervised learning method to predict promoters and enhancers based on their unique chromatin modification signatures.  We trained Hidden Markov models (HMMs) on the histone modification data for known promoters and enhancers, and then used the trained HMMs to identify promoter or enhancer like sequences in the human genome. Using a simulated annealing (SA) procedure, we searched for the most informative combination and the optimal window size of histone marks. CONCLUSION: Compared with the previous methods, the HMM method can capture the complex patterns of histone modifications particularly from the weak signals. Cross validation and scanning the ENCODE regions showed that our method outperforms the previous profile-based method in mapping promoters and enhancers. We also showed that including more histone marks can further boost the performance of our method. This observation suggests that the HMM is robust and is capable of integrating information from multiple histone marks. To further demonstrate the usefulness of our method, we applied it to analyzing genome wide ChIP-Seq data in three mouse cell lines and correctly predicted active and inactive promoters with positive predictive values of more than 80%. The software is available at http://http:/nash.ucsd.edu/chromatin.tar.gz.,"
---