---
title: 'DBCLS BioHackathon 2026 report: QPX: Pathway analysis environment for non-model organisms'
title_short: 'BioHackJP26: QPX'
tags:
  - Multi-omics
  - Pathway analysis
authors:
  - name: Hidemasa Bono
    orcid: 0000-0003-4413-0651
    affiliation: 1
    role: Conceptualization, Writing - original draft
  - name: Naoya Oec
    orcid: 0000-0002-7491-4994
    affiliation: 2
    role: System development, Validation
  - name: Haruka Tanimoto
    orcid: 0009-0000-9313-6318
    affiliation: 1
    role: Data creation
  - name: Tomohiro Taguchi
    orcid: 0009-0006-4779-4188
    affiliation: 1
    role: Data creation
  - name: Amane Kurata
    orcid: 0009-0001-2531-5506
    affiliation: 1
    role: Data creation
  - name: Ryo Nozu
    orcid: 0000-0002-1099-3152
    affiliation: 1
    role: Validation, Data creation
affiliations:
  - name: Hiroshima University
    ror: 03t78wx29
    index: 1
  - name: Dogrun Inc.
    index: 2
date: 18 September 2026
cito-bibliography: paper.bib
event: BH26JP
biohackathon_name: "DBCLS BioHackathon 2026"
biohackathon_url:   "https://2026.biohackathon.org/"
biohackathon_location: "Matsuyama, Japan, 2026"
group: QPX
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackathon-japan/BH26-QPX
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Bono H \emph{et al.}
---


# Introduction

As part of the DBCLS BioHackathon 2026, we here report the development of pathway analysis environment called Quest for Pathways with eXpression (QPX) designed for non-model organisms.

# Results and Discussion

Following BH23 [@BH23rep] and BH25 [@BH25rep], discussions continued at BH26 with the aim of enhancing the usability of QPX. 
At BH26, together with three new members from Hiroshima University (two undergraduate students and one postdoctoral researcher), we worked on the following points toward the development of pathway data for non-model organisms.

## PathLift in use

PathLift is a command line interface (CLI) tool that ‘lifts’ pathways in Graphical Pathway Markup Language (GPML) from WikiPathways by mapping them to gene IDs in other species, using an ortholog mapping table. 
It outputs a GPML file in which the GeneProduct nodes from the source species (e.g. human) have been replaced and expanded to candidate gene nodes for the target species.
Create new pathways for non-model organisms with public DB ID annotations

Following domestic BioHackathon in Japan (BH26.6), we conducted several projects to generate pathway data for non-model organisms using PathLift.

As an example of cross-species pathway reuse, we used PathLift to map an *Arabidopsis thaliana* mitochondrial complex I pathway to *Oryza sativa* gene candidates (Fig. 1). The resulting GPML retains the pathway layout while displaying the corresponding rice gene IDs.

As an example of cross-species pathway reuse, we used PathLift to map an *Arabidopsis thaliana* mitochondrial complex I pathway to *Oryza sativa* gene candidates (Fig. 1). The resulting GPML retains the pathway layout while displaying the corresponding rice gene IDs.

## QPX in Practice 

We created several annotated pathway diagrams and used them for biological pathway analysis (Table 1).
  
Table 1: New pathways created in BH26

| Pathway | Species |  Note |
| -------- | --------  | -------- |
| Glycolysis and gluconeogenesis (`WP534`) | *Homo sapiens* | Integration of (meta-analysis of) transcriptomes and proteome data  |
| Pentose phosphate, etc | *Symplocarpus renifolius* | Integration of metabolome and transcriptome data |
| Food Allergy–Associated Mast Cell Activation Pathway |  *Homo sapiens* | |
| Mitochondrial complex I | *Arabidopsis thaliana*  <br /> *Oryza sativa* | |
| Photosynthetic carbon reduction (`WP1461`) | *Arabidopsis thaliana* | |

### Integration of transcriptomes and proteome data

Use case for the integration of multiple omics data was investigated.
Differentially abundant proteins (DAPs) in hypoxic stress from proteome and Meta-analysis of public transcriptomes and hypoxic stress were extracted from manuscripts below.

1.  Transcriptome: hypoxic stress RNA-seq data (HN-score) collected in "Multi-Omic Meta-Analysis of Transcriptomes and the Bibliome Uncovers Novel Hypoxia-Inducible Genes. DOI: 10.3390/biomedicines9050582" [@ono_2021].
2. Proteome: differentially abundant proteins (DAPs) flags in "Proteomic-Based Analysis of Hypoxia- and Physioxia-Responsive Proteins and Pathways in Diffuse Large B-Cell Lymphoma. DOI: 10.3390/cells10082025"


### Integration of transcriptome and metabolome data

A minimal set for reproducing the display of gene expression and metabolome data from the thermogenic tissues Hot_F / Hot_P of the Asian skunk cabbage (*Symplocarpus renifolius*) on pathway maps with QPX.

## Future work

...

## Acknowledgements

We thank Dr. Egon Willighagen for the continuous support in curating pathways created and inclusion to WikiPathways. 
We also thank Dr. Evan Bolton for pointing the useful resource in PubChem.
We deeply thank organizers of BH26 at Matsuyama (13-19 September 2026) for giving us a chance to refine the QPX system.

# References


