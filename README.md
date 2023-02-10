# Data and figures code from Pietto et al (Dev. Psychol, 2023)
These are the data and figures code from Pietto et al (Dev. Psychol, 2023). Analysis were carried out using Matlab and [EEGLAB v2020_0](https://sccn.ucsd.edu/eeglab/index.php). Also, for the computation of brain network metrics we used the Brain Connectivity Toolbox available [here](https://sites.google.com/site/bctnet/). For further details please refer to Pietto et al (Dev. Psychol, 2023).

This project is part of a larger collaboration between the Unidad de Neurobiología Aplicada (CEMIC - CONICET, Argentina; https://cemic.edu.ar/una.php/) and the Laboratorio de Inteligencia Artificial Aplicada (Instituto de Cs. de la Computación, Fac. de Cs. Exactas y Naturales, UBA - CONICET, Argentina; https://liaa.dc.uba.ar/). Our general goal is to study the influence of adverse environmental conditions on brain function and the effectiveness of cognitive interventions for changing neural activity related to executive functioning.

In the present study we examined the impact of two individualized cognitive interventions with Executive Functions-demanding activities on brain connectivity in preschoolers from low socioeconomic status homes, using complex network analysis. At baseline, participants were classified as high- or low- performers based on their performance in an inhibitory control task, and then they were assigned into intervention and control groups within each performance level. Before and after the intervention, the neural activity of each child was recorded at rest using a mobile electroencephalogram device. We found significant intervention-related changes in global efficiency, global strength, and the strength of long-range connections in the theta frequency band in the intervention low-performing group.

# How to cite us
#### Please, if you like it / use it cite us:
Pietto, M. L., Giovannetti, F., Segretin, M. S., Kamienkowski, J. E., & Lipina, S. J. (2023). Increased integration of functional connectivity after cognitive intervention in preschoolers from low socioeconomic status. Developmental Psychology.

# Data
Piettoetal_Training-functional-connectivity-in-preschoolers involved eleven arrays. In particular, two of them contain the adjacency matrices used to generate all the metrics implemented in the study. The networks from the EEG data: "adjacency_matrices_normalized_all_thresholds", and the equivalents random networks: "adjacency_matrices_normalized_all_thresholds_random". Two arrays include the means of clustering coefficients ("means_clustering_coef_all_thresholds") and path lengths ("means_path_length_all_thresholds") at the different thresholds used to compute and compare small-world parameters ("small_worldness_all_thresholds"). The data also comprise the clustering coefficients ("clustering_coef_all_channels"), strength ("strength_all_channels"), and strength parameters of long- ("strength_long_range_all_channels") and short-range connections ("strength_short_range_all_channels") from all eeg channels. The array "means_all_brain_network_measures" includes the metrics used in the statistical analyses, tables, and figures. Finally, the vector "GROUPS" contains each subject's group ID.

|Name 	                                                   | Size 	  | Bytes   | Class  |	Description|
|----------------------------------------------------------|--------------------|--------|-------------|--------------------------------------------------------------
|adjacency_matrices_normalized_all_thresholds              | 1X2      | 1982832 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|adjacency_matrices_normalized_all_thresholds{1} and {2}   | 1x1      | 991312  | struct |  Adjacency matrices in theta and alpha frequency bands |
|adjacency_matrices_normalized_all_thresholds{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x14x8x79      | 495488  | single | Channels, Channels,Thresholds, Subjects  |
|adjacency_matrices_normalized_all_thresholds_random       | 1X2      | 1982832 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|adjacency_matrices_normalized_all_thresholds_random{1} and {2}   | 1x1      | 991312  | struct |  Adjacency matrices in theta and alpha frequency bands |
|adjacency_matrices_normalized_all_thresholds_random{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x14x8x79      | 495488  | single | Channels, Channels,Thresholds, Subjects  |
|means_clustering_coef_all_thresholds                       | 1X2      | 21104 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|means_clustering_coef_all_thresholds{1} and {2}   | 1x1      | 10448  | struct |  Clustering coefficients of networks in theta and alpha frequency bands |
|means_clustering_coef_all_thresholds{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 79x8x2      | 5056  | single | Subjects, Thresholds, Type of network |
|means_path_length_all_thresholds                       | 1X2      | 41328 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|means_path_length_all_thresholds{1} and {2}   | 1x1      | 20560  | struct |  Path lengths of networks in theta and alpha frequency bands |
|means_path_length_all_thresholds{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 79x8x2      | 10112  | double | Subjects, Thresholds, Type of network |
|small_worldness_all_thresholds                       | 1X2      | 10992 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|small_worldness_all_thresholds{1} and {2}   | 1x1      | 5392  | struct |  Small worldness parameters in theta and alpha frequency bands |
|small_worldness_all_thresholds{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 79x8      | 2528  | single | Subjects, Thresholds |
|clustering_coef_all_channels                       | 1X2      | 18576 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|clustering_coef_all_channels{1} and {2}   | 1x1      | 9184  | struct |  Clustering coefficients of all channels in theta and alpha frequency bands |
|clustering_coef_all_channels{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x79      | 4424  | single | Channels, Subjects ||clustering_coef_all_channels                       | 1X2      | 18576 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|clustering_coef_all_channels{1} and {2}   | 1x1      | 9184  | struct |  Clustering coefficients of all channels in theta and alpha frequency bands |
|clustering_coef_all_channels{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x79      | 4424  | single | Channels, Subjects |
|strength_all_channels                       | 1X2      | 18576 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|strength_all_channels{1} and {2}   | 1x1      | 9184  | struct |  Strength parameters of all channels in theta and alpha frequency bands |
|strength_all_channels{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x79      | 4424  | single | Channels, Subjects |
|strength_long_range_all_channels                       | 1X2      | 36272 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|strength_long_range_all_channels{1} and {2}   | 1x1      | 18032  | struct |  Strength of long-range connections of all channels in theta and alpha frequency bands |
|strength_long_range_all_channels{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x79      | 8848  | double | Channels, Subjects |
|strength_short_range_all_channels                       | 1X2      | 36272 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|strength_short_range_all_channels{1} and {2}   | 1x1      | 18032  | struct |  Strength of short-range connections of all channels in theta and alpha frequency bands |
|strength_short_range_all_channels{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x79      | 8848  | double | Channels, Subjects |
|means_all_brain_network_measures                       | 1X1      | 9916 | struct |  data: Network metrics. Varnames: metrics's names |
|means_all_brain_network_measures.data                  | 1x2      | 7792  | cell |  Strength of short-range connections of all channels in theta and alpha frequency bands |
|means_all_brain_network_measures.data{1} and .data{2} | 79x12      | 3792  | single | Subjects, Metrics |
|means_all_brain_network_measures.varnames | 1x12      | 1788  | cell | Metrics names |
|GROUPS | 79x1      | 632  | Double | Subject's group ID |

Note.
Thresholds levels: 1 = 0.2; 2 = 0.3; 3 = 0.4; 4 = 0.5; 5 = 0.6; 6 = 0.7; 7 = 0.8; 8 = 0.9.
Channels names: 1 = AF3;  2 = F7; 3 = F3; 4 = FC5; 5 = T7; 6 = P7; 7 = O1; 8 = O2; 9 = P8; 10 = T8; 11 = FC6; 12 = F4; 13 = F8; 14 = AF4.
Subject's group ID: 1 = Control low-performers; 2 = Control high-performers; 3 = Experimental low-performers; 4 = Experimental high-performers.
