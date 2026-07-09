<div align="center">

# Awesome DNA Foundation Models

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
- 📚 **Curated resources included**: representative DNA foundation models, pretraining corpus categories, evaluation benchmarks, review figures, and a graded evidence ladder for sequence-to-function claims.
- 🤝 **Community-driven**: found a missing model, benchmark, dataset, paper link, or correction? Feel free to open an issue or submit a pull request.

<p align="center">
  <img src="figs/fig1.png" alt="Operational framework for foundational capability in DNA foundation models" width="100%">
</p>

## News

- **[2026-07-09]** Initial README release with the review framework, model landscape, corpus taxonomy, benchmark map, and evidence ladder.

## Contents

- [Tag Legend](#tag-legend)
- [DNA Foundation Models](#dna-foundation-models)
- [Pretraining Corpora](#pretraining-corpora)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Evidence Ladder](#evidence-ladder)
- [Figures](#figures)
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

| Corpus type | Data composition | Representative sources | Representative models |
| --- | --- | --- | --- |
| Single-species reference genome | Continuous fragments from one reference genome | GRCh38/hg38, T2T-CHM13, hg19, mm10/mm39, TAIR10 | HyenaDNA, Caduceus, GROVER, Gene42, OmniReg-GPT |
| Population-scale and variant-aware genome | Multi-individual genomes, haplotypes, SNPs, indels, and variant-containing sequences | 1000 Genomes Project, 3,202 high-coverage human genomes, Human Pangenome Reference Consortium | Nucleotide Transformer, GENA-LM |
| Multi-species reference genome | Animal, plant, fungal, bacterial, and other assembled genomes | Ensembl Genomes, NCBI RefSeq, NCBI GenBank, Phytozome | Nucleotide Transformer, DNABERT-2, AIDO.DNA, GENA-LM |
| Prokaryotic and phage genome | Bacterial, archaeal, phage, and related prokaryotic genomes | OpenGenome, NCBI RefSeq Bacteria/Archaea, GenBank Prokaryotic Genomes, IMG/VR | Evo, Evo 1.5 |
| Metagenomic and environmental genome | Environmental metagenomic contigs, MAGs, and uncultivated microbial sequences | GenomeOcean corpus, IMG/M, MGnify, JGI Metagenome, GOLD, Tara Oceans | GenomeOcean, Evo2 |
| Viral, plasmid, and mobile genetic element | Viral, phage, plasmid, transposon, and other mobile-element sequences | NCBI Virus, GenBank Viral, IMG/VR, PhagesDB, PLSDB | Evo, Evo2, LucaVirus |
| Cross-domain and pan-genomic | Bacteria, archaea, eukaryotes, viruses, metagenomes, and organelles | OpenGenome2 | Evo2 |

## Benchmarks and Evaluation

Benchmarks should be interpreted as biological probes. A strong local classification score does not by itself establish long-range regulatory modeling, perturbation response, or mechanistic sequence-to-function understanding.

| Benchmark | Year | Task type | Input length |  |
| --- | --- | --- | --- | --- |
| Genomic Benchmarks | 2023 | Sequence classification | Hundreds bp to several kb |  |
| GUE / GUE+ | 2023/2024 | Multi-task sequence classification | 70 bp to 10 kb |  |
| Nucleotide Transformer Benchmark | 2023/2025 | Functional genomics prediction | 6 kb to 12 kb |  |
| BEND | 2023/2024 | Genome annotation prediction | Local windows to long genomic intervals |  |
| GenBench | 2024 | Multi-domain genomic prediction | 30 bp to 196 kb |  |
| DART-Eval | 2024/2025 | Regulatory DNA prediction | Regulatory elements and local contexts |  |
| Long-Range Benchmark (LRB) | 2023-2025 | Long-context expression and variant prediction | Tens kb to hundreds kb |  |
| DNALONGBENCH | 2025 | Long-range regulatory prediction | 10 kb to 1 Mb |  |
| Benchmarking DNA FMs | 2025 | Cross-task embedding benchmark | 64 bp to 500 kb |  |
| DeepSEA / Enformer-style | 2015/2021 | Functional genomics prediction | 1 kb to 196 kb |  |
| Variant-effect and clinical benchmarks | 2013-2025 | Variant-effect prediction | Local windows to hundreds kb |  |
| NABench | 2025 | Fitness prediction | Assay-dependent |  |

## Evidence Ladder

<p align="center">
  <img src="../figs/fig6_evidence_ladder.png" alt="Evidence ladder for DNA foundation model claims" width="100%">
</p>

Evidence for DNA foundation capability should be graded by what is actually tested:

1. **Weak evidence**: parameter count, context length, pretraining corpus size, or average local benchmark performance.
2. **Moderate evidence**: frozen-embedding transfer, multi-task functional genomics prediction, cross-species transfer, or long-context tasks with careful controls.
3. **Strong evidence**: distance-stratified long-range regulatory evaluation, perturbation-aware variant-effect prediction, strict out-of-distribution splits, calibrated effect-size prediction, and interpretable biological attributions.
4. **Highest evidence**: experimental validation through MPRA, CRISPRi, saturation mutagenesis, Perturb-seq, synthetic sequence design, or closed-loop model-guided experiments.

## Figures

| Figure | File | Main message |
| --- | --- | --- |
| Foundational capability framework | [`figs/fig1.png`](figs/fig1.png) | Scale alone does not define foundation capability. |
| Model design landscape | [`figs/fig2_models.png`](../figs/fig2_models.png) | DNA foundation models have diversified across architectures, objectives, contexts, and corpora. |
| Corpus signal and bias | [`figs/fig3_pretraining_corpus_bias_signal.png`](../figs/fig3_pretraining_corpus_bias_signal.png) | Each corpus type provides useful signal and systematic bias. |
| Long-context regulatory use | [`figs/fig4_long_context_regulatory_use.png`](../figs/fig4_long_context_regulatory_use.png) | Long context is a prerequisite, not proof, of distal regulatory modeling. |
| Biological priors | [`figs/fig5_biological_priors_vs_nlp.png`](../figs/fig5_biological_priors_vs_nlp.png) | DNA modeling requires priors that generic text modeling does not provide. |
| Evidence ladder | [`figs/fig6_evidence_ladder.png`](../figs/fig6_evidence_ladder.png) | Stronger claims require perturbation, OOD evaluation, interpretability, and validation. |
| Modular biological AI systems | [`figs/fig7_modular_biological_ai_system.png`](../figs/fig7_modular_biological_ai_system.png) | DNA models are likely to function as components in larger biological AI systems. |

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

This README structure is inspired by community-maintained survey repositories such as `Awesome-WAM`, while the taxonomy, evidence criteria, corpus categories, benchmark map, and figures are based on the accompanying DNA foundation model review manuscript.
