# RepViz
Data for the repertoire summary visualization project (CSE 512)

## Introduction
The `Data` folder currently includes 12 datasets.
Each `*_obs.csv` contains summaries of tens of thousands of DNA readings sequenced from a patients's IgH (immunoglobulin heavy chain) locus.
These summaries are either based on the raw "mature" sequence read or derived from the inferred "naive" sequence obtained from [`partis`](https://github.com/psathyrella/partis).
Thus, each row of the dataset corresponds to one sequence in the repertoire of BCRs, on which different summary statistics are computed in each column.
Each `*_sim.csv` contains the same summaries, but for a dataset that was simulated based on the individual's original observed dataset.
This simulation was also conducted via `partis`; more details about the simulation can be found in `partis`'s manual, given in the above link.

The following table details the metadata of each dataset.
In particular, there are three patients initialed "FV", "GMC", and "IB", each of whom blood samples were taken at 1 hour and again at 8 days following the time of an influenza vaccination.

| name   | patient | time (post-vaccination) | dataset type |
|--------|---------|-------------------------|--------------|
| f1_obs | FV      | 1 hour                  | observed     |
| f1_sim | FV      | 1 hour                  | simulated    |
| f2_obs | FV      | 8 days                  | observed     |
| f2_sim | FV      | 8 days                  | simulated    |
| g1_obs | GMC     | 1 hour                  | observed     |
| g1_sim | GMC     | 1 hour                  | simulated    |
| g2_obs | GMC     | 8 days                  | observed     |
| g2_sim | GMC     | 8 days                  | simulated    |
| i1_obs | IB      | 1 hour                  | observed     |
| i1_sim | IB      | 1 hour                  | simulated    |
| i2_obs | IB      | 8 days                  | observed     |
| i2_sim | IB      | 8 days                  | simulated    |

Each of the above datasets includes identical columns names, i.e. the same summary stastics were computed for each dataset.
The following table describes the values of each column (NOTE - new columns may be added in the future):

| name | description |
|------|-------------|
| GCContent | The fraction of guanine and cytosine in the mature sequence |
| CDR3Length | The length of the sequence's inferred CDR3 region (i.e. the third complementarity-determining region) |
| Hydrophobicity | The average hydrophobicity of the CDR3's amino acid sequence |
| AliphaticIndex | The relative volume of the CDR3 occupied by aliphatic side chains (alanine, valine, isoleucine, and leucine) |
| GRAVY | The Grand Average of Hydropathicity (GRAVY) index of the CDR3's amino acid sequences |
| VGene3PDeletionLength | Length of inferred V gene 3' deletion |
| DGene3PDeletionLength | Length of inferred D geme 3' deletion |
| DGene5PDeletionLength | Length of inferred D gene 5' deletion |
| JGene5PDeletionLength | Length of inferred J gene 5' deletion |
| VDInsertionLength | Length of inferred VD insertion |
| DJInsertionLength | Length of inferred DJ insertion |
