# DiGCellNet
data processing:
Filter out the rows with variable name logFC from data.v6 to get data_v6_log.xlsx.
Filter out the data with Disease as Type 2 diabetes from data_v6_log.xlsx to get t2dall.xlsx.
Download the T2D-related gene data GeneCards-T2D.csv from GeneCards, filter out the data whose Category is Protein Coding, and get GeneCards-T2D-selected.xlsx.

run label.py:
Specify celltype(for example, Delta), load data t2dall.xlsx and GeneCards-T2D-selected.xlsx, get label_Delta.xlsx.

run combine.py：
input label_Delta.xlsx and PPI_400.emb，get feature_with_label_nod2vec_Delta.txt.

run DiGCellNet.py
Get the results of all methods, record the results. Then run figure.py to get Figure2.

run Enrichment.py performs enrichment analysis and gets the result Figure4.

Verify the results on an independent data set, download the independent data set human_islets.xlsx, run violin.py to get Figure4.
