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
  --tl-accent:        #1a6b8a;
  --tl-accent-light:  #e0f4f8;
  --tl-dot-empty:     #b0aaa2;
  --tl-dot-active:    #1a6b8a;
  --tl-shadow-sm:     0 1px 4px rgba(0,0,0,0.10);
  --tl-shadow-hover:  0 6px 20px rgba(0,0,0,0.15);
  --tl-card-bg:       #ffffff;
  --tl-panel-bg:      #ffffff;
  --tl-tag-text:      #1a6b8a;
  --tl-tag-bg:        #e0f4f8;
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
    --tl-accent:        #4db8d4;
    --tl-accent-light:  #0d2f3a;
    --tl-dot-empty:     #55555f;
    --tl-dot-active:    #4db8d4;
    --tl-shadow-sm:     0 1px 4px rgba(0,0,0,0.40);
    --tl-shadow-hover:  0 6px 20px rgba(0,0,0,0.55);
    --tl-card-bg:       #2a2a32;
    --tl-panel-bg:      #2a2a32;
    --tl-tag-text:      #4db8d4;
    --tl-tag-bg:        #0d2f3a;
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
    2019: {
      1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],
      11:[
        { label: 'Illustration du <i>bag-of-words</i>', emoji: '👜', details: { title: 'Illustration du bag-of-words', body: ['Le <i>bag-of-words</i> (sac de mots en français) est la technique qui était majoritairement utilisée avant l\'apparition des modèles basés sur les réseaux de neurones tels que les RNN.', 'Premier article de la série NLP du blog.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Bag-of-word/' }] } },
        { label: 'Illustration du <i>word embedding</i> et de Word2Vec', emoji: '📏', details: { title: 'Illustration du word embedding et de Word2Vec', body: ['Illustration du word embedding et d\'une de ses applications : le word2vec de Google.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/word_embedding/' }] } },
        { label: 'Illustration des RNN, LSTM, GRU et ELMo', emoji: '➿', details: { title: 'Les RNN, LSTM, GRU et ELMo', body: ['Illustration des réseaux de neurones récurrents, des Long short-term memory, des Gated Recurrent Unit et de ELMo.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/RNN-LSTM-GRU-ELMO/' }] } },
        { label: 'Le Seq2Seq et le processus d\'attention', emoji: '🎯', details: { title: 'Le Seq2Seq et le processus d\'attention', body: ['Illustration du principe de séquence vers séquence et du processus d\'attention en traitement du langage naturel.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Seq2seq-et-attention/' }] } },
        { label: 'Illustration du Transformer', emoji: '🤖', details: { title: 'Illustration du Transformer', body: ['Illustration du modèle Transformer de Vaswani et al.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Transformer/' }] } }
      ],
      12:[
        { label: 'Illustration de BERT', emoji: '🧸', details: { title: 'Illustration de BERT', body: ['Illustration du modèle BERT de Devlin et al. et de ses dérivés français : CamemBERT et FlauBERT.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/BERT/' }] } },
        { label: 'Illustration du GPT-2', emoji: '💬', details: { title: 'Illustration du GPT-2', body: ['Illustration du modèle GPT-2 de Radford et al.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/GPT2/' }] } }
      ]
    },
    2020: {
      1:[],2:[],3:[],
      4:[
        { label: 'Les architectures issues du Transformer', emoji: '🔤', details: { title: 'Les architectures issues du Transformer', body: ['Aperçu des architectures basées sur le Transformer de Vaswani et al.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Les-architectures-transformers/' }] } },
        { label: 'Tâches et jeux de données en NLP', emoji: '📚', details: { title: 'Tâches et jeux de données en NLP', body: ['Tâches et jeux de données fréquemment utilisés dans les publications de NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Taches-et-jeux-de-donnees-en-NLP/' }] } }
      ],
      5:[
        { label: 'Prétraitement et tokenizers en NLP', emoji: '✂️', details: { title: 'Prétraitement et tokenizers en NLP', body: ['Illustration des divers prétraitements réalisables en NLP ainsi que des différents tokenizers fréquemment utilisés.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Les-tokenizers/' }] } }
      ],
      6:[
        { label: 'Illustration du Reformer', emoji: '🕶️', details: { title: 'Illustration du Reformer', body: ['Illustration du modèle Reformer de Kitaev et Kaiser.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Reformer/' }] } },
        { label: 'Illustration d\'ALBERT', emoji: '🧠', details: { title: 'Illustration d\'ALBERT', body: ['Illustration du modèle ALBERT de Lan et al.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/ALBERT/' }] } }
      ],
      7:[],8:[],9:[],10:[],
      11:[
        { label: 'L\'augmentation de données en NLP', emoji: '📈', details: { title: 'L\'augmentation de données en NLP', body: ['Un aperçu des techniques disponibles pour réaliser de l\'augmentation de données textuelles en traitement du langage naturel.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Data-augmentation-in-NLP/' }] } }
      ],
      12:[]
    },
    2021: {
      1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],
      11:[
        { label: 'Cours NYU — Yann LeCun & Alfredo Canziani (éd. 2020)', emoji: '🎓', details: { title: 'Cours de deep learning NYU (éd. 2020)', body: ['Traduction française du cours sur l\'apprentissage profond (édition 2020) de Yann LeCun et Alfredo Canziani.', '19 unités — 33 vidéos (~45h), 74 pages web, 16 notebooks Jupyter (PyTorch).'], links: [{ label: 'Site dédié', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-nyu/' }] } }
      ],
      12:[]
    },
    2022: {
      1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],
      10:[
        { label: 'Cours NYU — Yann LeCun & Alfredo Canziani (éd. 2021)', emoji: '🎓', details: { title: 'Cours de deep learning NYU (éd. 2021)', body: ['Traduction française du cours sur l\'apprentissage profond (édition 2021) de Yann LeCun et Alfredo Canziani.'], links: [{ label: 'Site dédié', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-21-nyu/' }] } }
      ],
      11:[
        { label: 'Traduction du cours NLP de Hugging Face', emoji: '🤗', details: { title: 'Cours NLP — Hugging Face', body: ['Traduction du cours de traitement automatique du langage de Hugging Face.', '10 chapitres — 76 vidéos (~5h), 78 pages web, 61 notebooks Jupyter (PyTorch & TensorFlow).'], links: [{ label: 'Commencer à apprendre', url: 'https://huggingface.co/learn/nlp-course/fr/chapter1/1' }] } }
      ],
      12:[]
    },
    2023: {
      1:[],2:[],3:[],4:[],5:[],6:[],
      7:[
        { label: 'Introduction aux SSM et au S4', emoji: '〽️', details: { title: 'Introduction aux SSM et au S4', body: ['Bases des State Space Models en apprentissage profond, illustrées via le modèle S4.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/ssm/introduction_ssm/' }] } },
        { label: 'Historique des SSM en 2022', emoji: '📖', details: { title: 'Historique des SSM en 2022', body: ['Revue de littérature des State Space Models parus lors de l\'année 2022.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/ssm/ssm_en_2022/' }] } }
      ],
      8:[
        { label: 'Traduction du cours audio de Hugging Face', emoji: '🤗', details: { title: 'Cours audio — Hugging Face', body: ['Traduction du cours d\'audio de Hugging Face. 8 unités — 46 pages web.'], links: [{ label: 'Lire le cours', url: 'https://huggingface.co/learn/audio-course/fr/' }] } },
        { label: 'Jeux de données audio pour le français', emoji: '🎵', details: { title: 'Jeux de données audio pour le français', body: ['Référencement de jeux de données pour pré-entraîner un modèle audio puis le fine-tuner sur une tâche particulière.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/audio/dataset_audio_fr/' }] } },
        { label: 'Traduction du cours diffusion de Hugging Face', emoji: '🤗', details: { title: 'Cours diffusion — Hugging Face', body: ['Traduction du cours sur les modèles de diffusion de Hugging Face. 4 chapitres — 17 pages web, 8 notebooks Jupyter.'], links: [{ label: 'Commencer à apprendre', url: 'https://github.com/huggingface/diffusion-models-class/tree/main/units/fr' }] } }
      ],
      9:[
        { label: 'QAmemBERT (110M ou 336M params, 512 tokens)', emoji: '❓', details: { title: 'QAmemBERT', body: ['Première version des modèles de Question Answering en français. Disponibles en taille base (110M) et large (336M), contexte de 512 tokens. Téléchargé plus de 160 000 fois.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91' }, { label: 'Article de blog', url: 'https://lbourdois.github.io/blog/QA/' }] } },
        { label: 'DFP — Dataset of French Prompts', emoji: '📝', details: { title: 'Dataset of French Prompts (DFP)', body: ['113 129 978 lignes portant sur 30 tâches de NLP différentes.', '724 prompts écrits sous forme impérative, de tutoiement et de vouvoiement. Téléchargé plus de 90 000 fois.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/DFP' }] } }
      ],
      10:[
        { label: 'frenchSUM — French Summarization dataset', emoji: '📄', details: { title: 'frenchSUM', body: ['Jeu de données de résumé automatique en français.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ' }] } },
        { label: 'Évolution des SSM en 2023', emoji: '〽️', details: { title: 'Évolution des SSM en 2023', body: ['Revue de littérature des State Space Models parus lors de l\'année 2023.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/ssm/ssm_en_2023/' }] } }
      ],
      11:[],12:[]
    },
    2024: {
      1:[
        { label: 'NERmemBERT (110M ou 336M params, 512 tokens, 3–4 entités)', emoji: '🔍', details: { title: 'NERmemBERT', body: ['Première version des modèles de Reconnaissance d\'Entités Nommées en français. Disponibles en taille base (110M) et large (336M), contexte de 512 tokens, 3 ou 4 entités. Téléchargé plus de 185 000 fois.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4' }, { label: 'Article de blog', url: 'https://lbourdois.github.io/blog/NER/' }] } }
      ],
      2:[
        { label: 'FAT5 v0 (Flash Attention T5)', emoji: '⚡', details: { title: 'FAT5 v0', body: ['Première version publique du FAT5 : implémentation du T5 en PyTorch avec un objectif UL2 optimisé pour GPGPU via des noyaux CUDA et Triton personnalisés.'], links: [{ label: 'GitHub', url: 'https://github.com/catie-aq/flashT5' }] } },
        { label: 'FrenchSTS — Sentence Similarity dataset', emoji: '👥', details: { title: 'FrenchSTS', body: ['Jeu de données de similarité sémantique (Sentence Textual Similarity) en français.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ' }] } }
      ],
      3:[],
      4:[
        { label: 'French QA & résumé — longues séquences (8K–256K tokens)', emoji: '📏', details: { title: 'French QA & summarization — longues séquences', body: ['Jeux de données de Question Answering et de résumé automatique en français pour de longues séquences (8K à 256K tokens).'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ' }] } },
        { label: 'Article : toujours vérifier la qualité des datasets', emoji: '🔬', details: { title: 'Toujours vérifier la qualité des jeux de données', body: ['Article sur le problème des fuites et des données dupliquées dans les jeux de données de NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/LLE/' }] } }
      ],
      5:[],6:[],
      7:[
        { label: '🔒 In the vault (not yet public)', emoji: '🔒', details: { title: 'En attente de publication', body: ['Projet finalisé mais en attente d\'autorisation pour sa mise en ligne.'], links: [] } }
      ],
      8:[],9:[],10:[],
      11:[
        { label: 'QAmemBERTa (111M params, 1 024 tokens)', emoji: '❓', details: { title: 'QAmemBERTa', body: ['Modèle de Question Answering en français basé sur CamemBERTa, 111M paramètres, contexte de 1 024 tokens.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91' }] } },
        { label: 'NERmemBERTa (111M params, 1 024 tokens)', emoji: '🔍', details: { title: 'NERmemBERTa', body: ['Modèle de Reconnaissance d\'Entités Nommées en français basé sur CamemBERTa, 111M paramètres, contexte de 1 024 tokens.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4' }] } }
      ],
      12:[]
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
