---
permalink: /projets/
title: "Projets"
classes: wide
sidebar: false
---

⚠️ Page en cours de restructuration

Sur cette page vous pouvez trouver les contenus sur lesquels j'ai travaillé (à titre personnel ou professionnel) mais qui sont référencés sur d'autres sites que mon blog personnel. Il s'agit principalement de traductions de cours, et des créations de jeux de données et de modèles.

<br>
  
<h2>Tous les projets</h2>

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
  --tl-panel-w:       400px;
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
  max-width: 350px;
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
        { label: 'Illustration du <i>bag-of-words</i>', emoji: '👜', details: { title: 'Illustration du bag-of-words', body: ['Le <i>bag-of-words</i> est la technique qui était majoritairement utilisée avant l’apparition des modèles basés sur les réseaux de neurones tel que les RNN (eux-mêmes moins utilisés aujourd’hui au profit des transformers). C\'est avant tout un article servant à initier la série sur les articles de blog consacré au NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Bag-of-word/' }] } },
        { label: 'Illustration du <i>word embedding</i>', emoji: '📏', details: { title: 'Illustration du word embedding', body: ['Illustration du word embedding et d\'une de ses applications : le word2vec de Google. Permet de comprendre par la suite des concepts cruciaux en NLP comme l\'autosupervisé ou ce que sont que les modèles d\'embedding énormément utilisé pour la recherche de documents / les moteurs de recherche. Il s\'agit d\'une traduction de l\'<a href="https://jalammar.github.io/illustrated-word2vec/">article de blog</a> de Jay Allamar.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/word_embedding/' }] } }
      ],
      12:[
        { label: 'Illustration des RNN, LSTM, GRU et ELMo', emoji: '➿', details: { title: 'Les RNN, LSTM, GRU et ELMo', body: ['Illustration des réseaux de neurones récurrents, des Long short-term memory, des Gated Recurrent Unit et de ELMo. Ces techniques étaient utilisées avant l\'avènement des transformers. Les passer en revue est crucial pour maîtriser des concepts toujours utilisés actuellement dans des architectures comme les SSM par exemple. Note : la partie sur ELMo est une traduction de l\'<a href="https://jalammar.github.io/illustrated-bert/">article de blog</a> de Jay Allamar.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/RNN-LSTM-GRU-ELMO/' }] } },
        { label: 'Le Seq2Seq et le processus d\'attention', emoji: '🎯', details: { title: 'Le Seq2Seq et le processus d\'attention', body: ['Illustration du principe de séquence à séquence et du processus d\'attention de Cho et al. (2014). Article de blog à absolument lire pour comprendre le mécanisme d\'attention que transformers reprennent en le parallélisant. Il s\'agit d\'une traduction de l\'<a href="https://jalammar.github.io/visualizing-neural-machine-translation-mechanics-of-seq2seq-models-with-attention/">article de blog</a> de Jay Allamar.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Seq2seq-et-attention/' }] } },
        { label: 'Illustration du Transformer', emoji: '🤖', details: { title: 'Illustration du Transformer', body: ['Illustration du modèle Transformer de Vaswani et al. (2017). Il s\'agit d\'une traduction de l\'<a href="https://jalammar.github.io/illustrated-transformer/">article de blog</a> de Jay Allamar que j\'ai ponctuellement complété. Un essentiel à lire quand on s\'initie au NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Transformer/' }] } },
        { label: 'Illustration de BERT', emoji: '🧸', details: { title: 'Illustration de BERT', body: ['Illustration du modèle BERT de Devlin et al. (2018) et de ses dérivés français : CamemBERT et FlauBERT. Il s\'agit d\'une traduction de l\'<a href="https://jalammar.github.io/illustrated-bert/">article de blog</a> de Jay Allamar que j\'ai ponctuellement complété. Un essentiel à lire quand on s\'initie au NLP pour comprendre notamment les architectures de type encodeur.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/BERT/' }] } },
        { label: 'Illustration du GPT2', emoji: '💬', details: { title: 'Illustration du GPT2', body: ['Illustration du modèle GPT-2 de Radford et al. (2019) Il s\'agit d\'une traduction de l\'<a href="https://jalammar.github.io/illustrated-gpt2/">article de blog</a> de Jay Allamar que j\'ai ponctuellement complété. Un essentiel à lire quand on s\'initie au NLP pour comprendre notamment les architectures de type décodeur.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/GPT2/' }] } }
      ]
    },
    2020: {
      1:[
        { label: 'Les architectures issues du Transformer', emoji: '🔤', details: { title: 'Les architectures issues du Transformer', body: ['Aperçu des architectures basées sur le Transformer. Cet article datant de 2020, il retrace principalement les modèles de l\'époque et est surement à présent un peu dépassé.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Les-architectures-transformers/' }] } },
        { label: 'Tâches et jeux de données en NLP', emoji: '📚', details: { title: 'Tâches et jeux de données en NLP', body: ['Tâches et jeux de données fréquemment utilisés dans les publications de NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Taches-et-jeux-de-donnees-en-NLP/' }] } },
        { label: 'Prétraitement et tokenizers en NLP', emoji: '✂️', details: { title: 'Prétraitement et tokenizers en NLP', body: ['Illustration des divers prétraitements réalisables en NLP ainsi que des différents tokenizers fréquemment utilisés. Il s\'agit d\'une traduction de l\'<a href="https://web.archive.org/web/20200330042220/https://mlexplained.com/2019/11/06/a-deep-dive-into-the-wonderful-world-of-preprocessing-in-nlp/">article de blog</a> de Keita Kurita. Un essentiel à lire quand on s\'initie au NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Les-tokenizers/' }] } }        
      ],
      2:[
        { label: 'Illustration du Reformer', emoji: '🕶️', details: { title: 'Illustration du Reformer', body: ['Illustration du modèle Reformer de Kitaev et Kaiser (2020). Il s\'agit d\'une traduction de l\'<a href="https://towardsdatascience.com/illustrating-the-reformer-393575ac6ba0'/">article de blog</a> d'Alireza Dirafzoon.], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Reformer/' }] } }        
      ],
      3:[
        { label: 'Illustration d\'ALBERT', emoji: '🧠', details: { title: 'Illustration d\'ALBERT', body: ['Illustration du modèle ALBERT de Lan et al. (2020). Il s\'agit d\'une traduction de l\'<a href="https://amitness.com/posts/albert-visual-summary'/">article de blog</a> d'Amit Chaudhary.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/ALBERT/' }] } }
      ],
      4:[],
      5:[
        { label: 'L\'augmentation de données en NLP', emoji: '📈', details: { title: 'L\'augmentation de données en NLP', body: ['Un aperçu des techniques disponibles pour réaliser de l\'augmentation de données textuelles en traitement du langage naturel. Il s\'agit d\'une traduction de l\'<a href="https://amitness.com/posts/data-augmentation-for-nlp'/">article de blog</a> d'Amit Chaudhary.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/nlp/Data-augmentation-in-NLP/' }] } }
      ],
      6:[],7:[],8:[],9:[],10:[],11:[],12:[]
    },
    2021: {
      1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],
      9:[
        { label: 'Cours de NYU par Yann LeCun & Alfredo Canziani (éd. 2020)', emoji: '🎓', details: { title: 'Cours de deep learning de la NYU (éd. 2020)', body: ['Traduction française du cours sur l\'apprentissage profond (édition 2020) de Yann LeCun et Alfredo Canziani.', '19 unités — 33 vidéos (~45h), 74 pages web, 16 notebooks Jupyter.'], links: [{ label: 'Site dédié', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-nyu/' }] } }        
      ],
      10:[], 11:[], 12:[]
    },
    2022: {
      1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],
      9:[
        { label: 'Cours de NYU par Yann LeCun & Alfredo Canziani (éd. 2021)', emoji: '🎓', details: { title: 'Cours de deep learning NYU (éd. 2021)', body: ['Traduction française du cours sur l\'apprentissage profond (édition 2021) de Yann LeCun et Alfredo Canziani.'], links: [{ label: 'Site dédié', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-21-nyu/' }] } }        
      ],
      10:[],11:[],12:[]
    },
    2023: {
      1:[
        { label: 'Cours de NLP d\'Hugging Face', emoji: '🤗', details: { title: 'Cours de NLP d\'Hugging Face', body: ['Traduction du cours de traitement automatique du langage de Hugging Face.', '10 chapitres — 76 vidéos (~5h), 78 pages web, 61 notebooks Jupyter (PyTorch & TensorFlow).'], links: [{ label: 'Commencer à apprendre', url: 'https://huggingface.co/learn/nlp-course/fr/chapter1/1' }] } }        
      ],2:[],3:[],4:[],
      5:[
        { label: 'Modèles Word2vec', emoji: '📏', details: { title: 'Modèles Word2vec', body: ['TODO'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/Word2vec' }] } }              
      ],
      6:[
        { label: 'QAmemBERT', emoji: '❓', details: { title: 'QAmemBERT', body: ['Première version des modèles de Question Answering en français. Disponibles en taille base (110M) et large (336M), contexte de 512 tokens.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/QA/' }] } },
        { label: 'Cours sur les modèles de diffusion d\'Hugging Face', emoji: '🤗', details: { title: 'Cours sur les modèles de diffusion d\'Hugging Face', body: ['Traduction du cours sur les modèles de diffusion de Hugging Face. 4 chapitres — 17 pages web, 8 notebooks Jupyter.'], links: [{ label: 'Commencer à apprendre', url: 'https://github.com/huggingface/diffusion-models-class/tree/main/units/fr' }] } }
      ],
      7:[
        { label: 'Cours d\'audio d\'Hugging Face', emoji: '🤗', details: { title: 'Cours d\'audio d\'Hugging Face', body: ['Traduction du cours d\'audio de Hugging Face. 8 unités — 46 pages web.'], links: [{ label: 'Commencer à apprendre', url: 'https://huggingface.co/learn/audio-course/fr/' }] } }        
      ],
      8:[],
      9:[
        { label: 'Cours de NYU par Yann LeCun & Alfredo Canziani (version finale)', emoji: '🎓', details: { title: 'Cours de deep learning NYU (version finale)', body: ['Traduction française du cours sur l\'apprentissage profond (édition 2021) de Yann LeCun et Alfredo Canziani.'], links: [{ label: 'Site dédié', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-21-nyu/' }] } },
        { label: 'Dataset of French Prompts (DFP)', emoji: '📝', details: { title: 'Dataset of French Prompts (DFP)', body: ['113 129 978 lignes portant sur 30 tâches de NLP différentes.', '724 prompts écrits sous forme impérative, de tutoiement et de vouvoiement. Téléchargé plus de 90 000 fois.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/DFP' }] } }
      ],
      10:[
        { label: 'frenchSUM — French Summarization dataset', emoji: '📄', details: { title: 'frenchSUM', body: ['Jeu de données de résumé automatique en français.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/frenchSUM' }] } }
      ],
      11:[],12:[
        { label: 'Jeux de données audio pour le français', emoji: '🎵', details: { title: 'Jeux de données audio pour le français', body: ['Référencement de jeux de données pour pré-entraîner un modèle audio puis le fine-tuner sur une tâche particulière.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/audio/dataset_audio_fr/' }] } },
        { label: 'Introduction aux SSM et au S4', emoji: '〽️', details: { title: 'Introduction aux SSM et au S4', body: ['Bases des State Space Models en apprentissage profond, illustrées via le modèle S4.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/ssm/introduction_ssm/' }] } }
      ]
    },
    2024: {
      1:[
        { label: 'NERmemBERT', emoji: '🔍', details: { title: 'NERmemBERT', body: ['Première version des modèles de Reconnaissance d\'Entités Nommées en français. Disponibles en taille base (110M) et large (336M), contexte de 512 tokens, 3 ou 4 entités. Téléchargé plus de 185 000 fois.'], links: [{ label: 'Hugging Face CATIE', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/NER/' }] } }
      ],
      2:[
        { label: 'FrenchSTS', emoji: '👥', details: { title: 'FrenchSTS', body: ['Jeu de données de similarité sémantique (Sentence Textual Similarity) en français.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ' }] } },
        { label: 'Toujours vérifier la qualité des datasets', emoji: '🔬', details: { title: 'Toujours vérifier la qualité des jeux de données', body: ['Article sur le problème des fuites et des données dupliquées dans les jeux de données de NLP.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/LLE/' }] } }
      ],
      3:[],
      4:[
          { label: 'Historique des SSM en 2022', emoji: '📖', details: { title: 'Historique des SSM en 2022', body: ['Revue de littérature des State Space Models parus lors de l\'année 2022.'], links: [{ label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/ssm/ssm_en_2022/' }] } },
        { label: 'French QA & résumé longues séquences', emoji: '📏', details: { title: 'French QA & résumé longues séquences', body: ['Jeux de données de Question Answering et de résumé automatique en français pour de longues séquences (8K à 256K tokens).'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-long-sequences-datasets' }] } }
      ],
      5:[],6:[],7:[],
      8:[
        { label: 'Les papiers de Merve', emoji: '📷', details: { title: 'Les papiers de Merve', body: [''], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/spaces/merve/vision_papers' }] } }        
      ],
      9:[],10:[],
      11:[
        { label: 'QAmemBERTa', emoji: '❓', details: { title: 'QAmemBERTa', body: ['Modèle de Question Answering en français basé sur CamemBERTa, 111M paramètres, contexte de 1 024 tokens.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack' }] } },
        { label: 'NERmemBERTa', emoji: '🔍', details: { title: 'NERmemBERTa', body: ['Modèle de Reconnaissance d\'Entités Nommées en français basé sur CamemBERTa, 111M paramètres, contexte de 1 024 tokens.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack' }] } }
      ],
      12:[]
        },
    2025: {
      1: [{
        label: 'FAT5 (Flash Attention T5)', emoji: '⚡',
        details: {
          title: 'FAT5 (Flash Attention T5)',
          body: [
            'Le FAT5 est une implémentation du <a href="https://arxiv.org/abs/1910.10683">T5</a> en PyTorch avec un objectif <a href="https://arxiv.org/abs/2205.05131">UL2</a> optimisé pour GPGPU, développé avec <a href="https://b-albar.github.io/portfolio/">Boris Albar</a>.',
            'Elle utilise des noyaux CUDA et Triton personnalisés ainsi que des optimisations spécifiques pour augmenter le débit et réduire l\'utilisation de la mémoire d\'un facteur 2 par rapport à l\'implémentation originale de Hugging Face.',
            'Nous l\'avons appliquée en pré-entraînant un modèle en français de 147M paramètres sur une seule A100, pour un coût estimé à 1 200 € (instance Sesterce).'
          ],
          links: [
            { label: 'GitHub (Apache-2.0)', url: 'https://github.com/catie-aq/flashT5' },
            { label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-fat5-ul2' },
            { label: 'Lire l\'article', url: 'https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport' }
          ]
        }
      }],
      2: [
         { label: 'Un guide visuel sur la quantification', emoji: '🗜️', details: { title: 'Un guide visuel sur la quantification', body: ['TODO'], links: [ { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/Quantification/' }] } },
        { label: 'French VQA datasets', emoji: '🎯', details: { title: 'French VQA datasets', body: ['Jeux de données de <i>Visual Question Answering</i> en français, destinés à l\'entraînement de VLM.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-vqa-datasets' }] } },
        { label: 'French caption datasets', emoji: '🖌️', details: { title: 'French caption datasets', body: ['Jeux de données de description d\'images (<i>captioning</i>) en français.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-caption-datasets' }] } },
        { label: 'French visual retriever datasets', emoji: '🐶', details: { title: 'French visual retriever datasets', body: ['Jeux de données de recherche visuelle (visual retrieval) en français, destinés à l\'entraînement de modèles multimodaux.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-ocr-datasets' }] } }
      ],
      3: [
        { label: 'Guide d\'évaluation des LLM</i>', emoji: '⚖️', details: { title: 'Guide d\'évaluation des LLM', body: ['Traduction française du guide d\'évaluation des LLM rédigé par <a href="https://huggingface.co/clefourrier">Clémentine Fourrier</a>. Le contenu est structuré en 5 chapitres répartis sur 30 pages web et 3 notebooks Jupyter.'], links: [{ label: 'Lire le guide', url: 'https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM' }] } }
      ],
      4: [
       { label: 'Un guide visuel sur le mélange d\'experts (MoE)', emoji: '🥼', details: { title: 'Un guide visuel sur le mélange d\'experts (MoE)', body: ['TODO'], links: [ { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/MoE/' }] } },
        { label: 'ModernQAmemBERT', emoji: '❓', details: { title: 'ModernQAmemBERT', body: ['Modèle de <i>Question Answering</i> en français basé sur le ModernCamemBERT de 136M paramètres et de taille de contexte de 8 192 <i>tokens</i>.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack' }, { label: 'Article de blog', url: 'https://lbourdois.github.io/blog/QA/' }] } },
        { label: 'ModernNERmemBERT', emoji: '🔍', details: { title: 'modernNERmemBERT', body: ['Modèle de Reconnaissance d\'Entités Nommées en français basé sur le ModernCamemBERT de 136M paramètres et de taille de contexte de 8 192 <i>tokens</i>, reconnaissant 3 ou 4 entités.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack' }, { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/NER/' }] } }
      ],
      5: [
       { label: 'Un guide visuel sur les LLM avec raisonnement', emoji: '🧠', details: { title: 'Un guide visuel sur les LLM avec raisonnement', body: ['TODO'], links: [ { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/LLM_raisonnement/' }] } },
      ],
      6: [
        { label: 'Un guide visuel sur les agents IA', emoji: '🤖', details: { title: 'Un guide visuel sur les agents IA', body: ['TODO'], links: [ { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/LLM_Agents/' }] } },
        { label: 'NanoBEIR-fr', emoji: '🍺', details: { title: 'NanoBEIR-fr', body: ['Benchmark d\'évaluation de la recherche d\'information (Information Retrieval) en français, inspiré de NanoBEIR.'], links: [] } },
        { label: 'XMrec datasets (partie en français)', emoji: '🛒', details: { title: 'French XMrec', body: ['Partie en français du jeu de données XMrec, destiné à l\'évaluation des systèmes de recommandation multilingues.'], links: [] } }
      ],
      7: [
        { label: 'French sparse embedding V0', emoji: '✏️', details: { title: 'French sparse embedding V0', body: ['Premier modèle d\'embedding sparse entraîné spécifiquement pour le français.'], links: [] } },
        { label: 'FrenchNLI', emoji: '➡️', details: { title: 'FrenchNLI', body: ['Jeu de données d\'inférence en langage naturel (Natural Language Inference) en français.'], links: [] } },
        { label: 'French table-to-text datasets', emoji: '𝄜', details: { title: 'French table-to-text datasets', body: ['Jeux de données de génération de texte à partir de tableaux structurés, en français.'], links: [] } }
      ],
      8: [
        { label: 'French dense embedding', emoji: '✏️', details: { title: 'French dense embedding', body: ['Modèle d\'embedding dense entraîné spécifiquement pour le français.'], links: [] } }
      ],
      9: [
        { label: 'Cours sur les Agents IA d\'Hugging Face', emoji: '🤗', details: { title: 'Cours sur les Agents IA d\'Hugging Face', body: ['Traduction française du cours sur les agents IA de Hugging Face, réalisée avec <a href="https://github.com/knoel99">Kim Noel</a>. Le contenu est structuré en 4 unités (+ 3 bonus) réparties sur 74 pages web 🌐 et 16 notebooks Jupyter 📓.'], links: [{ label: 'Commencer à apprendre', url: 'https://huggingface.co/learn/agents-course/fr' }] } }
      ],
      10: [
        { label: 'Statistiques des modèles des 50 entités les plus téléchargés sur Hugging Face', emoji: '📊', details: { title: 'Statistiques des modèles des 50 entités les plus téléchargés sur Hugging Face', body: ['TODO'], links: [ { label: 'Lire l\'article', url: 'https://lbourdois.github.io/blog/HF_stats_models/' }] } },
        { label: 'French DPO and conversation datasets', emoji: '🤝', details: { title: 'French DPO & conversation datasets', body: ['Jeux de données de préférences (DPO) et de conversations en français, destinés au fine-tuning de LLM.'], links: [] } },
        { label: 'French think and toolcalling datasets', emoji: '🔧', details: { title: 'French think & toolcalling datasets', body: ['Jeux de données de raisonnement et d\'appel d\'outils (tool calling) en français.'], links: [] } },
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
    2026: { 1:[],2:[],3:[],
           4:[
             { label: 'Release in progress', emoji: '👀', details: { title: 'Release in progress', body: ['Release in progress.'], links: [] } }
           ],5:[],6:[],7:[],8:[],9:[],10:[],11:[],12:[] }
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

<br><br>

<div style="width: 100%; margin: 0; padding: 0;">

<h2>Projets principaux</h2>

<h3>Modèles et jeux de données en français</h3>

<h4>FAT5</h4>
<p>Le FAT5 est une implémentation du <a href="https://arxiv.org/abs/1910.10683">T5</a> en PyTorch avec un objectif <a href="https://arxiv.org/abs/2205.05131">UL2</a> optimisé pour GPGPU développé avec <a href="https://b-albar.github.io/portfolio/">Boris ALBAR</a>.<br>
Elle utilise des noyaux CUDA et Triton personnalisés ainsi que des optimisations spécifiques pour augmenter le débit et réduire l'utilisation de la mémoire pour l'entraînement et l'inférence d'un facteur 2 par rapport à l'implémentation originale disponible dans Hugging Face.<br>
Nous l'avons appliquée en pré-entraînant un modèle en français de 147M paramètres en utilisant uniquement une A100. Nous estimons ainsi pouvoir ramener le prix de pré-entraînement d'un tel modèle à seulement 1200€ (estimation faite sur une instance Sesterce).<br>
Le code de pré-entrainement est disponible sur <a href="https://github.com/catie-aq/flashT5">GitHub</a> sous licence Apache-2.0 et les poids du modèle entraîné sur le compte <a href="https://huggingface.co/collections/CATIE-AQ/catie-french-fat5-ul2-677697a35feea336389d6403">Hugging Face du CATIE</a>. Un article de blog détaillant notre méthodologie est disponible <a href="https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport">ici</a>.</p>

<h4>NER</h4>
<p>Les NERmemBERT constituent une famille de modèles de Reconnaissance d'Entités Nommées en français capable d'étiqueter jusqu'à 4 entités (Personnalités, Lieux, Organisations, Divers tel que des noms d'œuvre, de maladies, etc.). Ils sont disponibles en taille base (110M ou 136M de paramètres) et large (336M), gérant des contextes allant de 512 à 8192 tokens. Les poids sont disponibles gratuitement en open-source, tout comme les jeux de données ayant servis à l'entraînement. Le tout est disponible sur le compte <a href="https://huggingface.co/collections/CATIE-AQ/catie-french-ner-pack-658aefafe3f7a2dcf0e4dbb4">Hugging Face du CATIE</a>. Un article de blog détaillant la méthodologie adoptée est disponible <a href="https://lbourdois.github.io/blog/NER/">ici</a>.<br>
Ils ont été téléchargés plus de 185 000 fois depuis leur mise en ligne.</p>

<h4>Question Answering</h4>
<p>Les QAmemBERT constituent une famille de réponse aux questions en français capable d'indiquer si la réponse à une question est présente ou pas dans un texte de contexte associé. Ils sont disponibles en taille base (110M ou 136M de paramètres) et large (335M), gérant des contextes allant de 512 à 8192 tokens. Les poids sont disponibles gratuitement en open-source, tout comme le jeu de données ayant servis à l'entraînement. Le tout est disponible sur le compte <a href="https://huggingface.co/collections/CATIE-AQ/catie-french-qa-pack-650821750f44c341cdb8ec91">Hugging Face du CATIE</a>. Un article de blog détaillant la méthodologie adoptée est disponible <a href="https://lbourdois.github.io/blog/QA/">ici</a>.<br>
Ils ont été téléchargés plus de 160 000 fois depuis leur mise en ligne.</p>

<h4>DFP</h4>
<p><em>Dataset of French Prompts</em> (DFP) contient 113 129 978 lignes portant sur 30 tâches de NLP différentes.<br>
724 prompts ont été écrits sous forme impérative, de tutoiement et de vouvoiement afin de couvrir autant que possible les données de pré-entraînement utilisées par le modèle qui utilisera ces données et qui nous sont inconnues.</p>

<p>Les colonnes <em>inputs</em> et <em>targets</em> suivent le même format que l'ensemble de données <a href="https://huggingface.co/datasets/bigscience/xP3">xP3</a> de Muennighoff et al.<br>
L'ensemble des détails est disponible sur <a href="https://huggingface.co/datasets/CATIE-AQ/DFP">Hugging Face</a>.<br>
Il a été téléchargé plus de 90 000 fois depuis sa mise en ligne.</p>

<h4>La marmite</h4>
<p>Projet toujours en cours.<br>
Il s'agit de proposer un équivalent en français du jeu de données <a href="https://huggingface.co/datasets/HuggingFaceM4/the_cauldron"><em>the cauldron</em></a> afin de pouvoir entraîner un VLM en français.<br>
Ce jeu de données prendra en compte des données d'OCR (voir celles déjà disponibles en ligne <a href="https://huggingface.co/collections/lbourdois/french-ocr-datasets-67c8d3152330f11227e0d108">ici</a>), de captionning (voir celles déjà disponibles en ligne <a href="https://huggingface.co/collections/lbourdois/french-caption-datasets-67c8d2227284a5daa00c50b9">ici</a>), de VQA (voir celles déjà disponibles en ligne <a href="https://huggingface.co/collections/lbourdois/french-vqa-datasets-67c8d1a162a23ef0e9a2bc89">ici</a>) et de raisonnement.<br>
Les sous-jeux de données déjà en ligne ont été téléchargé plus de 50 000 fois depuis leur mise en ligne.</p>

<br><br>

<h3>Traductions</h3>

<h4>Cours de Yann Le Cun et Alfredo Canziani de la NYU</h4>
<p>Cette traduction a été la plus longue à effectuer s'étalant de 2020 à 2022.<br>
Le contenu est structuré en 19 unités réparties sur 33 vidéos 🎥 de cours (cours magistraux et travaux dirigés) d'une durée totale d'environ 45H, 74 pages web 🌐 résumant les vidéos via les notes prises par les étudiants pendant le cours, et 16 notebooks Jupyter 📓 (en PyTorch) utilisés lors des TD. Enfin un jeu de données de plus de 3000 données parallèles vérifiées manuellement a été créé pour entraîner un modèle de traduction.<br>
Vous pouvez retrouver toutes ces ressources sur le site internet dédié qui a été conçu à l'occasion : <a href="https://lbourdois.github.io/cours-dl-nyu/">https://lbourdois.github.io/cours-dl-nyu/</a>.</p>

<h4>Cours de Hugging Face 🤗</h4>

<h5>Cours de NLP</h5>
<p>En 2022, j'ai traduit le cours de traitement automatique du langage de Hugging Face.<br>
Le contenu est structuré en 10 chapitres comprenant un total de 76 vidéos 🎥 d'une durée totale d'environ 5H, de 78 pages web 🌐 et 61 notebooks Jupyter 📓  (en PyTorch et Tensorflow).<br>
Vous pouvez retrouver toutes ces ressources sur le site de <a href="https://huggingface.co/learn/nlp-course/fr/chapter1/1">Hugging Face</a>.</p>

<h5>Cours d'audio</h5>
<p>En 2023, j'ai traduit le cours d'audio de Hugging Face.<br>
Le contenu est structuré en 8 unités réparties sur 46 pages web 🌐.<br>
Vous pouvez retrouver toutes ces ressources sur le site de <a href="https://huggingface.co/learn/audio-course/fr/">Hugging Face</a>.</p>

<h5>Cours sur les modèles de diffusion</h5>
<p>En 2023, j'ai traduit le cours sur les modèles de diffusion de Hugging Face.<br>
Le contenu est structuré en 4 chapitres portant sur 17 pages web 🌐 et 8 notebooks Jupyter 📓 (en PyTorch).<br>
Vous pouvez retrouver toutes ces ressources sur le GitHub de <a href="https://github.com/huggingface/diffusion-models-class/tree/main/units/fr">Hugging Face</a> (le contenu n'ayant pas encore été propagé sur le site officiel).</p>

<h5>Cours sur les agents IA</h5>
<p>En 2025, j'ai participé avec <a href="https://github.com/knoel99">Kim NOEL</a> à la traduction du cours sur les agents IA de Hugging Face.<br>
Le contenu est structuré en 4 unités (+ 3 bonus) réparties sur 74 pages web 🌐 et 16 notebooks Jupyter 📓.<br>
Vous pouvez retrouver toutes ces ressources sur le site de <a href="https://huggingface.co/learn/agents-course/fr">Hugging Face</a>.</p>

<h5>Guide sur l'évaluation des LLM</h5>
<p>En  2025, j'ai traduit le <a href="https://github.com/huggingface/evaluation-guidebook/tree/main">guide</a> de <a href="https://huggingface.co/clefourrier">Clémentine FOURRIER</a>.<br>
Le contenu est structuré 5 chapitres répartis sur 30 pages web 🌐 et 3 notebooks Jupyter 📓.<br>
Vous pouvez retrouver toutes ces ressources <a href="https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM">ici</a>.</p>
</div>
