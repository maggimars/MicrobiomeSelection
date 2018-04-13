# MicrobiomeSelection

This repository contains the data and analysis workflows used to analyze the change in Drosophila microbiome throughout 5 rounds of selection in two diets. The analyses demonstrate varying results when using the `adonis` function in the R package `vegan` and the `beta-group-significance` function from the `diversity` plugin in Qiime2 to test differences between treatments. 

**The p-value calculated by PERMANOVA in Qiime2 is consistently lower than the p-value calculated by `adonis` function in R.** 

The `adonis` p-value for between group differences when both diets are included in the analysis is 0.023, the R-squared is 0.506 and the F.Model is 2.0557 (see: `PhyloseqMicrobiome.Rmd` or https://maggimars.github.io/MicrobiomeSelection/PhyloseqMicrobiome.html). When the same analysis is repeated in Qiime2, the p-value is 0.003 and the psuedo-F is 3.0469 (see: `Q2BrayCurtisSigTesting.mkd`, and view `bray_curtis_distance_significance.qzv` by dragging the file to a browser open to [view.qiime2.org](view.qiime2.org)). 

Similarly, we observed the same pattern when we subsetted our data to include only one diet. The `adonis` p-value for between group differences when only the NSD diet is included in the analysis is 0.07, the R-squared is 0.48397 and the F.Model is 1.98 (see: `PhyloseqMicrobiome.Rmd` or https://maggimars.github.io/MicrobiomeSelection/PhyloseqMicrobiome.html). When the same analysis is repeated in Qiime2, the p-value is 0.036 and the psuedo-F is 2.33631 (see: `Q2BrayCurtisSigTesting.mkd`, and view `bray_curtis_distance_significance.qzv` by dragging the file to a browser open to [view.qiime2.org](view.qiime2.org)).
