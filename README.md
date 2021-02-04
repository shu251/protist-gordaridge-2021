## Protistan predation pressure at hydrothermal vents

Associated code for data analysis, amplicon sequence processing, and figure generation for _in prep_ manuscript entitled **Protistan grazing impacts microbial communities and carbon cycling at deep-sea hydrothermal vents**.   

Hu, S.K., Herrera, E., Smith, A., Pachiadaki, M.G., Edgcomb, V.P., Sylva, S.P., et al. (_In prep_) Protistan grazing impacts microbial communities and carbon cycling at deep-sea hydrothermal vents.   


### [All code and analyses presented here.](https://shu251.github.io/protist-gordaridge-2021/)

### Description of contents

#### 1. Study background :ocean::volcano:

Microbial eukaryotes (or protists) in marine ecosystems are a link between microbial primary producers and all higher trophic levels. The rate at which heterotrophic protistan grazers consume microbial prey and recycle organic matter is an important component of marine microbial food webs and carbon cycling. At deep-sea hydrothermal vents, chemosynthetic bacteria and archaea form the basis of a food web in the absence of sunlight, but the role of protistan grazers in these highly productive ecosystems is largely unexplored.
Code presented here is for the analysis of grazing experiments, where hydrothermal vent fluid was used in grazing incubations, and amplicon sequences to characterize the protistan and prokaryotic communities associated with the hydrothermal vent environment.

#### 2. Working R environment :computer::yarn:

Using R version 3.6.1 with RMarkdown.

#### 3. Grazing experiment :test_tube::microscope:

Description of code that imports raw cell count information (derived from microscopy counts) and processes this information to determine FLP per eukaryotic cell and downstream estimates of grazing impact.

#### 4. Process 18S rRNA gene amplicons :dna::soap:

Imports raw Amplicon Sequence Variant (ASV) count files, conducted 'decontam' to remove potential contaminate ASVs, and quality checks taxonomy assignment.

#### Characterize protist diversity :toolbox::bar_chart:

Analysis of protist community structure and diversity by averaging across replicate samples, summing to individual taxonomic groups for visualization purposes, and ordination analysis to explore sample-to-sample differences.

#### Classify protist distribution :ocean::cocktail:

18S rRNA gene derived ASVs were classified based on their distribution among samples. ASVs found throughout the entire hydrothermal vent system, including the background seawater environment were classified as 'cosmopolitan'. 'Resident' ASVs were those found only within the hydrothermal vent fluid.

#### Protistan distribution and diversity across samples :card_index_dividers::ocean:

#### Process 16S rRNA gene amplicons

#### Network analysis

#### Regression analysis


### Graphical comic abstract
![vent-comic](figs/GR-comic-protistsession.jpg)


#### Last updated
Feb 1, 2021


#### Notes on RMarkdown compilation

Instructions adapted from [here](https://resources.github.com/whitepapers/github-and-rstudio/).   
_Steps_:
Ahead of time, make sure the repo is started by adding R as an .ignore option.
1. From cloned repo, open RStudio project with all contents, update .Rmd file
2. Save and use Knitr to compile .html and update index files stored in /docs
3. These /docs files were made possible by including this header line in the RMarkdown file:
```
knit: (function(input_file, encoding) {
  out_dir <- 'docs';
  rmarkdown::render(input_file,
 encoding=encoding,
 output_file=file.path(dirname(input_file), out_dir, 'index.html'))})
```
4. Once changes have been saved and Knit complete, commit and comment all changes to git
5. push changes
6. Under settings, set GitHub Pages Source to main branch and /docs
