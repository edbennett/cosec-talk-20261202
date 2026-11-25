# Backup Slides

---

# arXiv survey

-

## Survey scope

* Every hep-lat arXiv submission from 2021
  * Including cross-lists
  * Skim-read plus keyword searches
* Series of questions: yes/no, categorisation, and free text
  * Answers based solely on text of paper
* Data and analysis code are available on [Zenodo](https://doi.org/10.5281/zenodo.6584001)

-

## What computations does an LFT paper do?

A very reductive view:

1. Generate field configurations
2. Measures observables on configurations
3. Analyses, plots, tabulates measured observables

Less focus on emerging techniques, e.g.

* tensor networks
* quantum simulation

-

## High level numbers

Out of 1,229 arXiv submissions in 2021:

![Bar charts breaking down arXiv submissions](plots/all_numerical.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

* Use of preprints is already decades ahead of many disciplines! <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## Why cite software?

Citing software:
* Gives credit to those who built it
  * Avoids paper-centric metrics
  * Justifies funding maintenance
* More precisely specifies what was done
  * Implementations vary in subtle details
  * Referring to an algorithm is not sufficient

-

## Setting the scene: Acknowledging HPC

![Bar chart breaking down arXiv submissions by whether they acknowledge HPC resources. The majority of hep-lat submissions worldwide and the vast majority in the UK do. Most crosslists do not.](plots/acknowledges_compute_resources.svg) <!-- .element height="700px" -->

-

## Aside: The importance of a compute ecosystem

![Bar chart breaking down the 91 numerical lattice papers; over 70 acknowledge HPC resources, over a third acknowledge DiRAC, and over a sixth acknowledge Supercomputing Wales](plots/dirac_scw.svg) <!-- .element height="700px" -->

-

## How many submissions specify _any_ software?

![Bar chart breaking down arXiv submissions by whether they acknowledge software. The majortity do not. A slight majority in the UK do.](plots/specifies_any_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## How is software acknowledged?

![Bar chart breaking down submissions specifying software by the method of psecification. Citation to a paper is most common.](plots/how_specifies_any_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## Where does software live?

![Bar chart breaking down the locations used for software in use. GitHub is the most popular, followed by Zenodo.](plots/all_software_locations.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="500px" -->

* Zenodo is a data repository, gives DOIs
* GitHub is a code collaboration/hosting service; does not

-

## Generating field configurations

* Usually using Monte Carlo methods to sample from some action
* Usually extremely expensive
  * Hard to test automated workflows end-to-end
  * Hard for others to reproduce (wait for Moore's law?)
  * Open sharing of configurations is good
    * Needs infrastructure (more later)
* Reproducibility efforts include:
  * Seedable RNG, RNG checkpoints
  * Include run parameters in output, configurations files
  * Include code version/commit ID within output
* Around 44% of publications do this

-

## Do authors specify how configurations are generated?

![Bar chart breaking down whether publications specify what software was used for generating configurations. Internationally the majority do not; in the UK a slight majority do.](plots/specifies_configuration_generation_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="600px" -->

The UK is significantly better than average here. <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## What software is used to generate configurations?

![Bar chart showing the top ten software packages used for configuration generation. Out of 100 papers, 14 use openQCD, 9 CL2QCD, and 7 each MILC, HiRep, FGrid, Chroma, BQCD](plots/configuration_generation_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="500px" -->

* 11 indicate unreleased modifications <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
* More only name toolkits (e.g. Grid, Chroma) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## What about work that doesn't generate configurations?

![Bar chart breaking down whether publications use existing field configurations; around 39% do. The majority of worldwide papers don't, but a slight majority of UK papers do.](plots/uses_existing_configurations.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## How are existing configurations acknowledged?

![Bar chart breaking down how existing ensembles are acknowledged or cited. The overwhelming majority are citations to papers.](plots/how_specify_ensembles.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px"""-->

-

## Lattice Data Grids

* [International Lattice Data Grid](https://hpc.desy.de/ildg/)
  * Defines protocols and standards
  * Local deployments (_Regional Grids_):
    * US, UK, Europe, Japan, Australia
* FAIR before FAIR
* Early-ish example of open science

-

## How many papers acknowledge ILDG/an RG?

![Bar chart breaking down whether papers acknowledge a lattice data grid. Less than 5% do; 0% within the UK.](plots/acknowledges_data_grid.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## Which RGs are acknowledged?

![Bar chart showing which lattice data grids are acknowledged. 14 of 14 use the JLDG; 10 also acknowledge ILDG.](plots/which_data_grids.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="500px"-->

* Japan has the most active(ly cited) RG <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
* Either the others aren't used, or aren't cited <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## Performing measurements

![Bar chart breaking down whether publications specify what software was used for measurement. A significant majority internationally and a small majority in the UK do not](plots/specifies_measurement_software.svg) <!-- .element height="700px" -->

-

## What measurement codes are in use?

![Bar chart showing the top ten measurement codes. Chroma has 45 uses, QUDA 22, MILC and Grid 16.](plots/measurement_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="500px" -->

* 27 indicate unreleased modifications <!-- .element: class="fragment fade-in" data-fragment-index="2" width="700px" -->
* More only name toolkits (e.g. Grid, Chroma) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## Use of open data

(Excluding field configurations)

![Bar chart breaking down how publications acknowledge data they have used; the overwhelming majority are citations to papers](plots/how_acknowledges_other_data.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="500px" -->

* Acknowledgements to individuals <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
* Not FAIR <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## Do authors publish data?

![Bar chart breaking down how whether publications publish data. The overwhelming majority do not.](plots/publish_any_data.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="1300px" -->

-

## Where are data published?

![Bar chart showing where data are published. Out of 38 submissions, 12 publish data directly on the arXiv, 5 on GitLab, 3 each on Unibi and Zenodo.](plots/used_data_repositories.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## Data analysis

* Experimental research:
  * Does not generate configurations
  * Does not perform computationally reproducible "measurements"
  * Still has a substantial reproducibility effort
  * $\Rightarrow$ Data analysis of measurement results is the key reproducibility question

-

## Do authors specify _any_ software used for analysis?

![Bar graph breaking down whether software used for data analysis is specified. The vast majority of publications do not specify any software.](plots/specifies_analysis_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## What software is specified?

![Bar graph showing the top 10 software packages acknowledged by hep-lat publications and crosslists. The top 5 in hep-lat are Mathematica, gvar, numpy, matplotlib, and lsqfit.](plots/acknowledged_analysis_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## Do authors publish a full analysis workflow?

![Bar graph breaking down whether authors publish a full or partial analysis workflow. The overwhelming majority do not; only single digit numbers out of a thousand publish in full.](plots/publish_analysis_workflow.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" height="700px" -->

-

## Who is generating configurations?

![Breakdown of collaborations generating configurations used by others](plots/used_configuration_generating_collaborations.svg) <!-- .element height="700px" -->

-

## How is data analysis software cited?

![Bar chart showing how data analysis software is cited in hep-lat and crosslists. Citations to papers dominate in both, but cross-lists have far more instances of naming a piece of software with no other citation or reference.](plots/how_analysis_software_cited.svg) <!-- .element height="700px" -->

---

# Community survey

-

<!-- .element data-background-color="white" -->

![](./community-plots/benefit_from_others_data_frequency.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/code_publishing_services_cloud.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/code_quality.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/consider_publishing.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/current_location.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/current_position.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/data_format_documentation.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/data_management_plan.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/data_publishing_services_cloud.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/distance_from_ideal.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/ease_of_reproduction.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/eosc_familiarity.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/fair_data_familiarity.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/how_automated.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/importance_for_reproducibility.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/institutional_repositories.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/language_preferences.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/lattice_tool_cloud.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/made_code_available.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/metadata_familiarity.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/most_important_for_reproducibility.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/nonlattice_tool_cloud.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/on_request.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/open_science_familiarity.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/open_science_incentives_cloud.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/open_science_participation.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/open_science_useful.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/persistent_identifier_familiarity.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/styles_of_plotting.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/styles_of_tabulation.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/text_or_graphical.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/time_to_regenerate.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/version_controlled_or_backups.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/why_not_made_code_available.svg) <!-- .element height="600px" -->

-

<!-- .element data-background-color="white" -->

![](./community-plots/why_not_made_data_available.svg) <!-- .element height="600px" -->

---

# Guide Contents

-

## About this document

- Introduction
- How to read this document
- Version history
- Definitions
  - Reproducibility
  - FAIR
  - Open Science
  - Copyright and licensing
  - Paper stages
  - Persistent identifiers
  - Keywords
- Tool-assisted research

-

## Publications

- Open Access
- `author.xml`
- Acknowledgments
- Additional statements

-

## Data

- What to include in a data release
  - Final numbers
  - Input files
  - Data from HPC
  - Repackaged data
  - Metadata and analysis parameters
  - Documentation
- Where and how to publish a data release
  - Where to publish
  - Obtaining a DOI before data are ready
  - Structuring the release
  - Completing the upload form
- Field configurations

-

## Workflows

<div style="width: 49%; float: left">

- Workflow essentials
  - `README`
  - `LICENSE`
  - `CITATION.cff`
  - `.gitignore`
  - `.pre-commit-config.yaml`
- Workflow management
  - Structuring a workflow
- Structuring the repository
  - Environment definition
  - Libraries
- Assets to generate
  - Plots; Tables; Definitions; Data assets

</div>

<div style="width: 49%; float: right">

- Metadata &amp; provenance tracking
- Standard tools and techniques
  - Code review
  - Statistics and fits
  - Continuous Integration
- Numerical reproducibility
  - Randomness
- Testing a workflow
- Publishing a workflow
  - Preparing an archive
  - What to include in a release
  - Completing the upload form

</div>

-

## HPC Software

- Open Source and Community Software
- Data formats
- Workflows
  - `hmcdj`
  - `PlateSpinner`

-

## Appendices

- Checklist for publishing a journal article
- Applying these techniques outside of lattice
  - Data
  - Workflows
  - Publications
