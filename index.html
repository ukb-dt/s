<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Neuron Σ — Tantrum Bayesian Cycle</title>
  <style>
    :root {
      --bg: #0a0f1c;
      --membrane: #1a2332;
      --cytoplasm: #2b3347;
      --ink: #e6edf3;
      --dim: #7d8a99;
      --synapse: #546a9a;
      --soma: #f1c40f;
      --axon: #e67e22;
      --glow: rgba(127, 240, 217, 0.3);
      --active: #7ff0d9;
      --theta: #dc2626;
      --sigma: #9370db;
      --h: #32cd32;
      --delta: #f39c12;
      --theta-prime: #e67e22;
    }

    * { box-sizing: border-box; }
    body {
      margin: 0; padding: 0; background: var(--bg);
      font-family: 'Inter', system-ui, sans-serif;
      color: var(--ink); overflow: hidden; height: 100vh;
    }

    .neuron-container {
      position: relative; width: 100vw; height: 100vh;
      display: flex; align-items: center; justify-content: center;
    }

    .neuron {
      position: relative; width: min(800px, 90vw); height: min(600px, 85vh);
      background: radial-gradient(ellipse at center, var(--membrane) 0%, var(--bg) 100%);
      border-radius: 50%; border: 2px solid var(--cytoplasm);
    }

    .title {
      position: absolute; top: 20px; left: 50%; transform: translateX(-50%);
      font-size: clamp(16px, 3vw, 24px); font-weight: 700; color: var(--active);
      text-align: center; z-index: 100;
    }

    /* Soma - the cell body at center */
    .soma {
      position: absolute; top: 50%; left: 50%; 
      transform: translate(-50%, -50%);
      width: min(160px, 20vw); height: min(160px, 20vw);
      background: radial-gradient(circle, var(--soma) 0%, var(--axon) 100%);
      border: 3px solid var(--active); border-radius: 50%;
      display: flex; flex-direction: column; justify-content: center; align-items: center;
      font-weight: 800; color: #2c3e50; cursor: pointer;
      transition: all 0.4s ease; z-index: 10;
      box-shadow: 0 0 30px rgba(241, 196, 15, 0.4);
    }
    .soma:hover { 
      transform: translate(-50%, -50%) scale(1.08); 
      box-shadow: 0 0 40px var(--glow);
    }
    .soma .symbol { font-size: clamp(24px, 4vw, 32px); margin-bottom: 8px; }
    .soma .label { font-size: clamp(10px, 1.5vw, 14px); text-align: center; line-height: 1.2; }

    /* Afferent terminals - floating in synaptic cleft */
    .afferent {
      position: absolute; width: min(100px, 12vw); height: min(60px, 8vw);
      background: linear-gradient(135deg, var(--membrane), var(--cytoplasm));
      border: 2px solid var(--synapse); border-radius: 12px;
      display: flex; flex-direction: column; justify-content: center; align-items: center;
      font-weight: 600; color: var(--ink); cursor: pointer;
      transition: all 0.3s ease; z-index: 5;
      opacity: 0.8;
    }
    .afferent:hover { 
      opacity: 1; transform: scale(1.12); 
      box-shadow: 0 0 25px var(--glow);
      border-color: var(--active);
    }
    .afferent .symbol { font-size: clamp(18px, 3vw, 24px); font-weight: 800; margin-bottom: 4px; }
    .afferent .label { font-size: clamp(8px, 1.2vw, 10px); text-align: center; line-height: 1.1; color: var(--dim); }

    /* Specific afferent positions */
    .afferent-theta { 
      bottom: min(80px, 12%); left: 50%; transform: translateX(-50%);
      border-color: var(--theta);
    }
    .afferent-theta .symbol { color: var(--theta); }

    .afferent-sigma { 
      left: min(60px, 8%); top: 50%; transform: translateY(-50%);
      border-color: var(--sigma);
    }
    .afferent-sigma .symbol { color: var(--sigma); }

    .afferent-h { 
      top: min(80px, 12%); left: 50%; transform: translateX(-50%);
      border-color: var(--h);
    }
    .afferent-h .symbol { color: var(--h); }

    /* Axon - extending east from soma */
    .axon {
      position: absolute; right: min(40px, 5%); top: 50%; transform: translateY(-50%);
      width: min(140px, 18vw); height: min(80px, 10vw);
      background: linear-gradient(90deg, var(--axon), var(--theta-prime));
      border: 2px solid var(--theta-prime); border-radius: 8px 20px 20px 8px;
      display: flex; flex-direction: column; justify-content: center; align-items: center;
      font-weight: 600; color: #2c3e50; cursor: pointer;
      transition: all 0.3s ease; z-index: 8;
      box-shadow: 0 0 20px rgba(230, 126, 34, 0.3);
    }
    .axon:hover { 
      transform: translateY(-50%) scale(1.05); 
      box-shadow: 0 0 30px var(--glow);
    }
    .axon .symbol { font-size: clamp(20px, 3.5vw, 28px); font-weight: 800; margin-bottom: 4px; color: var(--theta-prime); }
    .axon .label { font-size: clamp(8px, 1.2vw, 11px); text-align: center; line-height: 1.1; }

    /* Ion channels - subtle connection lines */
    .ion-channel {
      position: absolute; width: 2px; background: var(--synapse);
      opacity: 0.4; z-index: 1; transition: all 0.3s ease;
    }
    .ion-channel.active { opacity: 0.8; background: var(--active); width: 3px; }

    /* Detail islands that appear on hover */
    .detail-island {
      position: absolute; background: rgba(26, 35, 50, 0.95);
      border: 2px solid var(--active); border-radius: 12px;
      padding: 16px; max-width: 280px; z-index: 20;
      opacity: 0; visibility: hidden; transform: scale(0.8);
      transition: all 0.3s ease; backdrop-filter: blur(10px);
    }
    .detail-island.show { 
      opacity: 1; visibility: visible; transform: scale(1); 
    }
    .detail-island h3 { 
      color: var(--active); font-size: 16px; margin: 0 0 12px 0; 
    }
    .detail-island p { 
      color: var(--ink); font-size: 13px; line-height: 1.4; margin: 8px 0; 
    }
    .detail-island .matrix {
      background: var(--cytoplasm); border-radius: 6px; padding: 8px;
      font-family: 'Monaco', monospace; font-size: 11px; color: var(--dim);
    }

    /* Eternal recurrence indicator */
    .recurrence {
      position: absolute; top: 50%; left: 50%;
      transform: translate(-50%, -50%);
      width: min(320px, 40vw); height: min(320px, 40vw);
      border: 1px dashed var(--synapse); border-radius: 50%;
      opacity: 0.3; z-index: 1; pointer-events: none;
      animation: rotate 60s linear infinite;
    }

    @keyframes rotate {
      from { transform: translate(-50%, -50%) rotate(0deg); }
      to { transform: translate(-50%, -50%) rotate(360deg); }
    }

    .eternal-label {
      position: absolute; bottom: 20px; right: 20px;
      font-size: 11px; color: var(--dim); font-style: italic;
    }
  </style>
</head>
<body>
  <div class="neuron-container">
    <div class="neuron">
      <div class="title">Neuron Σ — Tantrum Bayesian Cycle</div>
      <div class="recurrence"></div>

      <!-- Soma - integrative cell body -->
      <div class="soma" data-island="soma">
        <div class="symbol">ΔS</div>
        <div class="label">Soma<br/>Integration</div>
      </div>

      <!-- Afferent terminals in synaptic cleft -->
      <div class="afferent afferent-theta" data-island="theta">
        <div class="symbol">θ</div>
        <div class="label">Limbic<br/>flood</div>
      </div>

      <div class="afferent afferent-sigma" data-island="sigma">
        <div class="symbol">Σ</div>
        <div class="label">Compression<br/>bottleneck</div>
      </div>

      <div class="afferent afferent-h" data-island="h">
        <div class="symbol">h(t)</div>
        <div class="label">Salience<br/>switch</div>
      </div>

      <!-- Axon - output projection -->
      <div class="axon" data-island="axon">
        <div class="symbol">θ′</div>
        <div class="label">Axonal<br/>output</div>
      </div>

      <div class="eternal-label">eternal recurrence • ion channel feedback</div>

      <!-- Detail Islands -->
      <div class="detail-island" id="island-theta" style="bottom: 120px; left: 40%;">
        <h3>θ — Limbic Flood</h3>
        <p>Ascending arousal signals from amygdala. Raw likelihood gradients: tempo, pitch, biomarkers demanding compression.</p>
      </div>

      <div class="detail-island" id="island-sigma" style="left: 120px; top: 40%;">
        <h3>Σ — Unified Compression</h3>
        <p>Two modes within one symbol:</p>
        <div class="matrix">
          diagonal: PFC self-regulation/ngikhona<br/>
          off-diagonal: mirror neuron co-regulation/sawubona
        </div>
      </div>

      <div class="detail-island" id="island-h" style="top: 120px; left: 40%;">
        <h3>h(t) — Salience Switch</h3>
        <p>Network bifurcation point. Toggle between tantrum cascade and co-regulation pathway based on compression success.</p>
      </div>

      <div class="detail-island" id="island-soma" style="top: 35%; right: 35%;">
        <h3>ΔS — Soma Integration</h3>
        <p>Cell body integrates all afferent signals. Ritual outcomes (noodles) become posteriors stored in cellular memory.</p>
      </div>

      <div class="detail-island" id="island-axon" style="right: 20px; top: 35%;">
        <h3>θ′ — Axonal Output</h3>
        <p>Bidirectional soil: descending priors from family ledger meet ascending likelihoods. Feedback completes the eternal cycle.</p>
      </div>
    </div>
  </div>

  <script>
    const elements = document.querySelectorAll('[data-island]');
    const islands = document.querySelectorAll('.detail-island');

    elements.forEach(element => {
      const islandId = 'island-' + element.getAttribute('data-island');
      const island = document.getElementById(islandId);
      
      if (island) {
        element.addEventListener('mouseenter', () => {
          islands.forEach(i => i.classList.remove('show'));
          island.classList.add('show');
        });

        element.addEventListener('mouseleave', () => {
          setTimeout(() => island.classList.remove('show'), 150);
        });

        // Keep island visible when hovering over it
        island.addEventListener('mouseenter', () => {
          island.classList.add('show');
        });

        island.addEventListener('mouseleave', () => {
          island.classList.remove('show');
        });
      }
    });
  </script>
</body>
</html>
