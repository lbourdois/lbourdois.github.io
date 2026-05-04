---
permalink: /en/projets/
title: "Projects"
classes: wide
sidebar: false
---

On this page you can find a summary of the open-source content I have worked on personally (in blue) or professionally (in green).
Listed here are mainly contents published on sites other than my personal blog — primarily course translations, as well as dataset and model releases.

<div id="tl-wrap">
<div id="tl-tabs-row">
 <div id="tl-nav"></div>
 <button id="tl-filter-toggle" title="All projects">All projects</button>
</div>

<style>
/* ── Force full width ── */
.page__content { max-width: 100% !important; width: 100% !important; }
.page { max-width: 100% !important; width: 100% !important; }
/* ── Light theme variables ── */
#tl-wrap {
  --tl-border: #d0ccc6;
  --tl-border-strong: #b0aaa2;
  --tl-text: #1a1814;
  --tl-secondary: #5a5550;
  --tl-muted: #9a938c;
  --tl-dot-empty: #b0aaa2;
  --tl-shadow-sm: 0 1px 4px rgba(0,0,0,0.10);
  --tl-shadow-hover: 0 6px 20px rgba(0,0,0,0.15);
  --tl-card-bg: #ffffff;
  --tl-panel-bg: #ffffff;
  --tl-tab-active-bg: #1a1814;
  --tl-tab-active-fg: #ffffff;
  --tl-radius: 9px;
  --tl-panel-w: 500px;
  --tl-accent-perso: #1a6b8a;
  --tl-accent-perso-light: #e0f4f8;
  --tl-accent-pro: #2d6a4f;
  --tl-accent-pro-light: #e8f5ee;
  --tl-dot-active: #2d6a4f;
  font-family: inherit;
  font-size: 15px;
  line-height: 1.5;
  color: var(--tl-text);
  width: 100%;
}
/* ── Dark theme variables ── */
@media (prefers-color-scheme: dark) {
  #tl-wrap {
    --tl-border: #3a3a42;
    --tl-border-strong: #55555f;
    --tl-text: #e8e6e0;
    --tl-secondary: #b0adb8;
    --tl-muted: #72707a;
    --tl-dot-empty: #55555f;
    --tl-shadow-sm: 0 1px 4px rgba(0,0,0,0.40);
    --tl-shadow-hover: 0 6px 20px rgba(0,0,0,0.55);
    --tl-card-bg: #2a2a32;
    --tl-panel-bg: #2a2a32;
    --tl-accent-perso: #4db8d4;
    --tl-accent-perso-light: #0d2f3a;
    --tl-accent-pro: #52b788;
    --tl-accent-pro-light: #1a3528;
    --tl-dot-active: #52b788;
  }
}
/* ── Local reset ── */
#tl-wrap *, #tl-wrap *::before, #tl-wrap *::after { box-sizing: border-box; }
#tl-wrap p, #tl-wrap h2, #tl-wrap h3 { margin: 0; padding: 0; }
/* ── Main layout ── */
#tl-layout { display: flex; align-items: flex-start; width: 100%; gap: 0; }
#tl-col { flex: 1; min-width: 0; }
/* ── Year tabs ── */
#tl-tabs-row { display: flex; align-items: center; gap: 10px; flex-wrap: wrap; margin-bottom: 28px; }
#tl-nav { display: flex; gap: 6px; flex-wrap: wrap; }
.tl-tab {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 12.5px; font-weight: 500;
  padding: 5px 16px; border-radius: 100px;
  border: 1.5px solid var(--tl-border-strong);
  background: transparent; color: var(--tl-text);
  cursor: pointer; transition: all 0.15s ease;
  line-height: 1.4; opacity: 0.65;
}
.tl-tab:hover { border-color: var(--tl-text); color: var(--tl-text); opacity: 1; }
.tl-tab.tl-active {
  background: var(--tl-tab-active-bg); border-color: var(--tl-tab-active-bg);
  color: var(--tl-tab-active-fg); opacity: 1;
}
/* ── Filter toggle ── */
#tl-filter-toggle {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 12px; font-weight: 500;
  padding: 5px 14px; border-radius: 100px;
  border: 1.5px solid var(--tl-border-strong);
  background: transparent; color: var(--tl-text);
  cursor: pointer; transition: all 0.15s ease;
  line-height: 1.4; opacity: 0.65; margin-left: auto;
}
#tl-filter-toggle:hover { opacity: 1; }
#tl-filter-toggle.active {
  background: var(--tl-tab-active-bg); border-color: var(--tl-tab-active-bg);
  color: var(--tl-tab-active-fg); opacity: 1;
}
/* ── Year section ── */
.tl-year { display: none; animation: tlFadeUp 0.25s ease both; }
.tl-year.tl-visible { display: block; }
@keyframes tlFadeUp {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}
/* ── Month row ── */
.tl-row { display: flex; align-items: flex-start; min-height: 38px; }
.tl-row.tl-has { min-height: 50px; }
.tl-mlabel { width: 72px; flex-shrink: 0; text-align: right; padding-right: 14px; padding-top: 15px; }
.tl-mname {
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 10.5px; font-weight: 500; letter-spacing: 0.07em;
  text-transform: uppercase; color: var(--tl-muted); transition: color 0.18s;
}
.tl-row:hover .tl-mname { color: var(--tl-secondary); }
.tl-dotcol { width: 20px; flex-shrink: 0; display: flex; justify-content: center; padding-top: 18px; }
.tl-dot {
  width: 10px; height: 10px; border-radius: 50%;
  border: 2px solid var(--tl-dot-empty); background: transparent;
  transition: border-color 0.18s, background 0.18s, transform 0.18s; flex-shrink: 0;
}
.tl-row.tl-has .tl-dot.tl-dot-perso { border-color: var(--tl-accent-perso); background: var(--tl-accent-perso); }
.tl-row.tl-has .tl-dot.tl-dot-pro { border-color: var(--tl-accent-pro); background: var(--tl-accent-pro); }
.tl-row.tl-has .tl-dot.tl-dot-mixed { border-color: var(--tl-accent-pro); background: var(--tl-accent-perso); }
.tl-row:hover .tl-dot { transform: scale(1.2); }
.tl-entries {
  flex: 1; padding: 7px 0 14px 16px;
  display: flex; flex-wrap: wrap; gap: 7px; align-items: flex-start;
}
/* ── Card ── */
.tl-card {
  display: inline-flex !important; align-items: flex-start; gap: 6px;
  background: var(--tl-card-bg) !important;
  border: 1.5px solid var(--tl-border) !important;
  border-radius: var(--tl-radius) !important;
  padding: 7px 12px !important;
  color: var(--tl-text) !important;
  font-size: 13px !important; line-height: 1.45 !important;
  box-shadow: var(--tl-shadow-sm) !important;
  max-width: 350px; cursor: pointer; text-decoration: none !important;
  transition: transform 0.15s ease, box-shadow 0.15s ease, border-color 0.15s ease, color 0.15s ease;
}
.tl-card:hover { transform: translateY(-2px); box-shadow: var(--tl-shadow-hover) !important; }
.tl-card.tl-card-active { box-shadow: none !important; transform: none; }
/* Personal (blue) */
.tl-card.tl-perso:hover { border-color: var(--tl-accent-perso) !important; color: var(--tl-accent-perso) !important; }
.tl-card.tl-perso.tl-card-active {
  border-color: var(--tl-accent-perso) !important;
  background: var(--tl-accent-perso-light) !important;
  color: var(--tl-accent-perso) !important;
}
/* Professional (green) */
.tl-card.tl-pro:hover { border-color: var(--tl-accent-pro) !important; color: var(--tl-accent-pro) !important; }
.tl-card.tl-pro.tl-card-active {
  border-color: var(--tl-accent-pro) !important;
  background: var(--tl-accent-pro-light) !important;
  color: var(--tl-accent-pro) !important;
}
.tl-emoji { font-size: 14px; flex-shrink: 0; margin-top: 1px; line-height: 1.45; }
/* ── Detail panel ── */
#tl-panel {
  width: var(--tl-panel-w); flex-shrink: 0;
  position: sticky; top: 80px;
  max-height: calc(100vh - 100px); overflow-y: auto;
  background: var(--tl-panel-bg);
  border: 1.5px solid var(--tl-border);
  border-radius: 12px; padding: 30px 26px 26px; margin-left: 28px;
  opacity: 0; transform: translateX(12px); pointer-events: none;
  transition: opacity 0.25s ease, transform 0.3s cubic-bezier(0.22,1,0.36,1);
}
#tl-panel.tl-panel-open { opacity: 1; transform: translateX(0); pointer-events: auto; }
#tl-panel-close {
  position: absolute; top: 12px; right: 12px;
  width: 26px; height: 26px; border-radius: 50%;
  border: 1.5px solid var(--tl-border); background: transparent;
  cursor: pointer; display: flex; align-items: center; justify-content: center;
  color: var(--tl-muted); font-size: 14px; line-height: 1;
  transition: border-color 0.15s, color 0.15s;
}
#tl-panel-close:hover { border-color: var(--tl-text); color: var(--tl-text); }
.tl-panel-tag {
  display: inline-block;
  font-family: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
  font-size: 10px; font-weight: 500; letter-spacing: 0.08em; text-transform: uppercase;
  color: var(--tl-current-accent, var(--tl-accent-pro));
  background: var(--tl-current-accent-light, var(--tl-accent-pro-light));
  border-radius: 4px; padding: 2px 8px; margin-bottom: 12px;
}
#tl-panel-title {
  font-size: 1.25rem !important; font-weight: 600 !important;
  letter-spacing: -0.01em; line-height: 1.25; margin-bottom: 14px !important;
  color: var(--tl-text) !important; border: none !important; padding: 0 !important;
}
#tl-panel-body { font-size: 13px; color: var(--tl-secondary); line-height: 1.7; }
#tl-panel-body p + p { margin-top: 10px; }
#tl-panel-body a { color: var(--tl-current-accent, var(--tl-accent-pro)); text-decoration: underline; }
#tl-panel-links { margin-top: 18px; display: flex; flex-direction: column; gap: 7px; }
.tl-plink {
  display: inline-flex !important; align-items: center; gap: 6px;
  font-size: 13px !important;
  color: var(--tl-current-accent, var(--tl-accent-pro)) !important;
  text-decoration: none !important;
  border: 1.5px solid var(--tl-current-accent, var(--tl-accent-pro)) !important;
  border-radius: var(--tl-radius) !important; padding: 6px 12px !important;
  transition: background 0.15s; width: fit-content; background: transparent !important;
}
.tl-plink:hover { background: var(--tl-current-accent-light, var(--tl-accent-pro-light)) !important; }
.tl-plink svg { width: 12px; height: 12px; flex-shrink: 0; }
/* ── Mobile ── */
@media (max-width: 900px) {
  #tl-layout { flex-direction: column; }
  #tl-panel {
    position: fixed; bottom: 0; left: 0; right: 0;
    width: 100%; max-height: 60vh;
    border-radius: 12px 12px 0 0; border-bottom: none;
    margin-left: 0; top: auto; transform: translateY(16px); z-index: 9999;
  }
  #tl-panel.tl-panel-open { transform: translateY(0); }
  .tl-mlabel { width: 52px; }
}
</style>

<div id="tl-layout">
  <div id="tl-col">
    <div id="tl-main"></div>
  </div>
  <div id="tl-panel">
    <button id="tl-panel-close">✕</button>
    <div class="tl-panel-tag" id="tl-panel-tag"></div>
    <h2 id="tl-panel-title"></h2>
    <div id="tl-panel-body"></div>
    <div id="tl-panel-links"></div>
  </div>
</div>

</div>

<script>
(function () {
  var MONTHS = ['Jan','Feb','Mar','Apr','May','Jun','Jul','Aug','Sep','Oct','Nov','Dec'];
  var MONTHS_L = ['January','February','March','April','May','June','July','August','September','October','November','December'];
  var ICON = '<svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M6 3H3a1 1 0 0 0-1 1v9a1 1 0 0 0 1 1h9a1 1 0 0 0 1-1v-3M10 2h4m0 0v4m0-4L7 9"/></svg>';

  /* ════════════════════════════════════════════════════════════════
     DATA
     Each entry: { label, emoji, pro?, details? }
     details: { title?, body: [HTML paragraphs], links?: [{label,url}] }
  ════════════════════════════════════════════════════════════════ */
var DATA = {
  2019: {
    1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],9:[],10:[],
    11:[
      { label: 'Bag-of-words illustration', emoji: '👜', pro: false, details: { title: 'Bag-of-words illustration', body: ['The bag-of-words is the technique that was predominantly used before the advent of neural-network-based models such as RNNs (themselves now largely superseded by transformers). This is primarily an introductory article opening a blog series on NLP.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Bag-of-word/' }] } },
      { label: 'Word embedding illustration', emoji: '📏', pro: false, details: { title: 'Word embedding illustration', body: ['Illustration of word embedding and one of its applications: Google\'s word2vec. Helps understand crucial NLP concepts such as self-supervised learning and embedding models widely used for document retrieval and search engines. This is a translation of Jay ALAMMAR\'s blog post.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/word_embedding/' }] } }
    ],
    12:[
      { label: 'RNN, LSTM, GRU and ELMo illustration', emoji: '➿', pro: false, details: { title: 'RNN, LSTM, GRU and ELMo', body: ['Illustration of recurrent neural networks, Long Short-Term Memory, Gated Recurrent Units and ELMo. These techniques were used before the advent of transformers. Reviewing them is crucial to master concepts still used in architectures like SSMs. Note: the ELMo section is a translation of Jay ALAMMAR\'s blog post.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/RNN-LSTM-GRU-ELMO/' }] } },
      { label: 'Seq2Seq and the attention mechanism', emoji: '🎯', pro: false, details: { title: 'Seq2Seq and the attention mechanism', body: ['Illustration of the sequence-to-sequence principle and the attention mechanism of Cho et al. (2014). A must-read to understand the attention mechanism that transformers parallelize. This is a translation of Jay ALAMMAR\'s blog post.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Seq2seq-et-attention/' }] } },
      { label: 'The Transformer illustrated', emoji: '🤖', pro: false, details: { title: 'The Transformer illustrated', body: ['Illustration of the Transformer model by Vaswani et al. (2017). This is a translation of Jay ALAMMAR\'s blog post, with occasional additions. An essential read when getting started with NLP.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Transformer/' }] } },
      { label: 'BERT illustrated', emoji: '🧸', pro: false, details: { title: 'BERT illustrated', body: ['Illustration of the BERT model by Devlin et al. (2018) and its French derivatives: CamemBERT and FlauBERT. This is a translation of Jay ALAMMAR\'s blog post, with additions. An essential read to understand encoder-type architectures.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/BERT/' }] } },
      { label: 'GPT-2 illustrated', emoji: '💬', pro: false, details: { title: 'GPT-2 illustrated', body: ['Illustration of the GPT-2 model by Radford et al. (2019). This is a translation of Jay ALAMMAR\'s blog post, with additions. An essential read to understand decoder-type architectures.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/GPT2/' }] } }
    ]
  },
  2020: {
    1:[
      { label: 'Transformer-derived architectures', emoji: '🔤', pro: false, details: { title: 'Transformer-derived architectures', body: ['Overview of Transformer-based architectures. Written in 2020, it mainly covers models of that era and is now somewhat outdated.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Les-architectures-transformers/' }] } },
      { label: 'NLP tasks and datasets', emoji: '📚', pro: false, details: { title: 'NLP tasks and datasets', body: ['Review of tasks and datasets frequently used in NLP publications.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Taches-et-jeux-de-donnees-en-NLP/' }] } },
      { label: 'Preprocessing and tokenizers in NLP', emoji: '✂️', pro: false, details: { title: 'Preprocessing and tokenizers in NLP', body: ['Illustration of various preprocessing techniques in NLP as well as different tokenizers in common use. This is a translation of Keita KURITA\'s blog post. A must-read when getting started with NLP.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Les-tokenizers/' }] } }
    ],
    2:[
      { label: 'The Reformer illustrated', emoji: '🕶️', pro: false, details: { title: 'The Reformer illustrated', body: ['Illustration of the Reformer model by KITAEV and KAISER (2020). This is a translation of Alireza DIRAFZOON\'s blog post.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Reformer/' }] } }
    ],
    3:[
      { label: 'AlBERT illustrated', emoji: '🧠', pro: false, details: { title: 'AlBERT illustrated', body: ['Illustration of the AlBERT model by LAN et al. (2020). This is a translation of Amit CHAUDHARY\'s blog post.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/ALBERT/' }] } }
    ],
    4:[],
    5:[
      { label: 'Data augmentation in NLP', emoji: '📈', pro: false, details: { title: 'Data augmentation in NLP', body: ['An overview of the techniques available for text data augmentation in natural language processing. This is a translation of Amit CHAUDHARY\'s blog post.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/nlp/Data-augmentation-in-NLP/' }] } }
    ],
    6:[],7:[],8:[],9:[],10:[],11:[],12:[]
  },
  2021: {
    1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],
    9:[
      { label: 'Deep Learning course by Yann LeCun & Alfredo Canziani (2020 ed.)', emoji: '🎓', pro: false, details: { title: 'Deep Learning course by Yann LeCun & Alfredo Canziani (2020 ed.)', body: ['From August 2020 to August 2021, I translated the 2020 edition of the Introduction to Deep Learning course by Yann LeCun and Alfredo Canziani taught at New York University. This work required approximately 600 hours to produce a French translation of: • 28 lecture videos 🎥 (lectures and lab sessions) totalling around 40h, • 59 website pages 🌐 summarising the videos through student notes, • 16 Jupyter notebooks 📓 used during labs. The 2020 edition covers: deep learning history and motivation, gradient descent and backpropagation, ConvNets, RNNs/LSTMs, attention and seq2seq, optimisation techniques, energy-based models (EBM), contrastive and generative methods (GAN), auto-encoders (DAE, VAE), self-supervised learning for computer vision, transformers, graph neural networks (GNN) and much more!'], links: [{ label: 'Course website', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-nyu/' }] } }
    ],
    10:[], 11:[], 12:[
      { label: 'French table-to-text datasets', pro: true, emoji: '𝄜', details: { title: 'French table-to-text datasets', body: ['Table-to-text generation datasets (web_nlg, e2e_nlg, viggo) translated from English to French. At the time I was exploring PEFT methods (LoRA had not yet been released) and needed datasets to replicate publication results (LI and LIANG\'s Prefix-Tuning among others). Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-table-to-text-datasets' }] } }
    ]
  },
  2022: {
    1:[],2:[],3:[],4:[],5:[],6:[],7:[],8:[],
    9:[
      { label: 'Deep Learning course by Yann LeCun & Alfredo Canziani (2021 ed.)', emoji: '🎓', pro: false, details: { title: 'Deep Learning course by Yann LeCun & Alfredo Canziani (2021 ed.)', body: ['Translation of the 2021 edition of the course. For this edition, only the new content compared to the 2020 edition was translated, namely guest contributions (researchers at Meta at the time) invited by Yann to give lectures on their areas of specialisation.'], links: [{ label: 'Course website', url: 'https://lbourdois.github.io/cours-dl-nyu/' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/projets/cours-dl-21-nyu/' }] } }
    ],
    10:[],11:[],12:[]
  },
  2023: {
    1:[
      { label: 'Hugging Face NLP Course', emoji: '🤗', pro: false, details: { title: 'Hugging Face NLP Course', body: ['Announced in January 2023, I translated the Hugging Face NLP course from April to June 2022. The entirely free, ad-free content covers: - An overview of transformers: general architecture, NLP tasks, biases and limitations, etc. - How to use the 🤗 Transformers library: pipeline API, loading/saving models and tokenizers, etc. - How to fine-tune a pre-trained model on a text classification task - How to share models/tokenizers: how the Hub works, how to create a model card, etc. - How to use the 🤗 Datasets library: loading datasets, preprocessing, loading and computing metrics, etc. - How to use the 🤗 Tokenizer library: different tokenizer types (BPE, WordPiece, Unigram), creating custom ones, how fast tokenizers work. - What the main NLP tasks are and how to handle them: named entity recognition, question answering, translation, summarisation, etc. A total of 10 chapters comprising 76 videos (~5h), 78 web pages, and 61 Jupyter notebooks (PyTorch & TensorFlow).'], links: [{ label: 'Start learning', url: 'https://huggingface.co/learn/nlp-course/fr/chapter1/1' }] } }
    ],2:[],3:[],4:[],
    5:[
      { label: 'Word2vec models', emoji: '📏', pro: false, details: { title: 'Word2vec models', body: ['Migration of 339 Word2vec-type models to the Hugging Face Hub.'], links: [{ label: 'Hugging Face organisation', url: 'https://huggingface.co/Word2vec' }] } }
    ],
    6:[
      { label: 'QAmemBERT', emoji: '❓', pro: true, details: { title: 'QAmemBERT', body: ['First version of the French Question Answering models I worked on. Fine-tuned from CamemBERT. Available in base (110M) and large (336M) sizes with a context length of 512 tokens. Accompanied by the training dataset and an explanatory blog post. Developed in collaboration with Boris ALBAR and Pierre BEDU at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-qa' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/QA/' }] } },
      { label: 'Hugging Face Diffusion Models Course', emoji: '🤗', pro: false, details: { title: 'Hugging Face Diffusion Models Course', body: ['Translation of the introductory Hugging Face diffusion models course. 4 chapters totalling 17 web pages and 8 Jupyter notebooks covering: - Getting started with the 🤗 Diffusers library and implementing a diffusion model from scratch, - Fine-tuning an existing diffusion model on new data and exploring guided conditional generation, - Exploring Stable Diffusion, a powerful latent diffusion model capable of text-to-image generation, - Advanced techniques such as DDIM (denoising diffusion implicit models) and applying diffusion models to audio generation.'], links: [{ label: 'Start learning', url: 'https://lbourdois.github.io/diffusion-course/' }] } }
    ],
    7:[
      { label: 'Hugging Face Audio Course', emoji: '🤗', pro: false, details: { title: 'Hugging Face Audio Course', body: ['Translation of the Hugging Face audio course. This introductory course (less comprehensive than the NLP one) consists of 8 chapters totalling 46 web pages covering: - Techniques for audio data repair and processing, - An overview of different audio tasks, - Exploration of different audio transformer architectures and their use cases, - A first practical application: building a music genre classifier, - A second application on automatic speech recognition, - A third application on speech synthesis, - A fourth application combining the previous three to build a voice assistant.'], links: [{ label: 'Start learning', url: 'https://huggingface.co/learn/audio-course/fr/' }] } }
    ],
    8:[],
    9:[
      { label: 'Deep Learning course by Yann LeCun & Alfredo Canziani (final version)', emoji: '🎓', pro: false, details: { title: 'Deep Learning course by Yann LeCun & Alfredo Canziani (final version)', body: ['Final version of the NYU deep learning course including the 2020, 2021 and 2022 editions. A dedicated website was created summarising the 19 units (lectures and practicals): 33 videos (~45h total), 74 web pages of student notes, 16 Jupyter notebooks. A parallel dataset of 3,000 French–English pairs was also compiled from the course to train machine translation models.'], links: [{ label: 'Course website', url: 'https://lbourdois.github.io/cours-dl-nyu/' }] } },
      { label: 'Dataset of French Prompts (DFP)', emoji: '📝', pro: true, details: { title: 'Dataset of French Prompts (DFP)', body: ['Dataset of French prompts covering 30 different NLP tasks (semantic similarity, paraphrase detection, textual inference, sentiment analysis, question answering, summarisation, NER, etc.). It groups 107,796,041 rows from 34 source datasets, with 724 prompts written in imperative form, informal and formal registers. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/DFP' }] } }
    ],
    10:[
      { label: 'FrenchSUM', pro: true, emoji: '📄', details: { title: 'FrenchSUM', body: ['French automatic summarisation dataset aggregating 11 open-source sources (XWikis, MLSUM, OrangeSum, XLSum, CrossSum, WikinewsFR, etc.), cleaned to remove leakage and duplicates. 841,673 rows in total: 788,358 train, 26,935 validation, 26,380 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/frenchSUM' }] } },
      { label: 'FrenchNLI', emoji: '➡️', pro: true, details: { title: 'FrenchNLI', body: ['Dataset aggregating all open-source French natural language inference (NLI) datasets. Concatenates 10 cleaned sources with leakage and duplicate removal. 569,895 rows: 555,798 train, 3,780 validation, 10,317 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-nli-pack' }] } },
      { label: 'frenchKEYWORDS', emoji: '🏷️', pro: true, details: { title: 'frenchKEYWORDS', body: ['French keyword extraction dataset aggregating 4 open-source sources (wikinews-fr-100, termith-eval, taln-archives, papyrus), cleaned for leakage and duplicates. 16,471 rows: 12,002 train, 1,488 validation, 2,981 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/frenchKEYWORDS' }] } }
    ],
    11:[
      { label: 'FrenchPARAPHRASE', emoji: '👥', pro: true, details: { title: 'FrenchPARAPHRASE', body: ['French paraphrase dataset aggregating 7 open-source sources (tatoeba_mt, TaPaCo, PAWS-X, paraphrasing_french_5000, paraphrasing_french, paragraphss_paraphrasing, multi_paraphrasing_french), cleaned for leakage and duplicates. 254,513 rows: 251,753 train, 1,857 validation, 903 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-paraphrase-dataset' }] } },
      { label: 'Breton audio archive', emoji: '🗃️', pro: false, details: { title: 'Breton audio archive', body: ['I collected as many Breton-language recordings as possible found online to form an archive (~14,000 hours of audio). The goal is to preserve these recordings for long-term accessibility (websites can disappear, which has a strong impact for a minority language). As some sources are likely copyright-protected, the archive is made available exclusively to researchers at French research institutes (INRIA, CNRS, etc.) and French universities.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/Bretagne/br-archive-sonore-en-breton' }] } }
    ],12:[
      { label: 'French audio datasets', emoji: '👂', pro: false, details: { title: 'French audio datasets', body: ['Reference collection of French audio datasets for pre-training an audio model and then fine-tuning it on a specific task (transcription, classification, translation, etc.). The full collection (~117,000 hours of audio) was opened publicly in May 2025. As some sources are likely copyright-protected, it is available exclusively to researchers at French research institutes (INRIA, CNRS, etc.) and French universities.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-audio-datasets-pretraining' }] } },
      { label: 'CFP', emoji: '💬', pro: true, details: { title: 'Chat French Prompts (CFP)', body: ['Dataset of native French prompts (non-translated) aggregating 11 open-source sources, manually cleaned. 56,277 rows covering many tasks (question answering, text generation, classification, NER, etc.). Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/CFP' }] } },
      { label: 'Introduction to SSMs and S4', emoji: '〽️', pro: false, details: { title: 'Introduction to SSMs and S4', body: ['Introduction to the basics of State Space Models (SSM) in deep learning, illustrated via the S4 model by Albert GU et al. (2021). The article details the three views of an SSM (continuous, recurrent, convolutional), discretisation via the trapezoidal method, and initialisation of the A matrix via HiPPO. This is the first blog post of the series dedicated to this model family.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/ssm/introduction_ssm/' }] } }
    ]
  },
  2024: {
    1:[
      { label: 'NERmemBERT', emoji: '🔍', pro: true, details: { title: 'NERmemBERT', body: ['First version of the French Named Entity Recognition models. Fine-tuned from CamemBERT. Available in base (110M) and large (336M) sizes with a context length of 512 tokens. Accompanied by the training datasets and an explanatory blog post. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-ner' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/NER/' }] } }
    ],
    2:[
      { label: 'FrenchSTS', emoji: '👥', pro: true, details: { title: 'FrenchSTS', body: ['French semantic textual similarity dataset aggregating 11 open-source sources (STSB, SICK-fr, STS12 to STS16-fr, OrdalieFR, OpusParcus, MUSTS, STS22), cleaned for leakage and duplicates. 45,726 rows: 12,227 train, 3,526 validation, 29,973 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-sts-pack' }] } },
      { label: 'Always check dataset quality', emoji: '🔬', pro: false, details: { title: 'Always check dataset quality', body: ['Article analysing the quality of 596 datasets available on the Hugging Face Hub, measuring split leakage and duplicate data. Over 60% of the test samples analysed contain a bias (duplications or leakage).'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/LLE/' }] } },
      { label: 'FrenchSIMPLIFICATION', emoji: '👓', pro: true, details: { title: 'FrenchSIMPLIFICATION', body: ['French text simplification dataset aggregating 4 open-source sources (CLEAR, Wikilarge, BiSECT, Alector), cleaned for leakage and duplicates. 785,625 rows: 781,801 train, 2,385 validation, 1,439 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/frenchSIMPLIFICATION' }] } }
    ],
    3:[],
    4:[
      { label: 'SSM history in 2022', emoji: '📖', pro: false, details: { title: 'SSM history in 2022', body: ['Literature review of State Space Models published in 2022, following the S4 introduction article. Covers theoretical advances (S4 V2, DSS, S4D, GSS, Mega, Liquid-S4, S5, SGConv) and the first concrete SSM applications to audio (SaShiMi), video (ViS4mer), images (S4ND, CCNN) and time series (SSSD).'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/ssm/ssm_en_2022/' }] } },
      { label: 'FrenchSUM long sequences', emoji: '📚', pro: true, details: { title: 'FrenchSUM long sequences', body: ['French automatic summarisation and long-text datasets. french_books_summaries contains 949 French books with their summaries (1,513 rows). Accompanied by french_books containing 2,075 French books without summaries, intended for pre-training. Both datasets target very long sequences (up to 262K tokens). Developed at CATIE.'], links: [{ label: 'french_books_summaries', url: 'https://huggingface.co/datasets/CATIE-AQ/french_books_summaries' }, { label: 'french_books', url: 'https://huggingface.co/datasets/CATIE-AQ/french_books' }] } },
      { label: 'Narrativeqa fr', emoji: '❓', pro: true, details: { title: 'Narrativeqa fr', body: ['French Question Answering dataset on long literary texts (novels). Contains 143 natively French books with their questions and answers, translated from the narrativeqa dataset. 4,207 questions and 7,771 answers: 3,070 train, 382 validation, 753 test. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/datasets/CATIE-AQ/french_narrativeqa' }] } }
    ],
    5:[],6:[],7:[],
    8:[
      { label: 'Merve\'s papers', emoji: '📷', pro: false, details: { title: 'Merve\'s papers', body: ['Hugging Face Space grouping around thirty summaries of recent publications in computer vision and VLM. Written by Merve NOYAN, I centralised them in this app when I was following the field at the time.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/spaces/merve/vision_papers' }] } }
    ],
    9:[],
    10:[
      { label: 'Breton ASR data collection', pro: false, emoji: '🗣️', details: { title: 'Breton ASR data collection', body: ['Porting and cleaning of Breton audio datasets on Hugging Face to facilitate ASR model training in this language.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/Bretagne/br-audio-finetuning-asr-en-breton' }] } },
      { label: 'Breton/French translation data collection', pro: false, emoji: '📚', details: { title: 'Breton/French translation data collection', body: ['Porting and cleaning of Breton/French translation datasets on Hugging Face to facilitate training of such models.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/Bretagne/br-traduction-propre' }] } }
    ],
    11:[
      { label: 'QAmemBERTa', emoji: '❓', pro: true, details: { title: 'QAmemBERTa', body: ['Second version of the French Question Answering models. Fine-tuned from CamemBERT2 and CamemBERTa. Available in 111M parameter size with a context length of 1,024 tokens. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-qa' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/QA/' }] } },
      { label: 'NERmemBERTa', emoji: '🔍', pro: true, details: { title: 'NERmemBERTa', body: ['Second version of the French Named Entity Recognition models. Fine-tuned from CamemBERT2 and CamemBERTa. Available in 111M parameter size with a context length of 1,024 tokens. Available with 3 or 4 entity types (persons, locations, organisations + misc if 4 entities chosen). Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-ner' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/NER/' }] } }
    ],
    12:[
      { label: 'French VQA datasets', emoji: '👁️', pro: false, details: { title: 'French VQA datasets', body: ['Visual Question Answering datasets in French (either original or translated from English), intended for VLM training. These datasets are part of the "La marmite" project, whose goal is to eventually provide a French equivalent of Hugging Face\'s the cauldron dataset.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-vqa-datasets' }] } },
      { label: 'French caption datasets', emoji: '✍️', pro: false, details: { title: 'French caption datasets', body: ['Image captioning datasets in French (either original or translated from English). Part of the "La marmite" project.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-caption-datasets' }] } },
      { label: 'French retriever datasets', emoji: '🐶', pro: false, details: { title: 'French retriever datasets', body: ['Visual retrieval datasets in French (either original or translated from English) for multimodal model training. Part of the "La marmite" project.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-retriever-datasets' }] } }
    ]
  },
  2025: {
    1: [{
      label: 'FAT5 (Flash Attention T5)', emoji: '⚡', pro: true,
      details: {
        title: 'FAT5 (Flash Attention T5)',
        body: [
          'FAT5 is a PyTorch implementation of T5 with a UL2 objective optimised for GPGPU, developed with Boris ALBAR at CATIE throughout 2024. It uses custom CUDA and Triton kernels along with specific optimisations to increase throughput and reduce memory usage by a factor of 2 compared to the original Hugging Face implementation. We applied it by pre-training a 147M-parameter French model on a single A100, for an estimated cost of €1,200 (Sesterce instance).'
        ], links: [ { label: 'GitHub (Apache-2.0)', url: 'https://github.com/catie-aq/flashT5' }, { label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/catie-french-fat5-ul2' }, { label: 'Read the article', url: 'https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport' }] }
    }],
    2: [
      { label: 'A visual guide to quantisation', emoji: '🗜️', pro: false, details: { title: 'A visual guide to quantisation', body: ['Translation of Maarten GROOTENDORST\'s blog post. Covers in over 50 visuals the main concepts of quantisation: floating-point number representation, symmetric and asymmetric quantisation, post-training methods (GPTQ, GGUF) and quantisation during training (BitNet, BitNet 1.58b).'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/Quantification/' }] } }
    ],
    3: [
      { label: 'French OCR datasets', emoji: '📝', pro: false, details: { title: 'French OCR datasets', body: ['OCR datasets in French (either original or translated from English), intended for VLM training. Part of the "La marmite" project.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-ocr-datasets' }] } },
      { label: 'LLM evaluation guide', emoji: '⚖️', pro: true, details: { title: 'LLM evaluation guide', body: ['French translation of the LLM evaluation guide written by Clémentine FOURRIER. The guide addresses both beginners and advanced users, covering the three main families of evaluation: automated benchmarks, human evaluation and the LLM-as-a-judge approach. Structured in 5 chapters across 30 web pages and 3 Jupyter notebooks. Developed at CATIE.'], links: [{ label: 'Read the guide', url: 'https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM' }] } }
    ],
    4: [
      { label: 'A visual guide to mixture of experts (MoE)', emoji: '🥼', pro: false, details: { title: 'A visual guide to mixture of experts (MoE)', body: ['Translation of Maarten GROOTENDORST\'s blog post. Covers in over 50 visuals the key concepts of mixture of experts: experts and routers, load balancing (KeepTopK, Switch Transformer), MoE applied to vision (V-MoE, Soft-MoE) and analysis of active vs. sparse parameters using Mixtral 8x7B as an example.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/MoE/' }] } },
      { label: 'ModernQAmemBERT', emoji: '❓', pro: true, details: { title: 'ModernQAmemBERT', body: ['Third version of the French Question Answering models. Fine-tuned from ModernCamemBERT. Available in 136M parameter size with a context length of 8,192 tokens. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-qa' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/QA/' }] } },
      { label: 'ModernNERmemBERT', emoji: '🔍', pro: true, details: { title: 'ModernNERmemBERT', body: ['Third version of the French Named Entity Recognition models. Fine-tuned from ModernCamemBERT. Available in 136M parameter size with a context length of 8,192 tokens. Available with 3 or 4 entity types. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-ner' }, { label: 'Read the article', url: 'https://lbourdois.github.io/blog/NER/' }] } }
    ],
    5: [
      { label: 'A visual guide to reasoning LLMs', pro: false, emoji: '🧠', details: { title: 'A visual guide to reasoning LLMs', body: ['Translation of Maarten GROOTENDORST\'s blog post. Explores in over 50 visuals the paradigm shift towards inference-time compute: scaling laws, solution verification (ORM, PRM, Best-of-N, Monte Carlo tree search), proposal distribution modification (STaR) and step-by-step construction of DeepSeek-R1.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/LLM_raisonnement/' }] } },
      { label: 'Breton packs', pro: false, emoji: '📚', details: { title: 'Breton packs', body: ['Update of previously created Breton data, porting of new datasets to Hugging Face (over 200 datasets in total), cleaning and organisation into several collections.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/breton-packs' }] } }
    ],
    6: [
      { label: 'A visual guide to AI agents', emoji: '🤖', pro: false, details: { title: 'A visual guide to AI agents', body: ['Translation of Maarten GROOTENDORST\'s blog post. Covers in over 60 visuals the main components of LLM agents: memory (short- and long-term, RAG), tools (Toolformer, Anthropic\'s MCP), planning (ReAct, Reflexion, Self-Refine) and multi-agent systems (AutoGen, MetaGPT, CAMEL).'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/LLM_Agents/' }] } },
      { label: 'NanoBEIR-fr', emoji: '🍺', pro: true, details: { title: 'NanoBEIR-fr', body: ['Translation of the NanoBEIR benchmark into French to provide a French IR evaluation dataset. Note: it has not been cleaned (no removal of leakage, duplicates, empty or aberrant data) even though it contains errors. This decision was taken following a discussion with Tom Aarsen so that the dataset can be easily used with the Sentence Transformers library (cleaning would have broken the library pipeline). Post-processing of results is recommended. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/nanobeir-fr' }] } },
      { label: 'XMrec datasets (French part)', pro: true, emoji: '🛒', details: { title: 'French XMrec', body: ['Porting to Hugging Face of the French portion of the XMrec dataset, intended for evaluating multilingual recommender systems. Developed at CATIE.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/CATIE-AQ/xmrec-french-part-reviews-and-metadata-datasets' }] } }
    ],
    7: [
      { label: 'French DPO and conversation datasets', emoji: '🤝', pro: false, details: { title: 'French DPO and conversation datasets', body: ['Preference (DPO) and conversation datasets in French for LLM fine-tuning.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-dpo-and-conversation-datasets' }] } }
    ],
    8: [
      { label: 'Breton Whisper models', pro: false, emoji: '🌬️', details: { title: 'Breton Whisper models', body: ['Training of two Whisper models in Breton. One producing Breton transcriptions from Breton audio, the other producing French transcriptions from Breton audio. These models have no particular performance claims and should be viewed as an experiment/V0 to establish a baseline.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/Bretagne/models' }] } }
    ],
    9: [
      { label: 'Hugging Face AI Agents Course', emoji: '🤗', pro: true, details: { title: 'Hugging Face AI Agents Course', body: ['Translation of the Hugging Face AI agents course, carried out with Kim NOEL. 4 units (+ 3 bonus) totalling 74 web pages and 16 Jupyter notebooks covering: - A theoretical introduction to agents (Thought-Action-Observation cycle, ReAct approach), - The smolagents, LlamaIndex and LangGraph libraries, - How to code an agentic RAG tool, - A final project evaluated via the GAIA leaderboard. Bonus units cover fine-tuning for function calling, agent observability and evaluation, and building an agent to play Pokémon. Developed at CATIE.'], links: [{ label: 'Start learning', url: 'https://huggingface.co/learn/agents-course/fr' }] } }
    ],
    10: [
      { label: 'Model statistics of the 50 most-downloaded entities on Hugging Face', emoji: '📊', pro: false, details: { title: 'Model statistics of the 50 most-downloaded entities on Hugging Face', body: ['Analysis of Hugging Face Hub download data with a focus on the 50 most-downloaded open-source entities, which alone account for 80% of downloads. The article details their breakdown by country, entity type, modality, task, language and model size.'], links: [{ label: 'Read the article', url: 'https://lbourdois.github.io/blog/HF_stats_models/' }] } },
      { label: 'French reasoning and tool-calling datasets', emoji: '🛠️', pro: false, details: { title: 'French reasoning and tool-calling datasets', body: ['Reasoning and tool-calling datasets in French (either original or translated from English) for LLM training.'], links: [{ label: 'Hugging Face', url: 'https://huggingface.co/collections/lbourdois/french-think-and-toolcalling-datasets' }] } }
    ],
    11: [],
    12: []
  },
  2026: { 1:[],2:[],3:[],4:[],
    5:[{ label: 'Release in progress', emoji: '👀', pro: true, details: { title: 'Release in progress', body: ['Release in progress.'], links: [] } }],6:[],7:[],8:[],9:[],10:[],11:[],12:[] }
};

  /* ── Panel ── */
  var panel = document.getElementById('tl-panel');
  var panelTag = document.getElementById('tl-panel-tag');
  var panelTitle = document.getElementById('tl-panel-title');
  var panelBody = document.getElementById('tl-panel-body');
  var panelLinks = document.getElementById('tl-panel-links');
  var activeCard = null;
  var filterPro = null;

  function openPanel(entry, m, y) {
    var isPro = !!entry.pro;
    panel.style.setProperty('--tl-current-accent', isPro ? 'var(--tl-accent-pro)' : 'var(--tl-accent-perso)');
    panel.style.setProperty('--tl-current-accent-light', isPro ? 'var(--tl-accent-pro-light)' : 'var(--tl-accent-perso-light)');
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

  /* ── Filter toggle ── */
  var filterBtn = document.getElementById('tl-filter-toggle');
  filterBtn.addEventListener('click', function () {
    if (filterPro === null) { filterPro = false; filterBtn.textContent = 'Personal only'; filterBtn.classList.add('active'); }
    else if (filterPro === false) { filterPro = true; filterBtn.textContent = 'Professional only'; }
    else { filterPro = null; filterBtn.textContent = 'All projects'; filterBtn.classList.remove('active'); }
    applyFilter();
  });

  function applyFilter() {
    document.querySelectorAll('.tl-card').forEach(function (card) {
      var isPro = card.dataset.pro === 'true';
      if (filterPro === null) { card.style.display = ''; }
      else if (filterPro === true) { card.style.display = isPro ? '' : 'none'; }
      else { card.style.display = isPro ? 'none' : ''; }
    });
  }

  /* ── Build ── */
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
      var allPro = entries.length && entries.every(function(e){ return e.pro; });
      var allPerso = entries.length && entries.every(function(e){ return !e.pro; });
      var dotType = !entries.length ? '' : (allPro ? ' tl-dot-pro' : (allPerso ? ' tl-dot-perso' : ' tl-dot-mixed'));
      dotCol.innerHTML = '<div class="tl-dot' + dotType + '"></div>';

      row.appendChild(lbl);
      row.appendChild(dotCol);

      if (entries.length) {
        var col = document.createElement('div');
        col.className = 'tl-entries';
        entries.forEach(function (e) {
          var card = document.createElement('div');
          card.className = 'tl-card' + (e.pro ? ' tl-pro' : ' tl-perso');
          card.dataset.pro = e.pro ? 'true' : 'false';
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

---

## Key projects

### French models and datasets

**FAT5**

FAT5 is a PyTorch implementation of T5 with a UL2 objective optimised for GPGPU, developed with Boris ALBAR.

It uses custom CUDA and Triton kernels along with specific optimisations to increase throughput and reduce memory usage for training and inference by a factor of 2 compared to the original Hugging Face implementation.

We applied it by pre-training a 147M-parameter French model using a single A100. The estimated pre-training cost for such a model is only €1,200 (Sesterce instance estimate).

The pre-training code is available on GitHub under Apache-2.0 and the trained model weights are available on CATIE's Hugging Face account. A blog post detailing our methodology is available [here](https://huggingface.co/spaces/CATIE-AQ/FAT5-rapport).

**NER**

The NERmemBERT family consists of French Named Entity Recognition models capable of labelling up to 4 entity types (Persons, Locations, Organisations, Misc such as work titles, diseases, etc.). Available in base (110M or 136M parameters) and large (336M) sizes, handling contexts from 512 to 8,192 tokens. Weights are freely available as open-source, as are the training datasets. Everything is available on CATIE's Hugging Face account. A blog post detailing the methodology is available [here](https://lbourdois.github.io/blog/NER/).

They have been downloaded more than 185,000 times since their release.

**Question Answering**

The QAmemBERT family consists of French question answering models capable of determining whether the answer to a question is present or absent in an associated context text. Available in base (110M or 136M parameters) and large (335M) sizes, handling contexts from 512 to 8,192 tokens. Weights are freely available as open-source, as is the training dataset. A blog post detailing the methodology is available [here](https://lbourdois.github.io/blog/QA/).

They have been downloaded more than 160,000 times since their release.

**DFP**

The Dataset of French Prompts (DFP) contains 113,129,978 rows covering 30 different NLP tasks.

724 prompts were written in imperative form, informal and formal registers to cover as broadly as possible the pre-training data used by models that will use these inputs.

The inputs and targets columns follow the same format as the xP3 dataset by Muennighoff et al. Full details are available on [Hugging Face](https://huggingface.co/datasets/CATIE-AQ/DFP).

It has been downloaded more than 90,000 times since its release.

**La marmite**

Project still in progress.

The goal is to provide a French equivalent of the cauldron dataset to train a French VLM. It will include OCR data ([available here](https://huggingface.co/collections/lbourdois/french-ocr-datasets)), captioning data ([available here](https://huggingface.co/collections/lbourdois/french-caption-datasets)), VQA data ([available here](https://huggingface.co/collections/lbourdois/french-vqa-datasets)) and reasoning data.

The sub-datasets already online have been downloaded more than 50,000 times since their release.

---

### Translations

**Yann LeCun & Alfredo Canziani's NYU course**

This translation was the longest to complete, spanning from 2020 to 2022.

The content is structured in 19 units across 33 lecture videos 🎥 (lectures and lab sessions) totalling approximately 45 hours, 74 web pages 🌐 summarising the videos via student notes, and 16 Jupyter notebooks 📓 (PyTorch) used during labs. A parallel dataset of over 3,000 manually verified pairs was also created to train a translation model.

All resources are available on the dedicated website: [https://lbourdois.github.io/cours-dl-nyu/](https://lbourdois.github.io/cours-dl-nyu/).

**Hugging Face 🤗 courses**

*NLP course*

In 2022, I translated the Hugging Face natural language processing course. The content is structured in 10 chapters comprising 76 videos 🎥 (~5h), 78 web pages 🌐 and 61 Jupyter notebooks 📓 (PyTorch and TensorFlow). All resources are available on the [Hugging Face website](https://huggingface.co/learn/nlp-course/fr/chapter1/1).

*Audio course*

In 2023, I translated the Hugging Face audio course. The content is structured in 8 units across 46 web pages 🌐. All resources are available on the [Hugging Face website](https://huggingface.co/learn/audio-course/fr/).

*Diffusion models course*

In 2023, I translated the Hugging Face diffusion models course. The content is structured in 4 chapters covering 17 web pages 🌐 and 8 Jupyter notebooks 📓 (PyTorch). All resources are available on [Hugging Face's GitHub](https://lbourdois.github.io/diffusion-course/).

*AI agents course*

In 2025, I contributed with Kim NOEL to the translation of the Hugging Face AI agents course. The content is structured in 4 units (+ 3 bonus) across 74 web pages 🌐 and 16 Jupyter notebooks 📓. All resources are available on the [Hugging Face website](https://huggingface.co/learn/agents-course/fr).

*LLM evaluation guide*

In 2025, I translated Clémentine FOURRIER's guide. The content is structured in 5 chapters across 30 web pages 🌐 and 3 Jupyter notebooks 📓. All resources are available [here](https://huggingface.co/spaces/CATIE-AQ/Guide_Evaluation_LLM).
