---
permalink: /en/cours/
title: "Courses"
classes: wide
sidebar: false
---

Find here all the courses and guides I have translated.

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

  .course-card__hero--nlp {
    background: linear-gradient(135deg, #f8c63f 0%, #f4b540 45%, #ee9b21 100%);
  }

  .course-card__hero--nlp img {
    object-fit: contain;
    width: 92%;
    height: 92%;
    margin: 0.55rem auto 0;
  }

  .course-card__hero--diffusion {
    background: linear-gradient(135deg, #1fa0c9 0%, #2a87d2 45%, #4f6ef0 100%);
  }

  .course-card__hero--diffusion img {
    object-fit: contain;
    width: 92%;
    height: 92%;
    margin: 0.55rem auto 0;
  }

  .course-card__hero--guide {
    background: linear-gradient(135deg, #5d5f6e 0%, #7b7f92 45%, #4d566f 100%);
  }

  .course-card__hero--guide img {
    object-fit: contain;
    width: 92%;
    height: 92%;
    margin: 0.55rem auto 0;
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
      <img src="/assets/images/cours/nyu-deep-learning.png" alt="NYU Course">
      <span class="course-card__chip">NYU</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Yann LeCun and Alfredo Canziani's Course</h3>
      <div class="course-card__stats">19 units, 33 videos (~ 45h) 🎥, 74 web pages 🌐, 16 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/nlp-course/fr/chapter1/1" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero course-card__hero--nlp">
      <img src="/assets/images/cours/hf-nlp-academic-huggy.png" alt="NLP Course">
      <span class="course-card__chip">NLP</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Hugging Face NLP Course</h3>
      <div class="course-card__stats">10 chapters, 76 videos 🎥, 78 web pages 🌐, 61 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/audio-course/fr/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-audio-learn.png" alt="Audio Course">
      <span class="course-card__chip">Audio</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Hugging Face Audio Course</h3>
      <div class="course-card__stats">8 units, 46 web pages 🌐</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/learn/agents-course/fr" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero">
      <img src="/assets/images/cours/hf-agents-learn.png" alt="AI Agents Course">
      <span class="course-card__chip">AI Agents</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Hugging Face AI Agents Course</h3>
      <div class="course-card__stats">4 units (+ 3 bonus), 74 web pages 🌐, 16 notebooks 📓</div>
    </div>
  </a>
  
  <a class="course-card" href="https://lbourdois.github.io/diffusion-course/" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero course-card__hero--diffusion">
      <img src="/assets/images/cours/hf-diffusion-huggy.png" alt="Diffusion Course">
      <span class="course-card__chip">Diffusion</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Hugging Face Diffusion Models Course</h3>
      <div class="course-card__stats">4 units, 17 web pages 🌐, 8 notebooks 📓</div>
    </div>
  </a>

  <a class="course-card" href="https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM" target="_blank" rel="noopener noreferrer">
    <div class="course-card__hero course-card__hero--guide">
      <img src="/assets/images/cours/hf-evaluate-banner.png" alt="LLM Evaluation Guide">
      <span class="course-card__chip">Evaluation</span>
    </div>
    <div class="course-card__body">
      <h3 class="course-card__title">Clémentine Fourrier's LLM Evaluation Guide</h3>
      <div class="course-card__stats">5 chapters, 30 web pages 🌐, 3 notebooks 📓</div>
    </div>
  </a>
</div>
