

README

Walktrap-GM - Walktrap for Genomic Modules
Author: Deanna Petrochilos
License: GNU GPL

The following functions run weights for Walktrap-BM, find the optimal step size, and score communties.  Included in sample data are an interactome built from KEGG and HPRD pairwise interactions and gene symbols and fold change values for GSE14520. 
 

#DATA:

interactome.net: interactome containing pairwise interactions parsed from KEGG and HPRD

GSE14520.GS: gene Symbols for GSE14520
  
GSE7390.FC: fold Change values for GSE14520      
   



#calc.weights: calculates vertex weights, edge weights and random distribution for weight values

calc.weights(network, geneSymbols, foldChange)

returns vector weights (vweights), edge weights (eweights), distribution (dist)


example: wlk.weights <- calc.weights(interactome.net, GSE14520.GS, GSE7390.FC)



  

#opt.step.size: searches for optimal step size, should be run after generating object with walktrap.community() 

walktrap.community(network, steps, merges, modularity, labels, membership, weights)
opt.step.size <- function(testNet, wtcMerges, vweights, dist, threshold, modularity ) 

returns optimal step size

example:
wtc <- walktrap.community(network, steps, merges, modularity, labels, membership, weights)
opt.step.size <- function(interactome.net, wtc$merges, wlk.weights$vweights, wlk.weights$dist, 200, wlk.weights$modularity)



   
score.communities: calculates scores for biological modules found by Walktrap

score.communities(optStepSize, testNet, wtcMerges, vweights, dist) 

returns matrix with community id, community score and community size

example: score.communities(opt.step.size, interactome.net, wtc$merges, wlk.weights$vweights, wlk.weights$dist) 




