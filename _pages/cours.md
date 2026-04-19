---
permalink: /cours/
title: "Cours"
classes: wide
sidebar: false
---

Retrouvez ici l'ensemble des cours et guides que j'ai traduits

<style>
  .page__content {
    max-width: 100% !important;
    width: 100% !important;
  }

  .page {
    max-width: 100% !important;
    width: 100% !important;
  }

  .courses-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.3rem;
    margin-top: 1rem;
  }

  .course-card {
    display: flex;
    flex-direction: column;
    border: 1px solid #303749;
    border-radius: 16px;
    overflow: hidden;
    background: #161b27;
    text-decoration: none !important;
    color: inherit !important;
    transition: transform 0.18s ease, box-shadow 0.18s ease, border-color 0.18s ease;
    min-height: 100%;
  }

  .course-card:hover {
    transform: translateY(-3px);
    border-color: #6c8dff;
    box-shadow: 0 12px 28px rgba(0, 0, 0, 0.35);
  }

  .course-card__hero {
    height: 190px;
    position: relative;
    overflow: hidden;
  }

  .course-card__hero img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .course-card__chip {
    display: inline-block;
    position: absolute;
    top: 0.75rem;
    right: 0.75rem;
    border: 1px solid rgba(255, 255, 255, 0.5);
    background: rgba(0, 0, 0, 0.45);
    color: #ffffff;
    border-radius: 999px;
    font-size: 0.72rem;
    letter-spacing: 0.02em;
    padding: 0.24rem 0.65rem;
    z-index: 1;
  }

  .course-card__body {
    padding: 0.95rem 1rem 0.9rem;
    display: flex;
    flex-direction: column;
    gap: 0;
    flex: 1;
  }

  .course-card__title {
    margin: 0 0 0.7rem;
    font-size: 1.13rem;
    line-height: 1.3;
    color: #f3f5f9;
  }

  .course-card__text {
    margin: 0;
    color: #c5ccd8;
    line-height: 1.55;
    font-size: 0.94rem;
  }

  .course-card__stats {
    margin-top: 0;
    color: #9da7b8;
    font-size: 0.83rem;
  }

  @media (max-width: 900px) {
    .courses-grid { grid-template-columns: 1fr; }
  }
</style>

<div class="courses-grid">
  <a class="course-card" href="https://lbourdois.github.io/cours-dl-nyu/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/nyu-deep-learning.png" alt="Cours NYU">
      <span class="course-card__chip">NYU</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours de deep learning New York University</h3>
      <p class="course-card__text">Cours de Yann Le Cun et Alfredo Canziani (editions 2020 à 2022).</p>
      <div class="course-card__stats">33 videos d'une durée total de 45h, 74 pages web de notes, 16 notebooks</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/nlp-course/fr/chapter1/1" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-nlp-learn.png" alt="Cours NLP">
      <span class="course-card__chip">NLP</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours de NLP d'Hugging Face</h3>
      <p class="course-card__text">Traduction du cours de traitement automatique du langage avec les ressources du parcours complet.</p>
      <div class="course-card__stats">10 chapitres, 76 videos, 78 pages, 61 notebooks</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/audio-course/fr/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-audio-learn.png" alt="Cours Audio">
      <span class="course-card__chip">Audio</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours d'Audio d'Hugging Face</h3>
      <p class="course-card__text">Traduction du cours Audio, pense pour la pratique de bout en bout sur des cas reels.</p>
      <div class="course-card__stats">8 unites, 46 pages web - 2023</div>
    </div>
  </a>

  <a class="course-card" href="https://github.com/huggingface/diffusion-models-class/tree/main/units/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-diffusion-learn.jpg" alt="Cours Diffusion">
      <span class="course-card__chip">Diffusion</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours de Diffusion d'Hugging Face</h3>
      <p class="course-card__text">Traduction du cours sur les modeles de diffusion, axe sur la pratique et les notebooks.</p>
      <div class="course-card__stats">4 chapitres, 17 pages, 8 notebooks</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/agents-course/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-agents-learn.png" alt="Cours Agents IA">
      <span class="course-card__chip">Agents IA</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours sur les Agents IA d'Hugging Face</h3>
      <p class="course-card__text">Cours Agents IA, avec modules principaux et bonus.</p>
      <div class="course-card__stats">4 unites (+3 bonus), 74 pages, 16 notebooks</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-evaluate-banner.png" alt="Guide evaluation LLM">
      <span class="course-card__chip">Guide</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Guide sur l'evaluation des LLM</h3>
      <p class="course-card__text">Traduction du guide de Clementine Fourrier sur les bonnes pratiques d'evaluation des LLM.</p>
      <div class="course-card__stats">5 chapitres, 30 pages, 3 notebooks</div>
    </div>
  </a>
</div>
