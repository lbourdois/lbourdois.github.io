---
permalink: /projets/
title: "Projets"
classes: wide
sidebar: false
---

<style>
/* ── Forcer la pleine largeur (repris de l'original) ── */
.page__content {
  max-width: 100% !important;
  width: 100% !important;
}
.page {
  max-width: 100% !important;
  width: 100% !important;
}

/* ── Variables thème clair (défaut) ── */
#tl-wrap {
  --tl-border:        #d0ccc6;
  --tl-border-strong: #b0aaa2;
  --tl-text:          #1a1814;
  --tl-secondary:     #5a5550;
  --tl-muted:         #9a938c;
  --tl-accent:        #2d6a4f;
  --tl-accent-light:  #e8f5ee;
  --tl-dot-empty:     #b0aaa2;
  --tl-dot-active:    #2d6a4f;
  --tl-shadow-sm:     0 1px 4px rgba(0,0,0,0.10);
  --tl-shadow-hover:  0 6px 20px rgba(0,0,0,0.15);
  --tl-card-bg:       #ffffff;
  --tl-panel-bg:      #ffffff;
  --tl-tag-text:      #2d6a4f;
  --tl-tag-bg:        #e8f5ee;
  --tl-tab-active-bg: #1a1814;
  --tl-tab-active-fg: #ffffff;
  --tl-radius:        9px;
  --tl-panel-w:       340px;
  font-family: inherit;
  font-size: 15px;
  line-height: 1.5;
  color: var(--tl-text);
  width: 100%;
}

/* ── Variables thème sombre ── */
@media (prefers-color-scheme: dark) {
  #tl-wrap {
    --tl-border:        #3a3a42;
    --tl-border-strong: #55555f;
    --tl-text:          #e8e6e0;
    --tl-secondary:     #b0adb8;
    --tl-muted:         #72707a;
    --tl-accent:        #52b788;
    --tl-accent-light:  #1a3528;
    --tl-dot-empty:     #55555f;
    --tl-dot-active:    #52b788;
    --tl-shadow-sm:     0 1px 4px rgba(0,0,0,0.40);
    --tl-shadow-hover:  0 6px 20px rgba(0,0,0,0.55);
    --tl-card-bg:       #2a2a32;
    --tl-panel-bg:      #2a2a32;
    --tl-tag-text:      #52b788;
    --tl-tag-bg:        #1a3528;
  }
}

/* ── Reset local uniquement dans #tl-wrap ── */
#tl-wrap *, #tl-wrap *::before, #tl-wrap *::after {
  box-sizing: border-box;
}
#tl-wrap p, #tl-wrap h2, #tl-wrap h3 {
  margin: 0; padding: 0;
}

/* ── Layout principal ── */
#tl-layout {
  display: flex;
  align-items: flex-start;
  width: 100%;
  gap: 0;
}

#tl-col {
  flex: 1;
  min-width: 0;
}

/* ── Onglets années ── */
#tl-nav {
  display: flex;
  gap: 6px;
  flex-wrap: wrap;
  margin-bottom: 28px;
}
.tl-tab {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 12.5px;
  font-weight: 500;
  padding: 5px 16px;
  border-radius: 100px;
  border: 1.5px solid var(--tl-border-strong);
  background: transparent;
  color: var(--tl-text);
  cursor: pointer;
  transition: all 0.15s ease;
  line-height: 1.4;
  opacity: 0.65;
}
.tl-tab:hover {
  border-color: var(--tl-text);
  color: var(--tl-text);
  opacity: 1;
}
.tl-tab.tl-active {
  background: var(--tl-tab-active-bg);
  border-color: var(--tl-tab-active-bg);
  color: var(--tl-tab-active-fg);
  opacity: 1;
}

/* ── Section année ── */
.tl-year {
  display: none;
  animation: tlFadeUp 0.25s ease both;
}
.tl-year.tl-visible { display: block; }

@keyframes tlFadeUp {
  from { opacity: 0; transform: translateY(8px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ── Ligne mois ── */
.tl-row {
  display: flex;
  align-items: flex-start;
  min-height: 38px;
}
.tl-row.tl-has { min-height: 50px; }

/* Label mois */
.tl-mlabel {
  width: 72px;
  flex-shrink: 0;
  text-align: right;
  padding-right: 14px;
  padding-top: 15px;
}
.tl-mname {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 10.5px;
  font-weight: 500;
  letter-spacing: 0.07em;
  text-transform: uppercase;
  color: var(--tl-muted);
  transition: color 0.18s;
}
.tl-row:hover .tl-mname { color: var(--tl-secondary); }

/* Point */
.tl-dotcol {
  width: 20px;
  flex-shrink: 0;
  display: flex;
  justify-content: center;
  padding-top: 18px;
}
.tl-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  border: 2px solid var(--tl-dot-empty);
  background: transparent;
  transition: border-color 0.18s, background 0.18s, transform 0.18s;
  flex-shrink: 0;
}
.tl-row.tl-has .tl-dot {
  border-color: var(--tl-dot-active);
  background: var(--tl-dot-active);
}
.tl-row:hover .tl-dot { transform: scale(1.2); }

/* Entrées */
.tl-entries {
  flex: 1;
  padding: 7px 0 14px 16px;
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
  align-items: flex-start;
}

/* Carte cliquable */
.tl-card {
  display: inline-flex !important;
  align-items: flex-start;
  gap: 6px;
  background: var(--tl-card-bg) !important;
  border: 1.5px solid var(--tl-border) !important;
  border-radius: var(--tl-radius) !important;
  padding: 7px 12px !important;
  color: var(--tl-text) !important;
  font-size: 13px !important;
  line-height: 1.45 !important;
  box-shadow: var(--tl-shadow-sm) !important;
  max-width: 280px;
  cursor: pointer;
  text-decoration: none !important;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease, color 0.15s ease;
}
.tl-card:hover {
  transform: translateY(-2px);
  box-shadow: var(--tl-shadow-hover) !important;
  border-color: var(--tl-accent) !important;
  color: var(--tl-accent) !important;
}
.tl-card.tl-card-active {
  border-color: var(--tl-accent) !important;
  background: var(--tl-accent-light) !important;
  color: var(--tl-accent) !important;
  box-shadow: none !important;
  transform: none;
}
.tl-emoji {
  font-size: 14px;
  flex-shrink: 0;
  margin-top: 1px;
  line-height: 1.45;
}

/* ── Panneau détail (droite) ── */
#tl-panel {
  width: var(--tl-panel-w);
  flex-shrink: 0;
  position: sticky;
  top: 80px;
  max-height: calc(100vh - 100px);
  overflow-y: auto;
  background: var(--tl-panel-bg);
  border: 1.5px solid var(--tl-border);
  border-radius: 12px;
  padding: 30px 26px 26px;
  margin-left: 28px;
  opacity: 0;
  transform: translateX(12px);
  pointer-events: none;
  transition: opacity 0.25s ease, transform 0.3s cubic-bezier(0.22,1,0.36,1);
}
#tl-panel.tl-panel-open {
  opacity: 1;
  transform: translateX(0);
  pointer-events: auto;
}

#tl-panel-close {
  position: absolute;
  top: 12px; right: 12px;
  width: 26px; height: 26px;
  border-radius: 50%;
  border: 1.5px solid var(--tl-border);
  background: transparent;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--tl-muted);
  font-size: 14px;
  line-height: 1;
  transition: border-color 0.15s, color 0.15s;
}
#tl-panel-close:hover { border-color: var(--tl-text); color: var(--tl-text); }

.tl-panel-tag {
  display: inline-block;
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--tl-tag-text);
  background: var(--tl-tag-bg);
  border-radius: 4px;
  padding: 2px 8px;
  margin-bottom: 12px;
}

#tl-panel-title {
  font-size: 1.25rem !important;
  font-weight: 600 !important;
  letter-spacing: -0.01em;
  line-height: 1.25;
  margin-bottom: 14px !important;
  color: var(--tl-text) !important;
  border: none !important;
  padding: 0 !important;
}

#tl-panel-body {
  font-size: 13px;
  color: var(--tl-secondary);
  line-height: 1.7;
}
#tl-panel-body p + p { margin-top: 10px; }
#tl-panel-body a { color: var(--tl-accent); text-decoration: underline; }

#tl-panel-links {
  margin-top: 18px;
  display: flex;
  flex-direction: column;
  gap: 7px;
}
.tl-plink {
  display: inline-flex !important;
  align-items: center;
  gap: 6px;
  font-size: 13px !important;
  color: var(--tl-accent) !important;
  text-decoration: none !important;
  border: 1.5px solid var(--tl-accent) !important;
  border-radius: var(--tl-radius) !important;
  padding: 6px 12px !important;
  transition: background 0.15s;
  width: fit-content;
  background: transparent !important;
}
.tl-plink:hover { background: var(--tl-accent-light) !important; }
.tl-plink svg { width: 12px; height: 12px; flex-shrink: 0; }

/* ── Mobile ── */
@media (max-width: 900px) {
  #tl-layout { flex-direction: column; }
  #tl-panel {
    position: fixed;
    bottom: 0; left: 0; right: 0;
    width: 100%; max-height: 60vh;
    border-radius: 12px 12px 0 0;
    border-bottom: none;
    margin-left: 0; top: auto;
    transform: translateY(16px);
    z-index: 9999;
  }
  #tl-panel.tl-panel-open { transform: translateY(0); }
  .tl-mlabel { width: 52px; }
}
</style>

<div id="tl-wrap">
  <div id="tl-layout">
    <div id="tl-col">
      <nav id="tl-nav" aria-label="Années"></nav>
      <div id="tl-main"></div>
    </div>
    <aside id="tl-panel" aria-live="polite">
      <button id="tl-panel-close" title="Fermer">&#x2715;</button>
      <div id="tl-panel-tag" class="tl-panel-tag"></div>
      <h2 id="tl-panel-title"></h2>
      <div id="tl-panel-body"></div>
      <div id="tl-panel-links"></div>
    </aside>
  </div>
</div>

<script>
(function () {
  var MONTHS   = ['Jan','Fév','Mar','Avr','Mai','Jun','Jul','Aoû','Sep','Oct','Nov','Déc'];
  var MONTHS_L = ['Janvier','Février','Mars','Avril','Mai','Juin','Juillet','Août','Septembre','Octobre','Novembre','Décembre'];
  var ICON     = '<svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3H3a1 1 0 00-1 1v9a1 1 0 001 1h9a1 1 0 001-1v-3M10 2h4m0 0v4m0-4L7 9"/></svg>';

  /* ════════════════════════════════════════════════════════════════
     DATA
     Chaque entrée : { label, emoji, details? }
     details : { title?, body: [paragraphes HTML], links?: [{label,url}] }
  ════════════════════════════════════════════════════════════════ */
  var DATA = {
    2019: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] },
    2020: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] },
    2021: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] },
    2022: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] },
    2023: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] },
    2024: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] },
    2025: {
      1: [{
        label: 'FAT5 (official release)', emoji: '⚡',
        details: {
          title: 'FAT5',
          body: [
            'Le FAT5 est une implémentation du <a href="https://arxiv.org/abs/1910.10683">T5</a> en PyTorch avec un objectif <a href="https://arxiv.org/abs/2205.05131">UL2</a> optimisé pour GPGPU, développé avec <a href="https://b-albar.github.io/portfolio/">Boris Albar</a>.',
            'Elle utilise des noyaux CUDA et Triton personnalisés ainsi que des optimisations spécifiques pour augmenter le débit et réduire l\'utilisation de la mémoire d\'un facteur 2 par rapport à l\'implémentation originale de Hugging Face.',
            'Nous l\'avons appliquée en pré-entraînant un modèle en français de 147M paramètres sur une seule A100, pour un coût estimé à 1 200 € (instance Sesterce).'
          ],
          links: [
            { label: 'GitHub (Apache-2.0)', url: 'https://github.com/catie-aq/flashT5' },
            { label: 'Modèle — Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-fat5-ul2-677697a35feea336389d6403' },
            { label: 'Article de blog', url: 'https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport' }
          ]
        }
      }],
      2: [
        { label: 'French VQA datasets', emoji: '🎯', details: { title: 'French VQA datasets', body: ['Jeux de données de Visual Question Answering en français, destinés à l\'entraînement de VLM.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-vqa-datasets-67c8d1a162a23ef0e9a2bc89' }] } },
        { label: 'French caption datasets', emoji: '🖌️', details: { title: 'French caption datasets', body: ['Jeux de données de description d\'images (captioning) en français.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-caption-datasets-67c8d2227284a5daa00c50b9' }] } },
        { label: 'French visual retriever datasets', emoji: '🐶', details: { title: 'French visual retriever datasets', body: ['Jeux de données de recherche visuelle (visual retrieval) en français, destinés à l\'entraînement de modèles multimodaux.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-ocr-datasets-67c8d3152330f11227e0d108' }] } }
      ],
      3: [
        { label: 'Traduction FR du LLM Evaluation guidebook', emoji: '⚖️', details: { title: 'Guide d\'évaluation des LLM', body: ['Traduction française du guide d\'évaluation des LLM rédigé par <a href="https://huggingface.co/clefourrier">Clémentine Fourrier</a>. Le contenu est structuré en 5 chapitres répartis sur 30 pages web et 3 notebooks Jupyter.'], links: [{ label: 'Lire le guide', url: 'https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM' }] } }
      ],
      4: [
        { label: 'ModernQAmembert (136M params, 8 192 tokens)', emoji: '❓', details: { title: 'ModernQAmembert', body: ['Modèle de Question Answering en français basé sur ModernBERT, 136M paramètres, contexte de 8 192 tokens. Téléchargé plus de 160 000 fois.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91' }, { label: 'Article de blog', url: 'https://lbourdois.github.io/blog/QA/' }] } },
        { label: 'modernNERmemBERT (136M params, 8 192 tokens)', emoji: '🔍', details: { title: 'modernNERmemBERT', body: ['Modèle de Reconnaissance d\'Entités Nommées en français basé sur ModernBERT, 136M paramètres, contexte de 8 192 tokens, reconnaissant 3 ou 4 entités. Téléchargé plus de 185 000 fois.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4' }, { label: 'Article de blog', url: 'https://lbourdois.github.io/blog/NER/' }] } }
      ],
      5: [],
      6: [
        { label: 'NanoBEIR-fr (évaluation IR en français)', emoji: '🏆', details: { title: 'NanoBEIR-fr', body: ['Benchmark d\'évaluation de la recherche d\'information (Information Retrieval) en français, inspiré de NanoBEIR.'], links: [] } },
        { label: 'XMrec datasets — partie française', emoji: '🛒', details: { title: 'XMrec (partie française)', body: ['Partie française du jeu de données XMrec, destiné à l\'évaluation des systèmes de recommandation multilingues.'], links: [] } }
      ],
      7: [
        { label: 'French sparse embedding V0', emoji: '✏️', details: { title: 'French sparse embedding V0', body: ['Premier modèle d\'embedding sparse entraîné spécifiquement pour le français.'], links: [] } },
        { label: 'FrenchNLI', emoji: '➡️', details: { title: 'FrenchNLI', body: ['Jeu de données d\'inférence en langage naturel (Natural Language Inference) en français.'], links: [] } },
        { label: 'French table-to-text datasets', emoji: '📋', details: { title: 'French table-to-text datasets', body: ['Jeux de données de génération de texte à partir de tableaux structurés, en français.'], links: [] } }
      ],
      8: [
        { label: 'French dense embedding', emoji: '✏️', details: { title: 'French dense embedding', body: ['Modèle d\'embedding dense entraîné spécifiquement pour le français.'], links: [] } }
      ],
      9: [
        { label: 'Traduction FR du cours AI Agents (Hugging Face)', emoji: '🤗', details: { title: 'Cours AI Agents — Hugging Face', body: ['Traduction française du cours sur les agents IA de Hugging Face, réalisée avec <a href="https://github.com/knoel99">Kim Noel</a>. Le contenu est structuré en 4 unités (+ 3 bonus) réparties sur 74 pages web et 16 notebooks Jupyter.'], links: [{ label: 'Lire le cours', url: 'https://huggingface.co/learn/agents-course/fr' }] } }
      ],
      10: [
        { label: 'French DPO and conversation datasets', emoji: '🤝', details: { title: 'French DPO & conversation datasets', body: ['Jeux de données de préférences (DPO) et de conversations en français, destinés au fine-tuning de LLM.'], links: [] } },
        { label: 'French think and toolcalling datasets', emoji: '🔧', details: { title: 'French think & toolcalling datasets', body: ['Jeux de données de raisonnement et d\'appel d\'outils (tool calling) en français.'], links: [] } }
      ],
      11: [
        { label: 'French summarization models', emoji: '💧', details: { title: 'French summarization models', body: ['Modèles de résumé automatique de texte en français.'], links: [] } }
      ],
      12: [
        { label: 'French paraphrases pack', emoji: '👥', details: { title: 'French paraphrases pack', body: ['Collection de jeux de données de paraphrase en français.'], links: [] } },
        { label: 'French simplification dataset', emoji: '👓', details: { title: 'French simplification dataset', body: ['Jeu de données de simplification de textes en français.'], links: [] } },
        { label: 'French keywords extraction dataset', emoji: '🏷️', details: { title: 'French keywords extraction dataset', body: ['Jeu de données d\'extraction de mots-clés en français.'], links: [] } }
      ]
    },
    2026: { 1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] }
  };

  /* ── Panneau ── */
  var panel      = document.getElementById('tl-panel');
  var panelTag   = document.getElementById('tl-panel-tag');
  var panelTitle = document.getElementById('tl-panel-title');
  var panelBody  = document.getElementById('tl-panel-body');
  var panelLinks = document.getElementById('tl-panel-links');
  var activeCard = null;

  function openPanel(entry, m, y) {
    var d = entry.details || {};
    panelTag.textContent = MONTHS_L[m - 1] + ' ' + y;
    panelTitle.textContent = d.title || entry.label;
    panelBody.innerHTML = '';
    (d.body || [entry.label]).forEach(function (para) {
      var p = document.createElement('p');
      p.innerHTML = para;
      panelBody.appendChild(p);
    });
    panelLinks.innerHTML = '';
    (d.links || []).forEach(function (lk) {
      var a = document.createElement('a');
      a.className = 'tl-plink';
      a.href = lk.url;
      a.target = '_blank';
      a.rel = 'noopener noreferrer';
      a.innerHTML = ICON + lk.label;
      panelLinks.appendChild(a);
    });
    panel.classList.add('tl-panel-open');
  }

  function closePanel() {
    panel.classList.remove('tl-panel-open');
    if (activeCard) { activeCard.classList.remove('tl-card-active'); activeCard = null; }
  }

  document.getElementById('tl-panel-close').addEventListener('click', closePanel);
  document.addEventListener('keydown', function (e) { if (e.key === 'Escape') closePanel(); });

  /* ── Construction ── */
  var years = Object.keys(DATA).map(Number).sort(function (a, b) { return b - a; });
  var activeYear = years[0];

  function buildSection(year) {
    var sec = document.createElement('div');
    sec.className = 'tl-year';
    sec.id = 'tl-y' + year;
    for (var m = 1; m <= 12; m++) {
      var entries = DATA[year][m] || [];
      var row = document.createElement('div');
      row.className = 'tl-row' + (entries.length ? ' tl-has' : '');

      var lbl = document.createElement('div');
      lbl.className = 'tl-mlabel';
      lbl.innerHTML = '<span class="tl-mname">' + MONTHS[m - 1] + '</span>';

      var dotCol = document.createElement('div');
      dotCol.className = 'tl-dotcol';
      dotCol.innerHTML = '<div class="tl-dot"></div>';

      row.appendChild(lbl);
      row.appendChild(dotCol);

      if (entries.length) {
        var col = document.createElement('div');
        col.className = 'tl-entries';
        entries.forEach(function (e) {
          var card = document.createElement('div');
          card.className = 'tl-card';
          card.setAttribute('role', 'button');
          card.setAttribute('tabindex', '0');
          card.innerHTML = (e.emoji ? '<span class="tl-emoji">' + e.emoji + '</span>' : '') +
                           '<span>' + e.label + '</span>';
          var clickFn = (function (entry, month, yr) {
            return function () {
              if (activeCard === card) { closePanel(); return; }
              if (activeCard) activeCard.classList.remove('tl-card-active');
              activeCard = card;
              card.classList.add('tl-card-active');
              openPanel(entry, month, yr);
            };
          })(e, m, year);
          card.addEventListener('click', clickFn);
          card.addEventListener('keydown', function (ev) {
            if (ev.key === 'Enter' || ev.key === ' ') clickFn();
          });
          col.appendChild(card);
        });
        row.appendChild(col);
      }
      sec.appendChild(row);
    }
    return sec;
  }

  var nav = document.getElementById('tl-nav');
  years.forEach(function (y) {
    var btn = document.createElement('button');
    btn.className = 'tl-tab' + (y === activeYear ? ' tl-active' : '');
    btn.textContent = y;
    btn.addEventListener('click', function () {
      document.querySelectorAll('.tl-tab').forEach(function (t) { t.classList.remove('tl-active'); });
      btn.classList.add('tl-active');
      document.querySelectorAll('.tl-year').forEach(function (s) { s.classList.remove('tl-visible'); });
      var target = document.getElementById('tl-y' + y);
      if (target) { target.classList.remove('tl-visible'); void target.offsetWidth; target.classList.add('tl-visible'); }
      activeYear = y;
      closePanel();
    });
    nav.appendChild(btn);
  });

  var mainEl = document.getElementById('tl-main');
  years.forEach(function (y) {
    var sec = buildSection(y);
    if (y === activeYear) sec.classList.add('tl-visible');
    mainEl.appendChild(sec);
  });
})();
</script>
