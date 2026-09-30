---
title: "Tomogram Reconstruction and Gold Fiducial Removal with WarpTools, Etomo, and Fidder" # Required
authors: "Garrels C, **Barad BA**, Reichow SL" # Bold name of labmembers by wrapping with ** **
journal: "protocols.io" # Full Journal name or bioRxiv
pub_date: "2025-06-03" # YYYY-MM-DD - v4, latest version
image: 'img/pub/2025_garrels.webp' # Use CDN! PLACEHOLDER - needs upload
pmid: # Pubmed ID - can put "TBD"
# pmcid: 'PMC4589481' # Optional Pubmed Central ID
pdf: 'pdf/2025_garrels.pdf' # Use CDN! PLACEHOLDER - needs upload
# pdbs: # Optional, can put as many as you want
# - 3J9I
# emdbs: #Optional, can put as many as you want
# - 5623
github: # Optional, can put as many as you want
- description: fidder
  url: teamtomo/fidder
links: # Optional, can put as many as you want
- name: protocols.io - 10.17504/protocols.io.6qpvr8qbblmk/v4
  url: https://doi.org/10.17504/protocols.io.6qpvr8qbblmk/v4
publish: true # Switch to true when ready!
---

While gold nanoparticle fiducials greatly improve tilt-series alignment in cryo-electron tomography data, they can cause artifacts during later image processing steps. We present a workflow for high-quality fiducial removal using fidder, an open-source python package. This protocol demonstrates how to flexibly incorporate fidder into tomogram reconstruction using Warp and Etomo.
