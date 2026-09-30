---
title: "Surface morphometrics reveals local membrane thickness variation in organellar subcompartments" # Required
authors: "Medina M<sup>†</sup>, Chang YT<sup>†</sup>, Rahmani H, **Frank M**, Khan Z, Fuentes D, Heberle FA, Waxham MN, **Barad BA<sup>✉</sup>**, Grotjahn DA<sup>✉</sup>" # Bold name of labmembers by wrapping with ** **
journal: "Journal of Cell Biology" # Full Journal name or bioRxiv
pub_date: "2026-03-02" # YYYY-MM-DD
image: 'img/pub/2025_medina_chang.webp' # Use CDN!
pmid: '41474626' # Pubmed ID - can put "TBD"
pmcid: 'PMC12755900' # Optional Pubmed Central ID
biorxiv: '2025.04.30.651574' # Optional biorxiv id - the full id used in the doi, which is formatted YYYY.MM.DD.ID on new preprints
pdf: 'pdf/2026_medina.pdf' # Use CDN! Published JCB version - see pdf_upload/
# pdbs: # Optional, can put as many as you want
# - 3J9I
# emdbs: #Optional, can put as many as you want
# - 5623
# paired_maps_and_models: # optional
# - pdb: 3J9J
#   emdb: 5623
github: # Optional, can put as many as you want
- description: Surface Morphometrics Toolkit
  url: GrotjahnLab/surface_morphometrics
# links: # Optional, can put as many as you want
# - name: Fraser Lab
#   url: https://fraserlab.com
# - name: Paper Submission Celebration Photo
#   url: https://twitter.com/fraser_lab/status/562799246689460224
publish: true # Switch to true when ready!
---

Lipid bilayers form the basis of organellar architecture, structure, and compartmentalization in the cell. Decades of biophysical, biochemical, and imaging studies on purified or in vitro-reconstituted liposomes have shown that variations in lipid composition influence the physical properties of membranes, such as thickness and curvature. However, similar studies characterizing these membrane properties within the native cellular context have remained technically challenging. Recent advancements in cellular cryo-electron tomography (cryo-ET) imaging enable high-resolution, three-dimensional views of native organellar membrane architecture preserved in near-native conditions. We previously developed a "Surface Morphometrics" pipeline that generates surface mesh reconstructions to model and quantify cellular membrane ultrastructure from cryo-ET data. Here, we expand this pipeline to measure the distance between the phospholipid head groups of the membrane bilayer as a readout of membrane thickness. Using this approach, we demonstrate thickness variations both within and between distinct organellar membranes. We show that organellar membrane thickness positively correlates with other features, such as membrane curvedness, in cells. Further, we show that subcompartments of the mitochondrial inner membrane exhibit varying membrane thicknesses that are independent of whether the mitochondria are in fragmented or elongated networks. We also demonstrate that our technique, when applied to three-dimensional data, yields results that match existing measurements obtained from two-dimensional data of in vitro samples. Finally, we demonstrate that large membrane-associated macromolecular complexes exhibit distinct density profiles that correlate with local variations in membrane thickness. Overall, our updated Surface Morphometrics pipeline provides a framework for investigating how changes in membrane composition in various cellular and disease contexts affect organelle ultrastructure and function.
