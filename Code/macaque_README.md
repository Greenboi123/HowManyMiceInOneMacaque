 

## **Copyright & License**

To respect the intellectual property rights, protect the rights of data authors, expand services of the data center, and evaluate the application potential of data, data users should clearly indicate the source of the data and the author of the data in the research results generated by using the data (including published papers, articles, data products, and unpublished research reports, data products and other results). For re-posting (second or multiple releases) data, the author must also indicate the source of the original data.

Example of acknowledgement statement is included below: The dataset is provided by Brain Science Data Center, Chinese Academy of Sciences (https://braindatacenter.cn/).

## Reference of Data

Yidi Sun.(2023).Cell type annotation dataset for the spatial transcriptome of the macaque cortex.Brain Science Data Center,Chinese Academy of Sciences. https://cstr.cn/33145.11.BSDC.1685409749.1663093488869060610.https://doi.org/10.12412/BSDC.1685411291.30001.

## Data Description

### spatial transcriptome

~~~shell
#eg: 
cat total_gene_T100.type20230503-macaque1-contour2.round.txt | head 
chip    gene    x       y       cell_id gene_area       rx      ry      expr
T100    A2M     14488   67681   1       931     47973   53731   0.69
T100    ABTB2   14488   67681   1       931     47973   53731   0.69
T100    ACSL1   14488   67681   1       931     47973   53731   1.39
T100    ADAMTS17        14488   67681   1       931     47973   53731   0.69
T100    AKR1B1  14488   67681   1       931     47973   53731   0.69
T100    ALDOC   14488   67681   1       931     47973   53731   1.61
#"total_gene_T100*.txt" file provided the gene expression and spatial position for per cell.
#rx, ry: the exact positions.
#expr: the normalized expression calculated by "SCTnormalize" function from Seurat R package.
#gene_area: the region id, and you can find its corresponding region name in "regions-macaque*.csv" file.
~~~

~~~shell
#eg:
cat ST.CellID.CellType.3monkeys.tsv | head
macaque slide   cell_id celltype        SubClass        Class
macaque1        T155    3       L4.2    L4      GLU
macaque1        T155    5       L6.4    L6      GLU
macaque1        T155    8       OLG.8   OLG     NonNeuron
macaque1        T155    14      L4/5.12 L4/5    GLU
macaque1        T155    15      L2/3.8  L2/3    GLU
macaque1        T155    17      VLMC.1  VLMC    NonNeuron
macaque1        T155    19      L4/5.3  L4/5    GLU
macaque1        T155    20      VIP.8   VIP     GABA
macaque1        T155    24      L2/3.6  L2/3    GLU
~~~

~~~sh
cytpe_region_ration.xlsx
#eg:
	ASC.1	ASC.10	ASC.11	ASC.12
1/2	0.007014598	6.76047E-05	0.001401287	9.79578E-05
10mc	0.003526723	7.1371E-05	0.003813147	2.03917E-05
10mr	0.005906907	0.000122349	0.001768487	7.69838E-05
10o	0.006149509	9.39299E-05	0.001639933	0.000103647
11l	0.003713555	6.58263E-05	0.002291852	9.05111E-05
11m	0.003278378	7.87222E-05	0.002315875	7.085E-05
#This file provided the proportions of 226 cell types in 143 brain regions that can be used to build 3D rendering.
~~~

### single nucleus transcriptome

We provided the raw counts matrix of the single-cell transcriptome of two monkeys, along with the metadata information of the corresponding cells, including the library name, region, brain_area, cell type.                                                                snRNA.sparseMatrix_Monkey1.counts.rds                                                                       snRNA.sparseMatrix_Monkey2.counts.rds                                                                                    snRNA.metadata.2monkeys.rds

## Article Citation

Chen A, Sun Y, Lei Y, et al. Single-cell spatial transcriptome reveals cell-type organization in the macaque cortex [published online ahead of print, 2023 Jul 7]. *Cell*. 2023;S0092-8674(23)00679-7. doi:10.1016/j.cell.2023.06.009             https://doi.org/10.1016/j.cell.2023.06.009