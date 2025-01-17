---
title: "MidSurfer: A Parameter-Free Approach for Mid-Surface Extraction from Segmented Volumetric Data" # Required
authors: "Boneš E<sup>†</sup>, Khan D<sup>†</sup>, Bohak C, **Barad BA**, Grotjahn DA, Viola I, Theußl T" # Bold name of labmembers by wrapping with ** **
journal: "arXiv" # Full Journal name or bioRxiv
pub_date: "2024-04-07" # YYYY-MM-DD
image: 'img/pub/2024_bones.webp' # Use CDN!
pmid: 'TBD' # Pubmed ID - can put "TBD"
# pmcid: 'PMC4589481' # Optional Pubmed Central ID
arxiv: '2405.19339' # Optional biorxiv id - the full id used in the doi, which is formatted YYYY.MM.DD.ID on new preprints
pdf: pdf/2024_bones.pdf # Use CDN!
# pdbs: # Optional, can put as many as you want
# - 3J9I
# emdbs: #Optional, can put as many as you want
# - 5623
# paired_maps_and_models: # optional
# - pdb: 3J9J
#   emdb: 5623
# github: # Optional, can put as many as you want
# - code: EMRinger
#   url: fraser-lab/EMRinger
# links: # Optional, can put as many as you want
# - name: Fraser Lab
#   url: https://fraserlab.com
# - name: Paper Submission Celebration Photo
#   url: https://twitter.com/fraser_lab/status/562799246689460224
publish: true # Switch to true when ready!
---

n the field of volumetric data processing and analysis, extracting mid-surfaces from thinly bounded compartments is crucial for tasks such as surface area estimation and accurate modeling of biological structures, yet it has lacked a standardized approach. To bridge this gap, we introduce MidSurfer--a novel parameter-free method for extracting mid-surfaces from segmented volumetric data. Our method produces smooth, uniformly triangulated meshes that accurately capture the structural features of interest. The process begins with the Ridge Field Transformation step that transforms the segmented input data, followed by the Mid-Polyline Extraction Algorithm that works on individual volume slices. Based on the connectivity of components, this step can result in either single or multiple polyline segments that represent the structural features. These segments form a coherent series across the volume, creating a backbone of regularly distributed points on each slice that represents the mid-surface. Subsequently, we employ a Polyline Zipper Algorithm for triangulation that connects these polyline segments across neighboring slices, yielding a detailed triangulated mid-surface mesh. Our findings demonstrate that this method surpasses previous techniques in versatility, simplicity of use, and accuracy. Our approach is now publicly available as a plugin for ParaView, a widely-used multi-platform tool for data analysis and visualization, and can be found at [this https URL](https://github.com/kaust-vislab/MidSurfer) .