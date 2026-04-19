---
permalink: /cours/
title: "Cours"
classes: wide
sidebar: false
---

Retrouvez ici l'ensemble des cours et guides que j'ai traduits, dans une presentation en cartes inspiree de la page Learn de Hugging Face.

<style>
  .courses-intro {
    color: #a8b0bd;
    margin-bottom: 1rem;
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
    height: 172px;
    padding: 1rem;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    position: relative;
    overflow: hidden;
  }

  .course-card__hero::after {
    content: "";
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at 90% 10%, rgba(255, 255, 255, 0.22), transparent 35%);
    pointer-events: none;
  }

  .course-card__icon {
    width: 42px;
    height: 42px;
    border-radius: 11px;
    background: rgba(255, 255, 255, 0.2);
    display: inline-flex;
    align-items: center;
    justify-content: center;
    font-size: 1.25rem;
    z-index: 1;
  }

  .course-card__chip {
    display: inline-block;
    border: 1px solid rgba(255, 255, 255, 0.45);
    background: rgba(0, 0, 0, 0.2);
    color: #ffffff;
    border-radius: 999px;
    font-size: 0.72rem;
    letter-spacing: 0.02em;
    padding: 0.24rem 0.65rem;
    z-index: 1;
  }

  .course-card__body {
    padding: 1rem 1rem 1.05rem;
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    flex: 1;
  }

  .course-card__title {
    margin: 0;
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
    color: #9da7b8;
    font-size: 0.83rem;
  }

  .course-card__cta {
    margin-top: auto;
    color: #9fbcff;
    font-size: 0.9rem;
    font-weight: 600;
  }

  .hero-nyu { background: linear-gradient(135deg, #5f2b9f, #7f43ca 55%, #9f69e0); }
  .hero-nlp { background: linear-gradient(135deg, #f39f2f, #f4b248 45%, #d07d17); }
  .hero-audio { background: linear-gradient(135deg, #e4556a, #f4798a 45%, #a9457f); }
  .hero-diff { background: linear-gradient(135deg, #18a3b2, #2dbfd0 45%, #2b7da9); }
  .hero-agents { background: linear-gradient(135deg, #2d6cdf, #4e87ff 45%, #3a4fc2); }
  .hero-eval { background: linear-gradient(135deg, #69707f, #878f9f 45%, #57606f); }

  @media (max-width: 900px) {
    .courses-grid { grid-template-columns: 1fr; }
  }
</style>

<p class="courses-intro">2 cartes par ligne, avec un visuel, un resume court et un acces direct vers chaque ressource.</p>

<div class="courses-grid">
  <a class="course-card" href="https://lbourdois.github.io/cours-dl-nyu/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero hero-nyu">
      <span class="course-card__icon">🎓</span>
      <span class="course-card__chip">NYU</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours de deep learning NYU</h3>
      <p class="course-card__text">Traduction du cours de Yann LeCun et Alfredo Canziani (editions 2020 et 2021), avec contenus pedagogiques complets.</p>
      <div class="course-card__stats">33 videos, 74 pages de notes, 16 notebooks - 2020 -> 2022</div>
      <div class="course-card__cta">Commencer le cours -></div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/nlp-course/fr/chapter1/1" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero hero-nlp">
      <span class="course-card__icon">🤗</span>
      <span class="course-card__chip">NLP</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours NLP Hugging Face</h3>
      <p class="course-card__text">Traduction du cours de traitement automatique du langage avec les ressources du parcours complet.</p>
      <div class="course-card__stats">10 chapitres, 76 videos, 78 pages, 61 notebooks - 2022</div>
      <div class="course-card__cta">Commencer le cours -></div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/audio-course/fr/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero hero-audio">
      <span class="course-card__icon">🎧</span>
      <span class="course-card__chip">Audio</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours Audio Hugging Face</h3>
      <p class="course-card__text">Traduction du cours Audio, pense pour la pratique de bout en bout sur des cas reels.</p>
      <div class="course-card__stats">8 unites, 46 pages web - 2023</div>
      <div class="course-card__cta">Commencer le cours -></div>
    </div>
  </a>

  <a class="course-card" href="https://github.com/huggingface/diffusion-models-class/tree/main/units/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero hero-diff">
      <span class="course-card__icon">🧪</span>
      <span class="course-card__chip">Diffusion</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours Diffusion Hugging Face</h3>
      <p class="course-card__text">Traduction du cours sur les modeles de diffusion, axe sur la pratique et les notebooks.</p>
      <div class="course-card__stats">4 chapitres, 17 pages, 8 notebooks - 2023</div>
      <div class="course-card__cta">Voir le contenu -></div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/agents-course/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero hero-agents">
      <span class="course-card__icon">🤖</span>
      <span class="course-card__chip">Agents IA</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Cours Agents IA Hugging Face</h3>
      <p class="course-card__text">Participation a la traduction du cours Agents IA (avec Kim Noel), avec modules principaux et bonus.</p>
      <div class="course-card__stats">4 unites (+3 bonus), 74 pages, 16 notebooks - 2025</div>
      <div class="course-card__cta">Commencer le cours -></div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero hero-eval">
      <span class="course-card__icon">⚖️</span>
      <span class="course-card__chip">Guide</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Guide d'evaluation des LLM</h3>
      <p class="course-card__text">Traduction du guide de Clementine Fourrier sur les bonnes pratiques d'evaluation des LLM.</p>
      <div class="course-card__stats">5 chapitres, 30 pages, 3 notebooks - 2025</div>
      <div class="course-card__cta">Lire le guide -></div>
    </div>
  </a>
</div>
