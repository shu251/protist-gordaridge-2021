## Protistan predation pressure at hydrothermal vents

Associated code for data analysis, amplicon sequence processing, and figure generation for _in prep_ manuscript entitled **Protistan grazing impacts microbial communities and carbon cycling at deep-sea hydrothermal vents**.   

Hu, S.K., Herrera, E., Smith, A., Pachiadaki, M.G., Edgcomb, V.P., Sylva, S.P., et al. (In prep) Protistan grazing impacts microbial communities and carbon cycling at deep-sea hydrothermal vents.   


[All code and analyses present here.](https://shu251.github.io/protist-gordaridge-2021/)

### Description of contents

#### 1. Set up and introduce study

Microbial eukaryotes (or protists) in marine ecosystems are a link between microbial primary producers and all higher trophic levels. The rate at which heterotrophic protistan grazers consume microbial prey and recycle organic matter is an important component of marine microbial food webs and carbon cycling. At deep-sea hydrothermal vents, chemosynthetic bacteria and archaea form the basis of a food web in the absence of sunlight, but the role of protistan grazers in these highly productive ecosystems is largely unexplored. Here, we paired grazing experiments with a molecular survey to quantify protistan grazing and to characterize the composition of vent-associated protists in low-temperature venting fluids from Gorda Ridge in the North East (NE) Pacific Ocean. Results revealed protists exert higher predation pressure at vents compared to the surrounding deep seawater environment and may account for consuming 28-62% of the daily stock of prokaryotic biomass within the hydrothermal vent food web. The vent-associated protistan community was more species rich relative to the background deep sea, and patterns in the distribution and co-occurrence of vent microbes provided additional insights into potential predator-prey interactions. Ciliates, followed by dinoflagellates, Syndiniales, rhizaria, and stramenopiles dominated the vent protist community and included bacterivorous species, species known to host symbionts, and parasites. Our findings provide an estimate of protistan grazing pressure within hydrothermal vent food webs, highlighting the role that diverse deep-sea protistan communities have in carbon cycling.

#### 2. Working R environment

Using R version 3.6.1

#### 3. Grazing experiment


#### 4. Process 18S rRNA gene amplicons

#### Characterize protist diversity

#### Classify protist distribution

#### Protistan distribution and diversity across samples

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
