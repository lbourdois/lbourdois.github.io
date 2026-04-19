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
    height: 230px;
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
    padding: 0.78rem 1rem 0.72rem;
    display: flex;
    flex-direction: column;
    gap: 0;
    flex: 1;
  }

  .course-card__title {
    margin: 0 0 0.45rem;
    font-size: 1.13rem;
    line-height: 1.3;
    color: #f3f5f9;
  }

  p.course-card__text {
    margin: 0;
    color: #c5ccd8;
    line-height: 1.45;
    font-size: 0.94rem;
  }

  .course-card__stats {
    margin-top: 0;
    color: #9da7b8;
    font-size: 0.83rem;
  }

  @media (max-width: 900px) {
    .courses-grid { grid-template-columns: 1fr; }
    .course-card__hero { height: 210px; }
  }
</style>

<div class="courses-grid">
  <a class="course-card" href="https://lbourdois.github.io/cours-dl-nyu/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/nyu-deep-learning.png" alt="Cours NYU">
      <span class="course-card__chip">NYU</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours de Yann Le Cun et Alfredo Canziani</h3>
      <div class="course-card__stats">19 unités, 33 videos (~ 45h) 🎥, 74 pages web 🌐, 16 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/nlp-course/fr/chapter1/1" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-nlp-learn.png" alt="Cours NLP">
      <span class="course-card__chip">NLP</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours de NLP d'Hugging Face</h3>
      <div class="course-card__stats">10 chapitres, 76 videos 🎥, 78 pages web 🌐, 61 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/audio-course/fr/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-audio-learn.png" alt="Cours Audio">
      <span class="course-card__chip">Audio</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours d'Audio d'Hugging Face</h3>
      <div class="course-card__stats">8 unites, 46 pages web 🌐</div>
    </div>
  </a>

  <a class="course-card" href="https://github.com/huggingface/diffusion-models-class/tree/main/units/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-diffusion-learn.jpg" alt="Cours Diffusion">
      <span class="course-card__chip">Diffusion</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours sur les modèles de diffusion d'Hugging Face</h3>
      <div class="course-card__stats">4 unités, 17 pages web 🌐, 8 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/agents-course/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-agents-learn.png" alt="Cours Agents IA">
      <span class="course-card__chip">Agents IA</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours sur les Agents IA d'Hugging Face</h3>
      <div class="course-card__stats">4 unites (+ 3 bonus), 74 pages web 🌐, 16 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-evaluate-banner.png" alt="Guide evaluation LLM">
      <span class="course-card__chip">Guide</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Guide de Clementine Fourrier sur l'evaluation des LLM </h3>
      <div class="course-card__stats">5 chapitres, 30 pages web 🌐, 3 notebooks 📓</div>
    </div>
  </a>
</div>
