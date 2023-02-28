## Dimension reduction serial runs

## Description
This project asks the following question: if you run t-SNE or UMAP over and over for 100 times or more, how different does each map look from each other map? Is each map radically different? Is each map similar? Are there "pockets" of stability?

## Scripts in src/

### bootstrapper.Rmd
This is the code that runs t-SNE and UMAP over and over on a CyTOF dataset, found in data/.

### make_plots.Rmd
Takes the output of the previous script, plots each of the runs, and combines them into a gif for each dimension reduction algorithm. 

### make_conjoined_plots.Rmd
Same as above, but makes a gif that combines the t-SNE and UMAP plots.

### image_ordering.Rmd
Takes the images produced in make_plots.Rmd, and orders them based on similarity. This allows one to determine if there are pockets of stability in terms of the broader island placement. 

## Example
Below is the output of make_conjoined_plots.Rmd.

![](tsne_and_umap.gif)

## Acknowledgements
Marie Burns for allowing me to use her CyTOF data. Mike Leipold for giving me the idea to produce image_ordering.Rmd. 