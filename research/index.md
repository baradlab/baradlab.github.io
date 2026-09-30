---
title: Research in the Barad Lab
layout: parallax
group: research
banner: img/site/banners/square_wireframe.webp
---

# Research

The Barad lab uses cellular cryo-electron tomography (cryoET) to understand how the membranes of barrier tissues are organized in health and remodeled in disease. What defines our approach is that we do both halves of the problem in one lab: we build the experimental pipeline that captures cellular structure natively — from vitrification through cryo-focused ion beam (cryo-FIB) milling and correlative fluorescence microscopy — and we develop the computational methods that turn a tomogram into quantified membrane structure. Holding both lets us ask a question the field has not been equipped to answer: how an intact, differentiated barrier is built at molecular resolution, and how it fails under stress and disease.

## Imaging the barrier at molecular resolution

Barrier tissues separate an organism from its environment, and they do so through the precise membrane architecture of a differentiated epithelium. We are building toward imaging that architecture directly, beginning with the gut epithelium.

Our first application is infection of the gut. The intestinal epithelium is a barrier that enteric pathogens have to breach, subvert, or rebuild in order to establish themselves, and the membrane remodeling that accompanies that process is exactly what cryoET and quantitative ultrastructural analysis are suited to resolve. Studying infection in the gut lets us work in a system where the insult is defined and controllable, while still asking how a differentiated barrier holds together and how it comes apart.

Our longer-term goal is to read the pathology of barrier disease directly in patient-derived tissue, at molecular resolution, rather than inferring it from simplified models — imaging organoid and primary-cell models grown from patient material to find structural lesions of the diseased gut barrier that current methods cannot detect. This is the most ambitious direction in the lab, and the one we are most committed to.

OHSU is well suited to this work: the university pairs deep strength in host–pathogen interactions and chemical biology with the Pacific Northwest Cryo-EM Center, alongside cryo-FIB and cryo-fluorescence instrumentation on campus, letting us vitrify diverse patient-derived samples and collect tomographic data locally and at scale.

## Quantifying membrane ultrastructure

CryoET provides three-dimensional views inside cells, with proteins, membranes, and filaments preserved in vitreous ice. Methods for extracting high-resolution protein structures from tomograms have advanced quickly; far less effort has gone into measuring cellular ultrastructure *quantitatively*, which is what makes structure-in-context studies possible.

We build the tools that close that gap. The [Surface Morphometrics Toolkit](https://github.com/GrotjahnLab/surface_morphometrics) converts membrane segmentations into quantified mesh models, turning changes in membrane geometry from a qualitative impression into a statistically rigorous measurement. It reconstructs open surfaces from cellular membrane segmentations and characterizes membrane curvature, thickness, and filament interactions in detail. The toolkit has been adopted widely across the cellular tomography community, and has been used to show how mitochondrial fission is organized by cytoskeletal elements, how cytoplasmic ribosomes on mitochondria alter the local membrane environment, and how prohibitin complexes associate with distinct membrane microdomains.

In the lab we are now extending this foundation from measuring membrane *shape* to identifying the molecules that create it, using model-guided analysis of tomogram density to read membrane composition, membrane-associated protein structure, and cytoskeletal organization out of the same dataset.

## Membrane remodeling in infection

Pathogens are masterful manipulators of host cells, and the membrane rearrangements they drive are both a biological question in their own right and the entry point for our work on the gut barrier above.

With the Överby and Carlson labs at Umeå University, we applied the Surface Morphometrics Toolkit to cells infected with Langat virus, a tick-borne flavivirus that models its highly pathogenic relatives, and quantified the membrane remodeling at viral replication organelles. This resolved how genome replication, virion budding, and particle maturation are spatially coupled, and revealed a previously undescribed membrane thickening that does not track with RNA replication and is instead likely linked to production of nonstructural proteins.

We also use cryoET to characterize how mammalian cells respond to intracellular bacterial infection, through cytoskeletal rearrangement and membrane remodeling. By learning how bacterial effector proteins drive large-scale cellular reorganization, we aim to expose the regulatory mechanisms that govern cellular architecture more generally — and to carry those measurements into the intestinal epithelium, where the same effectors act on a barrier rather than on an isolated cell.

## Methods and tools we build

A measurement is only a readout of mechanism if it can be shown to be correct. That principle runs through the lab's methods work, from [EMRinger](https://github.com/fraser-lab/EMRinger) — which measures Coulomb potential around modeled side chains to validate backbone placement in cryo-EM models, and has become a standard benchmark for modeling and refinement software — through the surface morphometrics work above.

We are committed to releasing our tools openly, and to building them so that other groups can ask these questions of their own data. Our software is available on [GitHub](https://github.com/GrotjahnLab/surface_morphometrics), and our published work is listed on the [publications](/publications) page.
