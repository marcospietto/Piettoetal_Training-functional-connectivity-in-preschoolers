# Data and figures code from Pietto et al (Dev. Psychol, 2023)
These are the data and figures code from Pietto et al (Dev. Psychol, 2023). Analysis were carried out using Matlab and [EEGLAB v2020_0](https://sccn.ucsd.edu/eeglab/index.php). Also, for the computation of brain network metrics we used the Brain Connectivity Toolbox available [here](https://sites.google.com/site/bctnet/). For further details please refer to Pietto et al (Dev. Psychol, 2023).

This project is part of a larger collaboration between the Unidad de Neurobiología Aplicada (CEMIC - CONICET, Argentina; https://cemic.edu.ar/una.php/) and the Laboratorio de Inteligencia Artificial Aplicada (Instituto de Cs. de la Computación, Fac. de Cs. Exactas y Naturales, UBA - CONICET, Argentina; https://liaa.dc.uba.ar/). Our general goal is to study the influence of adverse environmental conditions on brain function and the effectiveness of cognitive interventions for changing neural activity related to executive functioning.

In the present study we examined the impact of two individualized cognitive interventions with Executive Functions-demanding activities on brain connectivity in preschoolers from low socioeconomic status homes, using complex network analysis. At baseline, participants were classified as high- or low- performers based on their performance in an inhibitory control task, and then they were assigned into intervention and control groups within each performance level. Before and after the intervention, the neural activity of each child was recorded at rest using a mobile electroencephalogram device. We found significant intervention-related changes in global efficiency, global strength, and the strength of long-range connections in the theta frequency band in the intervention low-performing group.

# How to cite us
#### Please, if you like it / use it cite us:
Pietto, M. L., Giovannetti, F., Segretin, M. S., Kamienkowski, J. E., & Lipina, S. J. (2023). Increased integration of functional connectivity after cognitive intervention in preschoolers from low socioeconomic status. Developmental Psychology.

# Data
Data involved eleven structures. In particular, two structures contain the adjacency matrices used to generate all the metrics implemented in the study. The networks from the data: "adjacency_matrices_normalized_all_thresholds", and the equivalents random networks: "matrices adjacency_matrices_normalized_all_thresholds". Two structures include the means of clustering coefficients ("means_clustering_coef_all_thresholds") and path lengths ("means_path_length_all_thresholds") at the different thresholds used to compute and compare small-world parameters ("small_worldness_all_thresholds"). The data also comprise the clustering coefficients ("clustering_coef_all_channels"), strength ("strength_all_channels"), and strength parameters of long- ("strength_long_range_all_channels") and short-range connections ("strength_short_range_all_channels") from all eeg channels. The structure "means_all_brain_network_measures" includes the metrics used in the statistical analyses, tables, and figures. Finally, the vector "GROUPS" contains each subject's group ID.

|Name 	                                                   | Size 	  | Bytes   | Class  |	Description|
|----------------------------------------------------------|--------------------|--------|-------------|--------------------------------------------------------------
|adjacency_matrices_normalized_all_thresholds              | 1X2      | 1982832 | cell |  Cell n1: pre-intervention session. Cell n2: post-intervention session |
|adjacency_matrices_normalized_all_thresholds{1} and {2}   | 1x1      | 991312  | struct |  Adjacency matrices in theta and alpha frequency bands |
|adjacency_matrices_normalized_all_thresholds{1}.Theta, {1}.Alpha, {2}.Theta and {2}.Alpha | 14x14x8x79      | 495488  | single | Channels, Channels,Thresholds, Subjects  |
|DATA.stimulus_locked.ERP and .ERSP                        | 1x2      | 430784  | cell   |  Cell n1: pre-intervention session. Cell n2: post-intervention session.|
|DATA.response_locked.ERP and .ERSP                        | 1x2      | 425264  | cell   |  Cell n1: pre-intervention session. Cell n2: post-intervention session.|
|DATA.stimulus_locked.ERP{1}, .ERP{2}, ERSP{1} and ERSP{2} | 115x78x3 | 215280  | double |  Samples, Subjects, Correct trials: 1- Go; 2- NoGo; 3- NoGo minus Go.|
|DATA.response_locked.ERP{1}, .ERP{2}, ERSP{1} and ERSP{2} | 115x77x3 | 212520  | double |  Samples, Subjects, Responses: 1- Correct Go; 2- Error NoGo; 3- Error minus Correct.|
