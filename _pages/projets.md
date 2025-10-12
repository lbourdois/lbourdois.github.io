---
permalink: /projets/
title: "Projets"
classes: single
---

Sur cette page vous pouvez trouver les contenus sur lesquels j'ai travaillé (à titre personnel ou professionnel) mais qui sont référencés sur d'autres sites que mon blog personnel. Il s'agit principalement de traductions de cours, et des créations de jeux de données et de modèles.

<br><br>

<!--
# Vue d'ensemble

<iframe
	src="https://lbourdois-roadmap.static.hf.space"
	frameborder="0"
	width="950"
	height="1500"
></iframe>

<br><br><br>
-->

# Modèles et jeux de données en français

## FAT5
Le FAT5 est une implémentation du [T5](https://arxiv.org/abs/1910.10683) en PyTorch avec un objectif [UL2](https://arxiv.org/abs/2205.05131) optimisé pour GPGPU développé avec [Boris ALBAR](https://b-albar.github.io/portfolio/).  
Elle utilise des noyaux CUDA et Triton personnalisés ainsi que des optimisations spécifiques pour augmenter le débit et réduire l'utilisation de la mémoire pour l'entraînement et l'inférence d'un facteur 2 par rapport à l'implémentation originale disponible dans Hugging Face.  
Nous l'avons appliquée en pré-entraînant un modèle en français de 147M paramètres en utilisant uniquement une A100. Nous estimons ainsi pouvoir ramener le prix de pré-entraînement d'un tel modèle à seulement 1200€ (estimation faite sur une instance Sesterce).   
Le code de pré-entrainement est disponible sur [GitHub](https://github.com/catie-aq/flashT5) sous licence Apache-2.0 et les poids du modèle entraîné sur le compte [Hugging Face du CATIE]([https://huggingface.co/CATIE-AQ](https://huggingface.co/collections/CATIE-AQ/catie-french-fat5-ul2-677697a35feea336389d6403)). Un article de blog détaillant notre méthodologie est disponible [ici](https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport).

## NER
Les NERmemBERT constituent une famille de modèles de Reconnaissance d’Entités Nommées en français capable d’étiqueter jusqu’à 4 entités (Personnalités, Lieux, Organisations, Divers tel que des noms d’œuvre, de maladies, etc.). Ils sont disponibles en taille base (110M ou 136M de paramètres) et large (336M), gérant des contextes allant de 512 à 8192 tokens. Les poids sont disponibles gratuitement en open-source, tout comme les jeux de données ayant servis à l’entraînement. Le tout est disponible sur le compte [Hugging Face du CATIE](https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4). Un article de blog détaillant la méthodologie adoptée est disponible [ici](https://lbourdois.github.io/blog/NER/).<br>
Ils ont été téléchargés plus de 185 000 fois depuis leur mise en ligne.

## Question Answering
Les QAmemBERT constituent une famille de réponse aux questions en français capable d’indiquer si la réponse à une question est présente ou pas dans un texte de contexte associé. Ils sont disponibles en taille base (110M ou 136M de paramètres) et large (335M), gérant des contextes allant de 512 à 8192 tokens. Les poids sont disponibles gratuitement en open-source, tout comme le jeu de données ayant servis à l’entraînement. Le tout est disponible sur le compte [Hugging Face du CATIE](https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91). Un article de blog détaillant la méthodologie adoptée est disponible [ici](https://lbourdois.github.io/blog/QA/).<br>
Ils ont été téléchargés plus de 160 000 fois depuis leur mise en ligne.

## DFP
*Dataset of French Prompts* (DFP) contient 113 129 978 lignes portant sur 30 tâches de NLP différentes.  
724 prompts ont été écrits sous forme impérative, de tutoiement et de vouvoiement afin de couvrir autant que possible les données de pré-entraînement utilisées par le modèle qui utilisera ces données et qui nous sont inconnues.

Les colonnes *inputs* et *targets* suivent le même format que l'ensemble de données [xP3](https://huggingface.co/datasets/bigscience/xP3) de Muennighoff et al.  
L'ensemble des détails est disponible sur [Hugging Face](https://huggingface.co/datasets/CATIE-AQ/DFP).<br>
Il a été téléchargé plus de 75 000 fois depuis sa mise en ligne.

## La marmite
Projet toujours en cours.  
Il s'agit de proposer un équivalent en français du jeu de données [*the cauldron*](https://huggingface.co/datasets/HuggingFaceM4/the_cauldron) afin de pouvoir entraîner un VLM en français.  
Ce jeu de données prendra en compte des données d'OCR (voir celles déjà disponibles en ligne [ici](https://huggingface.co/collections/lbourdois/french-ocr-datasets-67c8d3152330f11227e0d108)), de captionning (voir celles déjà disponibles en ligne [ici](https://huggingface.co/collections/lbourdois/french-caption-datasets-67c8d2227284a5daa00c50b9)), de VQA (voir celles déjà disponibles en ligne [ici](https://huggingface.co/collections/lbourdois/french-vqa-datasets-67c8d1a162a23ef0e9a2bc89)) et de raisonnement.  
Les sous-jeux de données déjà en ligne ont été téléchargé plus de 25 000 fois depuis leur mise en ligne.

<br><br><br>

# Traductions
## Cours de Yann Le Cun et Alfredo Canziani de la NYU
Cette traduction a été la plus longue à effectuer s'étalant de 2020 à 2022.  
Le contenu est structuré en 19 unités réparties sur 33 vidéos 🎥 de cours (cours magistraux et travaux dirigés) d’une durée totale d’environ 45H, 74 pages web 🌐 résumant les vidéos via les notes prises par les étudiants pendant le cours, et 16 notebooks Jupyter 📓 (en PyTorch) utilisés lors des TD. Enfin un jeu de données de plus de 3000 données parallèles vérifiées manuellement a été créé pour entraîner un modèle de traduction.  
Vous pouvez retrouver toutes ces ressources sur le site internet dédié qui a été conçu à l'occasion : [https://lbourdois.github.io/cours-dl-nyu/](https://lbourdois.github.io/cours-dl-nyu/).

## Cours de Hugging Face 🤗
### Cours de NLP
En 2022, j'ai traduit le cours de traitement automatique du langage de Hugging Face.  
Le contenu est structuré en 10 chapitres comprenant un total de 76 vidéos 🎥 d'une durée totale d'environ 5H, de 78 pages web 🌐 et 61 notebooks Jupyter 📓  (en PyTorch et Tensorflow).  
Vous pouvez retrouver toutes ces ressources sur le site de [Hugging Face](https://huggingface.co/learn/nlp-course/fr/chapter1/1).

### Cours d'audio
En 2023, j'ai traduit le cours d'audio de Hugging Face.  
Le contenu est structuré en 8 unités réparties sur 46 pages web 🌐.  
Vous pouvez retrouver toutes ces ressources sur le site de [Hugging Face](https://huggingface.co/learn/audio-course/fr/).

### Cours sur les modèles de diffusion
En 2023, j'ai traduit le cours sur les modèles de diffusion de Hugging Face.  
Le contenu est structuré en 4 chapitres portant sur 17 pages web 🌐 et 8 notebooks Jupyter 📓 (en PyTorch).  
Vous pouvez retrouver toutes ces ressources sur le GitHub de [Hugging Face](https://github.com/huggingface/diffusion-models-class/tree/main/units/fr) (le contenu n'ayant pas encore été propagé sur le site officiel).

### Cours sur les agents IA
En 2025, j'ai participé avec [Kim NOEL](https://github.com/knoel99) à la traduction du cours sur les agents IA de Hugging Face.  
Le contenu est structuré en 4 unités (+ 3 bonus) réparties sur 74 pages web 🌐 et 16 notebooks Jupyter 📓.  
Vous pouvez retrouver toutes ces ressources sur le site de [Hugging Face](https://huggingface.co/learn/agents-course/fr).

### Guide sur l'évaluation des LLM
En  2025, j'ai traduit le [guide](https://github.com/huggingface/evaluation-guidebook/tree/main) de [Clémentine Fourrier](https://huggingface.co/clefourrier).  
Le contenu est structuré 5 chapitres répartis sur 30 pages web 🌐 et 3 notebooks Jupyter 📓.  
Vous pouvez retrouver toutes ces ressources [ici](https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM).
