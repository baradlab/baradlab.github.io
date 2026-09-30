---
title: Research in the Barad Lab
layout: parallax
group: research
banner: img/site/banners/square_wireframe.webp
---

# Research

We use cellular cryo-electron tomography (cryoET) to look inside cells and see their membranes directly — no fixation, no stains, no labels. Freeze a cell fast enough and everything stays where it was: membranes, filaments, and protein complexes, all still in place. We find that genuinely remarkable, and we spend our time trying to make the most of it.

The question we keep coming back to is how barrier tissues — the sheets of cells that hold an organism apart from the world — are put together at this scale, and what happens to them when something goes wrong.

Answering that takes two fairly different skill sets, and we do both under one roof. At the bench we run the whole pipeline that gets a cell into the microscope intact: vitrification, cryo-focused ion beam (cryo-FIB) milling, and correlative fluorescence microscopy. At the computer we build the methods that turn a tomogram into numbers you can reason about. Most people here pick up some of each, and projects can lean toward whichever end you find more interesting.

## The gut barrier, and what gets through it

The intestinal epithelium is a remarkably good barrier, and it is one that enteric pathogens have to breach, subvert, or rebuild in order to get anywhere. That makes infection a great way in: the insult is defined, we control when it happens, and the membrane remodeling that follows is exactly the kind of thing cryoET is good at catching.

Longer term, we would love to look at barrier disease in tissue that came from a patient, rather than inferring it from simplified models — imaging organoid and primary-cell models to look for structural changes in the gut barrier that other methods cannot see. It is the hardest thing on our list and the one we are most excited about.

OHSU is a good place to try it. There is real depth here in host–pathogen interactions and chemical biology, and between the Pacific Northwest Cryo-EM Center and the cryo-FIB and cryo-fluorescence instruments on campus, we can prepare tricky samples and collect tomographic data locally instead of shipping them somewhere else.

## Measuring membranes, not just describing them

CryoET gives you a three-dimensional view inside a cell, with everything preserved in vitreous ice. Pulling high-resolution protein structures out of tomograms has come a long way; measuring the *shape* of the cell around those proteins has had much less attention, and that is what lets you connect a structure to its context.

So we build tools for it. The [Surface Morphometrics Toolkit](https://github.com/GrotjahnLab/surface_morphometrics) turns membrane segmentations into quantified mesh models, so a change in membrane geometry becomes something you can measure and put an error bar on rather than something you squint at. It reconstructs open surfaces from cellular membrane segmentations and characterizes curvature, thickness, and filament interactions. Other groups have picked it up too, and it has been used to look at how mitochondrial fission is organized by cytoskeletal elements, how cytoplasmic ribosomes on mitochondria change the membrane around them, and how prohibitin complexes sit in distinct membrane microdomains.

What we are working on now is going from measuring membrane *shape* to working out which molecules produce it — using model-guided analysis of tomogram density to read membrane composition, membrane-associated protein structure, and cytoskeletal organization out of the same dataset. There is a lot of open ground here, and it is a good place to start a project.

## What infection does to a membrane

Pathogens are extraordinary cell biologists, and watching what they do to host membranes is both a good question in itself and how we get at the gut barrier.

Working with the Överby and Carlson labs at Umeå University, we applied the toolkit to cells infected with Langat virus, a tick-borne flavivirus that stands in for its more dangerous relatives, and measured how membranes are remodeled at viral replication organelles. We could see how genome replication, virion budding, and particle maturation are arranged relative to each other, and we found a membrane thickening nobody had described before — one that does not track with RNA replication, and is more likely tied to making nonstructural proteins.

We also use cryoET to watch how mammalian cells respond to intracellular bacterial infection, through cytoskeletal rearrangement and membrane remodeling. Bacterial effectors drive cellular reorganization on a scale that is hard to miss, and understanding how they do it tells us something general about how cells govern their own architecture. The next step is taking those measurements into the intestinal epithelium, where the same effectors are acting on a barrier instead of a single cell.

## Tools we build and give away

We care a lot about whether a measurement is actually right, because otherwise it is not telling you anything about mechanism. That thread runs from [EMRinger](https://github.com/fraser-lab/EMRinger), which checks whether a protein backbone has been modeled correctly into a cryo-EM map, through to the membrane work above.

We release our software openly and try to build it so other people can ask these questions of their own data. Our code is on [GitHub](https://github.com/GrotjahnLab/surface_morphometrics), and our papers are on the [publications](/publications) page.

## Come work on this with us

Much of what we want to do has not been done yet, which means there is room for someone to take a piece of it and make it theirs. If you like the idea of learning to freeze cells, mill them with an ion beam, and then write the code that makes sense of what comes out — or if you are strong at one of those and curious about the other — we would like to hear from you.

We do not always have a position formally advertised, and that has never been the real constraint. Take a look at [joining the lab](/join) and get in touch.
