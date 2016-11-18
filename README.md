# Examples accompanying the paper *Superheat: An R package for  creating beautiful heatmaps for visualizing complex data* by Rebecca  L Barter and Bin Yu

This paper contains three open source examples, each of which is based on a
publicly available dataset. These examples are

* Case study I: combining data sources to explore global organ
transplantation trends

* Case study II: uncovering correlations in language using word2vec

* Case study III: ??


Read below to understand how to reproduce these examples yourself.


## Reproducing the examples

1. Clone this repository using `git clone
https://github.com/rlbarter/superheat-examples`

1. Install R and RStudio.

1. Open RStudio and set the wordking directory to the
   `/superheat-examples` folder that you cloned onto your machine.

1. Install the required packages by running
`source("00-install-packages.R")` inside your RStudio console.

1. Install superheat using
`devtools::install_github("rlbarter/superheat")`.

1. Open the .Rmd file for the example you would like to recreate.  For
   example, if you want to recreate Case Study 1, open the `organ.Rmd`
   file in RStudio.

1. Hit the "Knit" button in RStudio.

1. Wait for the document to compile.

1. Explore the html file containing the code, analysis and figures.

1. Edit and play with the code as you wish!



## Case Study I: combining data sources to explore global organ
transplantation trends

The data for this example comes from two sources. The first is from
the Global
Observatory on Donation and Transplantation database curated by WHO
which can be downloaded from
[here](http://www.transplant-observatory.org/export-database/). The
second dataset comes from the United Nations Development Program's
Human Development Reports which can be downloaded from
[here](http://hdr.undp.org/en/data#).




## Case study II: uncovering correlations in language using word2vec


Word2Vec is an extremely popular group of models for embedding words
into high dimensional spaces such that their relative distances to one
another convey semantic meaning. The canonical example of the success
of these word embeddings is the following example

$$\overrightarrow{\text{man}} - \overrightarrow{\text{king}} + \overrightarrow{\text{woman}} = \overrightarrow{\text{queen}}$$

That is, that if you take the word vector for "man'', subtract the
word vector for "king'' and add the word vector for "woman", you
approximately arrive at the word vector for  ''queen''. These models
are quite remarkable and are an exciting step towards teaching
machines to understand language.

In 2013, Google published pre-trained vectors trained on part of the
Google News dataset which consists of around 100 billion words. The
model contains 300-dimensional vectors for 3 million words and phrases
and these vectors can be downloaded from
[here](\url{https://code.google.com/archive/p/word2vec/).

The original file is `GoogleNews-vectors-negative300.bin.gz`, and the
`convert_word2vec.py` file in the `/word2vec` folder of this
repository contains code to convert the original file to a .csv
format. An R version has been generated and is called
`GoogleNews.RData`.


