<div align="center">

<p align="center">
  <img src="figures/DNA-Foundation-Models.png" alt="DNA Foundation Models logo" width="180">
</p>

<h1 align="center">Awesome DNA Foundation Models</h1>

### What Makes a DNA Foundation Model Foundational?

[![Paper](https://img.shields.io/badge/Paper-coming_soon-64748b)](#citation)
[![arXiv](https://img.shields.io/badge/arXiv-coming_soon-b31b1b.svg)](#)
[![PDF](https://img.shields.io/badge/PDF-local_draft-2563eb)](../latex/main.pdf)
[![Project Page](https://img.shields.io/badge/Project_Page-coming_soon-0f766e)](#)
[![Contributions](https://img.shields.io/badge/Contributions-welcome-16a34a)](#contributing)

**A curated survey repository for DNA foundation models, genomic pretraining corpora, benchmarks, and evidence criteria for sequence-to-function generalization.**

</div>

This repository accompanies our survey on **DNA Foundation Models (DNAFMs)**, an emerging class of pretrained genomic sequence models for learning sequence representations, regulatory signals, and sequence-to-function relationships. We will keep this repo continuously updated as the field evolves.

- 🧬 **A systematic DNAFM survey**, covering model architectures, pretraining objectives, tokenization strategies, training corpora, benchmark protocols, and downstream biological tasks.
- 🧭 **A foundation-capability framework**, asking what makes a DNA model genuinely foundational beyond parameter scale, context length, and local fine-tuning scores.
- 🔬 **Evidence criteria included**: long-range regulatory use, DNA-specific biological priors, perturbational generalization, evolutionary supervision, and modular biological AI systems.
- 📚 **Curated resources included**: representative DNA foundation models, pretraining corpus categories, and evaluation benchmarks.
- 🤝 **Community-driven**: found a missing model, benchmark, dataset, paper link, or correction? Feel free to open an issue or submit a pull request.

<p align="center">
  <img src="figs/fig1.png" alt="Operational framework for foundational capability in DNA foundation models" width="100%">
</p>

## News

- **[2026-07-09]** Initial README release with the review framework, model landscape, corpus taxonomy, and benchmark map.

## Contents

- [Tag Legend](#tag-legend)
- [DNA Foundation Models](#dna-foundation-models)
- [Pretraining Corpora](#pretraining-corpora)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Contributing](#contributing)
- [Citation](#citation)
- [Acknowledgements](#acknowledgements)

## Tag Legend

### Model design tags

- ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) causal language modeling
- ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) masked language modeling
- ![AR+MLM](https://img.shields.io/badge/Objective-AR%2BMLM-9333ea) hybrid autoregressive and masked objectives
- ![Diffusion](https://img.shields.io/badge/Objective-Diffusion-db2777) discrete diffusion or diffusion-style sequence modeling
- ![Contrastive](https://img.shields.io/badge/Objective-Contrastive-0891b2) species-aware or representation contrast
- ![Auxiliary](https://img.shields.io/badge/Objective-Auxiliary-475569) additional supervised or biological objectives

### Biological scope tags

- ![Human/Eukaryotic](https://img.shields.io/badge/Corpus-Human%2FEukaryotic-15803d) human or eukaryotic reference-centered data
- ![Multi-species](https://img.shields.io/badge/Corpus-Multi--species-0f766e) genomes across multiple species
- ![Prokaryotic/Phage](https://img.shields.io/badge/Corpus-Prokaryotic%2FPhage-ca8a04) bacterial, archaeal, or phage genomes
- ![Metagenomic](https://img.shields.io/badge/Corpus-Metagenomic-854d0e) metagenomic or environmental sequences
- ![Viral/Mobile](https://img.shields.io/badge/Corpus-Viral%2FMobile-b91c1c) viruses, plasmids, phages, or mobile elements
- ![Plant](https://img.shields.io/badge/Corpus-Plant--specific-65a30d) plant-focused genomes or plant regulatory sequence data
- ![Cross-domain](https://img.shields.io/badge/Corpus-Cross--domain-4338ca) bacteria, archaea, eukaryotes, viruses, organelles, and metagenomes

### Evidence tags

- ![Long-range](https://img.shields.io/badge/Evidence-Long--range-0f766e) enhancer-gene, eQTL, chromatin contact, TAD, or distal variant evidence
- ![Biological priors](https://img.shields.io/badge/Evidence-Biological_priors-2563eb) reverse complementarity, coordinates, coding frame, conservation, cell state, or 3D genome priors
- ![Perturbation](https://img.shields.io/badge/Evidence-Perturbation-b91c1c) variant effect, mutagenesis, CRISPR, MPRA, eQTL, or design validation
- ![OOD](https://img.shields.io/badge/Evidence-OOD_splits-7c2d12) chromosome, species, gene, cell-type, variant-class, or clade-level splits

## DNA Foundation Models

The table below follows the model landscape summarized in the manuscript. Official paper, code, and model links are shown only when verified; unavailable resources are omitted.

| Model | Model Type | Pretraining Corpus | Released | Links |
| --- | --- | --- | --- | --- |
| Evo 1 | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![OpenGenome](https://img.shields.io/badge/Corpus-OpenGenome-ca8a04) | 2024.02 | 📄 [Paper](https://www.science.org/doi/10.1126/science.ado9336)<br>💻 [Code](https://github.com/evo-design/evo)<br>📘 [Tutorial](https://colab.research.google.com/github/evo-design/evo/blob/main/scripts/hello_evo.ipynb)<br>🤗 [Model](https://huggingface.co/togethercomputer/evo-1-131k-base) |
| Evo 1.5 | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![OpenGenome](https://img.shields.io/badge/Corpus-OpenGenome-ca8a04) | 2024.12 | 📄 [Paper](https://www.nature.com/articles/s41586-025-09749-7)<br>💻 [Code](https://github.com/evo-design/evo)<br>📘 [Tutorial](https://colab.research.google.com/github/evo-design/evo/blob/main/scripts/hello_evo.ipynb)<br>🤗 [Model](https://huggingface.co/evo-design/evo-1.5-8k-base) |
| Evo 2 | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![OpenGenome2](https://img.shields.io/badge/Corpus-OpenGenome2-4338ca) | 2025.02 | 📄 [Paper](https://www.nature.com/articles/s41586-026-10176-5)<br>💻 [Code](https://github.com/ArcInstitute/evo2)<br>📘 [Tutorial](https://github.com/ArcInstitute/evo2/tree/main/notebooks)<br>🤗 [Model](https://huggingface.co/arcinstitute/evo2_7b) |
| Nucleotide Transformer v1 | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![GRCh38, 1000G, multi-species](https://img.shields.io/badge/Corpus-GRCh38%2C_1000G%2C_multi--species-0f766e) | 2023.01 | 📄 [Paper](https://www.nature.com/articles/s41592-024-02523-z)<br>💻 [Code](https://github.com/instadeepai/nucleotide-transformer)<br>📘 [Tutorial](https://github.com/instadeepai/nucleotide-transformer/blob/main/docs/nucleotide_transformer.md)<br>🤗 [Model](https://huggingface.co/collections/InstaDeepAI/nucleotide-transformer) |
| Nucleotide Transformer v2 | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![850 species genomes](https://img.shields.io/badge/Corpus-850_species_genomes-0f766e) | 2024.01 | 📄 [Paper](https://www.nature.com/articles/s41592-024-02523-z)<br>💻 [Code](https://github.com/instadeepai/nucleotide-transformer)<br>📘 [Tutorial](https://github.com/instadeepai/nucleotide-transformer/blob/main/docs/nucleotide_transformer.md)<br>🤗 [Model](https://huggingface.co/InstaDeepAI/nucleotide-transformer-v2-500m-multi-species) |
| Nucleotide Transformer v3 | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![OpenGenome2](https://img.shields.io/badge/Corpus-OpenGenome2-4338ca) | 2025.12 | 📄 [Paper](https://www.biorxiv.org/content/10.64898/2025.12.22.695963v1)<br>💻 [Code](https://github.com/instadeepai/nucleotide-transformer)<br>📘 [Tutorial](https://github.com/instadeepai/nucleotide-transformer/blob/main/docs/nucleotide_transformer_v3.md)<br>🤗 [Model](https://huggingface.co/InstaDeepAI/NTv3_650M_pre) |
| Caduceus | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Human reference genome](https://img.shields.io/badge/Corpus-Human_reference_genome-15803d) | 2024.03 | 📄 [Paper](https://proceedings.mlr.press/v235/schiff24a.html)<br>💻 [Code](https://github.com/kuleshov-group/caduceus)<br>🤗 [Model](https://huggingface.co/kuleshov-group/caduceus-ps_seqlen-131k_d_model-256_n_layer-16) |
| DNABERT | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Human reference genome](https://img.shields.io/badge/Corpus-Human_reference_genome-15803d) | 2020.09 | 📄 [Paper](https://doi.org/10.1093/bioinformatics/btab083)<br>💻 [Code](https://github.com/jerryji1993/DNABERT)<br>📘 [Tutorial](https://github.com/jerryji1993/DNABERT/tree/master/examples)<br>🤗 [Model](https://huggingface.co/zhihan1996/DNA_bert_6) |
| DNABERT-2 | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![135 species genomes](https://img.shields.io/badge/Corpus-135_species_genomes-0f766e) | 2023.06 | 📄 [Paper](https://arxiv.org/abs/2306.15006)<br>💻 [Code](https://github.com/MAGICS-LAB/DNABERT_2)<br>📘 [Tutorial](https://github.com/MAGICS-LAB/DNABERT_2#4-quick-start)<br>🤗 [Model](https://huggingface.co/zhihan1996/DNABERT-2-117M) |
| DNABERT-S | ![Contrastive](https://img.shields.io/badge/Objective-Contrastive-0891b2) | ![GenBank multi-species](https://img.shields.io/badge/Corpus-GenBank_multi--species-0f766e) | 2024.02 | 📄 [Paper](https://arxiv.org/abs/2402.08777)<br>💻 [Code](https://github.com/MAGICS-LAB/DNABERT_S)<br>📘 [Tutorial](https://github.com/MAGICS-LAB/DNABERT_S#4-quick-start)<br>🤗 [Model](https://huggingface.co/zhihan1996/DNABERT-S) |
| HyenaDNA | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Human reference genome](https://img.shields.io/badge/Corpus-Human_reference_genome-15803d) | 2023.06 | 📄 [Paper](https://arxiv.org/abs/2306.15794)<br>💻 [Code](https://github.com/HazyResearch/hyena-dna)<br>📘 [Tutorial](https://colab.research.google.com/drive/1wyVEQd4R3HYLTUOXEEQmp_I8aNC_aLhL?usp=sharing)<br>🤗 [Model](https://huggingface.co/LongSafari/hyenadna-large-1m-seqlen-hf) |
| Genos | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Pangenome + mammalian](https://img.shields.io/badge/Corpus-Pangenome_%2B_mammalian-2563eb) | 2025.10 | 📄 [Paper](https://doi.org/10.1093/gigascience/giaf132)<br>💻 [Code](https://github.com/BGI-HangzhouAI/Genos)<br>📘 [Tutorial](https://github.com/BGI-HangzhouAI/Genos/tree/main/Notebooks)<br>🤗 [Model](https://huggingface.co/collections/BGI-HangzhouAI/genos) |
| OmniReg-GPT | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Human T2T v2 regulatory](https://img.shields.io/badge/Corpus-Human_T2T_v2_regulatory-15803d) | 2025.07 | 📄 [Paper](https://doi.org/10.1038/s41467-025-65066-7)<br>💻 [Code](https://github.com/wawpaopao/OmniReg-GPT)<br>📘 [Tutorial](https://github.com/wawpaopao/OmniReg-GPT/tree/main/example)<br>🤗 [Model](https://zenodo.org/records/14893616) |
| GENA-LM | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Human T2T, multi-species](https://img.shields.io/badge/Corpus-Human_T2T%2C_multi--species-0f766e) | 2023.06 | 📄 [Paper](https://doi.org/10.1093/nar/gkae1310)<br>💻 [Code](https://github.com/AIRI-Institute/GENA_LM)<br>📘 [Tutorial](https://github.com/AIRI-Institute/GENA_LM/tree/main/examples)<br>🤗 [Model](https://huggingface.co/AIRI-Institute/gena-lm-bigbird-base-t2t) |
| GROVER | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Human reference genome](https://img.shields.io/badge/Corpus-Human_reference_genome-15803d) | 2023.07 | 📄 [Paper](https://doi.org/10.1038/s42256-024-00872-0) |
| GenomeOcean | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Metagenomics, microbial](https://img.shields.io/badge/Corpus-Metagenomics%2C_microbial-854d0e) | 2025.01 | 📄 [Paper](https://www.biorxiv.org/content/10.1101/2025.01.30.635558v2)<br>💻 [Code](https://github.com/jgi-genomeocean/genomeocean)<br>📘 [Tutorial](https://github.com/jgi-genomeocean/genomeocean/tree/main/examples)<br>🤗 [Model](https://huggingface.co/pGenomeOcean/GenomeOcean-4B) |
| GENERator v1 | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![RefSeq eukaryotic](https://img.shields.io/badge/Corpus-RefSeq_eukaryotic-15803d) | 2025.02 | 📄 [Paper](https://arxiv.org/abs/2502.07272)<br>💻 [Code](https://github.com/GenerTeam/GENERator)<br>📘 [Tutorial](https://github.com/GenerTeam/GENERator#-quick-start)<br>🤗 [Model](https://huggingface.co/GenerTeam/GENERator-eukaryote-3b-base) |
| GENERator v2 | ![CLM + auxiliary](https://img.shields.io/badge/Objective-CLM_%2B_auxiliary-475569) | ![RefSeq eukaryotic + prokaryotic](https://img.shields.io/badge/Corpus-RefSeq_eukaryotic_%2B_prokaryotic-ca8a04) | 2026.01 | 📄 [Paper](https://www.biorxiv.org/content/10.64898/2026.01.27.702015v1)<br>💻 [Code](https://github.com/GenerTeam/GENERator)<br>📘 [Tutorial](https://github.com/GenerTeam/GENERator#-quick-start)<br>🤗 [Model](https://huggingface.co/GenerTeam/GENERator-v2-prokaryote-3b-base) |
| AIDO.DNA | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![796 species genomes](https://img.shields.io/badge/Corpus-796_species_genomes-0f766e) | 2024.12 | 📄 [Paper](https://doi.org/10.1101/2024.12.01.625444)<br>💻 [Code](https://github.com/genbio-ai/ModelGenerator)<br>📘 [Tutorial](https://github.com/genbio-ai/AIDO-Foundations-Tutorials)<br>🤗 [Model](https://huggingface.co/genbio-ai/AIDO.DNA-7B) |
| LucaOne | ![MLM + supervised](https://img.shields.io/badge/Objective-MLM_%2B_supervised-475569) | ![RefSeq + UniProt](https://img.shields.io/badge/Corpus-RefSeq_%2B_UniProt-4338ca) | 2024.05 | 📄 [Paper](https://www.nature.com/articles/s42256-025-01044-4)<br>💻 [Code](https://github.com/LucaOne/LucaOne)<br>📘 [Tutorial](https://github.com/LucaOne/LucaOne#6-embedding-inference)<br>🤗 [Model](https://huggingface.co/collections/LucaGroup/lucaone) |
| LucaVirus | ![MLM + supervised](https://img.shields.io/badge/Objective-MLM_%2B_supervised-475569) | ![OpenVirus viral sequences](https://img.shields.io/badge/Corpus-OpenVirus_viral_sequences-b91c1c) | 2025.06 | 📄 [Paper](https://www.biorxiv.org/content/10.1101/2025.06.14.659722v1)<br>💻 [Code](https://github.com/LucaOne/LucaVirus)<br>🤗 [Model](https://huggingface.co/collections/LucaGroup/lucavirus) |
| GPN | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Arabidopsis + Brassicales](https://img.shields.io/badge/Corpus-Arabidopsis_%2B_Brassicales-65a30d) | 2022.08 | 📄 [Paper](https://doi.org/10.1073/pnas.2311219120)<br>💻 [Code](https://github.com/songlab-cal/gpn)<br>📘 [Tutorial](https://github.com/songlab-cal/gpn/blob/main/examples/ss/basic_example.ipynb)<br>🤗 [Model](https://huggingface.co/songlab/gpn-brassicales) |
| GPN-MSA | ![MSA-based MLM](https://img.shields.io/badge/Objective-MSA--based_MLM-2563eb) | ![Multi-species WGA](https://img.shields.io/badge/Corpus-Multi--species_WGA-0f766e) | 2023.10 | 📄 [Paper](https://www.nature.com/articles/s41587-024-02511-w)<br>💻 [Code](https://github.com/songlab-cal/gpn)<br>📘 [Tutorial](https://github.com/songlab-cal/gpn/blob/main/examples/msa/basic_example.ipynb)<br>🤗 [Model](https://huggingface.co/songlab/gpn-msa-sapiens) |
| megaDNA | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Phage genomes](https://img.shields.io/badge/Corpus-Phage_genomes-ca8a04) | 2023.12 | 📄 [Paper](https://www.biorxiv.org/content/10.1101/2023.12.18.572218v3)<br>💻 [Code](https://github.com/lingxusb/megaDNA)<br>📘 [Tutorial](https://github.com/lingxusb/megaDNA/blob/main/notebook/megaDNA_generate.ipynb)<br>🤗 [Model](https://huggingface.co/lingxusb/megaDNA_updated) |
| AgroNT | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![48 plant genomes](https://img.shields.io/badge/Corpus-48_plant_genomes-65a30d) | 2023.10 | 📄 [Paper](https://www.nature.com/articles/s42003-024-06465-2)<br>💻 [Code](https://github.com/instadeepai/nucleotide-transformer)<br>📘 [Tutorial](https://github.com/instadeepai/nucleotide-transformer/blob/main/docs/agro_nucleotide_transformer.md)<br>🤗 [Model](https://huggingface.co/collections/InstaDeepAI/agro-nucleotide-transformer-65b25c077cd0069ad6f6d344) |
| ProkBERT | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![NCBI RefSeq microbial](https://img.shields.io/badge/Corpus-NCBI_RefSeq_microbial-ca8a04) | 2024.01 | 📄 [Paper](https://www.frontiersin.org/articles/10.3389/fmicb.2023.1331233)<br>💻 [Code](https://github.com/nbrg-ppcu/prokbert)<br>📘 [Tutorial](https://github.com/nbrg-ppcu/prokbert/blob/main/examples/Inference.ipynb)<br>🤗 [Model](https://huggingface.co/neuralbioinfo/prokbert-mini) |
| SpeciesLM | ![Species-aware MLM](https://img.shields.io/badge/Objective-Species--aware_MLM-0891b2) | ![806 fungal genomes](https://img.shields.io/badge/Corpus-806_fungal_genomes-0f766e) | 2023.01 | 📄 [Paper](https://doi.org/10.1101/2023.01.26.525670)<br>💻 [Code](https://github.com/gagneurlab/SpeciesLM)<br>📘 [Tutorial](https://github.com/gagneurlab/SpeciesLM/blob/main/ModelUsage.ipynb)<br>🤗 [Model](https://huggingface.co/gagneurlab/SpeciesLM) |
| Mistral-DNA | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Human, bacterial, yeast, viral](https://img.shields.io/badge/Corpus-Human%2C_bacterial%2C_yeast%2C_viral-4338ca) | 2024 | 💻 [Code](https://github.com/raphaelmourad/Mistral-DNA)<br>📘 [Tutorial](https://github.com/raphaelmourad/Mistral-DNA#prediction-mutation-effect-with-zero-shot-learning-using-the-pretrained-model)<br>🤗 [Model](https://huggingface.co/RaphaelMourad/Mistral-DNA-v1-422M-hg38) |
| PlantCAD | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![16 angiosperm genomes](https://img.shields.io/badge/Corpus-16_angiosperm_genomes-65a30d) | 2024.06 | 📄 [Paper](https://doi.org/10.1073/pnas.2421738122)<br>💻 [Code](https://github.com/plantcad/plantcad)<br>📘 [Tutorial](https://github.com/plantcad/plantcad/blob/main/notebooks/examples.ipynb)<br>🤗 [Model](https://huggingface.co/collections/kuleshov-group/plantcaduceus-512bp-len-665a229ee098db706a55e44a) |
| PlantCAD2 | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![65 angiosperm genomes](https://img.shields.io/badge/Corpus-65_angiosperm_genomes-65a30d) | 2025.08 | 📄 [Paper](https://www.biorxiv.org/content/10.1101/2025.08.27.672609v3)<br>💻 [Code](https://github.com/plantcad/plantcad)<br>📘 [Tutorial](https://github.com/plantcad/plantcad/blob/main/docs/PlantCAD2-overview.md)<br>🤗 [Model](https://huggingface.co/collections/kuleshov-group/plantcad2-67e437e241a382671371a572) |
| HybriDNA | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Large-scale DNA corpus](https://img.shields.io/badge/Corpus-Large--scale_DNA_corpus-64748b) | 2025.02 | 📄 [Paper](https://arxiv.org/abs/2502.10807)<br>🤗 [Model](https://huggingface.co/Mishamq/HybriDNA-7B) |
| Gene42 | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Human genome](https://img.shields.io/badge/Corpus-Human_genome-15803d) | 2025.03 | 📄 [Paper](https://arxiv.org/abs/2503.16565)<br>🤗 [Model](https://huggingface.co/inceptionai) |
| MxDNA | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Human reference + benchmark](https://img.shields.io/badge/Corpus-Human_reference_%2B_benchmark-15803d) | 2024.12 | 📄 [Paper](https://doi.org/10.52202/079017-2112)<br>💻 [Code](https://github.com/qiaoqiaoLF/MxDNA) |
| METAGENE-1 | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Wastewater metagenomics](https://img.shields.io/badge/Corpus-Wastewater_metagenomics-854d0e) | 2025.01 | 📄 [Paper](https://doi.org/10.32388/fmepo7)<br>💻 [Code](https://github.com/metagene-ai/metagene-pretrain)<br>📘 [Tutorial](https://github.com/metagene-ai/metagene-pretrain/tree/main/train/tutorials)<br>🤗 [Model](https://huggingface.co/metagene-ai/METAGENE-1) |
| Life-Code | ![MLM + auxiliary](https://img.shields.io/badge/Objective-MLM_%2B_auxiliary-475569) | ![DNA + RNA + protein](https://img.shields.io/badge/Corpus-DNA_%2B_RNA_%2B_protein-4338ca) | 2025.02 |  |
| UKBioBERT | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![UK Biobank variants](https://img.shields.io/badge/Corpus-UK_Biobank_variants-2563eb) | 2025.02 |  |
| JanusDNA | ![AR + MLM](https://img.shields.io/badge/Objective-AR_%2B_MLM-9333ea) | ![Large-scale DNA corpus](https://img.shields.io/badge/Corpus-Large--scale_DNA_corpus-64748b) | 2025.05 | 📄 [Paper](https://arxiv.org/abs/2505.17257)<br>💻 [Code](https://github.com/Qihao-Duan/JanusDNA)<br>🤗 [Model](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi%3A10.7910%2FDVN%2FHDT0RN&version=DRAFT) |
| Omni-DNA | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![DNA + multimodal tokens](https://img.shields.io/badge/Corpus-DNA_%2B_multimodal_tokens-4338ca) | 2025.02 | 📄 [Paper](https://arxiv.org/abs/2502.03499)<br>💻 [Code](https://github.com/Zehui127/Omni-DNA)<br>📘 [Tutorial](https://github.com/Zehui127/Omni-DNA#examples)<br>🤗 [Model](https://huggingface.co/collections/zehui127/omni-dna-67a2230c352d4fd8f4d1a4bd) |
| LOGO | ![MLM](https://img.shields.io/badge/Objective-MLM-2563eb) | ![Human hg19](https://img.shields.io/badge/Corpus-Human_hg19-15803d) | 2021.08 |  |
| DNAGPT | ![CLM + auxiliary](https://img.shields.io/badge/Objective-CLM_%2B_auxiliary-475569) | ![Mammalian DNA](https://img.shields.io/badge/Corpus-Mammalian_DNA-15803d) | 2023.07 | 📄 [Paper](https://www.biorxiv.org/content/10.1101/2023.07.11.548628v2)<br>💻 [Code](https://github.com/TencentAILabHealthcare/DNAGPT)<br>📘 [Tutorial](https://github.com/TencentAILabHealthcare/DNAGPT#example)<br>🤗 [Model](https://github.com/TencentAILabHealthcare/DNAGPT#download-pre-trained-weights) |
| ENBED | ![MLM + denoising](https://img.shields.io/badge/Objective-MLM_%2B_denoising-475569) | ![NCBI RefSeq multi-species](https://img.shields.io/badge/Corpus-NCBI_RefSeq_multi--species-0f766e) | 2023.11 | 📄 [Paper](https://doi.org/10.1093/bioadv/vbae117) |
| OmniNA | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Large-scale nucleotide](https://img.shields.io/badge/Corpus-Large--scale_nucleotide-4338ca) | 2024.01 | 📄 [Paper](https://doi.org/10.1101/2024.01.14.575543)<br>🤗 [Model](https://huggingface.co/XLS/OmniNA-1.7B) |
| regLM | ![CLM](https://img.shields.io/badge/Objective-CLM-7c3aed) | ![Yeast + human enhancers](https://img.shields.io/badge/Corpus-Yeast_%2B_human_enhancers-15803d) | 2023.10 | 📄 [Paper](https://www.biorxiv.org/content/10.1101/2024.02.14.580373v1)<br>💻 [Code](https://github.com/Genentech/regLM)<br>📘 [Tutorial](https://github.com/Genentech/regLM/blob/main/tutorials/tutorial.ipynb) |
| dnaHNet | ![Tokenizer-free CLM](https://img.shields.io/badge/Objective-Tokenizer--free_CLM-7c3aed) | ![Prokaryotic genomes](https://img.shields.io/badge/Corpus-Prokaryotic_genomes-ca8a04) | 2026.02 |  |
| D3LM | ![Discrete diffusion](https://img.shields.io/badge/Objective-Discrete_diffusion-db2777) | ![GRCh38, 1000G, multi-species](https://img.shields.io/badge/Corpus-GRCh38%2C_1000G%2C_multi--species-0f766e) | 2026.03 | 📄 [Paper](https://arxiv.org/abs/2603.01780)<br>🤗 [Model](https://huggingface.co/collections/Hengchang-Liu/d3lm) |


## Pretraining Corpora

Pretraining corpora are not just data sources; they define which biological regularities a model can access and which biases it may inherit.

| Representative sources | Data composition | Links |
| --- | --- | --- |
| GRCh38/hg38 | Human reference assembly used as the dominant coordinate system for reference-sequence pretraining and many human regulatory benchmarks. | 🌐 [NCBI Datasets](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000001405.40/)<br>🌐 [UCSC hg38](https://genome.ucsc.edu/cgi-bin/hgGateway?db=hg38) |
| T2T-CHM13 | Gapless telomere-to-telomere human assembly resolving centromeres, acrocentric short arms, segmental duplications, and other previously missing regions. | 🌐 [NCBI Datasets](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_009914755.1/) |
| hg19 | Legacy GRCh37/UCSC human reference widely used by older epigenomic annotations, regulatory datasets, and benchmark splits. | 🌐 [UCSC hg19](https://genome.ucsc.edu/cgi-bin/hgGateway?db=hg19) |
| mm10/mm39 | Mouse reference assemblies used for mammalian regulatory sequence modeling, mouse functional genomics tracks, and cross-species transfer. | 🌐 [UCSC mm10](https://genome.ucsc.edu/cgi-bin/hgGateway?db=mm10)<br>🌐 [UCSC mm39](https://genome.ucsc.edu/cgi-bin/hgGateway?db=mm39) |
| TAIR10 | Arabidopsis thaliana reference genome and gene annotation baseline for plant sequence-function datasets. | 🌐 [TAIR10 release](https://www.arabidopsis.org/download/index-auto.jsp?dir=%2Fdownload_files%2FGenes%2FTAIR10_genome_release) |
| 1000 Genomes Project | Phased human variants and haplotypes across global populations, enabling allele-specific or variant-aware sequence construction. | 🌐 [Project portal](https://www.internationalgenome.org/) |
| 3,202 high-coverage human genomes | High-depth 1000 Genomes GRCh38 call set with SNVs, indels, and structural variants for population-scale sequence variation. | 📦 [30x GRCh38 call set](https://www.internationalgenome.org/data-portal/data-collection/30x-grch38) |
| Human Pangenome Reference Consortium | Haplotype-resolved human pangenome assemblies and graph references capturing alternatives absent from a single linear reference. | 🌐 [Project portal](https://humanpangenome.org/) |
| Ensembl Genomes | Comparative genome and annotation resource for non-vertebrate eukaryotes, bacteria, plants, fungi, protists, and metazoa. | 🌐 [Portal](https://ensemblgenomes.org/) |
| NCBI RefSeq | Curated reference sequences and genome assemblies with standardised annotation across taxa. | 🌐 [RefSeq](https://www.ncbi.nlm.nih.gov/refseq/) |
| NCBI GenBank | Primary archival nucleotide sequence database containing submitted genomic sequences and assemblies before RefSeq curation. | 🌐 [GenBank](https://www.ncbi.nlm.nih.gov/genbank/) |
| Phytozome | JGI plant comparative genomics portal with plant genome assemblies, gene models, families, and functional annotations. | 🌐 [Portal](https://phytozome-next.jgi.doe.gov/) |
| OpenGenome | Evo pretraining corpus of prokaryotic and phage whole-genome sequences at single-nucleotide resolution. | 🤗 [Dataset](https://huggingface.co/datasets/LongSafari/open-genome) |
| NCBI RefSeq Bacteria/Archaea | Curated bacterial and archaeal assemblies and annotations used for microbial genome representation. | 🌐 [RefSeq prokaryotes](https://www.ncbi.nlm.nih.gov/refseq/about/prokaryotes/) |
| GenBank Prokaryotic Genomes | Broad submitted prokaryotic genome assemblies, including draft genomes and isolates with variable curation status. | 🌐 [NCBI Genome browser](https://www.ncbi.nlm.nih.gov/genome/browse#!/prokaryotes/) |
| IMG/VR | Viral genome catalogue from isolate and metagenomic data, useful for phage-inclusive microbial pretraining. | 🌐 [IMG/VR](https://img.jgi.doe.gov/vr/) |
| GenomeOcean corpus | Large-scale metagenomic assemblies used by GenomeOcean, emphasising microbial contigs from environmental and host-associated samples. | 💻 [Repository](https://github.com/jgi-genomeocean/genomeocean)<br>📄 [Paper](https://www.biorxiv.org/content/10.1101/2025.01.30.635558v2) |
| IMG/M | Integrated microbial genomes and microbiomes resource with metagenome projects, MAGs, isolate genomes, and functional annotations. | 🌐 [IMG/M](https://img.jgi.doe.gov/m/) |
| MGnify | EMBL-EBI metagenomics resource with assembled contigs, annotations, taxonomic profiles, and biome metadata. | 🌐 [MGnify](https://www.ebi.ac.uk/metagenomics/) |
| JGI Metagenome | JGI project portal for environmental sequencing projects and metagenomic datasets feeding IMG/M-style resources. | 🌐 [JGI portal](https://genome.jgi.doe.gov/portal/) |
| GOLD | Genome Online Database metadata catalogue for genome and metagenome projects, sampling environments, sequencing status, and study metadata. | 🌐 [GOLD](https://gold.jgi.doe.gov/) |
| Tara Oceans | Marine microbial, viral, and plankton omics samples from global ocean expeditions, available through ENA project records. | 📦 [ENA PRJEB402](https://www.ebi.ac.uk/ena/browser/view/PRJEB402) |
| NCBI Virus | Curated virus sequence portal with genome records, isolate metadata, host information, and sequence downloads. | 🌐 [NCBI Virus](https://www.ncbi.nlm.nih.gov/labs/virus/vssi/#/) |
| GenBank Viral | Submitted viral nucleotide records in GenBank, covering complete genomes, segments, isolates, and partial viral sequences. | 🌐 [GenBank](https://www.ncbi.nlm.nih.gov/genbank/) |
| IMG/VR | Viral isolate and metagenomic sequence catalogue supporting phage and environmental viral genome discovery. | 🌐 [IMG/VR](https://img.jgi.doe.gov/vr/) |
| PhagesDB | Community phage database with bacteriophage genomes, host annotations, clusters, and related metadata. | 🌐 [PhagesDB](https://phagesdb.org/) |
| PLSDB | Curated plasmid database containing plasmid sequences, host information, and metadata for mobile genetic element studies. | 🌐 [PLSDB](https://ccb-microbe.cs.uni-saarland.de/plsdb/) |
| OpenGenome2 | Cross-domain Evo 2 pretraining corpus spanning bacteria, archaea, eukaryotes, viruses, organelles, and metagenomic sequence. | 🤗 [Dataset](https://huggingface.co/datasets/arcinstitute/opengenome2) |

## Benchmarks and Evaluation

Benchmarks should be interpreted as biological probes. A strong local classification score does not by itself establish long-range regulatory modeling, perturbation response, or mechanistic sequence-to-function understanding.

| Benchmark | Year | Task type | Input length | Links |
| --- | --- | --- | --- | --- |
| Genomic Benchmarks | 2023.05 | Sequence classification | Hundreds bp to several kb | 📄 [Paper](https://doi.org/10.1186/s12863-023-01123-8)<br>💻 [Code](https://github.com/ML-Bioinfo-CEITEC/genomic_benchmarks) |
| GUE / GUE+ | 2023.06 / 2024.03 | Multi-task sequence classification | 70 bp to 10 kb | 📄 [Paper](https://arxiv.org/abs/2306.15006)<br>💻 [Code/Data](https://github.com/MAGICS-LAB/DNABERT_2#2-model-and-data) |
| Nucleotide Transformer Benchmark | 2023.01 / 2024.11 | Functional genomics prediction | 6 kb to 12 kb | 📄 [Paper](https://doi.org/10.1038/s41592-024-02523-z)<br>🤗 [Data](https://huggingface.co/datasets/InstaDeepAI/nucleotide_transformer_downstream_tasks)<br>🤗 [Revised data](https://huggingface.co/datasets/InstaDeepAI/nucleotide_transformer_downstream_tasks_revised) |
| BEND | 2023.11 / 2024.05 | Genome annotation prediction | Local windows to long genomic intervals | 📄 [Paper](https://arxiv.org/abs/2311.12570)<br>💻 [Code/Data](https://github.com/frederikkemarin/BEND) |
| GenBench | 2024.06 | Multi-domain genomic prediction | 30 bp to 196 kb | 📄 [Paper](https://arxiv.org/abs/2406.01627) |
| DART-Eval | 2024.12 | Regulatory DNA prediction | Regulatory elements and local contexts | 📄 [Paper](https://arxiv.org/abs/2412.05430)<br>💻 [Code](https://github.com/kundajelab/DART-Eval) |
| Long-Range Benchmark (LRB) | 2023.06-2025.01 | Long-context expression and variant prediction | Tens kb to hundreds kb | 📄 [HyenaDNA](https://arxiv.org/abs/2306.15794)<br>📄 [DNALongBench preprint](https://www.biorxiv.org/content/10.1101/2025.01.06.631595v1) |
| DNALONGBENCH | 2025.01 / 2025.11 | Long-range regulatory prediction | 10 kb to 1 Mb | 📄 [Paper](https://doi.org/10.1038/s41467-025-65077-4)<br>💻 [Code/Data](https://github.com/ma-compbio/DNALONGBENCH) |
| Benchmarking DNA FMs | 2024.08 / 2025.11 | Cross-task embedding benchmark | 64 bp to 500 kb | 📄 [Paper](https://doi.org/10.1038/s41467-025-65823-8)<br>📄 [Preprint](https://doi.org/10.1101/2024.08.16.608288) |
| DeepSEA / Enformer-style | 2015.08 / 2021.10 | Functional genomics prediction | 1 kb to 196 kb | 📄 [DeepSEA paper](https://www.nature.com/articles/nmeth.3547)<br>🌐 [DeepSEA server](https://deepsea.princeton.edu/)<br>📄 [Enformer paper](https://www.nature.com/articles/s41592-021-01252-x)<br>💻 [Enformer code](https://github.com/google-deepmind/deepmind-research/tree/master/enformer) |
| Variant-effect and clinical benchmarks | 2013.11-2025.01 | Variant-effect prediction | Local windows to hundreds kb | 🌐 [ClinVar](https://www.ncbi.nlm.nih.gov/clinvar/)<br>🌐 [CAGI](https://genomeinterpretation.org/)<br>📦 [MaveDB](https://www.mavedb.org/) |
| NABench | 2025.11 | Fitness prediction | Assay-dependent | 📄 [Paper](https://arxiv.org/abs/2511.02888)<br>💻 [Code/Data](https://github.com/mrzzmrzz/NABench) |

## Contributing

Contributions are welcome. Please open an issue or pull request if you find:

- a missing DNA, RNA, nucleotide, or regulatory-sequence foundation model;
- a missing benchmark, dataset, or evaluation protocol;
- a corrected paper, code, model, dataset, or project-page link;
- an incorrect tag, corpus category, context length, parameter count, or objective;
- a benchmark result that should be interpreted with stronger leakage, split, or biological-scope caveats.

When adding a paper, please include the source link and avoid unsupported claims about foundation capability. Prefer bounded descriptions such as `tested on long-range expression prediction` over broad claims such as `understands regulation`.

## Citation

The public citation will be updated when the paper is released. For now, cite the manuscript as:

```bibtex
@article{ye2026dnafoundationmodels,
  title   = {What Makes a DNA Foundation Model Foundational? Long-Range Regulation, Biological Priors, and Perturbational Generalization},
  author  = {Ye, Dong-Xin},
  year    = {2026},
  note    = {Manuscript in preparation}
}
```

## Acknowledgements

We thank the researchers and open-source communities whose work has advanced DNA foundation models, genomic language modeling, regulatory sequence modeling, and sequence-to-function prediction. This repository builds upon publicly available papers, codebases, pretrained models, datasets, benchmarks, and tutorials released by the broader computational biology, genomics, and machine learning communities.

We are especially grateful to the authors and maintainers of the DNA, RNA, nucleotide, regulatory-sequence, microbial, viral, plant, and cross-domain genome modeling resources curated in this repository. Their open scientific contributions make it possible to compare model architectures, pretraining corpora, evaluation protocols, and biological evidence across this rapidly evolving field.

We also thank the community members who report missing models, update links, suggest benchmark corrections, improve taxonomy labels, and contribute discussions on what should qualify as a genuinely foundational DNA model. Feedback, issues, and pull requests are highly appreciated and will help keep this resource accurate, transparent, and useful for future research.

If this repository is useful to your work, please consider citing the associated manuscript once available and starring the repository to support its continued maintenance.
