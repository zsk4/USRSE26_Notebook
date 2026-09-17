# Effective Tutorial Notebooks for Cloud Computing Workflows using Remote Sensing Datasets

Zachary Katz<sup>1</sup>, Tasha Snow<sup>2,3</sup>

<sup>1</sup> Department of Geophysics, Colorado School of Mines, Golden, CO \
<sup>2</sup> Earth System Science Interdisciplinary Center, University of Maryland, College Park, MD \
<sup>3</sup> Cryospheric Laboratory, NASA Goddard Space Flight Center, Greenbelt, MD 

Notebook submitted to USRSE 2026

## Contents

- [Overview](#overview)
- [Tutorial Abstract](#tutorial-abstract)
- [Files](#files)
- [Usage](#usage)

### Overview

We recommend viewing this Readme and the rendered notebooks at https://zsk4.github.io/USRSE26_Notebook/.

This tutorial, adapted from a [tutorial](https://book.cryointhecloud.com/swot-hr-w-is2/) we use to help train users on [CryoCloud](https://book.cryointhecloud.com/) (a Jupyter Hub designed to promote collaborative data-intensive Earth science computing), highlights components Research Software Engineers can think about when creating effective tutorials; scientists interested in learning how to implement large satellite (and other open-access) data cloud-computing workflows should use this [tutorial](https://book.cryointhecloud.com/swot-hr-w-is2/) and associated documentation. The included notebook ```CryoCloud_SWOT_Tutorial.ipynb``` walks users through streaming data from several sources (including NASA's Surface Water and Ocean Topography (SWOT) satellite), applying appropriate geophysical corrections, and plotting a comparison of heights between two satellite datasets over a rift on the Bach Ice Shelf in Antarctica We also include ```Local_SWOT_Tutorial.ipynb``` if running locally (i.e., not on CryoCloud). We showcase best practices in creating useful tutorials learned from running multiple tutorials about accessing geophysical datasets, including creating a tutorial that is quick to run and showcases flexibility/options for users, all while solving an interesting problem. ChatGPT and Github Copilot were used to aid algorithm development and figure creation code. All outputs were revised by the authors.

### Tutorial Abstract
Remote sensing research relies on high volumes of openly accessible data products from satellites spanning different time periods, data formats, and sizes. Traditionally, resources for data access have been limited to individual satellites based on funding mandates for specific missions, siloing tutorials and increasing complexity and cost for users to synthesize datasets to produce novel results. In this notebook, we demonstrate challenges and lessons learned in creating a tutorial notebook for onboarding users combining multiple datasets in a cloud computing environment. This notebook was presented to XX users onboarding to the CryoCloud JupyterHub, with overwhelmingly positive feedback. The notebook guides users to stream ICESat-2 altimetry data, SWOT altimetry data, Dynamic Atmosphere Corrections, background elevation and ice velocity, run a tide model, and plot a comparison of the ICESat-2 and SWOT elevations over a portion of an ice shelf. Through creating this tutorial, we learned three key ideas—speed, flexibility, and interest—that shape an effective data tutorial notebook. Effective tutorials are quick; no cell takes more than a minute to run to help users understand if the workflow is correct without investing significant time. This is often accomplished by using small test datasets but should also have tips for scaling up workflows to larger datasets. Effective tutorials are flexible, showing a full range of options so users can select which meets their needs; they are complete, so users can use the tutorial as a reference. Finally, effective tutorials are interesting, solving a real problem that engages the user. By striving to produce tutorials aligned with these key ideas, we believe they can be an effective tool for reducing the barrier to entry in remote sensing research, leading to more users and interesting science. This approach can be generalized to other fields with large open-access datasets.

### Files

| File | Description |
|------|-------------|
| `CryoCloud_SWOT_Tutorial.ipynb` | Annotated tutorial notebook for use on CryoCloud |
| `Local_SWOT_Tutorial.ipynb` | Alternative tutorial notebook for local use |
| `README.md` | This document, containing and overview and how to use this project |
| `Presentation.pdf` | Accompanying presentation to the tutorial when it was run as an introduction to CryoCloud |
| `USRSE26_SatellieDataTutorial.pdf` | PDF version of tutorial website |
| `USRSE26_SatellieDataTutorial.html` | HTML version of tutorial website |
| | |
| `myst.yml` | Rendering of MyST webpage |
| `pyproject.toml` | Metadata and project package requirements |
| `uv.lock` | Lockfile for use with uv environment creation |
| `Images` | Images used in tutorial |

### Usage
Follow the instructions in the notebooks to set up your free [NASA Earthdata Login](https://urs.earthdata.nasa.gov/) to download SWOT and ICESat-2 data and (optionally) your free [Aviso+ Login](https://www.aviso.altimetry.fr/en/data/data-access/registration-form.html) to download a Dynamic Atmospheric Correction (DAC) for correcting SWOT data.

#### To Run on CryoCloud
Using a default python environment on CryoCloud, clone this repository and run ```CryoCloud_SWOT_Tutorial.ipynb```. Any dependencies not in the default environment will be installed by the notebook.

#### To Run Locally
Clone this repository and use the included pyproject.toml and/or uv.lock to create an environment with the necessary dependencies. Run ```Local_SWOT_Tutorial.ipynb``` using that environment.

