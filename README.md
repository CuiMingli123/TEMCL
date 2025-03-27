# TEMCL
### TEMCL: Prediction of Drug-disease Associations Based on Transformer and Enhanced Multi-view Contrastive Learning
#### Flowchart of TEMCL. In part A, TEMCL uses transformer to extract high-order features of nodes. In part B, two different types of views are constructed, i.e., homogeneous hypergraphs and heterogeneous association graphs. In part C, HGCN and HGT are used to further extract node features, and contrastive learning is employed to obtain more representative characterizations. Finally, MLP is used for DDAs.
# Datasets:
- Details of Datasets
- In this study, three real datasets, including three types of associations, are used to assess the effectiveness of TEMCL.
- Datasets	Bdataset	Fdataset	Cdataset
- Drugs	269	593	663
- Diseases	598	313	409
- Proteins	1021	2741	993
- DDAs	18416	1933	2532
- Drug-protein Associations	3110	3243	3773
- Disease-protein Associations	5898	54265	10734
- Sparsity	0.1145	0.0104	0.0093
- we have summarized all the key parameters used in our experiments and provided their optimal values for each dataset. These parameters are carefully tuned to achieve optimal performance on each dataset. The details are as follows:
- Dataset	epoch, learning rate, weight-decay, dimension, layer, K, M						
- Bdataset	300	5e-4	1e−5	64	3	20	20
- Fdataset	200	1e-3	1e−5	64	2	20	20
- Cdataset	200	1e-3	1e−5	64	3	20	30

# Requirements:
- python 3.9.13
- cudatoolkit 11.3.1
- pytorch 1.10.0
- dgl 0.9.0
- networkx 2.8.4
- numpy 1.23.1
- scikit-learn 0.24.2
# Code:
- data_preprocess.py: Methods of data processing
- metric.py: Metrics calculation
- pos_contrast.py: Get positive and negative samples for contrastive learning
- Contrast.py: Code of graph contrastive learning
- model1.py: Model of TEMCL
- train_DDA1.py: Train the model

# Usage:
Execute ```python train_DDA1.py``` 

