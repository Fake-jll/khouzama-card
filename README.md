<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="theme-color" content="#0b0f1f" />
  <title>PLAYER DATA LOADED: KHOUZAMA ✨</title>

  <style>
    :root{
      --bg0:#070a14;
      --bg1:#0b1026;
      --panel:#0f1636cc;
      --panel2:#141b44cc;
      --stroke:#ffffff22;
      --stroke2:#cdbbff33;
      --txt:#f2f6ff;
      --muted:#b7c0da;
      --pink:#ffb7e6;
      --violet:#c7b7ff;
      --mint:#a6fff3;
      --gold:#ffd36b;
      --danger:#ff6b8a;
      --shadow: 0 22px 80px rgba(0,0,0,.65);
      --glow: 0 0 22px rgba(199,183,255,.22);
      --r:18px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --ui: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
    }

    /* Kawaii theme toggle */
    [data-theme="kawaii"]{
      --bg0:#080717;
      --bg1:#140b2b;
      --panel:#1a0f35cc;
      --panel2:#22124acc;
      --stroke:#ffffff22;
      --stroke2:#ffb7e633;
      --txt:#fff7ff;
      --muted:#d4cbe6;
      --pink:#ffd0ee;
      --violet:#d8caff;
      --mint:#bffcff;
      --gold:#ffe6a6;
      --glow: 0 0 26px rgba(255,183,230,.22);
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      color:var(--txt);
      background:
        radial-gradient(900px 480px at 12% 8%, rgba(255,183,230,.18), transparent 60%),
        radial-gradient(880px 520px at 86% 12%, rgba(199,183,255,.20), transparent 55%),
        radial-gradient(820px 520px at 50% 110%, rgba(166,255,243,.10), transparent 55%),
        linear-gradient(180deg, var(--bg0), var(--bg1));
      font-family: var(--ui);
      overflow-x:hidden;
    }

    /* Subtle scanlines / CRT vibe */
    body::before{
      content:"";
      position:fixed; inset:0;
      background:
        linear-gradient(to bottom, rgba(255,255,255,.05), rgba(0,0,0,0) 2px) 0 0/100% 6px;
      opacity:.08;
      pointer-events:none;
      mix-blend-mode:overlay;
      z-index:0;
    }

    /* Floating stickers */
    .floaty{
      position:fixed;
      width:180px;height:180px;
      border-radius:50%;
      filter: blur(0px);
      opacity:.18;
      pointer-events:none;
      z-index:0;
      animation: drift 10s ease-in-out infinite;
    }
    .f1{left:-40px; top:80px; background:radial-gradient(circle at 30% 30%, var(--pink), transparent 60%)}
    .f2{right:-60px; top:140px; background:radial-gradient(circle at 30% 30%, var(--violet), transparent 60%); animation-duration:13s}
    .f3{left:30%; bottom:-80px; background:radial-gradient(circle at 30% 30%, var(--mint), transparent 60%); animation-duration:12s}

    @keyframes drift{
      0%,100%{transform: translateY(0) translateX(0) scale(1)}
      50%{transform: translateY(-14px) translateX(10px) scale(1.04)}
    }

    /* ✅ HERO IMAGE (added) */
    .hero-ui{
      position:relative;
      z-index:1;
      max-width: 1100px;
      margin: 26px auto 10px;
      padding: 0 14px;
    }
    .hero-ui img{
      width:100%;
      height:auto;
      display:block;
      border-radius:22px;
      border:1px solid var(--stroke);
      box-shadow:
        0 18px 55px rgba(0,0,0,.55),
        0 0 40px rgba(199,183,255,.28);
    }

    .wrap{
      position:relative;
      z-index:1;
      max-width: 980px;
      margin: 0 auto;
      padding: 22px 14px 70px;
    }

    .topbar{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:12px;
      margin-bottom:14px;
    }

    .title{
      display:flex;
      flex-direction:column;
      gap:4px;
    }
    .title .k{
      font-family: var(--mono);
      letter-spacing:.12em;
      font-size:12px;
      color:var(--muted);
      opacity:.95;
    }
    .title .h{
      font-size:22px;
      font-weight:800;
      letter-spacing:.02em;
      display:flex;
      align-items:center;
      gap:10px;
    }
    .pill{
      font-family:var(--mono);
      font-size:11px;
      padding:6px 10px;
      border-radius:999px;
      background:linear-gradient(180deg, rgba(255,255,255,.10), rgba(255,255,255,.05));
      border:1px solid var(--stroke);
      box-shadow: var(--glow);
      white-space:nowrap;
    }

    .controls{
      display:flex;
      flex-wrap:wrap;
      gap:8px;
      justify-content:flex-end;
    }
    .btn{
      border:1px solid var(--stroke);
      background:linear-gradient(180deg, rgba(255,255,255,.10), rgba(255,255,255,.04));
      color:var(--txt);
      border-radius:12px;
      padding:10px 12px;
      cursor:pointer;
      transition: transform .15s ease, border-color .15s ease, box-shadow .15s ease;
      font-family:var(--mono);
      font-size:12px;
    }
    .btn:hover{
      transform: translateY(-1px);
      border-color: var(--stroke2);
      box-shadow: var(--glow);
    }
    .btn:active{transform: translateY(0px) scale(.99)}
    .btn.primary{
      border-color: rgba(255,183,230,.38);
      background: linear-gradient(135deg, rgba(255,183,230,.18), rgba(199,183,255,.14));
    }

    .grid{
      display:grid;
      grid-template-columns: 1.08fr .92fr;
      gap:14px;
      align-items:start;
    }
    @media (max-width: 860px){
      .grid{grid-template-columns:1fr}
      .controls{justify-content:flex-start}
    }

    .card{
      border-radius: var(--r);
      background: linear-gradient(180deg, var(--panel), var(--panel2));
      border: 1px solid var(--stroke);
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
      transform: translateY(10px);
      opacity:0;
      animation: enter .75s ease forwards;
    }
    .card.delay{animation-delay:.12s}
    .card.delay2{animation-delay:.24s}
    .card.delay3{animation-delay:.36s}

    @keyframes enter{
      to {transform: translateY(0); opacity:1;}
    }

    .card header{
      padding:14px 14px 12px;
      border-bottom:1px solid var(--stroke);
      display:flex;
      justify-content:space-between;
      align-items:flex-start;
      gap:10px;
    }
    .card header .left{
      display:flex;
      flex-direction:column;
      gap:6px;
      min-width:0;
    }
    .card header .right{
      display:flex;
      gap:8px;
      align-items:center;
      flex-wrap:wrap;
      justify-content:flex-end;
    }

    .playerName{
      font-size:18px;
      font-weight:900;
      letter-spacing:.05em;
      font-family:var(--mono);
      text-transform:uppercase;
      color:var(--violet);
      text-shadow: 0 0 22px rgba(199,183,255,.18);
      overflow:hidden;
      text-overflow:ellipsis;
      white-space:nowrap;
      max-width: 100%;
    }
    .metaRow{
      display:flex;
      flex-wrap:wrap;
      gap:8px;
      align-items:center;
    }
    .tag{
      display:inline-flex;
      gap:8px;
      align-items:center;
      padding:6px 10px;
      border-radius:999px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.16);
      font-family:var(--mono);
      font-size:11px;
      color:var(--muted);
    }
    .dot{width:6px;height:6px;border-radius:99px;background:var(--mint); box-shadow:0 0 12px rgba(166,255,243,.35)}
    .dot.off{background:rgba(255,255,255,.25); box-shadow:none}

    .content{padding:14px}
    .sectionTitle{
      font-family:var(--mono);
      font-size:12px;
      letter-spacing:.12em;
      color:var(--muted);
      margin: 2px 0 10px;
      display:flex;
      align-items:center;
      gap:8px;
    }

    /* stats */
    .stats{
      display:grid;
      gap:10px;
      padding: 10px 12px;
      border-radius:16px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.15);
      overflow:hidden;
      position:relative;
    }
    .stats::after{
      content:"";
      position:absolute; inset:0;
      background: radial-gradient(500px 200px at 10% 0%, rgba(255,183,230,.08), transparent 60%),
                  radial-gradient(500px 200px at 90% 10%, rgba(199,183,255,.10), transparent 60%);
      pointer-events:none;
    }

    .stat{
      position:relative;
      display:grid;
      grid-template-columns: 160px 1fr 54px;
      gap:10px;
      align-items:center;
      z-index:1;
    }
    @media (max-width: 520px){
      .stat{grid-template-columns: 1fr; gap:6px}
      .stat .pct{justify-self:start}
    }
    .stat .lbl{
      font-family:var(--mono);
      font-size:12px;
      color:var(--txt);
      opacity:.95;
    }
    .bar{
      height:10px;
      border-radius:999px;
      background: rgba(255,255,255,.08);
      border:1px solid var(--stroke);
      overflow:hidden;
      position:relative;
    }
    .bar > i{
      display:block;
      height:100%;
      width:0%;
      border-radius:999px;
      background: linear-gradient(90deg, var(--mint), var(--violet), var(--pink));
      filter: saturate(1.1);
      box-shadow: 0 0 18px rgba(199,183,255,.22);
      animation: fill 1.2s ease forwards;
    }
    .bar > i::after{
      content:"";
      position:absolute; inset:0;
      background: linear-gradient(90deg, rgba(255,255,255,.25), rgba(255,255,255,0));
      transform: translateX(-45%);
      animation: sheen 2.2s ease-in-out infinite;
      opacity:.25;
    }
    @keyframes fill{to{width:var(--w)}}
    @keyframes sheen{
      0%{transform:translateX(-55%)}
      50%{transform:translateX(60%)}
      100%{transform:translateX(60%)}
    }
    .pct{
      font-family:var(--mono);
      font-size:12px;
      color:var(--muted);
      justify-self:end;
    }

    /* lists */
    .list{
      margin:0;
      padding: 10px 14px;
      border-radius:16px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.15);
    }
    .list li{
      margin: 8px 0;
      line-height:1.4;
      color:var(--txt);
      opacity:.96;
    }
    .list li b{color:var(--pink)}
    .list .muted{color:var(--muted)}
    .smallRow{
      display:flex;
      flex-wrap:wrap;
      gap:8px;
      margin-top:10px;
      color:var(--muted);
      font-family:var(--mono);
      font-size:11px;
      opacity:.95;
    }

    /* inventory cards */
    .invGrid{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:10px;
    }
    @media (max-width: 520px){ .invGrid{grid-template-columns:1fr} }
    .inv{
      border-radius:16px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.15);
      padding:10px 12px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:10px;
      cursor:pointer;
      transition: transform .15s ease, border-color .15s ease;
      user-select:none;
    }
    .inv:hover{transform: translateY(-1px); border-color: var(--stroke2)}
    .inv .l{
      display:flex; gap:10px; align-items:center; min-width:0;
    }
    .icon{
      width:34px; height:34px; border-radius:12px;
      display:grid; place-items:center;
      background: linear-gradient(135deg, rgba(255,183,230,.18), rgba(199,183,255,.14));
      border:1px solid var(--stroke);
      box-shadow: var(--glow);
      flex:0 0 auto;
      font-size:16px;
    }
    .inv .txt{
      display:flex; flex-direction:column; gap:3px; min-width:0;
    }
    .inv .txt .t{
      font-family:var(--mono);
      font-size:12px;
      color:var(--txt);
      white-space:nowrap;
      overflow:hidden;
      text-overflow:ellipsis;
    }
    .inv .txt .d{
      font-size:12px;
      color:var(--muted);
      opacity:.9;
      white-space:nowrap;
      overflow:hidden;
      text-overflow:ellipsis;
    }
    .rarity{
      font-family:var(--mono);
      font-size:11px;
      padding:6px 8px;
      border-radius:999px;
      border:1px solid var(--stroke);
      color:var(--muted);
      background: rgba(255,255,255,.06);
      flex:0 0 auto;
    }
    .rarity.gold{color:#201400; border-color: rgba(255,211,107,.55); background: rgba(255,211,107,.18)}
    .rarity.pink{color:#2b0017; border-color: rgba(255,183,230,.55); background: rgba(255,183,230,.18)}
    .rarity.violet{color:#12002b; border-color: rgba(199,183,255,.55); background: rgba(199,183,255,.18)}

    /* secret modal */
    .secretBox{
      border-radius:16px;
      border:1px dashed rgba(199,183,255,.45);
      background: rgba(0,0,0,.12);
      padding:10px 12px;
      font-family:var(--mono);
      font-size:12px;
      color:var(--muted);
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:10px;
      cursor:pointer;
      user-select:none;
      transition: border-color .15s ease, transform .15s ease, box-shadow .15s ease;
    }
    .secretBox:hover{
      transform: translateY(-1px);
      border-color: rgba(255,183,230,.55);
      box-shadow: var(--glow);
    }
    .secretBox .lock{font-size:16px}
    .secretPanel{
      margin-top:10px;
      display:none;
      border-radius:16px;
      border:1px solid rgba(255,183,230,.35);
      background: rgba(0,0,0,.18);
      padding:12px 12px;
    }
    .secretPanel ul{margin:0; padding-left:18px}
    .secretPanel li{margin:8px 0; color:var(--txt); opacity:.95}
    .secretPanel b{color:var(--gold)}

    /* right column modules */
    .miniGrid{
      display:grid;
      gap:14px;
    }
    .chipRow{display:flex; gap:8px; flex-wrap:wrap}
    .chip{
      font-family:var(--mono);
      font-size:11px;
      padding:7px 10px;
      border-radius:999px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.14);
      color:var(--muted);
      cursor:pointer;
      transition:.15s;
      user-select:none;
    }
    .chip:hover{border-color: var(--stroke2); transform:translateY(-1px)}
    .chip.on{
      color:#0a0712;
      background: linear-gradient(135deg, rgba(166,255,243,.85), rgba(255,183,230,.7));
      border-color: rgba(255,255,255,.35);
    }

    /* pet */
    .pet{
      display:flex;
      align-items:center;
      gap:12px;
      padding:12px;
      border-radius:16px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.15);
    }
    .pet .face{
      width:54px;height:54px;border-radius:16px;
      display:grid;place-items:center;
      border:1px solid var(--stroke);
      background: radial-gradient(circle at 30% 30%, rgba(255,183,230,.22), rgba(199,183,255,.12));
      box-shadow: var(--glow);
      font-size:22px;
      transform-origin:center;
      animation: wiggle 2.6s ease-in-out infinite;
    }
    @keyframes wiggle{
      0%,100%{transform:rotate(0deg)}
      50%{transform:rotate(-4deg)}
    }
    .pet .ptext{
      display:flex; flex-direction:column; gap:4px;
    }
    .pet .ptext .t{
      font-family:var(--mono);
      font-size:12px;
      color:var(--txt);
      letter-spacing:.06em;
      text-transform:uppercase;
    }
    .pet .ptext .d{
      font-size:12px;
      color:var(--muted);
    }

    /* toast */
    .toast{
      position:fixed;
      left:50%;
      bottom:18px;
      transform:translateX(-50%) translateY(20px);
      opacity:0;
      background: rgba(0,0,0,.55);
      border:1px solid var(--stroke);
      border-radius: 999px;
      padding: 10px 12px;
      color: var(--txt);
      font-family: var(--mono);
      font-size: 12px;
      box-shadow: var(--shadow);
      z-index: 99;
      transition: .25s ease;
      pointer-events:none;
      max-width: calc(100% - 24px);
      white-space:nowrap;
      overflow:hidden;
      text-overflow:ellipsis;
    }
    .toast.show{
      opacity:1;
      transform:translateX(-50%) translateY(0);
    }

    /* sparkles canvas */
    canvas#spark{
      position:fixed;
      inset:0;
      pointer-events:none;
      z-index:2;
    }

    /* footer log */
    .syslog{
      font-family:var(--mono);
      font-size:11px;
      color:var(--muted);
      opacity:.92;
      line-height:1.55;
      border-radius:16px;
      border:1px solid var(--stroke);
      background: rgba(0,0,0,.14);
      padding:12px;
      margin-top:12px;
    }
    .syslog b{color:var(--pink)}
  </style>
</head>

<body data-theme="kawaii">
  <!-- ✅ HERO IMAGE FIRST (added) -->
  <div class="hero-ui">
    <img src="65652F8C-41FF-4D35-A6EE-C02E4509FC1B.png" alt="Khouzama Game UI">
  </div>

  <div class="floaty f1"></div>
  <div class="floaty f2"></div>
  <div class="floaty f3"></div>
  <canvas id="spark"></canvas>

  <div class="wrap">
    <div class="topbar">
      <div class="title">
        <div class="k">PLAYER DATA LOADED</div>
        <div class="h">
          KHOUZAMA <span class="pill" id="statusPill">Sound FX: enabled</span>
        </div>
      </div>

      <div class="controls">
        <button class="btn" id="btnTheme">Theme: KAWAII</button>
        <button class="btn" id="btnSfx">Toggle SFX</button>
        <button class="btn primary" id="btnReboot">Reboot</button>
      </div>
    </div>

    <div class="grid">
      <!-- LEFT: main profile -->
      <section class="card">
        <header>
          <div class="left">
            <div class="playerName" id="playerName">KHOUZAMA</div>
            <div class="metaRow">
              <span class="tag"><span class="dot" id="dotSfx"></span> Sound FX: <span id="sfxText">enabled</span></span>
              <span class="tag">🎂 Born: <b style="color:var(--txt)">May 31</b></span>
              <span class="tag">💜🖤 Main Colors: <b style="color:var(--violet)">Purple</b> + <b style="color:var(--muted)">Black</b></span>
              <span class="tag">✨ Signature: <b style="color:var(--pink)">Wide eyes</b> • Short haircut</span>
            </div>
          </div>
          <div class="right">
            <span class="pill">Cute RPG UI</span>
          </div>
        </header>

        <div class="content">
          <div class="sectionTitle">STATS</div>
          <div class="stats">
            <div class="stat">
              <div class="lbl">✨ Cuteness</div>
              <div class="bar"><i style="--w:94%"></i></div>
              <div class="pct">94%</div>
            </div>
            <div class="stat">
              <div class="lbl">🎮 Playfulness</div>
              <div class="bar"><i style="--w:90%"></i></div>
              <div class="pct">90%</div>
            </div>
            <div class="stat">
              <div class="lbl">🧠 Smart Moves</div>
              <div class="bar"><i style="--w:82%"></i></div>
              <div class="pct">82%</div>
            </div>
            <div class="stat">
              <div class="lbl">🌙 Night Energy</div>
              <div class="bar"><i style="--w:88%"></i></div>
              <div class="pct">88%</div>
            </div>
            <div class="stat">
              <div class="lbl">🫧 Soft Aura</div>
              <div class="bar"><i style="--w:86%"></i></div>
              <div class="pct">86%</div>
            </div>
          </div>

          <div class="sectionTitle" style="margin-top:14px;">PASSIVE TRAITS</div>
          <ul class="list">
            <li>🌸 <b>Softness</b> only shows with safe people.</li>
            <li>🧩 Notices micro-details. <span class="muted">(the tiny stuff)</span></li>
            <li>🫶 Carries more than she shows.</li>
            <li>🫧 Pulls back to breathe — not to hurt.</li>
            <li>😶 <b>Silence</b> = not satisfied.</li>
          </ul>

          <div class="smallRow">
            <span>Calm with strangers</span> •
            <span>Playful with her circle</span> •
            <span>Head + heart combo</span>
          </div>

          <div class="sectionTitle" style="margin-top:14px;">SECRET TRAIT (tap)</div>
          <div class="secretBox" id="secretToggle" role="button" aria-label="Toggle secret trait">
            <span class="lock">🔒</span>
            <span>Understands looks — no explanation needed.</span>
            <span class="pill">Tap to toggle</span>
          </div>
          <div class="secretPanel" id="secretPanel">
            <ul>
              <li>💪 Strongest version appears under pressure.</li>
              <li>🎛 Main switch: <b>honesty</b>.</li>
              <li>🍿 Combo: coffee + food + movies → calm state.</li>
            </ul>
          </div>

          <div class="sectionTitle" style="margin-top:14px;">INVENTORY</div>
          <div class="invGrid">
            <div class="inv" data-toast="Black coffee equipped ☕">
              <div class="l">
                <div class="icon">☕</div>
                <div class="txt">
                  <div class="t">Black coffee</div>
                  <div class="d">non-negotiable</div>
                </div>
              </div>
              <div class="rarity gold">MAIN</div>
            </div>

            <div class="inv" data-toast="Tissues added 🧻">
              <div class="l">
                <div class="icon">🧻</div>
                <div class="txt">
                  <div class="t">Tissues</div>
                  <div class="d">just in case</div>
                </div>
              </div>
              <div class="rarity">UTIL</div>
            </div>

            <div class="inv" data-toast="Latin playlist started 🎧">
              <div class="l">
                <div class="icon">🎧</div>
                <div class="txt">
                  <div class="t">Latin music</div>
                  <div class="d">mood booster</div>
                </div>
              </div>
              <div class="rarity violet">VIBE</div>
            </div>

            <div class="inv" data-toast="Online mode 📱✨">
              <div class="l">
                <div class="icon">📱</div>
                <div class="txt">
                  <div class="t">Phone + Internet</div>
                  <div class="d">always on</div>
                </div>
              </div>
              <div class="rarity pink">CORE</div>
            </div>

            <div class="inv" data-toast="Appreciation detected 💜">
              <div class="l">
                <div class="icon">💜</div>
                <div class="txt">
                  <div class="t">Appreciation</div>
                  <div class="d">calms her instantly</div>
                </div>
              </div>
              <div class="rarity violet">BUFF</div>
            </div>

            <div class="inv" data-toast="Reward claimed 🏆">
              <div class="l">
                <div class="icon">🏆</div>
                <div class="txt">
                  <div class="t">Rewards</div>
                  <div class="d">gives energy</div>
                </div>
              </div>
              <div class="rarity gold">BOOST</div>
            </div>
          </div>

          <div class="syslog" id="syslog">
            <div><b>SYSTEM LOG</b></div>
            <div>Boot sequence: OK.</div>
            <div>Profile integrity: stable.</div>
            <div>Trait scan: micro-detail awareness detected.</div>
            <div>Mode: night + cold weather preference locked.</div>
            <div>Warning: disrespect = instant boundary.</div>
            <div>Creative engine: best in controlled chaos.</div>
            <div>Secret trait: tap to reveal.</div>
          </div>
        </div>
      </section>

      <!-- RIGHT: side modules -->
      <aside class="miniGrid">
        <section class="card delay">
          <header>
            <div class="left">
              <div class="playerName" style="font-size:14px;color:var(--pink)">KAWAII VIBE MODULE</div>
              <div class="metaRow">
                <span class="tag">🌙 Night lover</span>
                <span class="tag">❄️ Cold weather</span>
                <span class="tag">🧁 Cute energy</span>
              </div>
            </div>
          </header>
          <div class="content">
            <div class="sectionTitle">VIBE</div>
            <ul class="list">
              <li>🌙 Night energy (sparkly brain hours).</li>
              <li>❄️ Cold weather lover — cozy hoodie mode.</li>
              <li>🌌 Open spaces &gt; closed rooms.</li>
              <li>💖 Feels herself with people she loves.</li>
              <li>🧠 Thinks &amp; creates best in <b>controlled chaos</b>.</li>
            </ul>

            <div class="sectionTitle" style="margin-top:12px;">MOOD BUTTONS</div>
            <div class="chipRow" id="moodRow">
              <div class="chip" data-m="sparkle">✨ Sparkle</div>
              <div class="chip" data-m="cozy">🫧 Cozy</div>
              <div class="chip" data-m="play">🎀 Play</div>
              <div class="chip" data-m="focus">🧠 Focus</div>
            </div>
          </div>
        </section>

        <section class="card delay2">
          <header>
            <div class="left">
              <div class="playerName" style="font-size:14px;color:var(--violet)">QUESTS & ACHIEVEMENTS</div>
              <div class="metaRow">
                <span class="tag">🎯 Goals</span>
                <span class="tag">🏅 Badges</span>
              </div>
            </div>
          </header>
          <div class="content">
            <div class="sectionTitle">QUESTS</div>
            <ul class="list">
              <li>☕ Get coffee → +10 mood.</li>
              <li>🎬 Movie + snack combo → calm state.</li>
              <li>💬 Honest talk → instant unlock.</li>
              <li>🧹 Reset alone time → energy refill.</li>
            </ul>

            <div class="sectionTitle" style="margin-top:12px;">ACHIEVEMENTS</div>
            <div class="invGrid">
              <div class="inv" data-toast="Achievement: Soft glow unlocked ✨">
                <div class="l">
                  <div class="icon">✨</div>
                  <div class="txt">
                    <div class="t">Soft Glow</div>
                    <div class="d">visible kindness</div>
                  </div>
                </div>
                <div class="rarity violet">RARE</div>
              </div>

              <div class="inv" data-toast="Achievement: Boundaries set 💅">
                <div class="l">
                  <div class="icon">💅</div>
                  <div class="txt">
                    <div class="t">Boundaries</div>
                    <div class="d">no disrespect</div>
                  </div>
                </div>
                <div class="rarity pink">EPIC</div>
              </div>
            </div>
          </div>
        </section>

        <section class="card delay3">
          <header>
            <div class="left">
              <div class="playerName" style="font-size:14px;color:var(--gold)">COMPANION</div>
              <div class="metaRow">
                <span class="tag">🧸 Kawaii Pet</span>
                <span class="tag">✨ Reactive</span>
              </div>
            </div>
          </header>
          <div class="content">
            <div class="sectionTitle">PET STATUS</div>
            <div class="pet" id="pet">
              <div class="face" id="petFace">🧸</div>
              <div class="ptext">
                <div class="t">BUBBLES</div>
                <div class="d" id="petLine">Tap me for sparkles ✨</div>
              </div>
            </div>

            <div class="sectionTitle" style="margin-top:12px;">LORE</div>
            <div class="syslog">
              <div>Attention finds her — she never asks.</div>
              <div>Those who know her well see pure generosity.</div>
              <div>From afar: strong charisma.</div>
              <div>One word: <b>ADORABLE</b>.</div>
            </div>
          </div>
        </section>
      </aside>
    </div>
  </div>

  <div class="toast" id="toast">...</div>

<script>
/* -----------------------------
   Kawaii Pro UI — interactions
------------------------------ */

const state = {
  sfx: true,
  theme: "kawaii", // kawaii | cyber
  mood: new Set(),
};

const toastEl = document.getElementById("toast");
const sfxText = document.getElementById("sfxText");
const dotSfx = document.getElementById("dotSfx");
const statusPill = document.getElementById("statusPill");
const btnSfx = document.getElementById("btnSfx");
const btnReboot = document.getElementById("btnReboot");
const btnTheme = document.getElementById("btnTheme");
const secretToggle = document.getElementById("secretToggle");
const secretPanel = document.getElementById("secretPanel");
const pet = document.getElementById("pet");
const petFace = document.getElementById("petFace");
const petLine = document.getElementById("petLine");
const moodRow = document.getElementById("moodRow");

/* ---------- Toast ---------- */
let toastTimer = null;
function toast(msg){
  toastEl.textContent = msg;
  toastEl.classList.add("show");
  clearTimeout(toastTimer);
  toastTimer = setTimeout(()=> toastEl.classList.remove("show"), 1600);
}

/* ---------- WebAudio SFX (no external files) ---------- */
let audioCtx = null;
function A(){
  if(!audioCtx){
    audioCtx = new (window.AudioContext || window.webkitAudioContext)();
  }
  return audioCtx;
}
function beep({type="sine", freq=660, dur=0.06, gain=0.05, slide=0}={}){
  if(!state.sfx) return;
  const ctx = A();
  const o = ctx.createOscillator();
  const g = ctx.createGain();
  const now = ctx.currentTime;

  o.type = type;
  o.frequency.setValueAtTime(freq, now);
  if(slide) o.frequency.exponentialRampToValueAtTime(freq * slide, now + dur);

  g.gain.setValueAtTime(0.0001, now);
  g.gain.exponentialRampToValueAtTime(gain, now + 0.01);
  g.gain.exponentialRampToValueAtTime(0.0001, now + dur);

  o.connect(g).connect(ctx.destination);
  o.start(now);
  o.stop(now + dur + 0.01);
}
function clickSfx(){
  beep({type:"triangle", freq:820, dur:0.05, gain:0.045, slide:1.3});
}
function toggleSfx(){
  beep({type:"square", freq:520, dur:0.06, gain:0.04, slide:0.9});
}
function rebootSfx(){
  if(!state.sfx) return;
  // cute "power up" chord
  beep({type:"sine", freq:440, dur:0.10, gain:0.04, slide:1.25});
  setTimeout(()=>beep({type:"sine", freq:550, dur:0.10, gain:0.04, slide:1.15}), 70);
  setTimeout(()=>beep({type:"sine", freq:660, dur:0.12, gain:0.05, slide:1.12}), 140);
}

/* ---------- Sparkles Canvas ---------- */
const canvas = document.getElementById("spark");
const ctx2d = canvas.getContext("2d");
let W=0,H=0;
let sparks=[];
function resize(){
  W = canvas.width = window.innerWidth * devicePixelRatio;
  H = canvas.height = window.innerHeight * devicePixelRatio;
  canvas.style.width = window.innerWidth+"px";
  canvas.style.height = window.innerHeight+"px";
}
window.addEventListener("resize", resize);
resize();

function addSpark(x,y, n=18){
  const px = x*devicePixelRatio;
  const py = y*devicePixelRatio;
  for(let i=0;i<n;i++){
    sparks.push({
      x:px, y:py,
      vx:(Math.random()*2-1)*2.2*devicePixelRatio,
      vy:(Math.random()*-1.8-0.6)*2.6*devicePixelRatio,
      life: 40+Math.random()*20,
      r: 2+Math.random()*2,
      t: 0,
    });
  }
}
function loop(){
  ctx2d.clearRect(0,0,W,H);
  for(let i=sparks.length-1;i>=0;i--){
    const p = sparks[i];
    p.t++;
    p.x += p.vx;
    p.y += p.vy;
    p.vy += 0.08*devicePixelRatio;
    const a = Math.max(0, 1 - p.t/p.life);

    // color blend cute
    ctx2d.globalAlpha = a;
    ctx2d.fillStyle = `rgba(${240},${220},${255},${a})`;
    ctx2d.beginPath();
    ctx2d.arc(p.x,p.y,p.r,0,Math.PI*2);
    ctx2d.fill();

    // tiny star cross
    ctx2d.strokeStyle = `rgba(255,183,230,${a})`;
    ctx2d.lineWidth = 1*devicePixelRatio;
    ctx2d.beginPath();
    ctx2d.moveTo(p.x-3*devicePixelRatio,p.y);
    ctx2d.lineTo(p.x+3*devicePixelRatio,p.y);
    ctx2d.moveTo(p.x,p.y-3*devicePixelRatio);
    ctx2d.lineTo(p.x,p.y+3*devicePixelRatio);
    ctx2d.stroke();

    if(p.t>p.life) sparks.splice(i,1);
  }
  requestAnimationFrame(loop);
}
loop();

/* ---------- Inventory item clicks ---------- */
document.querySelectorAll(".inv").forEach(el=>{
  el.addEventListener("click", (e)=>{
    clickSfx();
    const r = el.getBoundingClientRect();
    addSpark(r.left + r.width*0.6, r.top + r.height*0.4, 14);
    toast(el.getAttribute("data-toast") || "✨");
  });
});

/* ---------- Secret trait toggle ---------- */
let secretOpen=false;
secretToggle.addEventListener("click", ()=>{
  toggleSfx();
  secretOpen = !secretOpen;
  secretPanel.style.display = secretOpen ? "block" : "none";
  toast(secretOpen ? "Secret trait unlocked ✨" : "Secret trait hidden 🔒");
  const r = secretToggle.getBoundingClientRect();
  addSpark(r.left + r.width*0.2, r.top + r.height*0.7, secretOpen ? 22 : 10);
});

/* ---------- Pet interactions ---------- */
const petLines = [
  "Kyaa~ sparkle time! ✨",
  "I guard your mood bar 🧸💖",
  "Coffee quest? I’m in ☕",
  "Soft mode: ON 🫧",
  "No disrespect allowed 😤💅",
];
pet.addEventListener("click",(e)=>{
  clickSfx();
  petFace.style.animation = "none";
  // force reflow then restart bounce
  void petFace.offsetWidth;
  petFace.style.animation = "wiggle 2.6s ease-in-out infinite";
  petLine.textContent = petLines[Math.floor(Math.random()*petLines.length)];
  addSpark(e.clientX, e.clientY, 24);
});

/* ---------- Mood chips ---------- */
moodRow.querySelectorAll(".chip").forEach(chip=>{
  chip.addEventListener("click",(e)=>{
    toggleSfx();
    const key = chip.dataset.m;
    if(state.mood.has(key)){
      state.mood.delete(key);
      chip.classList.remove("on");
      toast(`Mood off: ${key}`);
    }else{
      state.mood.add(key);
      chip.classList.add("on");
      toast(`Mood on: ${key} ✨`);
      addSpark(e.clientX, e.clientY, 12);
    }
  });
});

/* ---------- Toggle SFX ---------- */
function renderSfx(){
  sfxText.textContent = state.sfx ? "enabled" : "disabled";
  statusPill.textContent = `Sound FX: ${state.sfx ? "enabled" : "disabled"}`;
  dotSfx.classList.toggle("off", !state.sfx);
}
btnSfx.addEventListener("click", ()=>{
  state.sfx = !state.sfx;
  renderSfx();
  toast(state.sfx ? "SFX enabled 🔊" : "SFX disabled 🔇");
  // play a tiny beep only when turning ON (so it doesn't beep when OFF)
  if(state.sfx) toggleSfx();
});
renderSfx();

/* ---------- Theme toggle ---------- */
btnTheme.addEventListener("click",(e)=>{
  toggleSfx();
  const body = document.body;
  const now = body.getAttribute("data-theme");
  const next = (now === "kawaii") ? "cyber" : "kawaii";
  body.setAttribute("data-theme", next);
  btnTheme.textContent = `Theme: ${next.toUpperCase()}`;
  toast(next === "kawaii" ? "Kawaii theme 💖" : "Cyber theme 🧠");
  addSpark(e.clientX, e.clientY, 18);
});

/* ---------- Reboot (replay animations) ---------- */
btnReboot.addEventListener("click",(e)=>{
  rebootSfx();
  toast("Rebooting… ✨");
  addSpark(e.clientX, e.clientY, 28);

  // replay bar animations by resetting widths
  document.querySelectorAll(".bar > i").forEach(i=>{
    const w = i.style.getPropertyValue("--w") || "80%";
    i.style.animation = "none";
    i.style.width = "0%";
    void i.offsetWidth;
    i.style.animation = "fill 1.2s ease forwards";
    i.style.setProperty("--w", w);
  });

  // close secret
  secretOpen = false;
  secretPanel.style.display = "none";
  // cute pet line reset
  petLine.textContent = "Tap me for sparkles ✨";
});

/* ---------- Auto sparkle on first user interaction (unlock audio policy) ---------- */
let unlocked = false;
function unlockOnce(e){
  if(unlocked) return;
  unlocked = true;
  try{ A(); }catch(_){}
  addSpark(window.innerWidth*0.5, 140, 26);
  toast("Welcome, Khouzama ✨");
  clickSfx();
  window.removeEventListener("pointerdown", unlockOnce);
}
window.addEventListener("pointerdown", unlockOnce, {passive:true});
</script>
</body>
</html>
