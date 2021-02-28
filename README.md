**Live slides: <https://predocday2021-mhall.netlify.app/>**

[TOC levels=1-3]: #

## Table of Contents
- [Abstract](#abstract)
- [Preprint](#preprint)
- [Run locally](#run-locally)
  - [Requirements](#requirements)
  - [Serve](#serve)

# Abstract

#### Nucleotide-resolution bacterial pan-genomics with reference graphs

The frequency distribution of genomic loci for many bacterial species is "U-shaped".
That is, loci are generally rare (accessory) or shared by most (core). One consequence
of this bimodal relationship is that two members of the same species might only have
half their genomic content in common. As such, a single reference can only be used to
describe core variation. Given much bacterial adaptability is facilitated by the
accessory genome, this is an unsatisfactory limitation.

We present a solution to the "single-reference" problem in the form of a novel
pan-genome graph approach. The method, implemented in the software [`pandora`][pandora],
describes samples as a recombinant of genomes within the pan-genome graph and detects
novel variation. Genotyping is performed with respect to an inferred reference genome
that best approximates the sample(s), thus producing a succinct variation
representation.

To illustrate the power of this paradigm, we analyse a set of 20 *E. coli* isolates and
show that we can recover at least 13k more accessory genome SNPs compared with
single-reference tools. Our method achieves comparable error rates with both Illumina
and Nanopore data, with a 6-24x lower error rate than other Nanopore variant-calling
tools.

# Preprint

> [Colquhoun, R. M. et al. Nucleotide-resolution bacterial pan-genomics with reference graphs. bioRxiv (2020) doi:10.1101/2020.11.12.380378.](https://doi.org/10.1101/2020.11.12.380378)

# Run locally

These slides are built on top of my [EBI template][template], using [reveal-hugo].

## Requirements

Firstly, to serve the slides locally, you need to have [Hugo][hugo] installed.

```shell
$ brew install hugo
# also install optional Pygments package for syntax highlighting in presentation
$ pip install Pygments
```

Hugo will serve the presentation as a local static site in your web browser and update
as you make changes in the source code of the presentation.

Next, clone this repository

```shell
$ repo="predocday-20210304"
$ git clone --recurse-submodules "https://github.com/mbhall88/$repo"
$ cd "$repo"
# if you forgot to give the recursive flag when cloning
$ git submodule update --init --recursive
```

## Serve

To serve the presentation in your web browser run the following from the root directory
of the repository.

```shell
$ hugo serve
```

In your web browser, navigate to <http://localhost:1313/>. Every time you make changes
this webpage will auto-reload to reflect those changes.

[hugo]: https://gohugo.io/
[pandora]: https://github.com/rmcolq/pandora
[reveal-hugo]: https://github.com/dzello/reveal-hugo
[template]: https://github.com/mbhall88/reveal-hugo-ebi
[config]: https://github.com/dzello/reveal-hugo#configuration
[example]: https://tac2.netlify.app/#/
[forestry-blog]: https://forestry.io/blog/harness-the-power-of-static-to-create-presentations/
[netlify]: https://www.netlify.com/
[netlify-docs]: https://docs.netlify.com/configure-builds/get-started/
[reveal-hugo-logo]: https://reveal-hugo.dzello.com/logo-example/#/
[reveal-hugo-tut]: https://github.com/dzello/reveal-hugo#tutorial
[revealjs]: https://revealjs.com/
[robot-lung]: https://revealjs-themes.dzello.com/robot-lung.html#/
[sections]: https://github.com/dzello/reveal-hugo#root-vs-section-presentations
[weight]: https://forestry.io/blog/harness-the-power-of-static-to-create-presentations/#additional-markdown-files

