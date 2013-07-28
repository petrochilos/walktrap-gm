walktrap-gm
===========
Type Package
Title Walktrap-GM (Walktrap for genomic modules) Version 1.0
Date 2013-07-28
Author Deanna Petrochilos
Maintainer Deanna Petrochilos <dpetroch@uw.edu>
Description walktrap.gm customizes the Walktrap random walk algorithm to discover communi-
ties associated with specific phenotypes in a genomic interactome. Functions in this package in- clude: calc.weights, opt.step.size, score.communities. calc.weights calculates edge and ver-
tex weights in the network and a random distribution of weights to be used in significance scor- ing. opt.step.size searches for an optimal number of merge steps in community find-
ing. score.communities determines scores for genomic modules. Included in sam-
ple data are an interactome built from KEGG and HPRD pairwise interactions and gene sym- bols and fold change values for GSE14520.
License GNU GPL
Collate ’calc.weights.R’ ’opt.step.size.R’ ’score.communities.R’

Requires igraph package
