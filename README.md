<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>PatricioCoding — Fractality In Code</title>
  
  <!-- SEO Meta Tags -->
  <meta name="description" content="Professional TradingView indicators for US traders – Harmonic Patterns, Gann, Elliott Wave, and algorithmic systems. Instant delivery.">
  <meta name="keywords" content="TradingView indicators, harmonic patterns, Gann theory, Elliott wave, algorithmic trading, Pine Script">
  <meta name="author" content="PatricioCoding">
  <meta name="robots" content="index, follow">
  <meta property="og:title" content="PatricioCoding – Pro Trading Indicators">
  <meta property="og:description" content="High-performance trading indicators designed to trade accurately in any market. Get instant access to premium TradingView tools.">
  <meta property="og:type" content="website">
  <meta property="og:url" content="https://patriciocoding.com">
  <meta property="og:image" content="og-image.png">
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="PatricioCoding – Pro Trading Indicators">
  <meta name="twitter:description" content="Professional TradingView indicators for US traders.">
  
  <link rel="canonical" href="https://patriciocoding.com/" />
  
  <!-- Favicon (data:image/svg+xml) -->
  <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ctext x='50%25' y='50%25' dominant-baseline='middle' text-anchor='middle' font-size='80' fill='%237b82ff'%3E📈%3C/text%3E%3C/svg%3E">
  
  <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;500;600;700;800;900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    /* ======== ESTILOS BASE ======== */
    :root {
      --bg:        #000000;
      --surface:   #0a0a0c;
      --card:      #0e0e12;
      --border:    #434551;
      --border2:   #2a2b35;
      --accent:    #434551;
      --neon:      #7b82ff;
      --neon2:     #a78bfa;
      --neon3:     #38bdf8;
      --text:      #e8e9f0;
      --muted:     #a0a0b0;
      --glow:      rgba(123,130,255,0.18);
      --red:       #ff0000;
      --success:   #00e6b8;
      --warning:   #ffb347;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    .nav-links a.linktree-link {
      color: var(--neon2);
      text-shadow: 0 0 6px rgba(167,139,250,0.4);
    }
    .nav-links a.linktree-link:hover {
      color: var(--neon);
      text-shadow: 0 0 10px var(--neon);
    }

    html { scroll-behavior: smooth; }

    body {
      background: radial-gradient(circle at 20% 30%, rgba(123,130,255,0.08) 0%, #000000 90%);
      overflow-x: hidden;
    }
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image: 
        repeating-linear-gradient(45deg, 
          rgba(123,130,255,0.03) 0px, 
          rgba(123,130,255,0.03) 2px,
          transparent 2px,
          transparent 8px),
        repeating-linear-gradient(-45deg, 
          rgba(123,130,255,0.02) 0px, 
          rgba(123,130,255,0.02) 1px,
          transparent 1px,
          transparent 6px);
      pointer-events: none;
      z-index: 0;
      animation: drift 20s linear infinite;
    }
    @keyframes drift {
      0% { background-position: 0 0; }
      100% { background-position: 40px 40px; }
    }
    body::after {
      content: '';
      position: fixed;
      inset: 0;
      background: radial-gradient(ellipse at 40% 50%, rgba(123,130,255,0.1) 0%, transparent 60%);
      pointer-events: none;
      z-index: 0;
      animation: pulseGlow 8s ease-in-out infinite;
    }
    @keyframes pulseGlow {
      0%, 100% { opacity: 0.4; transform: scale(1); }
      50% { opacity: 0.8; transform: scale(1.05); }
    }
    @media (prefers-reduced-motion: reduce) {
      .grid-overlay, body::before, body::after {
        animation: none;
        background: none;
      }
    }
    .grid-overlay {
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(123,130,255,0.12) 1px, transparent 1px),
        linear-gradient(90deg, rgba(123,130,255,0.12) 1px, transparent 1px);
      background-size: 50px 50px;
      pointer-events: none;
      z-index: 0;
    }
    .hero, .stats-bar, section, footer {
      position: relative;
      z-index: 2;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Plus Jakarta Sans', sans-serif;
      min-height: 100vh;
    }

    body.modal-open {
      overflow: hidden;
    }

    /* Cursor parpadeante unificado */
    .typed-cursor {
      display: inline-block;
      width: 2px;
      margin-left: 2px;
      background-color: var(--neon);
      animation: blink 0.7s step-end infinite;
    }
    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }

    /* ----- NAVBAR MEJORADA (responsive + accesibilidad) ----- */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1rem 2rem;
      background: rgba(0,0,0,0.85);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border2);
    }
    .nav-logo {
      font-family: 'Nunito', sans-serif;
      font-weight: 900;
      font-size: 1.15rem;
      letter-spacing: 0.02em;
      color: var(--text);
      text-decoration: none;
      z-index: 101;
    }
    .nav-logo span {
      color: var(--neon);
      text-shadow: 0 0 12px var(--neon);
    }
    /* Botón hamburguesa (solo visible en móvil) */
    .hamburger {
      display: none;
      background: transparent;
      border: none;
      cursor: pointer;
      width: 30px;
      height: 24px;
      position: relative;
      z-index: 102;
      flex-direction: column;
      justify-content: space-between;
    }
    .hamburger span {
      display: block;
      width: 100%;
      height: 2px;
      background-color: var(--text);
      transition: transform 0.2s ease, opacity 0.2s ease;
      border-radius: 2px;
    }
    .hamburger[aria-expanded="true"] span:nth-child(1) {
      transform: translateY(11px) rotate(45deg);
    }
    .hamburger[aria-expanded="true"] span:nth-child(2) {
      opacity: 0;
    }
    .hamburger[aria-expanded="true"] span:nth-child(3) {
      transform: translateY(-11px) rotate(-45deg);
    }
    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
      transition: transform 0.3s ease, opacity 0.3s ease;
    }
    .nav-links a {
      font-family: 'DM Mono', monospace;
      font-size: 0.78rem;
      color: var(--muted);
      text-decoration: none;
      letter-spacing: 0.02em;
      text-transform: uppercase;
      transition: color 0.2s;
    }
    .nav-links a:hover, 
    .nav-links a:focus-visible {
      color: var(--neon);
      outline: 2px solid var(--neon);
      outline-offset: 4px;
      border-radius: 4px;
    }
    button:focus-visible, a:focus-visible, .cat-btn:focus-visible, .btn-view:focus-visible {
      outline: 2px solid var(--neon);
      outline-offset: 2px;
      border-radius: 8px;
    }
    @media (max-width: 768px) {
      nav {
        padding: 0.8rem 1.25rem;
      }
      .hamburger {
        display: flex;
      }
      .nav-links {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        background: rgba(0,0,0,0.95);
        backdrop-filter: blur(20px);
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 2rem;
        padding: 5rem 2rem 3rem;
        transform: translateY(-100%);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.3s ease, opacity 0.3s ease;
        z-index: 99;
        border-bottom: 1px solid var(--border2);
      }
      .nav-links.open {
        transform: translateY(0);
        opacity: 1;
        pointer-events: all;
      }
      .nav-links li a {
        font-size: 1rem;
        padding: 0.5rem;
      }
      .indicators-grid {
        grid-template-columns: 1fr;
      }
      .stats-bar {
        gap: 0.8rem;
        flex-wrap: wrap;
      }
      .stat {
        min-width: 130px;
        padding: 1rem;
      }
      .modal-title {
        font-size: 1.3rem;
      }
      .guarantee-badge span {
        white-space: normal;
      }
    }

    .stats-bar {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1.5rem;
      border-top: 1px solid var(--border2);
      border-bottom: 1px solid var(--border2);
      background: rgba(14,14,18,0.8);
      backdrop-filter: blur(8px);
      padding: 0 1rem;
    }
    .stat {
      flex: 0 0 auto;
      min-width: 160px;
      padding: 1.5rem 1.5rem;
      text-align: center;
    }
    .stat-val {
      font-family: 'Nunito', sans-serif;
      font-size: 1.6rem;
      font-weight: 900;
      color: var(--neon);
      text-shadow: 0 0 12px rgba(123,130,255,0.4);
      display: block;
    }
    .stat-label {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      letter-spacing: 0.03em;
      color: var(--muted);
      text-transform: uppercase;
      margin-top: 0.25rem;
      display: block;
    }

    section {
      position: relative;
      z-index: 1;
      padding: 5rem 2rem;
      max-width: 1280px;
      margin: 0 auto;
    }
    .section-header {
      text-align: center;
      margin-bottom: 3.5rem;
    }
    .section-tag {
      font-family: 'DM Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 0.06em;
      color: var(--neon);
      text-transform: uppercase;
      margin-bottom: 0.75rem;
      display: block;
    }
    .section-title {
      font-family: 'Nunito', sans-serif;
      font-size: clamp(1.6rem, 3.5vw, 2.6rem);
      font-weight: 700;
      letter-spacing: -0.01em;
    }
    .section-title .hl { color: var(--neon); }

    .category-tabs {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 0.6rem;
      margin-bottom: 2.8rem;
      border-bottom: 1px solid var(--border2);
      padding-bottom: 1rem;
    }
    .cat-btn {
      background: transparent;
      border: 1px solid var(--border2);
      font-family: 'DM Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      padding: 0.5rem 1rem;
      border-radius: 60px;
      color: var(--muted);
      cursor: pointer;
      transition: all 0.2s ease;
      backdrop-filter: blur(4px);
    }
    .cat-btn:hover,
    .cat-btn:focus-visible {
      border-color: var(--neon);
      color: var(--neon);
      transform: translateY(-2px);
    }
    .cat-btn.active {
      background: rgba(123,130,255,0.12);
      border-color: var(--neon);
      color: var(--neon);
      text-shadow: 0 0 6px rgba(123,130,255,0.3);
      box-shadow: 0 0 8px rgba(123,130,255,0.2);
    }

    .indicators-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 1.5rem;
    }

    .card {
      background: var(--card);
      border: 1px solid var(--border2);
      border-radius: 14px;
      padding: 1.75rem;
      display: flex;
      flex-direction: column;
      gap: 1rem;
      position: relative;
      overflow: hidden;
      transition: border-color 0.3s, transform 0.3s, box-shadow 0.3s;
      animation: fadeUp 0.5s both;
    }
    .card::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--neon), transparent);
      opacity: 0;
      transition: opacity 0.3s;
    }
    .card:hover {
      border-color: rgba(123,130,255,0.4);
      transform: translateY(-4px);
      box-shadow: 0 8px 40px rgba(123,130,255,0.1);
    }
    .card:hover::before { opacity: 1; }
    .card-top {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
      gap: 1rem;
    }
    .card-num {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      color: var(--neon);
      letter-spacing: 0.03em;
      opacity: 0.7;
    }
    .card-badge {
      font-family: 'DM Mono', monospace;
      font-size: 0.6rem;
      letter-spacing: 0.02em;
      text-transform: uppercase;
      padding: 0.2rem 0.6rem;
      border-radius: 6px;
      border: 1px solid var(--border);
      color: var(--muted);
    }
    .card-badge.pro {
      border-color: rgba(123,130,255,0.4);
      color: var(--neon);
      background: rgba(123,130,255,0.08);
    }
    .card-badge.premium {
      border-color: rgba(167,139,250,0.4);
      color: var(--neon2);
      background: rgba(167,139,250,0.08);
    }
    .card-title {
      font-family: 'Nunito', sans-serif;
      font-size: 1rem;
      font-weight: 700;
      line-height: 1.3;
      letter-spacing: 0.02em;
    }
    .card-desc {
      font-size: 0.82rem;
      color: var(--muted);
      line-height: 1.65;
      flex: 1;
    }
    .card-meta {
      display: flex;
      gap: 1rem;
      flex-wrap: wrap;
    }
    .meta-pill {
      font-family: 'DM Mono', monospace;
      font-size: 0.62rem;
      letter-spacing: 0.02em;
      color: var(--muted);
      background: rgba(67,69,81,0.15);
      border: 1px solid var(--border2);
      border-radius: 50px;
      padding: 0.2rem 0.7rem;
    }
    .card-actions {
      display: flex;
      gap: 0.75rem;
      margin-top: 0.25rem;
    }
    .btn-view {
      flex: 1;
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.65rem 1rem;
      border-radius: 12px;
      border: 1px solid var(--border);
      background: transparent;
      color: var(--text);
      cursor: pointer;
      text-decoration: none;
      text-align: center;
      transition: border-color 0.2s, color 0.2s, background 0.2s;
    }
    .btn-view:hover,
    .btn-view:focus-visible {
      border-color: var(--neon3);
      color: var(--neon3);
      background: rgba(56,189,248,0.06);
    }

    /* Modal (con mejoras de foco) */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.85);
      backdrop-filter: blur(12px);
      z-index: 200;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1.5rem;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.25s ease;
    }
    .modal-overlay.open {
      opacity: 1;
      pointer-events: all;
    }
    .modal {
      background: linear-gradient(145deg, #0e0e12 0%, #09090c 100%);
      border: 1px solid rgba(123,130,255,0.3);
      border-radius: 28px;
      width: 100%;
      max-width: 620px;
      max-height: 85vh;
      display: flex;
      flex-direction: column;
      overflow: hidden;
      padding: 1.5rem;
      position: relative;
      transform: translateY(25px) scale(0.98);
      transition: transform 0.35s cubic-bezier(0.2, 0.9, 0.4, 1.1);
      box-shadow: 0 25px 45px rgba(0,0,0,0.5), 0 0 0 1px rgba(123,130,255,0.1);
    }
    .modal-overlay.open .modal { transform: translateY(0) scale(1); }

    .modal-scroll-area {
      flex: 1;
      overflow-y: auto;
      padding-right: 0.5rem;
      margin: 0.5rem 0;
    }
    .modal-scroll-area::-webkit-scrollbar {
      width: 4px;
    }
    .modal-scroll-area::-webkit-scrollbar-track {
      background: rgba(255,255,255,0.05);
      border-radius: 10px;
    }
    .modal-scroll-area::-webkit-scrollbar-thumb {
      background: var(--neon);
      border-radius: 10px;
    }

    .modal-close {
      position: absolute;
      top: 1rem; right: 1rem;
      background: rgba(255,255,255,0.03);
      border: 1px solid var(--border2);
      color: var(--muted);
      font-size: 1rem;
      width: 2rem; height: 2rem;
      border-radius: 40px;
      cursor: pointer;
      display: flex; align-items: center; justify-content: center;
      transition: all 0.2s;
      z-index: 5;
    }
    .modal-close:hover,
    .modal-close:focus-visible {
      border-color: var(--neon);
      color: var(--neon);
      background: rgba(123,130,255,0.1);
      outline: 2px solid var(--neon);
      outline-offset: 2px;
    }
    .modal-num {
      font-family: 'DM Mono', monospace;
      font-size: 0.7rem;
      color: var(--neon);
      letter-spacing: 0.04em;
      margin-bottom: 0.5rem;
    }
    .modal-title {
      font-family: 'Nunito', sans-serif;
      font-size: 1.6rem;
      font-weight: 800;
      margin-bottom: 1rem;
      line-height: 1.2;
      background: linear-gradient(135deg, #fff, var(--neon2));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      padding-right: 1.5rem;
    }
    .modal-body {
      font-size: 0.9rem;
      color: var(--text);
      line-height: 1.6;
      margin-bottom: 1rem;
      background: rgba(123,130,255,0.05);
      padding: 0.8rem 1rem;
      border-radius: 16px;
      border-left: 2px solid var(--neon);
    }
    .modal-features {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
      margin-bottom: 0.5rem;
    }
    .modal-features li {
      font-family: 'DM Mono', monospace;
      font-size: 0.75rem;
      color: var(--muted);
      padding: 0.5rem 0.75rem;
      background: rgba(67,69,81,0.15);
      border-radius: 12px;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }
    .modal-features li::before {
      content: "▹";
      color: var(--neon);
      font-size: 0.8rem;
    }
    .purchase-section {
      background: rgba(0,0,0,0.4);
      border-radius: 20px;
      padding: 1rem;
      margin: 0.5rem 0 0.5rem;
      border: 1px solid rgba(123,130,255,0.2);
      flex-shrink: 0;
    }
    .price-tag {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      margin-bottom: 1rem;
      flex-wrap: wrap;
    }
    .price-value {
      font-family: 'Nunito', sans-serif;
      font-size: 1.8rem;
      font-weight: 900;
      color: var(--success);
      letter-spacing: -0.02em;
    }
    .price-old {
      font-size: 1rem;
      color: var(--muted);
      text-decoration: line-through;
      margin-left: 0.5rem;
    }
    .badge-offer {
      background: linear-gradient(135deg, #ff4d4d, #ff1a1a);
      padding: 0.2rem 0.7rem;
      border-radius: 40px;
      font-size: 0.65rem;
      font-weight: bold;
      color: white;
      font-family: 'DM Mono', monospace;
    }
    .payment-methods {
      display: flex;
      flex-direction: column;
      gap: 0.7rem;
      margin-bottom: 1rem;
    }
    .payment-btn {
      display: flex;
      align-items: center;
      justify-content: space-between;
      background: rgba(20,20,28,0.8);
      border: 1px solid var(--border2);
      border-radius: 60px;
      padding: 0.7rem 1.2rem;
      text-decoration: none;
      transition: transform 0.2s, border-color 0.2s, background 0.2s;
      cursor: pointer;
    }
    .payment-btn:hover,
    .payment-btn:focus-visible {
      transform: scale(1.02);
      border-color: var(--neon);
      background: rgba(123,130,255,0.1);
      box-shadow: 0 4px 14px rgba(123,130,255,0.2);
      outline: none;
    }
    .payment-info {
      display: flex;
      align-items: center;
      gap: 0.8rem;
    }
    .payment-icon {
      font-size: 1.4rem;
      font-weight: bold;
    }
    .payment-name {
      font-family: 'DM Mono', monospace;
      font-size: 0.8rem;
      font-weight: 600;
      color: var(--text);
    }
    .payment-price {
      font-family: 'Nunito', sans-serif;
      font-weight: 800;
      color: var(--neon3);
      font-size: 0.9rem;
    }
    .payment-discount {
      background: rgba(0,230,184,0.2);
      padding: 0.2rem 0.5rem;
      border-radius: 30px;
      font-size: 0.65rem;
      color: var(--success);
    }
    .guarantee-badge {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      gap: 0.8rem;
      padding-top: 0.8rem;
      border-top: 1px dashed var(--border2);
    }
    .guarantee-badge span {
      font-family: 'DM Mono', monospace;
      font-size: 0.68rem;
      color: var(--muted);
      background: rgba(123,130,255,0.05);
      padding: 0.25rem 0.75rem;
      border-radius: 50px;
      white-space: nowrap;
    }
    .modal-actions {
      display: flex;
      gap: 0.75rem;
      flex-shrink: 0;
      margin-top: 0.5rem;
    }
    .btn-image, .btn-youtube, .btn-share {
      flex: 1;
      font-family: 'DM Mono', monospace;
      font-size: 0.7rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.7rem;
      border-radius: 40px;
      text-align: center;
      transition: all 0.2s;
      text-decoration: none;
      font-weight: 600;
      cursor: pointer;
    }
    .btn-image {
      background: rgba(167,139,250,0.15);
      border: 1px solid var(--neon2);
      color: var(--neon2);
    }
    .btn-image:hover,
    .btn-image:focus-visible {
      background: var(--neon2);
      color: #000;
      transform: translateY(-2px);
    }
    .btn-youtube {
      background: rgba(255,0,0,0.15);
      border: 1px solid var(--red);
      color: #ff6666;
    }
    .btn-youtube:hover,
    .btn-youtube:focus-visible {
      background: var(--red);
      color: white;
      transform: translateY(-2px);
    }
    .btn-share {
      background: rgba(56,189,248,0.15);
      border: 1px solid var(--neon3);
      color: var(--neon3);
    }
    .btn-share:hover,
    .btn-share:focus-visible {
      background: var(--neon3);
      color: #000;
      transform: translateY(-2px);
    }
    .toast-message {
      position: fixed;
      bottom: 20px;
      left: 50%;
      transform: translateX(-50%);
      background: rgba(0,0,0,0.9);
      color: var(--success);
      padding: 0.75rem 1.5rem;
      border-radius: 40px;
      font-family: 'DM Mono', monospace;
      font-size: 0.75rem;
      border: 1px solid var(--success);
      z-index: 300;
      pointer-events: none;
      opacity: 0;
      transition: opacity 0.2s;
    }
    footer {
      position: relative;
      z-index: 1;
      border-top: 1px solid var(--border2);
      padding: 2rem 3rem;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1rem;
    }
    .footer-brand {
      font-family: 'Nunito', sans-serif;
      font-weight: 900;
      font-size: 0.9rem;
      letter-spacing: 0.02em;
      color: var(--muted);
      text-align: center;
    }
    .footer-brand span { color: var(--neon); }
    .footer-copy {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      color: var(--muted);
      letter-spacing: 0.02em;
    }
    .legal-disclaimer {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      color: var(--muted);
      text-align: center;
      max-width: 800px;
      margin: 0.5rem auto 0;
      line-height: 1.4;
      border-top: 1px dashed var(--border2);
      padding-top: 1rem;
    }
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(18px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .social-icons {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin-top: 1rem;
      flex-wrap: wrap;
      align-items: center;
    }
    .social-img {
      width: 48px;
      height: 48px;
      object-fit: contain;
      transition: transform 0.2s, filter 0.2s;
      filter: brightness(0.8);
    }
    .social-img:hover,
    .social-img:focus-visible {
      transform: translateY(-3px);
      filter: brightness(1) drop-shadow(0 0 6px var(--neon));
    }
    @media (max-width: 768px) {
      .social-img { width: 32px; height: 32px; }
      .guarantee-badge span { white-space: normal; }
      .modal { max-width: 95%; padding: 1rem; }
      .modal-title { font-size: 1.3rem; }
    }
    .btn-primary {
      font-family: 'Nunito', sans-serif;
      font-size: 0.72rem;
      font-weight: 700;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.85rem 2rem;
      border-radius: 12px;
      border: none;
      background: var(--neon);
      color: #000;
      cursor: pointer;
      text-decoration: none;
      transition: box-shadow 0.25s, transform 0.2s;
      display: inline-block;
    }
    .btn-primary:hover {
      box-shadow: 0 0 24px rgba(123,130,255,0.6), 0 0 60px rgba(123,130,255,0.2);
      transform: translateY(-2px);
    }
    .hero {
      position: relative;
      z-index: 1;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 6rem 2rem 4rem;
      overflow: hidden;
    }
    .hero-glow {
      position: absolute;
      width: 600px;
      height: 600px;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(123,130,255,0.12) 0%, transparent 70%);
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      pointer-events: none;
    }
    .hero-tag {
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.06em;
      color: var(--neon);
      text-transform: uppercase;
      margin-bottom: 1.5rem;
      text-shadow: 0 0 6px var(--neon), 0 0 12px rgba(123,130,255,0.5);
      min-height: 2rem;
    }
    .hero h1 {
      font-family: 'Nunito', sans-serif;
      font-size: clamp(2.8rem, 7vw, 5.5rem);
      font-weight: 900;
      line-height: 1.05;
      letter-spacing: -0.02em;
      margin-bottom: 1rem;
    }
    .hero h1 .hl {
      color: var(--neon);
      text-shadow: 0 0 30px rgba(123,130,255,0.5), 0 0 60px rgba(123,130,255,0.2);
    }
    .hero-sub {
      font-size: 1rem;
      color: var(--muted);
      max-width: 480px;
      line-height: 1.5;
      margin-bottom: 0;
    }
    .hero-cta {
      display: flex;
      gap: 1rem;
      margin-top: 0.5rem;
      flex-wrap: wrap;
      justify-content: center;
    }
  </style>
</head>
<body>
<div class="grid-overlay"></div>

<nav>
  <a href="#" class="nav-logo">Patricio<span>Coding</span></a>
  <button class="hamburger" id="hamburgerBtn" aria-label="Menú principal" aria-expanded="false">
    <span></span><span></span><span></span>
  </button>
  <ul class="nav-links" id="navLinks">
    <li><a href="#indicators">Indicators</a></li>
    <li><a href="https://linktr.ee/patriciocoding" target="_blank" rel="noopener noreferrer" class="linktree-link">LINKTREE</a></li>
  </ul>
</nav>

<div class="hero">
  <div class="hero-glow"></div>
  <p class="hero-tag" id="typedTag"></p>
  <h1 id="typedTitle"></h1>
  <p class="hero-sub">High-performance trading indicators designed to trade accurately in any market.</p>
  <div class="social-icons">
    <a href="https://t.me/algoritmoatros" target="_blank" rel="noopener noreferrer"><img src="Telegram.png" alt="Canal de Telegram de PatricioCoding" class="social-img"></a>
    <a href="https://www.youtube.com/@PatricioCoding" target="_blank" rel="noopener noreferrer"><img src="YouTube.png" alt="Canal de YouTube de PatricioCoding" class="social-img"></a>
    <a href="https://www.instagram.com/bypatriciocoding/" target="_blank" rel="noopener noreferrer"><img src="Instagram.png" alt="Perfil de Instagram de PatricioCoding" class="social-img"></a>
  </div>
  <div class="hero-cta"><a href="#indicators" class="btn-primary">Show Indicators</a></div>
</div>

<div class="stats-bar">
  <div class="stat"><span class="stat-val">+20</span><span class="stat-label">Open Source Projects</span></div>
  <div class="stat"><span class="stat-val">TradingView</span><span class="stat-label">Solutions Projects</span></div>
  <div class="stat"><span class="stat-val">Pine Script</span><span class="stat-label">Language</span></div>
  <div class="stat"><span class="stat-val">24/7</span><span class="stat-label">Support</span></div>
</div>

<section id="indicators">
  <div class="section-header">
    <span class="section-tag">// PatricioCoding Projects</span>
    <h2 class="section-title">All <span class="hl">Indicators</span></h2>
  </div>
  <div class="category-tabs" id="categoryTabs"></div>
  <div class="indicators-grid" id="gridContainer"></div>
  <div class="legal-disclaimer" style="margin-top: 2.5rem; background: rgba(0,0,0,0.6); padding: 1rem; border-radius: 20px; border-left: 3px solid var(--warning);">
    <strong>⚠️ IMPORTANT NOTICE FOR US TRADERS:</strong> No financial advice – for educational purposes only. Hypothetical performance results have inherent limitations. Past performance does not guarantee future results. Trading financial instruments involves substantial risk of loss.<br>
    <span style="display: inline-block; margin-top: 0.5rem;">📜 <strong>CFTC Rule 4.41:</strong> Hypothetical or simulated performance results have certain inherent limitations. Unlike an actual performance record, simulated results do not represent actual trading. No representation is being made that any account will or is likely to achieve profits or losses similar to those shown.</span>
  </div>
</section>

<footer>
  <div class="footer-brand">Patricio<span>Coding</span></div>
  <div class="footer-copy">© 2023 PatricioCoding — Fractality In Code</div>
  <div class="legal-disclaimer">
    <strong>Risk Disclaimer:</strong> Trading financial instruments involves substantial risk of loss and is not suitable for every investor. Past performance does not guarantee future results. The indicators provided are educational tools – you assume full responsibility for your trading decisions. No representation is being made that any account will or is likely to achieve profits or losses similar to those discussed. US traders: CFTC Rule 4.41 - Hypothetical performance results have inherent limitations.
  </div>
</footer>

<div class="modal-overlay" id="modalOverlay">
  <div class="modal">
    <button class="modal-close" id="modalClose" aria-label="Cerrar modal">✕</button>
    <div class="modal-num" id="modalNum"></div>
    <div class="modal-title" id="modalTitle"></div>
    <div class="modal-scroll-area">
      <div style="margin: 0 0 1rem 0; font-size: 0.7rem; background: rgba(255,180,71,0.1); padding: 0.6rem; border-radius: 12px; color: var(--warning); text-align: center;">
        ⚠️ <strong>No financial advice</strong> – for educational purposes only. Hypothetical performance results have inherent limitations.
      </div>
      <div class="modal-body" id="modalBody"></div>
      <ul class="modal-features" id="modalFeatures"></ul>
    </div>
    <div class="purchase-section">
      <div class="price-tag" id="priceTag"></div>
      <div class="payment-methods" id="paymentMethodsContainer"></div>
      <div class="guarantee-badge">
        <span>🔒 Pay 100% Safe</span>
        <span>⚡ Instant Delivery (Hotmart & Gumroad)</span>
        <span>🛡️ Permanent Indicator</span>
      </div>
    </div>
    <div class="modal-actions">
      <a id="modalImageBtn" href="#" target="_blank" rel="noopener noreferrer" class="btn-image">Preview</a>
      <a id="modalYoutubeBtn" href="#" target="_blank" rel="noopener noreferrer" class="btn-youtube">▶ YouTube</a>
      <button id="modalShareBtn" class="btn-share">Copy link</button>
    </div>
  </div>
</div>
<div id="toastMessage" class="toast-message">✅ Link copied to clipboard</div>

<script>
  // ========== INDICADORES (COMPLETO) ==========
  const INDICATOR_CATEGORIES = [
    "Harmonic Patterns", "Gann Theory & Cycles", "Elliott Wave Analysis",
    "Market Structure & Breakout", "Algorithmic Trend Following", "Premium Plugins & Ecosystems", "Trading Utilities"
  ];
  
  let indicators = [
    { name: "Harmonic Pattern Scanner", desc: "Advanced TradingView indicator that detects 9 harmonic patterns (Gartley, Bat, Butterfly, Crab, ABCD, etc.) using three configurable ZigZag lengths (L1, L2, L3). It draws pattern structures, PRZ zones, Take Profit and Stop Loss levels, and generates alerts when a pattern is completed, with the option to anticipate from point C.", tags: ["Harmonic Patterns","ZigZag", "Technical Analysis", "TradingView", "Pattern Recognition"], badge: "pro", features: ["Detects harmonic patterns across three simultaneous ZigZag lengths for multi-timeframe analysis.", "Supports 9 patterns: ABCD, Alt_Bat, Gartley, Bat, Butterfly, Crab, DeepCrab, Shark, and 5-0.", "Displays PRZ lines, TP/SL levels, configurable alerts, and optional early visualization from point C."], youtubeUrl: "https://www.youtube.com/watch?v=H2GWsED2ILU", imageUrl: "HarmonicPattern.mp4", category: "Harmonic Patterns", price: 75, oldPrice: 80, buyLinks: { hotmart: "https://pay.hotmart.com/I105124090X", upwork: "https://www.upwork.com/services/product/development-it-the-harmonic-pattern-tradingview-indicator-1766183352521576448?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/HarmonicPattern", telegram: "https://t.me/algoritmoatros" } },
    { name: "Harmonic Reversal Scanner", desc: "Advanced TradingView indicator that detects 7 classic reversal patterns (Double Top, Double Bottom, Descending Triangle, Ascending Triangle, Symmetrical Triangle, Head and Shoulders, Inverse Head and Shoulders) using three configurable ZigZag lengths (L1, L2, L3). It draws pattern structures, projects breakout levels, and displays entry, stop loss, and take profit levels based on Fibonacci-like ratios.", tags: ["ReversalPatterns", "ZigZag ", "TechnicalAnalysis", "TradingView ", "ChartPatterns"], badge: "pro", features: ["Identifies key reversal patterns across three simultaneous ZigZag lengths for multi-timeframe confirmation.", "Supports 7 patterns: Double Top, Double Bottom, Descending Triangle, Ascending Triangle, Symmetrical Triangle, Head and Shoulders, and Inverse Head and Shoulders.", "Real-time alerts when wave patterns completeProjects breakout targets (Entry, TP1–TP3, Stop Loss) with customizable ratios and visual fills for pattern zones."], youtubeUrl: "https://www.youtube.com/watch?v=LFIjWjEcGTM", imageUrl: "HarmonicReversal.mp4", category: "Harmonic Patterns", price: 75, oldPrice: 80, buyLinks: { hotmart: "https://pay.hotmart.com/Y105124429E", upwork: "https://www.upwork.com/services/product/development-it-the-harmonic-reversal-tradingview-indicator-1766292603268657152?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/HarmonicReversal", telegram: "https://t.me/algoritmoatros" } },
    { name: "Reversal Bar Color & Pivots", desc: "Complete TradingView indicator pack combining Candle Color Oscillator and Zones & Pivots. The first colors candles in real time based on 5 oscillators (Stochastic, RSI, LBR, CCI, DTI) with custom bullish/neutral/bearish colors and alerts. The second draws dynamic pivot levels (Daily/Weekly/Monthly) with 6 calculation methods (Jackson, Traditional, Woodie, Classic, Camarilla, Custom), plus yesterday’s high/low/close, directional zones, and cloud fills for support/resistance.", tags: ["CandleColors", "PivotLevels ", "TechnicalAnalysis", "TradingView ", "SupportResistance"], badge: "pro", features: ["Color-code any candle based on Stochastic, RSI, LBR, CCI, or DTI – instantly see bullish/neutral/bearish momentum.", "Automatically plot daily, weekly, monthly pivots with 6 pivot types (Jackson, Traditional, Woodie, Classic, Camarilla, Custom) and customizable TP/SL zones.", "Includes yesterday’s high/low/close, midpoint lines, and cloud fills for clean visual support/resistance levels on any timeframe."], youtubeUrl: "https://www.youtube.com/watch?v=CHmnGMYpMSk", imageUrl: "ReversalBarandPivots.mp4", category: "Market Structure & Breakout", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/D105124506N", upwork: "https://www.upwork.com/services/product/development-it-the-reversal-bar-color-with-pivots-tradingview-indicator-1766294926204944384?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/PivotsAndReversalBar", telegram: "https://t.me/algoritmoatros" } },
    { name: "Darvas Box Break With Targets", desc: "Advanced TradingView indicator that automatically draws Darvas Boxes (based on highest highs and lowest lows over a configurable length) and generates breakout signals (Buy when price closes above the box top, Sell below the box bottom). It plots entry levels, stop loss, and up to three customizable take‑profit targets. Additionally, it includes a risk management table (portfolio size, risk %, position size, R/R) and a multi‑timeframe technical rating panel (MAs, oscillators, overall) for up to six user‑defined timeframes.", tags: ["DarvasBox", "BreakoutStrategy", "RiskManagement", "MultiTimeframeAnalysis", "TradingView"], badge: "pro", features: ["Automatically detects Darvas boxes and draws breakout signals (Buy/Sell) with customizable colors and box styles.", "Plots entry, stop loss, and three take‑profit levels (with editable ratios) and includes a live risk management table.", "Displays a multi‑timeframe panel with “All”, “MAs”, “Oscillators” ratings for up to 6 timeframes, plus a full backtesting version with SL/TP orders."], youtubeUrl: "https://www.youtube.com/watch?v=3vEbJ9nND0w", imageUrl: "DarvasBreak.mp4", category: "Market Structure & Breakout", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/A105124600Q", upwork: "https://www.upwork.com/services/product/development-it-the-darvas-box-break-with-targets-tradingview-indicator-1766299313085124608?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/DarvasBoxBreakWithTargets", telegram: "https://t.me/algoritmoatros" } },
    { name: "Trendline Break With Targets", desc: "Advanced TradingView indicator that automatically draws dynamic trendlines (support/resistance) based on pivot highs/lows using a configurable period. It detects breakouts above resistance or below support and generates Buy/Sell signals. Once a signal is triggered, it plots entry level, stop loss, and up to three take-profit targets (adjustable by ATR‑based bands) with full visual management.", tags: ["TrendlineBreak", "SupportResistance", "BreakoutStrategy", "ATRTargets", "TradingView"], badge: "pro", features: ["Automatically plots dynamic support/resistance trendlines from pivot highs/lows with customizable period and visual style.", "Generates Buy/Sell signals on trendline breaks and draws entry, stop loss, and up to three take‑profit levels (primary or secondary targets).", "Uses ATR‑based volatility bands to set target distances, and includes line/label extension and displacement options for clean chart management."], youtubeUrl: "https://www.youtube.com/watch?v=crGqtUgjlzQ", imageUrl: "TrendLineBreak.mp4", category: "Market Structure & Breakout", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/K105124732X", upwork: "https://www.upwork.com/services/product/development-it-the-trendline-break-with-targets-tradingview-indicator-1766303145311981568?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/TrendLineBreakWithTargets", telegram: "https://t.me/algoritmoatros" } },
    { name: "Elliott Wave", desc: "Manual Elliott Wave tool that lets you plot wave counts (0–5) by selecting pivot times directly on the chart. It draws the wave structure with customizable lines, projects three take‑profit levels for Waves 2, 3, 4, and 5 based on Fibonacci ratios, and includes optional vertical tracking lines and labels to mark each wave’s time position.", tags: ["ElliottWave", "WaveCounting", "FibonacciTargets", "ManualPivots", "TradingView"], badge: "pro", features: ["Manually define wave pivot times (0 to 4/5) via chart timestamps to build an Elliott Wave structure.", "Automatically calculates and displays three target levels for each wave using user‑defined Fibonacci ratios (e.g., 0.382, 0.618, 1.618).", "Visual tools include wave connection lines, target lines with labels, and optional vertical trackers (lines or bubbles) to monitor wave timing."], youtubeUrl: "https://www.youtube.com/watch?v=hA-idEIevLo", imageUrl: "ElliottWaveSimple.mp4", category: "Elliott Wave Analysis", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/Y105124794S", upwork: "https://www.upwork.com/services/product/development-it-the-elliott-wave-tradingview-indicator-1766306537006206976?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/ElliottWave", telegram: "https://t.me/algoritmoatros" } },
    { name: "Position Size Risk Reward", desc: "Multi‑asset risk/reward calculator for Futures, Crypto, and Stocks. Define a pivot time (or manual price levels) for entry, stop loss, and take profit (by multiplier or fixed price). The indicator automatically computes position size based on account size, risk percentage, leverage (Crypto), point value (Futures), and shares (Stocks).", tags: ["RiskReward", "PositionSizing", "MoneyManagement", "FuturesTrading", "CryptoRisk"], badge: "pro", features: ["Supports three asset classes: Futures (with contracts & point value), Crypto (with leverage), and Stocks (shares).", "Calculates position size, USD risk, profit target, and R/R ratio based on account risk % and user‑defined stop/target.", "Draws entry, stop loss, take profit, and 100% risk lines with configurable extension and labels showing all key metrics."], youtubeUrl: "https://www.youtube.com/watch?v=tE-SZSc_I3A", imageUrl: "RiskReward.mp4", category: "Trading Utilities", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/D105124844V", upwork: "https://www.upwork.com/services/product/development-it-the-position-size-tradingview-indicator-1766310474399174656?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/PositionSize", telegram: "https://t.me/algoritmoatros" } },
    { name: "Elliott Wave Setup Pullback", desc: "Pullback indicator that identifies retracement setups (Wave 2 retracing Wave 1) using two independent ZigZag periods (Intermediate and Major). When a pullback falls within a user‑defined retracement zone (e.g., 38.2%–78.6%), it draws target boxes and extension lines for multiple profit levels (T1, T2, T3) based on Fibonacci-like multipliers.", tags: ["PullbackSetup", "Retracement", "ZigZag", "FibonacciExtensions", "SwingTrading"], badge: "pro", features: ["Detects pullbacks (Wave 2) from Wave 1 using two customizable zigzag lengths (Intermediate and Major).", "Draws target zones (boxes) and horizontal lines for T1, T2, T3 based on user‑defined multipliers (e.g., 1.0×, 1.382×, 1.618×).", "Displays pullback percentage and Bull/Bear labels, with optional filtering to only show when Wave 3 exceeds Wave 1’s extreme."], youtubeUrl: "https://www.youtube.com/watch?v=CDb1RgKRMpg", imageUrl: "PullbackSetup.mp4", category: "Elliott Wave Analysis", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/B105124896E", upwork: "https://www.upwork.com/services/product/development-it-elliott-wave-setup-pullback-tradingview-indicator-1770255410262749184?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/ElliottWaveSetupPullback", telegram: "https://t.me/algoritmoatros" } },
    { name: "Algorithmic Renko", desc: "AlgoRenko is a complete trading system that combines Renko‑based trend detection (ATR brick size) with Stochastic candle coloring and a EMA cloud for support/resistance. It generates Buy/Sell signals when Renko bars reverse direction and close beyond a slow EMA filter. The system plots entry, stop loss (3× ATR), and three dynamic take‑profit levels (customizable percentages) with visual fills.", tags: ["AlgoRenko", "RenkoTrading", "BreakoutStrategy", "RiskManagement", "MultiTimeframeAnalysis"], badge: "pro", features: ["Generates Renko bars from ATR and triggers long/short signals on Renko reversals filtered by an EMA trend (MA2).", "Colors candles with Stochastic (overbought/oversold) and displays dynamic SL (3× ATR) and three TP levels (1%, 2%, 3% customizable).", "Includes a professional risk management table and an MTF panel with “All”, “MAs”, and “Oscillators” ratings for 6 timeframes, plus a backtesting engine with SL/TP orders."], youtubeUrl: "https://www.youtube.com/watch?v=_4qhYUg5syY", imageUrl: "AlgoRenko.mp4", category: "Algorithmic Trend Following", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/J105124959W", upwork: "https://www.upwork.com/services/product/development-it-algorithmic-renko-open-source-tradingview-indicator-1782780856922764750?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/AlgorithmicRenko", telegram: "https://t.me/algoritmoatros" } },
    { name: "Algorithmic SuperTrend", desc: "AlgoATR is an all‑in‑one trading system combining Stochastic candle coloring, a WaveTrend MA with dynamic colors, a Guppy T3 multiple moving average (20 lines with gradient fills), and a custom SuperTrend as the primary trend filter. It generates long/short signals when price crosses the SuperTrend and is confirmed by the WaveTrend MA.", tags: ["AlgoATR", "SuperTrend", "GuppyT3", "WaveTrend", "MultiTimeframeAnalysis"], badge: "pro", features: ["Combines Stochastic bars, WaveTrend MA, Guppy T3 cloud, and SuperTrend to generate high‑probability long/short signals.", "Automatically draws 3× ATR stop loss and three take‑profit levels (customizable percentages) with visual fills and labels.", "Includes professional risk management table, MTF rating panel, RSI reversal alerts, and FearZone candles for extreme market conditions, plus a backtesting engine."], youtubeUrl: "https://www.youtube.com/watch?v=JRnoBl6Tbas", imageUrl: "AlgoATR.mp4", category: "Algorithmic Trend Following", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/B105125003H", upwork: "https://www.upwork.com/services/product/development-it-algorithmic-supertrend-open-source-tradingview-indicator-1796907635136712320?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/AlgorithmicSuperTrend", telegram: "https://t.me/algoritmoatros" } },
    { name: "Gann Wave Advanced", desc: "Two manual Gann analysis tools for TradingView: Gann Extension Levels (3 points A, B, C) projects square‑root based extension targets (up to 9 levels, selectable series 1‑3 or 4‑6) for trending moves, with a background box showing 25%/50%/75% retracement zones. Gann Retracement Levels (2 points A, B) plots 12.5%, 25%, 37.5% retracement zones above/below the midpoint, plus a MOB (Make or Break) extension box.", tags: ["GannAnalysis", "SquareRootTheory", "ExtensionLevels", "RetracementZones", "TradingView"], badge: "pro", features: ["Define 2 or 3 pivot points on the chart to automatically generate Gann square root extension targets (Extensions) or precise 12.5%/25%/37.5% retracement levels (Retracements).", "Extension tool draws up to 9 horizontal target lines with color‑coded groups (1‑3, 4‑6); Retracement tool draws 6 zones with gradients and fills for quick visual reference.", "Both include MOB (Make or Break) boxes, time tracking lines/labels (optional), and full customization of direction, line style, and extension length."], youtubeUrl: "https://www.youtube.com/watch?v=DMGJWZXFXgs", imageUrl: "GannWaveAdvanced.mp4", category: "Gann Theory & Cycles", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/C105125047E", upwork: "https://www.upwork.com/services/product/development-it-gann-wave-advanced-open-source-tradingview-indicator-1826233746395002045?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/GannWaveAdvanced", telegram: "https://t.me/algoritmoatros" } },
    { name: "Gann Price Time Angles Advanced", desc: "Advanced manual Gann tool that draws price‑time angles (0°, 90°, 180°, 270°, 360° + secondary 45°, 135°, 215°, 315°) based on two user‑selected pivot points (A, B). It projects horizontal harmonic levels (price retracements at 1/8 increments), vertical time cycles (every 45° of time), diagonal price channels (converging lines), a full Gann Fan, and a Gann Star pattern.", tags: ["GannAnalysis", "PriceTimeAngles", "GannFan", "GeometricTrading", "TradingView"], badge: "pro", features: ["Draws main and secondary Gann angles (0°–360° and 45°–315°) from a start pivot, extending to the right edge of the chart.", "Plots vertical time cycles (every 45° of time), horizontal retracement levels (1/8, 1/4, 3/8, etc.), and diagonal price channels that connect harmonic time/price points.", "Includes optional Gann Fan (from the high or low) and Gann Star pattern, with customizable colors, line styles, and tracking labels for clear visual analysis."], youtubeUrl: "https://www.youtube.com/watch?v=Di20aX37d14", imageUrl: "GannAnglesAdvanced.mp4", category: "Gann Theory & Cycles", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/V105125123U", upwork: "https://www.upwork.com/services/product/development-it-gann-price-time-angles-advanced-open-source-tradingview-indicator-1837111228046446569?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/GannPriceTimeAnglesAdvanced", telegram: "https://t.me/algoritmoatros" } },
    { name: "Market Structure Break With Targets", desc: "Advanced TradingView indicator that combines polynomial regression trend channels (with curved bands at 38.2%, 50%, 61.8%, 78.6% levels), EMA‑ATR candle coloring (trend/transition zones), and market structure break detection (BOS/CHoCH). It identifies HH/HL/LL/LH swing points, plots breakout lines with labels, and generates Buy/Sell signals on confirmed breaks.", tags: ["MarketStructure", "PolynomialRegression", "BOS", "CHoCH", "MultiTimeframeAnalysi"], badge: "pro", features: ["Plots polynomial regression channels (5 curved lines at Fibonacci‑like levels) and colors candles based on EMA/ATR trend strength.", "Detects higher highs/lower lows, draws BOS/CHoCH lines with labels, and triggers long/short signals on structure breaks.", "Includes ATR‑based SL (3× ATR), three TP levels (user‑defined %), risk management table, MTF panel (6 timeframes), and a complete backtesting strategy."], youtubeUrl: "https://www.youtube.com/watch?v=6wsoGS1Ld9Q", imageUrl: "MarketStructure.mp4", category: "Market Structure & Breakout", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/T105125167X", upwork: "https://www.upwork.com/services/product/development-it-market-structure-break-with-targets-open-source-tradingview-indicator-1856384999497324136?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/MarketStructureBreakWithTargets", telegram: "https://t.me/algoritmoatros" } },
    { name: "Gann Price Time Angles Lite", desc: "Semi‑automatic Gann Angles tool that draws 1/1, 2/1, 3/1, 4/1, and 8/1 angles from a user‑selected pivot time. It uses a Major swing ZigZag (period 20–50) to determine price range and direction, then projects Gann retracement levels (0% to 100% in 12.5% increments) and vertical time lines every 45 bars.", tags: ["GannAngles", "GannTheory", "SwingTrading", "TechnicalAnalysis", "TradingView"], badge: "pro", features: ["Plots classic Gann angles (1/1, 2/1, 3/1, 4/1, 8/1) from a manually defined start time, using the major swing high/low at that pivot.", "Displays horizontal retracement levels (12.5% increments) and vertical time divisions (every 45 bars) for precise geometric analysis.", "Offers optional quadrant fills, angle extensions, and projection lines, with separate color controls for each angle group."], youtubeUrl: "https://www.youtube.com/watch?v=bLfphPWeEk4", imageUrl: "GannLite.mp4", category: "Gann Theory & Cycles", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/P105125220L", upwork: "https://www.upwork.com/services/product/development-it-gann-angles-lite-open-source-tradingview-indicator-1872395527074301291?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/itzvs", telegram: "https://t.me/algoritmoatros" } },
    { name: "Algorithmic Gann", desc: "AlgoGann is an automated Gann‑based trading system that combines Gann HiLo channels (smoothed with ATR), Gann bar coloring (up/down/inside/outside days), and Renko ATR to generate long/short signals. It includes dynamic support/resistance via a pivot‑based heatmap, classic pivot points, and ATR‑based stop loss + three take‑profit levels.", tags: ["AlgoGann", "GannHiLo", "RenkoATR", "MarketStructure", "TradingView"], badge: "pro", features: ["Identifies trend direction using Gann HiLo channels and bar types (up/down/inside/outside days) combined with Renko ATR reversals for entry signals.", "Plots dynamic support/resistance zones via a heatmap of clustered pivot points, plus classic pivot highs/lows.", "Includes ATR‑based stop loss (3× ATR), three take‑profit targets (1%, 2%, 3% editable), risk table, MTF panel, and complete backtesting strategy."], youtubeUrl: "https://www.youtube.com/watch?v=pdJoopbD9rw", imageUrl: "AlgoGann.mp4", category: "Algorithmic Trend Following", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/D105125276V", upwork: "https://www.upwork.com/services/product/development-it-algorithmic-gann-open-source-tradingview-indicator-1885803185970586545?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/AlgorithmicGann", telegram: "https://t.me/algoritmoatros" } },
    { name: "Elliott Wave Advanced", desc: "Semi‑automatic Elliott Wave tool that identifies wave sequences (Wave 2/B, Wave C, Wave 3, Wave 4, Wave 5) from a user‑selected pivot time. It uses three independent ZigZag swings (minor, intermediate, major) to define price legs and projects target zones (Minimum, Typical, Maximum, Extended) as colored boxes on the chart.", tags: ["ElliottWave", "WaveProjection", "ZigZag", "TechnicalAnalysis", "TradingView"], badge: "pro", features: ["Automatically detects Elliott Wave structures (2/B, C, 3, 4, 5) from a manual start point using three swing lengths.", "Draws price target boxes for each wave with multiple projection levels (Typical, Maximum, Extended) based on Fibonacci‑like ratios.", "Displays wave labels (1,2,3,4,5 or A,B,C) directly on the chart with full color and opacity customization."], youtubeUrl: "https://www.youtube.com/watch?v=vrZ9IC0f_x4", imageUrl: "ElliottWaveAdvanced.mp4", category: "Elliott Wave Analysis", price: 75, oldPrice: 80, buyLinks: { hotmart: "https://pay.hotmart.com/X105125321I", upwork: "https://www.upwork.com/services/product/development-it-elliott-wave-advanced-open-source-tradingview-indicator-1902486806915866872?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/ElliottWaveAdvanced", telegram: "https://t.me/algoritmoatros" } },
    { name: "Trailing Stop Multi-Mode Advanced", desc: "Advanced trailing stop manager with two independent operating modes: R‑based trailing (1.3R break‑even then +0.5R/0.25R step trails) and traditional trailing (ATR or percentage). You can choose automatic entry (using a selected bar’s high/low with ATR stop) or manual entry with custom prices.", tags: ["TrailingStop", "RiskManagement", "PositionSizing", "RTrading", "TradingView"], badge: "pro", features: ["Switch between R‑based profit trailing (customizable break‑even and step multiples) and classic ATR/percent trailing.", "Automatically calculates entry and initial stop from a timestamped bar, or use fully manual levels.", "Visualises all stop levels, step lines, hit markers, and updatable on‑chart labels for total trade transparency."], youtubeUrl: "https://www.youtube.com/watch?v=oHVogrtUCaU", imageUrl: "TrailingStopAdvanced.mp4", category: "Algorithmic Trend Following", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/F105125380Q", upwork: "https://www.upwork.com/services/product/development-it-advanced-multi-mode-trailing-stop-open-source-indicator-for-tradingview-1988968429076636109?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/AdvancedMultiModeTrailingStop", telegram: "https://t.me/algoritmoatros" } },
    { name: "MTP Analysis & MTP STF", desc: "This multi‑module indicator combines market structure detection (swing highs/lows of three degrees), real‑time reversal bar signals, and an adaptive ATR trailing stop on the price chart. A second panel displays a momentum histogram with dynamic strength bands, helping traders assess trend direction and potential exhaustion across multiple timeframes.", tags: ["MTPAnalysis", "MTPSTF", "HigherTimeframe", "ReversalBars", "TradingView"], badge: "pro", features: ["Identifies three tiers of market swings (minor, intermediate, major) and draws them as zig‑zag lines directly on the chart.", "Highlights potential reversal bars using a proprietary combination of price action, range position, and stochastic readings.", "Includes a separate momentum histogram with upper/lower strength bands to visualise trend direction and strength changes over time."], youtubeUrl: "https://www.youtube.com/watch?v=1hWsDSD25fI", imageUrl: "MTPAnalysisSTF.mp4", category: "Premium Plugins & Ecosystems", price: 100, oldPrice: 110, buyLinks: { hotmart: "https://pay.hotmart.com/S105125506U", upwork: "https://www.upwork.com/services/product/development-it-analysis-and-zone-controls-open-source-for-tradingview-2035845182035020203?ref=project_share&tier=2", gumroad: "https://patriciocoding.gumroad.com/l/MTPAnalysisMTPSTF", telegram: "https://t.me/algoritmoatros" } },
    { name: "MTP Analysis & MTP Decision Point", desc: "This indicator identifies swing pivots across three degrees (minor, intermediate, major) and projects Decision Point (DP) zones directly onto the price chart. Based on the selected pivot structure, it draws colored boxes representing typical and maximum DP levels using a ratio‑driven method on a logarithmic scale.", tags: ["MTPAnalysis", "MTPDecisionPoint", "ZigZag", "ReversalBars", "TradingView"], badge: "pro", features: ["Detects minor, intermediate, and major swing pivots and labels them with numbers for easy reference.", "Plots typical and maximum Decision Point boxes starting from a user‑selected pivot, indicating possible reversal or continuation zones.", "Allows full customization of pivot selection method (last pivot, pivots back, pivot number, or bar number) and zone width."], youtubeUrl: "https://www.youtube.com/watch?v=2ihLaCs3xP8", imageUrl: "AnalysisDP.mp4", category: "Premium Plugins & Ecosystems", price: 100, oldPrice: 110, buyLinks: { hotmart: "https://pay.hotmart.com/I105125418H", upwork: "https://www.upwork.com/services/product/development-it-analysis-and-zone-controls-open-source-for-tradingview-2035845182035020203?ref=project_share&tier=0", gumroad: "https://patriciocoding.gumroad.com/l/MTPAnalysisMTPDP", telegram: "https://t.me/algoritmoatros" } },
    { name: "MTP Analysis & MTP Wave Price Targets", desc: "This indicator integrates a multi‑level market structure analysis (minor, intermediate, and major swings) with a reversal bar detection system and an ATR‑based trailing stop. It complements pivot identification with price target projections based on Elliott Wave theory (WPT), drawing colored zones for minimum, typical, maximum, and extended levels.", tags: ["MTPAnalysis", "MTPDecisionPoint", "ZigZag", "ReversalBars", "TradingView"], badge: "pro", features: ["Automatically detects three degrees of pivots (minor, intermediate, major) and connects them with zig‑zag lines.", "Projects price target zones for Wave 2/B, C, 3, 4, and 5 structures with different probability levels.", "Includes reversal bar signals and a dynamic ATR‑based trailing stop to manage trend direction."], youtubeUrl: "https://www.youtube.com/watch?v=dsRTx14AoF4", imageUrl: "AnalysisWPT.mp4", category: "Premium Plugins & Ecosystems", price: 100, oldPrice: 110, buyLinks: { hotmart: "https://pay.hotmart.com/S105125462W", upwork: "https://www.upwork.com/services/product/development-it-analysis-and-zone-controls-open-source-for-tradingview-2035845182035020203?ref=project_share&tier=1", gumroad: "https://patriciocoding.gumroad.com/l/MTPAnalysisMTPWavePriceTargets", telegram: "https://t.me/algoritmoatros" } },
    { name: "Harmonic Pattern Complete (HPC) Advanced", desc: "This advanced indicator automatically detects complete harmonic patterns (Gartley, Bat, Alt Bat, Butterfly, Crab, Deep Crab) directly on the chart. It identifies swing pivots, applies Fibonacci ratios with configurable tolerance, and draws the full XABCD structure. The tool displays the Potential Reversal Zone (PRZ), Hidden Opportunity Point (HOP), take‑profit levels, and even projects incomplete patterns based on the best XABC candidate.", tags: ["HarmonicPatterns ", "Fibonacci", "PRZ", "TechnicalAnalysis", "TradingView"], badge: "pro", features: ["Detects six classic harmonic patterns using pivot points and Fibonacci ratio ranges with adjustable tolerance.", "Plots the XABCD structure, PRZ zone, HOP line, and three take‑profit levels (38.2%, 61.8%, 113% of XA leg).", "Projects the most probable pattern (XABC → D) in real time and draws dynamic refresh lines from B/C to the distal PRZ limit."], youtubeUrl: "https://www.youtube.com/watch?v=HsYxG3INxp8", imageUrl: "HPCAdvanced.mp4", category: "Harmonic Patterns", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/P105432582B", upwork: "https://www.upwork.com/services/product/development-it-harmonic-pattern-complete-advanced-open-source-indicator-for-tradingview-2046961995791152592?ref=project_share&tier=1", gumroad: "https://patriciocoding.gumroad.com/l/ehaeps", telegram: "https://t.me/algoritmoatros" } },
    { name: "Terminusa Swing & Oscillator", desc: "This all‑in‑one indicator merges a multi‑layer oscillator with a complete chart overlay. The oscillator (Terminusa) combines an Elliott Wave Oscillator (EWO) with a smoothed stochastic, adaptive breakout bands, and color‑coded tolerance zones to highlight momentum extremes. The overlay (Terminusa Swing) brings together Jackson Zones (dynamic support/resistance from a higher timeframe pivot‑based calculation), an XTL trend locator that colors bars and provides dynamic stops/targets, a clean intermediate ZigZag, and Fibonacci extensions with automatic wave labeling (0 to 5).", tags: ["Terminusa", "MultiModuleIndicator", "ElliottWaveOscillator", "JacksonZones", "FibonacciExtensions"], badge: "pro", features: ["Displays a hybrid oscillator (EWO + stochastic) with adaptive breakout bands and green/red tolerance fill zones for overbought/oversold extremes.", "Overlays Jackson Zones (pivot‑based S/R levels from higher timeframes), an XTL trend locator that paints bars and plots trailing stops/targets, plus a clean intermediate ZigZag.", "Automatically draws Fibonacci extension zones (1.382, 1.5, 1.618, 2.0) with wave labels (0‑5) and optionally filters them by contact with Jackson Zones, adding historical Bull/Bear percentage labels at pivot C."], youtubeUrl: "https://www.youtube.com/watch?v=c8EW8OJq6wg", imageUrl: "TerminusaSwing.mp4", category: "Premium Plugins & Ecosystems", price: 50, oldPrice: 60, buyLinks: { hotmart: "https://pay.hotmart.com/G105753103B", upwork: "https://www.upwork.com/services/product/development-it-terminusa-swing-oscillator-plugin-open-source-indicator-for-tradingview-2050267494942111395?ref=project_share", gumroad: "https://patriciocoding.gumroad.com/l/TerminusaPlugin", telegram: "https://t.me/algoritmoatros" } }
  ];
  
  let activeCategory = "all";

  function renderIndicators() {
    const container = document.getElementById('gridContainer');
    if (!container) return;
    container.innerHTML = '';
    const filtered = indicators.filter(ind => activeCategory === 'all' || ind.category === activeCategory);
    filtered.forEach((indicator) => {
      const globalIdx = indicators.findIndex(i => i.name === indicator.name);
      const card = document.createElement('div');
      card.className = 'card';
      card.innerHTML = `
        <div class="card-top"><span class="card-num">// ${String(globalIdx+1).padStart(2,'0')}</span><span class="card-badge ${indicator.badge}">${indicator.badge === 'premium' ? 'Premium' : 'Pro'}</span></div>
        <div class="card-title">${indicator.name}</div>
        <div class="card-desc">${indicator.desc.substring(0, 120)}${indicator.desc.length > 120 ? '...' : ''}</div>
        <div class="card-meta">${indicator.tags.map(t => `<span class="meta-pill">${t}</span>`).join('')}</div>
        <div class="card-actions"><button class="btn-view" data-idx="${globalIdx}">View</button></div>
      `;
      card.querySelector('.btn-view').addEventListener('click', () => openModal(globalIdx));
      container.appendChild(card);
    });
  }

  function buildCategoryTabs() {
    const tabsContainer = document.getElementById('categoryTabs');
    if (!tabsContainer) return;
    tabsContainer.innerHTML = '';
    const allBtn = document.createElement('button');
    allBtn.className = 'cat-btn';
    allBtn.textContent = '📈 ALL';
    allBtn.dataset.cat = 'all';
    allBtn.addEventListener('click', () => {
      activeCategory = 'all';
      document.querySelectorAll('.cat-btn').forEach(btn => btn.classList.remove('active'));
      allBtn.classList.add('active');
      renderIndicators();
    });
    tabsContainer.appendChild(allBtn);
    INDICATOR_CATEGORIES.forEach(cat => {
      const btn = document.createElement('button');
      btn.className = 'cat-btn';
      btn.textContent = cat;
      btn.dataset.cat = cat;
      btn.addEventListener('click', () => {
        activeCategory = cat;
        document.querySelectorAll('.cat-btn').forEach(btn => btn.classList.remove('active'));
        btn.classList.add('active');
        renderIndicators();
      });
      tabsContainer.appendChild(btn);
    });
    const firstActive = tabsContainer.querySelector('[data-cat="all"]');
    if (firstActive) firstActive.classList.add('active');
  }

  let currentModalIndex = null;
  let previousFocus = null;

  function openModal(idx) {
    const ind = indicators[idx];
    if (!ind) return;
    currentModalIndex = idx;
    previousFocus = document.activeElement;
    
    document.getElementById('modalNum').textContent = `// INDICATOR ${String(idx+1).padStart(2,'0')}`;
    document.getElementById('modalTitle').textContent = ind.name;
    document.getElementById('modalBody').textContent = ind.desc;
    document.getElementById('modalFeatures').innerHTML = ind.features.map(f => `<li>${f}</li>`).join('');
    document.getElementById('modalImageBtn').href = ind.imageUrl || "#";
    document.getElementById('modalYoutubeBtn').href = ind.youtubeUrl || "https://www.youtube.com/@PatricioCoding";
    
    const price = (ind.price !== undefined && !isNaN(ind.price)) ? ind.price : 0;
    const oldPrice = (ind.oldPrice !== undefined && !isNaN(ind.oldPrice)) ? ind.oldPrice : price;
    let discountHtml = '';
    if (oldPrice > price) {
      const discountPercent = Math.round((1 - price / oldPrice) * 100);
      discountHtml = `<span class="badge-offer">-${discountPercent}% OFF</span>`;
    } else {
      discountHtml = `<span class="badge-offer" style="background: #2a2b35; color: #7c7d8a;">PRECIO FIJO</span>`;
    }
    
    const priceTag = document.getElementById('priceTag');
    if (priceTag) {
      priceTag.innerHTML = `
        <div><span class="price-value">$${price.toFixed(2)} USD</span>
        ${oldPrice > price ? `<span class="price-old">$${oldPrice.toFixed(2)}</span>` : ''}</div>
        ${discountHtml}
      `;
    }
    
    const telegramPrice = (price * 0.9).toFixed(2);
    const paymentContainer = document.getElementById('paymentMethodsContainer');
    if (paymentContainer && ind.buyLinks) {
      paymentContainer.innerHTML = `
        <a href="${ind.buyLinks.hotmart || '#'}" target="_blank" rel="noopener noreferrer" class="payment-btn"><div class="payment-info"><span class="payment-icon">🔥</span><span class="payment-name">Hotmart</span></div><div class="payment-price">$${price.toFixed(2)}</div></a>
        <a href="${ind.buyLinks.upwork || '#'}" target="_blank" rel="noopener noreferrer" class="payment-btn"><div class="payment-info"><span class="payment-icon">⚡</span><span class="payment-name">Upwork</span></div><div class="payment-price">$${price.toFixed(2)}</div></a>
        <a href="${ind.buyLinks.gumroad || '#'}" target="_blank" rel="noopener noreferrer" class="payment-btn"><div class="payment-info"><span class="payment-icon">🍬</span><span class="payment-name">Gumroad</span></div><div class="payment-price">$${price.toFixed(2)}</div></a>
        <a href="${ind.buyLinks.telegram || '#'}" target="_blank" rel="noopener noreferrer" class="payment-btn"><div class="payment-info"><span class="payment-icon">💬</span><span class="payment-name">Telegram</span><span class="payment-discount">10% OFF</span></div><div class="payment-price">$${telegramPrice}</div></a>
      `;
    }
    
    document.getElementById('modalOverlay').classList.add('open');
    document.body.classList.add('modal-open');
    
    setTimeout(() => {
      const modal = document.querySelector('.modal');
      if (modal) {
        const focusable = modal.querySelectorAll('button, a, [href], input, select, textarea, [tabindex]:not([tabindex="-1"])');
        if (focusable.length) focusable[0].focus();
        modal.addEventListener('keydown', trapFocusHandler);
      }
    }, 50);
  }

  function trapFocusHandler(e) {
    const modal = document.querySelector('.modal');
    if (!modal) return;
    const focusable = modal.querySelectorAll('button, a, [href], input, select, textarea, [tabindex]:not([tabindex="-1"])');
    if (focusable.length === 0) return;
    const first = focusable[0];
    const last = focusable[focusable.length-1];
    if (e.key === 'Tab') {
      if (e.shiftKey) {
        if (document.activeElement === first) {
          last.focus();
          e.preventDefault();
        }
      } else {
        if (document.activeElement === last) {
          first.focus();
          e.preventDefault();
        }
      }
    }
  }

  function closeModal() {
    const modalEl = document.querySelector('.modal');
    if (modalEl && trapFocusHandler) modalEl.removeEventListener('keydown', trapFocusHandler);
    document.getElementById('modalOverlay').classList.remove('open');
    document.body.classList.remove('modal-open');
    if (previousFocus && previousFocus.focus) previousFocus.focus();
    currentModalIndex = null;
  }

  function copyIndicatorLink() {
    if (currentModalIndex === null) return;
    const indicator = indicators[currentModalIndex];
    if (!indicator) return;
    const url = new URL(window.location.href);
    url.hash = `ind-${currentModalIndex}`;
    navigator.clipboard.writeText(url.toString()).then(() => {
      const toast = document.getElementById('toastMessage');
      toast.style.opacity = '1';
      setTimeout(() => { toast.style.opacity = '0'; }, 2000);
    }).catch(() => {
      alert('Could not copy link. You can manually share the page URL.');
    });
  }

  function checkHashAndOpenModal() {
    const hash = window.location.hash;
    if (hash && hash.startsWith('#ind-')) {
      const idx = parseInt(hash.split('-')[1], 10);
      if (!isNaN(idx) && idx >= 0 && idx < indicators.length) {
        setTimeout(() => openModal(idx), 100);
      }
    }
  }

  // menú responsive
  const hamburger = document.getElementById('hamburgerBtn');
  const navLinks = document.getElementById('navLinks');
  if (hamburger && navLinks) {
    hamburger.addEventListener('click', () => {
      const expanded = hamburger.getAttribute('aria-expanded') === 'true' ? false : true;
      hamburger.setAttribute('aria-expanded', expanded);
      navLinks.classList.toggle('open');
      if (expanded) document.body.style.overflow = 'hidden';
      else document.body.style.overflow = '';
    });
    navLinks.querySelectorAll('a').forEach(link => {
      link.addEventListener('click', () => {
        navLinks.classList.remove('open');
        hamburger.setAttribute('aria-expanded', 'false');
        document.body.style.overflow = '';
      });
    });
  }

  document.addEventListener('DOMContentLoaded', () => {
    buildCategoryTabs();
    renderIndicators();
    const overlay = document.getElementById('modalOverlay');
    document.getElementById('modalClose').addEventListener('click', closeModal);
    overlay.addEventListener('click', (e) => { if (e.target === overlay) closeModal(); });
    document.addEventListener('keydown', (e) => { if (e.key === 'Escape') closeModal(); });
    document.getElementById('modalShareBtn').addEventListener('click', copyIndicatorLink);
    checkHashAndOpenModal();
  });

  // ========== NUEVO TYPEWRITER DEFINITIVO ==========
  (function() {
    const tagEl = document.getElementById('typedTag');
    const titleEl = document.getElementById('typedTitle');
    if (!tagEl || !titleEl) return;
    
    // Textos fijos
    const tagText = "// Trading Intelligence";
    const brandPrefix = "Patricio";
    const brandSuffix = "Coding";
    
    let step = 0; // 0: tag, 1: prefix, 2: suffix, 3: pausa, 4: borrar título, 5: borrar tag, 6: reiniciar
    let tagIndex = 0, prefixIndex = 0, suffixIndex = 0;
    let currentTag = "", currentTitle = "";
    let timeoutId = null;
    
    // cursor compartido
    let cursorSpan = null;
    function ensureCursor(parent) {
      if (cursorSpan && cursorSpan.parentNode) cursorSpan.remove();
      cursorSpan = document.createElement('span');
      cursorSpan.className = 'typed-cursor';
      cursorSpan.innerHTML = ' ';
      parent.appendChild(cursorSpan);
    }
    
    function updateDisplay() {
      tagEl.innerHTML = currentTag;
      if (currentTitle.length <= brandPrefix.length) {
        titleEl.innerHTML = currentTitle;
      } else {
        const plain = currentTitle.slice(0, brandPrefix.length);
        const colored = currentTitle.slice(brandPrefix.length);
        titleEl.innerHTML = plain + `<span class="hl">${colored}</span>`;
      }
    }
    
    function next() {
      timeoutId = null;
      if (step === 0) { // escribiendo tag
        if (tagIndex < tagText.length) {
          currentTag += tagText[tagIndex++];
          updateDisplay();
          timeoutId = setTimeout(next, 50);
        } else {
          ensureCursor(tagEl);
          step = 1;
          timeoutId = setTimeout(next, 200);
        }
      } 
      else if (step === 1) { // escribiendo "Patricio"
        if (prefixIndex < brandPrefix.length) {
          currentTitle += brandPrefix[prefixIndex++];
          updateDisplay();
          timeoutId = setTimeout(next, 50);
        } else {
          step = 2;
          timeoutId = setTimeout(next, 50);
        }
      }
      else if (step === 2) { // escribiendo "Coding"
        if (suffixIndex < brandSuffix.length) {
          currentTitle += brandSuffix[suffixIndex++];
          updateDisplay();
          timeoutId = setTimeout(next, 50);
        } else {
          ensureCursor(titleEl);
          step = 3;
          timeoutId = setTimeout(next, 1250);
        }
      }
      else if (step === 3) { // pausa
        step = 4;
        timeoutId = setTimeout(next, 200);
      }
      else if (step === 4) { // borrar título
        if (currentTitle.length > 0) {
          currentTitle = currentTitle.slice(0, -1);
          updateDisplay();
          timeoutId = setTimeout(next, 30);
        } else {
          if (cursorSpan && cursorSpan.parentNode === titleEl) cursorSpan.remove();
          step = 5;
          timeoutId = setTimeout(next, 50);
        }
      }
      else if (step === 5) { // borrar tag
        if (currentTag.length > 0) {
          currentTag = currentTag.slice(0, -1);
          updateDisplay();
          timeoutId = setTimeout(next, 30);
        } else {
          if (cursorSpan && cursorSpan.parentNode === tagEl) cursorSpan.remove();
          // reiniciar
          step = 0;
          tagIndex = 0; prefixIndex = 0; suffixIndex = 0;
          currentTag = ""; currentTitle = "";
          updateDisplay();
          timeoutId = setTimeout(next, 250);
        }
      }
    }
    
    // iniciar
    tagEl.innerHTML = '';
    titleEl.innerHTML = '';
    updateDisplay();
    next();
  })();
</script>
</body>
</html>