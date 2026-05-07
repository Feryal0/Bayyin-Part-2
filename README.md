# Bayyin: Arabic Readability Classification via Hybrid and Ensemble Architectures

This repository contains the implementation and refined dataset for multi-level Arabic readability assessment. The framework evaluates standalone Transformers, Hybrid BiLSTM-Attention models, and Stacked Generalization to address morphological complexity in Arabic NLP.

**Status:** Active research / academic project.


## Project Aim & Objectives

The main goal is to develop an AI tool that performs both **readability assessment** for the Arabic language.

Our key objectives include:
* To refine the Bayyin dataset by targeting the intermediate levels aiming to improve class-wise performance.
* To fine-tune and optimize State-of-the-Art (SOA) Arabic Large Language models to classify Arabic texts into defined proficiency levels.
* To create a classification framework that leverages multiple models to ensure better generalization and fewer mistakes.

## Dataset

The framework utilizes the **Refined Bayyin Dataset**, an expanded version of the original corpus.
* **Scale**: 44,917 Arabic sentences distributed across six readability levels.
* **Refinement Strategy**: To address overlap in intermediate levels (3–5), samples were reconstructed using the BAREC corpus, stratified by morphological complexity.
* **Data Sources**: Integrated data from BAREC, the Arabic E-Book Corpus, and the DARES (Saudi school curriculum) corpus.
* **Linguistic Forms**: Each sample is represented in four forms: Word, Lex (lemmatized), D3Tok (morphological segmentation), and D3Lex.
* **Preprocessing**: All text underwent standardized tashkeel and stop-word removal, letter normalization, and morphological stemming.

## Repository Structure

### Transformer Models
* `AraBERTv2Bayyin2.ipynb`
* `AraELCTRABayyin.ipynb`
* `arabicbertBayyin.ipynb`
* `camelbertmixBayyin2.ipynb`
* `camelbertmsaBayyin2.ipynb`
* `gigabertBayyin.ipynb`
* `marbertv2Bayyin.ipynb`
* `qaribBayyin.ipynb`

### Hybrid Models
* `bilstmBayyin2.ipynb`: Implementation of the Transformer-BiLSTM-Attention hybrid architecture.
* `arabertv2HandcraftedBayyin.ipynb`: Integration of transformer softmax scores with handcrafted linguistic features.
* `bilstm-multiencoding-hybrid.ipynb`: Multi-encoder framework (AraBERTv2, CamelBERT-MSA, and MARBERTv2) with a meta-classifier.

### Ensemble
* `EnsembleBayyin.ipynb`: Implementation of Stacking Generalization utilizing meta-learners such as SVM, XGBoost, and CatBoost.
* `Hierarchal_2_3_ensembel.ipynb`: Implementation of the two-stage hierarchical classification pipeline.


## Experimental Results

Performance metrics for the primary architectures evaluated on the refined Bayyin test set:

| Architecture | Model Variant | Accuracy | QWK |
| :--- | :--- | :---: | :---: |
| **Stacking Ensemble** | **SVM** | **0.8368** | **0.9015** |
| Hybrid Meta-Classifier | XGBoost | 0.8189 | 0.8868 |
| Standalone Transformer | AraBERTv2 | 0.7955 | 0.8851 |
| Hierarchical | Coarse-to-Fine | 0.8015 | 0.8835 |
## Contributors & contact
This project is submitted for the fulfillment of the requirements for the graduation project at the University of Jeddah. For questions about reproducing results or data access, open an issue on the repository or contact the repository owner.

**Contributors:**
* Sarah F. Alhalees (2219288) 
* Nagham A. Alshbrawi (2219273)
* Raya Y. Abu Aljamal (2310903) 
* Fatimah M. Alsinan (2310303) 
* Feryal E. Jadallah (2311180) 
* Bayan Z. Barmeem (2219206) 

**Supervisor:**
* Dr. Shahd Alahdal

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



