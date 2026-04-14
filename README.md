
  @import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&display=swap');

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: #0a0a0a;
    color: #00ff41;
    font-family: 'Share Tech Mono', 'Courier New', monospace;
    padding: 20px;
    min-height: 100vh;
  }

  .scanline {
    position: fixed; top: 0; left: 0; width: 100%; height: 100%;
    background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,255,65,0.015) 2px, rgba(0,255,65,0.015) 4px);
    pointer-events: none; z-index: 999;
  }

  .container { max-width: 860px; margin: 0 auto; position: relative; }

  /* Defacement header */
  .defaced-header {
    border: 1px solid #ff0033;
    padding: 18px;
    margin-bottom: 20px;
    position: relative;
    background: rgba(255,0,51,0.04);
    animation: borderPulse 2s infinite;
  }
  @keyframes borderPulse {
    0%,100% { border-color: #ff0033; box-shadow: 0 0 8px rgba(255,0,51,0.3); }
    50% { border-color: #ff4466; box-shadow: 0 0 18px rgba(255,0,51,0.6); }
  }

  .tag-line {
    font-size: 10px;
    color: #ff0033;
    letter-spacing: 4px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  .ascii-art {
    color: #00ff41;
    font-size: 11px;
    line-height: 1.2;
    text-shadow: 0 0 6px rgba(0,255,65,0.5);
    white-space: pre;
    overflow-x: auto;
  }

  .ph-flag-bar {
    display: flex;
    height: 4px;
    margin: 12px 0;
  }
  .ph-flag-bar .blue { flex: 1; background: #0038A8; }
  .ph-flag-bar .red  { flex: 1; background: #CE1126; }

  .hacked-by {
    color: #ff0033;
    font-size: 13px;
    letter-spacing: 2px;
    text-align: center;
    margin: 8px 0;
    animation: glitch 3s infinite;
  }
  @keyframes glitch {
    0%,96%,100% { transform: none; filter: none; }
    97% { transform: translateX(-2px); filter: hue-rotate(90deg); }
    98% { transform: translateX(2px); filter: hue-rotate(180deg); color: #fff; }
    99% { transform: none; filter: none; }
  }

  .msg-ph {
    text-align: center;
    color: #ffd700;
    font-size: 11px;
    letter-spacing: 3px;
    margin-top: 6px;
  }

  /* Terminal blocks */
  .terminal-block {
    border: 1px solid rgba(0,255,65,0.2);
    margin-bottom: 16px;
    background: rgba(0,0,0,0.5);
  }
  .terminal-block .t-header {
    background: rgba(0,255,65,0.08);
    padding: 5px 12px;
    font-size: 10px;
    color: #00ff41;
    letter-spacing: 2px;
    border-bottom: 1px solid rgba(0,255,65,0.15);
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .t-header .dots { display: flex; gap: 4px; }
  .t-header .dot { width: 8px; height: 8px; border-radius: 50%; }
  .dot-r { background: #ff5f56; }
  .dot-y { background: #ffbd2e; }
  .dot-g { background: #27c93f; }

  .terminal-block pre {
    padding: 14px;
    font-size: 12px;
    line-height: 1.7;
    overflow-x: auto;
  }

  .prompt { color: #ff0033; }
  .cmd    { color: #00ff41; }
  .key    { color: #00bfff; }
  .val    { color: #ffffff; }
  .comment{ color: #555; }
  .green-bright { color: #39ff14; }
  .yellow { color: #ffd700; }
  .red    { color: #ff4444; }
  .white  { color: #eee; }
  .orange { color: #ff8c00; }

  /* Whoami table */
  .info-table {
    width: 100%; border-collapse: collapse; font-size: 12px;
    font-family: 'Share Tech Mono', monospace;
  }
  .info-table td { padding: 4px 10px; vertical-align: top; }
  .info-table td:first-child { color: #00bfff; white-space: nowrap; min-width: 120px; }
  .info-table td:nth-child(2) { color: #00ff41; width: 20px; }
  .info-table td:last-child { color: #fff; }

  /* Stack section */
  .stack-row { margin-bottom: 8px; }
  .stack-cat { color: #555; font-size: 11px; margin-bottom: 2px; }
  .badge {
    display: inline-block;
    border: 1px solid;
    padding: 1px 7px;
    font-size: 11px;
    margin: 2px 3px 2px 0;
    border-radius: 2px;
  }
  .badge-green { border-color: #00ff41; color: #00ff41; background: rgba(0,255,65,0.07); }
  .badge-blue  { border-color: #00bfff; color: #00bfff; background: rgba(0,191,255,0.07); }
  .badge-gray  { border-color: #555; color: #888; background: rgba(85,85,85,0.07); }

  /* Diff log */
  .diff-add  { color: #39ff14; }
  .diff-warn { color: #ffd700; }
  .diff-del  { color: #ff4444; }

  /* Activity cron */
  .cron-row { display: flex; gap: 16px; margin-bottom: 4px; }
  .cron-time { color: #ff0033; min-width: 55px; }
  .cron-icon { min-width: 22px; }
  .cron-cmd  { color: #00ff41; }

  /* Stats */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 10px;
    padding: 14px;
    font-size: 11px;
  }
  .stat-box {
    border: 1px solid rgba(0,255,65,0.2);
    padding: 10px;
    text-align: center;
  }
  .stat-val { font-size: 22px; color: #00ff41; display: block; margin-bottom: 3px; }
  .stat-label { color: #555; font-size: 10px; letter-spacing: 1px; }

  /* Ping / social */
  .social-row { display: flex; gap: 10px; align-items: center; margin-bottom: 4px; font-size: 12px; }
  .social-key { color: #00bfff; min-width: 100px; }
  .social-arrow { color: #555; }
  .social-val { color: #fff; text-decoration: none; }
  .social-val:hover { color: #00ff41; }

  /* Footer */
  .footer-motto {
    text-align: center;
    border-top: 1px solid rgba(255,0,51,0.3);
    margin-top: 20px;
    padding-top: 14px;
    color: #555;
    font-size: 11px;
    letter-spacing: 3px;
  }
  .footer-motto span { color: #ff0033; }

  .blink { animation: blink 1s step-end infinite; }
  @keyframes blink { 50% { opacity: 0; } }

  .section-sep {
    border: none;
    border-top: 1px solid rgba(0,255,65,0.1);
    margin: 0;
  }

  /* Typing text */
  .typing-bar {
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid #00ff41;
    animation: typing 3.5s steps(60,end) 0.5s both, blinkCursor 0.75s step-end infinite;
    font-size: 11px;
    color: #00bfff;
    letter-spacing: 1px;
    max-width: 520px;
    margin: 6px auto 0;
  }
  @keyframes typing { from { width: 0; } to { width: 100%; } }
  @keyframes blinkCursor { 50% { border-color: transparent; } }

  .glitch-text {
    position: relative;
    display: inline-block;
  }
  .glitch-text::before,
  .glitch-text::after {
    content: attr(data-text);
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
  }
  .glitch-text::before {
    color: #ff0033;
    animation: glitch-1 2.5s infinite;
    clip-path: polygon(0 0, 100% 0, 100% 45%, 0 45%);
  }
  .glitch-text::after {
    color: #00bfff;
    animation: glitch-2 2.5s infinite;
    clip-path: polygon(0 55%, 100% 55%, 100% 100%, 0 100%);
  }
  @keyframes glitch-1 {
    0%,90%,100% { transform: none; }
    91% { transform: translateX(-3px); }
    93% { transform: translateX(2px); }
  }
  @keyframes glitch-2 {
    0%,90%,100% { transform: none; }
    92% { transform: translateX(3px); }
    94% { transform: translateX(-2px); }
  }
