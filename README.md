# RepViz
Data for the repertoire summary visualization project (CSE 512)

## Introduction
The `Data` folder currently includes two datasets.
`f1_obs.csv` contains summaries of each of roughly 26,000 DNA readings sequenced from an individual's IgH (immunoglobulin heavy chain) locus.
These summaries are either based on the raw "mature" sequence read or derived from the inferred "naive" sequence obtained from [`partis`](https://github.com/psathyrella/partis).
Thus, each row of the dataset corresponds to one sequence in the repertoire, on which different summary statistics are computed in each column.
`f1_sim.csv` contains the same summaries, but for a dataset that was simulated based on the individual's original observed dataset.
This simulation was also conducted via `partis`.

The following table describes the value of each column (summary):

| name | description |
|------|-------------|
| GCContent | The fraction of guanine and cytosine in the mature sequence |
| CDR3Length | The length of the sequence's inferred CDR3 region (i.e. the third complementarity-determining region) |
| Hydrophobicity | The average hydrophobicity of the CDR3's amino acid sequence |
| AliphaticIndex | The relative volume of the CDR3 occupied by aliphatic side chains (alanine, valine, isoleucine, and leucine) |
| GRAVY | The Grand Average of Hydropathicity (GRAVY) index of the CDR3's amino acid sequences
