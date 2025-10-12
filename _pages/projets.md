---
permalink: /projets/
title: "Projets"
classes: wide
sidebar: false
---

<style>
/* Forcer la largeur maximale pour le contenu */
.page__content {
    max-width: 100% !important;
    width: 100% !important;
}

/* S'assurer que le conteneur principal utilise toute la largeur */
.page {
    max-width: 100% !important;
    width: 100% !important;
}

/* Optimiser l'iframe pour la responsivité */
.full-width-iframe {
    width: 100%;
    height: 1200px;
    border: none;
    margin: 0;
    padding: 0;
}

.full-width-iframe-model_size {
    width: 100%;
    height: 500px;
    border: none;
    margin: 0;
    padding: 0;
}

.full-width-iframe-treemap {
    width: 100%;
    height: 800px;
    border: none;
    margin: 0;
    padding: 0;
}
  
/* Media query pour les écrans plus petits */
@media (max-width: 768px) {
    .full-width-iframe {
        height: 400px;
    }
}

<div style="width: 100%; margin: 0; padding: 0;">
	
<p>
Sur cette page vous pouvez trouver les contenus sur lesquels j'ai travaillé (à titre personnel ou professionnel) mais qui sont référencés sur d'autres sites que mon blog personnel. Il s'agit principalement de traductions de cours, et des créations de jeux de données et de modèles.</p>

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

<h1>Modèles et jeux de données en français</h1>

<h2>FAT5</h2>
<p>Le FAT5 est une implémentation du <a href="https://arxiv.org/abs/1910.10683">T5</a> en PyTorch avec un objectif <a href="https://arxiv.org/abs/2205.05131">UL2</a> optimisé pour GPGPU développé avec <a href="https://b-albar.github.io/portfolio/">Boris ALBAR</a>.<br>
Elle utilise des noyaux CUDA et Triton personnalisés ainsi que des optimisations spécifiques pour augmenter le débit et réduire l'utilisation de la mémoire pour l'entraînement et l'inférence d'un facteur 2 par rapport à l'implémentation originale disponible dans Hugging Face.<br>
Nous l'avons appliquée en pré-entraînant un modèle en français de 147M paramètres en utilisant uniquement une A100. Nous estimons ainsi pouvoir ramener le prix de pré-entraînement d'un tel modèle à seulement 1200€ (estimation faite sur une instance Sesterce).<br>
Le code de pré-entrainement est disponible sur <a href="https://github.com/catie-aq/flashT5">GitHub</a> sous licence Apache-2.0 et les poids du modèle entraîné sur le compte <a href="https://huggingface.co/collections/CATIE-AQ/catie-french-fat5-ul2-677697a35feea336389d6403">Hugging Face du CATIE</a>. Un article de blog détaillant notre méthodologie est disponible <a href="https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport">ici</a>.</p>

<h2>NER</h2>
<p>Les NERmemBERT constituent une famille de modèles de Reconnaissance d'Entités Nommées en français capable d'étiqueter jusqu'à 4 entités (Personnalités, Lieux, Organisations, Divers tel que des noms d'œuvre, de maladies, etc.). Ils sont disponibles en taille base (110M ou 136M de paramètres) et large (336M), gérant des contextes allant de 512 à 8192 tokens. Les poids sont disponibles gratuitement en open-source, tout comme les jeux de données ayant servis à l'entraînement. Le tout est disponible sur le compte <a href="https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4">Hugging Face du CATIE</a>. Un article de blog détaillant la méthodologie adoptée est disponible <a href="https://lbourdois.github.io/blog/NER/">ici</a>.<br>
Ils ont été téléchargés plus de 185 000 fois depuis leur mise en ligne.</p>

<h2>Question Answering</h2>
<p>Les QAmemBERT constituent une famille de réponse aux questions en français capable d'indiquer si la réponse à une question est présente ou pas dans un texte de contexte associé. Ils sont disponibles en taille base (110M ou 136M de paramètres) et large (335M), gérant des contextes allant de 512 à 8192 tokens. Les poids sont disponibles gratuitement en open-source, tout comme le jeu de données ayant servis à l'entraînement. Le tout est disponible sur le compte <a href="https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91">Hugging Face du CATIE</a>. Un article de blog détaillant la méthodologie adoptée est disponible <a href="https://lbourdois.github.io/blog/QA/">ici</a>.<br>
Ils ont été téléchargés plus de 160 000 fois depuis leur mise en ligne.</p>

<h2>DFP</h2>
<p><em>Dataset of French Prompts</em> (DFP) contient 113 129 978 lignes portant sur 30 tâches de NLP différentes.<br>
724 prompts ont été écrits sous forme impérative, de tutoiement et de vouvoiement afin de couvrir autant que possible les données de pré-entraînement utilisées par le modèle qui utilisera ces données et qui nous sont inconnues.</p>

<p>Les colonnes <em>inputs</em> et <em>targets</em> suivent le même format que l'ensemble de données <a href="https://huggingface.co/datasets/bigscience/xP3">xP3</a> de Muennighoff et al.<br>
L'ensemble des détails est disponible sur <a href="https://huggingface.co/datasets/CATIE-AQ/DFP">Hugging Face</a>.<br>
Il a été téléchargé plus de 75 000 fois depuis sa mise en ligne.</p>

<h2>La marmite</h2>
<p>Projet toujours en cours.<br>
Il s'agit de proposer un équivalent en français du jeu de données <a href="https://huggingface.co/datasets/HuggingFaceM4/the_cauldron"><em>the cauldron</em></a> afin de pouvoir entraîner un VLM en français.<br>
Ce jeu de données prendra en compte des données d'OCR (voir celles déjà disponibles en ligne <a href="https://huggingface.co/collections/lbourdois/french-ocr-datasets-67c8d3152330f11227e0d108">ici</a>), de captionning (voir celles déjà disponibles en ligne <a href="https://huggingface.co/collections/lbourdois/french-caption-datasets-67c8d2227284a5daa00c50b9">ici</a>), de VQA (voir celles déjà disponibles en ligne <a href="https://huggingface.co/collections/lbourdois/french-vqa-datasets-67c8d1a162a23ef0e9a2bc89">ici</a>) et de raisonnement.<br>
Les sous-jeux de données déjà en ligne ont été téléchargé plus de 25 000 fois depuis leur mise en ligne.</p>

<br><br><br>

<h1>Traductions</h1>

<h2>Cours de Yann Le Cun et Alfredo Canziani de la NYU</h2>
<p>Cette traduction a été la plus longue à effectuer s'étalant de 2020 à 2022.<br>
Le contenu est structuré en 19 unités réparties sur 33 vidéos 🎥 de cours (cours magistraux et travaux dirigés) d'une durée totale d'environ 45H, 74 pages web 🌐 résumant les vidéos via les notes prises par les étudiants pendant le cours, et 16 notebooks Jupyter 📓 (en PyTorch) utilisés lors des TD. Enfin un jeu de données de plus de 3000 données parallèles vérifiées manuellement a été créé pour entraîner un modèle de traduction.<br>
Vous pouvez retrouver toutes ces ressources sur le site internet dédié qui a été conçu à l'occasion : <a href="https://lbourdois.github.io/cours-dl-nyu/">https://lbourdois.github.io/cours-dl-nyu/</a>.</p>

<h2>Cours de Hugging Face 🤗</h2>

<h3>Cours de NLP</h3>
<p>En 2022, j'ai traduit le cours de traitement automatique du langage de Hugging Face.<br>
Le contenu est structuré en 10 chapitres comprenant un total de 76 vidéos 🎥 d'une durée totale d'environ 5H, de 78 pages web 🌐 et 61 notebooks Jupyter 📓  (en PyTorch et Tensorflow).<br>
Vous pouvez retrouver toutes ces ressources sur le site de <a href="https://huggingface.co/learn/nlp-course/fr/chapter1/1">Hugging Face</a>.</p>

<h3>Cours d'audio</h3>
<p>En 2023, j'ai traduit le cours d'audio de Hugging Face.<br>
Le contenu est structuré en 8 unités réparties sur 46 pages web 🌐.<br>
Vous pouvez retrouver toutes ces ressources sur le site de <a href="https://huggingface.co/learn/audio-course/fr/">Hugging Face</a>.</p>

<h3>Cours sur les modèles de diffusion</h3>
<p>En 2023, j'ai traduit le cours sur les modèles de diffusion de Hugging Face.<br>
Le contenu est structuré en 4 chapitres portant sur 17 pages web 🌐 et 8 notebooks Jupyter 📓 (en PyTorch).<br>
Vous pouvez retrouver toutes ces ressources sur le GitHub de <a href="https://github.com/huggingface/diffusion-models-class/tree/main/units/fr">Hugging Face</a> (le contenu n'ayant pas encore été propagé sur le site officiel).</p>

<h3>Cours sur les agents IA</h3>
<p>En 2025, j'ai participé avec <a href="https://github.com/knoel99">Kim NOEL</a> à la traduction du cours sur les agents IA de Hugging Face.<br>
Le contenu est structuré en 4 unités (+ 3 bonus) réparties sur 74 pages web 🌐 et 16 notebooks Jupyter 📓.<br>
Vous pouvez retrouver toutes ces ressources sur le site de <a href="https://huggingface.co/learn/agents-course/fr">Hugging Face</a>.</p>

<h3>Guide sur l'évaluation des LLM</h3>
<p>En  2025, j'ai traduit le <a href="https://github.com/huggingface/evaluation-guidebook/tree/main">guide</a> de <a href="https://huggingface.co/clefourrier">Clémentine Fourrier</a>.<br>
Le contenu est structuré 5 chapitres répartis sur 30 pages web 🌐 et 3 notebooks Jupyter 📓.<br>
Vous pouvez retrouver toutes ces ressources <a href="https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM">ici</a>.</p>
</div>
