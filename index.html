<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>PatricioCoding — Fractality In Code</title>
  <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;500;600;700;800;900&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
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
      --muted:     #7c7d8a;
      --glow:      rgba(123,130,255,0.18);
      --red:       #ff0000;   /* ← agrega esta línea */
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
    }
    /* Capa de líneas dinámicas (diagonales animadas) */
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
/* Animación de las líneas para que se deslicen */
    @keyframes drift {
      0% { background-position: 0 0; }
      100% { background-position: 40px 40px; }
    }
/* Capa extra: un suave resplandor neón que se mueve */
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
/* Mejora la cuadrícula original (ahora con líneas neón más visibles) */
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
/* Asegurar que el contenido esté por encima */
    .hero, .stats-bar, section, footer {
      position: relative;
      z-index: 2;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'Plus Jakarta Sans', sans-serif;
      min-height: 100vh;
      overflow-x: hidden;
    }

/* Cursor para typewriter */
    .cursor {
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
    /* ── GRID BACKGROUND ── */
    body::before {
      content: '';
      position: fixed;
      inset: 0;
      background-image:
        linear-gradient(rgba(67,69,81,0.07) 1px, transparent 1px),
        linear-gradient(90deg, rgba(67,69,81,0.07) 1px, transparent 1px);
      background-size: 40px 40px;
      pointer-events: none;
      z-index: 0;
    }

    /* ── NOISE OVERLAY ── */
    body::after {
      content: '';
      position: fixed;
      inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
      pointer-events: none;
      z-index: 0;
      opacity: 0.4;
    }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 1rem 3rem;
      background: rgba(0,0,0,0.75);
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
    }

    .nav-logo span {
      color: var(--neon);
      text-shadow: 0 0 12px var(--neon);
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
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

    .nav-links a:hover { color: var(--neon); }

    /* ── HERO ── */
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
    /* Efecto glow permanente en el tag */
      text-shadow: 0 0 6px var(--neon), 0 0 12px rgba(123,130,255,0.5);
      transition: text-shadow 0.3s;
}

    .hero h1 {
      font-family: 'Nunito', sans-serif;
      font-size: clamp(2.8rem, 7vw, 5.5rem);
      font-weight: 900;
      line-height: 1.05;
      letter-spacing: -0.02em;
      margin-bottom: 1rem;
      opacity: 0;
      animation: fadeUp 0.7s 0.35s forwards;
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
      margin-bottom: 0.0rem;
      opacity: 0;
      animation: fadeUp 0.7s 0.5s forwards;
    }

    .hero-cta {
      display: flex;
      gap: 1rem;
      margin-top: 0.5rem;
      flex-wrap: wrap;
      justify-content: center;
      opacity: 0;
      animation: fadeUp 0.7s 0.65s forwards;
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
    }

    .btn-primary:hover {
      box-shadow: 0 0 24px rgba(123,130,255,0.6), 0 0 60px rgba(123,130,255,0.2);
      transform: translateY(-2px);
    }

    .btn-ghost {
      font-family: 'Nunito', sans-serif;
      font-size: 0.72rem;
      font-weight: 700;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.85rem 2rem;
      border-radius: 12px;
      border: 1px solid var(--border);
      background: transparent;
      color: var(--text);
      cursor: pointer;
      text-decoration: none;
      transition: border-color 0.25s, color 0.25s, transform 0.2s;
    }

    .btn-ghost:hover {
      border-color: var(--neon);
      color: var(--neon);
      transform: translateY(-2px);
    }

    /* ── STATS BAR ── */
    .stats-bar {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1.5rem;         /* espacio entre bloques */
      border-top: 1px solid var(--border2);
      border-bottom: 1px solid var(--border2);
      background: rgba(14,14,18,0.8);
      backdrop-filter: blur(8px);
      padding: 0 1rem;
    }

    .stat {
  /* quita flex:1 y max-width fija */
      flex: 0 0 auto;
      min-width: 160px;
      padding: 1.5rem 1.5rem;
      text-align: center;
      border-right: none;   /* quita borde lateral, o ponlo como gap */
    }
    .stat:last-child { border-right: none; }

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

    /* ── SECTION ── */
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

    /* ── INDICATORS GRID ── */
    .indicators-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
      gap: 1.5rem;
    }

    /* ── CARD ── */
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

    .btn-view:hover {
      border-color: var(--neon3);
      color: var(--neon3);
      background: rgba(56,189,248,0.06);
    }

    .btn-pay {
      flex: 1;
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.65rem 1rem;
      border-radius: 12px;
      border: none;
      background: var(--neon);
      color: #000;
      cursor: pointer;
      text-decoration: none;
      text-align: center;
      font-weight: 700;
      transition: box-shadow 0.2s, transform 0.2s;
    }

    .btn-pay:hover {
      box-shadow: 0 0 18px rgba(123,130,255,0.55);
      transform: translateY(-1px);
    }

    /* ---- NUEVO BOTÓN ROJO PARA YOUTUBE ---- */
    .btn-youtube {
      flex: 1;
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.65rem 1rem;
      border-radius: 12px;
      border: none;
      background: var(--red);
      color: white;
      cursor: pointer;
      text-decoration: none;
      text-align: center;
      font-weight: 700;
      transition: box-shadow 0.2s, transform 0.2s, background 0.2s;
    }

/* Botón para comprar (neon3) */
    .btn-buy {
      flex: 1;
      font-family: 'DM Mono', monospace;
      font-size: 0.72rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      padding: 0.65rem 1rem;
      border-radius: 12px;
      border: none;
      background: var(--neon3);
      color: whitesmoke;
      cursor: pointer;
      text-decoration: none;
      text-align: center;
      font-weight: 700;
      transition: box-shadow 0.2s, transform 0.2s, background 0.2s;
    }

    .btn-buy:hover {
      background: #2aa0d0;
      box-shadow: 0 0 18px rgba(56,189,248,0.6);
      transform: translateY(-1px);
    }


    .btn-youtube:hover {
      background: #e60000;
      box-shadow: 0 0 18px rgba(255, 77, 77, 0.6);
      transform: translateY(-1px);
    }

    /* ---- MODAL ---- */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.85);
      backdrop-filter: blur(8px);
      z-index: 200;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1.5rem;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.25s;
    }

    /* ── MODAL ── */
    .modal-overlay {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.85);
      backdrop-filter: blur(8px);
      z-index: 200;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 1.5rem;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.25s;
    }

    .modal-overlay.open {
      opacity: 1;
      pointer-events: all;
    }

    .modal {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 12px;
      width: 100%;
      max-width: 560px;
      padding: 2.25rem;
      position: relative;
      transform: translateY(20px);
      transition: transform 0.3s;
    }

    .modal-overlay.open .modal { transform: translateY(0); }

    .modal-close {
      position: absolute;
      top: 1.25rem; right: 1.25rem;
      background: none;
      border: 1px solid var(--border2);
      color: var(--muted);
      font-size: 1rem;
      width: 2rem; height: 2rem;
      border-radius: 12px;
      cursor: pointer;
      display: flex; align-items: center; justify-content: center;
      transition: border-color 0.2s, color 0.2s;
    }
    .modal-close:hover { border-color: var(--neon); color: var(--neon); }

    .modal-num {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      color: var(--neon);
      letter-spacing: 0.04em;
      margin-bottom: 0.5rem;
    }

    .modal-title {
      font-family: 'Nunito', sans-serif;
      font-size: 1.35rem;
      font-weight: 700;
      margin-bottom: 1rem;
      line-height: 1.3;
    }

    .modal-divider {
      height: 1px;
      background: var(--border2);
      margin: 1rem 0;
    }

    .modal-body {
      font-size: 0.85rem;
      color: var(--muted);
      line-height: 1.75;
      margin-bottom: 1.25rem;
    }

    .modal-features {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 0.5rem;
      margin-bottom: 1.75rem;
    }

    .modal-features li {
      font-family: 'DM Mono', monospace;
      font-size: 0.75rem;
      color: var(--text);
      padding: 0.5rem 0.75rem;
      background: rgba(67,69,81,0.12);
      border-left: 2px solid var(--neon);
      border-radius: 0 4px 4px 0;
    }

    .modal-actions {
      display: flex;
      gap: 0.75rem;
    }

    /* ── FOOTER ── */
    footer {
      position: relative;
      z-index: 1;
      border-top: 1px solid var(--border2);
      padding: 2rem 3rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .footer-brand {
      font-family: 'Nunito', sans-serif;
      font-weight: 900;
      font-size: 0.9rem;
      letter-spacing: 0.02em;
      color: var(--muted);
    }

    .footer-brand span { color: var(--neon); }

    .footer-copy {
      font-family: 'DM Mono', monospace;
      font-size: 0.65rem;
      color: var(--muted);
      letter-spacing: 0.02em;
    }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(18px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    /* stagger cards */
    .card:nth-child(1)  { animation-delay: 0.05s }
    .card:nth-child(2)  { animation-delay: 0.10s }
    .card:nth-child(3)  { animation-delay: 0.15s }
    .card:nth-child(4)  { animation-delay: 0.20s }
    .card:nth-child(5)  { animation-delay: 0.25s }
    .card:nth-child(6)  { animation-delay: 0.30s }
    .card:nth-child(7)  { animation-delay: 0.35s }
    .card:nth-child(8)  { animation-delay: 0.40s }
    .card:nth-child(9)  { animation-delay: 0.45s }
    .card:nth-child(10) { animation-delay: 0.50s }
    .card:nth-child(11) { animation-delay: 0.55s }
    .card:nth-child(12) { animation-delay: 0.60s }
    .card:nth-child(13) { animation-delay: 0.65s }
    .card:nth-child(14) { animation-delay: 0.70s }
    .card:nth-child(15) { animation-delay: 0.75s }
    .card:nth-child(16) { animation-delay: 0.80s }
    .card:nth-child(17) { animation-delay: 0.85s }
    .card:nth-child(18) { animation-delay: 0.90s }
    .card:nth-child(19) { animation-delay: 0.95s }
    .card:nth-child(20) { animation-delay: 1.00s }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      nav { padding: 1rem 1.25rem; }
      .nav-links { display: none; }
      .indicators-grid { grid-template-columns: 1fr; }
      footer { flex-direction: column; text-align: center; }
      .stats-bar { flex-wrap: wrap; }
      .stat { min-width: 50%; border-right: none; border-bottom: 1px solid var(--border2); }
      .social-img { width: 32px; height: 32px; }
    }
/* Iconos de redes sociales - VERSIÓN MEJORADA */
.social-icons {
  display: flex;
  justify-content: center;
  gap: 1.0rem;
  margin-top: 0.5rem;
  flex-wrap: wrap;
  clear: both;        /* fuerza salto de línea */
  width: 100%;        /* ocupa todo el ancho */
}

.social-img {
  width: 48px;        /* más grande para mejor resolución */
  height: 48px;
  object-fit: contain;  /* evita deformación */
  transition: transform 0.2s, filter 0.2s;
  filter: brightness(0.8);
  /* eliminamos el círculo, fondo y borde */
  background: none;
  border: none;
  border-radius: 0;
  padding: 0;
}

.social-img:hover {
  transform: translateY(-3px);
  filter: brightness(1) drop-shadow(0 0 6px var(--neon));
}

/* Panel minimalista de opciones de compra */
.buy-options-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.7);
  backdrop-filter: blur(4px);
  z-index: 300;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.2s;
}

.buy-options-overlay.show {
  opacity: 1;
  pointer-events: all;
}

.buy-options-panel {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 20px;
  padding: 1.5rem;
  width: 280px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(0,0,0,0.5);
  transform: scale(0.95);
  transition: transform 0.2s;
}

.buy-options-overlay.show .buy-options-panel {
  transform: scale(1);
}

.buy-options-panel h4 {
  font-family: 'DM Mono', monospace;
  color: var(--neon);
  letter-spacing: 0.05em;
  font-size: 0.9rem;
  margin-bottom: 1.2rem;
  text-transform: uppercase;
}

.buy-options-buttons {
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
}

.buy-option-btn {
  background: rgba(255,255,255,0.03);
  border: 1px solid var(--border2);
  border-radius: 40px;
  padding: 0.6rem 1rem;
  font-family: 'DM Mono', monospace;
  font-size: 0.75rem;
  font-weight: 500;
  text-transform: uppercase;
  color: var(--text);
  text-decoration: none;
  transition: all 0.2s;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.6rem;
}

/* Colores específicos por plataforma */
.buy-option-btn[data-platform="hotmart"] {
  background: #ff6b00;
  border-color: #ff6b00;
  color: white;
}
.buy-option-btn[data-platform="hotmart"]:hover {
  background: #e05a00;
  transform: translateX(4px);
  box-shadow: 0 0 12px rgba(255,107,0,0.5);
}

.buy-option-btn[data-platform="upwork"] {
  background: #6fda44;
  border-color: #6fda44;
  color: white;
}
.buy-option-btn[data-platform="upwork"]:hover {
  background: #5bc02e;
  transform: translateX(4px);
  box-shadow: 0 0 12px rgba(111,218,68,0.5);
}

.buy-option-btn[data-platform="gumroad"] {
  background: #ff90e8;
  border-color: #ff90e8;
  color:white;
}
.buy-option-btn[data-platform="gumroad"]:hover {
  background: #e67bcf;
  transform: translateX(4px);
  box-shadow: 0 0 12px rgba(255,144,232,0.5);
}

.buy-option-btn[data-platform="telegram"] {
  background: #0088cc;
  border-color: #0088cc;
  color: white;
}
.buy-option-btn[data-platform="telegram"]:hover {
  background: #0077b3;
  transform: translateX(4px);
  box-shadow: 0 0 12px rgba(0,136,204,0.5);
}

/* Eliminar estilos genéricos que interfieran */
.buy-option-btn:hover {
  border-color: inherit;
  background: inherit; /* se redefine arriba */
}

.buy-option-btn:hover {
  border-color: var(--neon);
  background: rgba(123,130,255,0.1);
  color: var(--neon);
  transform: translateX(4px);
}

.close-buy-panel {
  margin-top: 1.2rem;
  background: none;
  border: none;
  color: var(--muted);
  font-size: 0.7rem;
  cursor: pointer;
  font-family: 'DM Mono', monospace;
  transition: color 0.2s;
}

.close-buy-panel:hover {
  color: var(--neon);
}

  </style>
</head>
<body>
<div class="grid-overlay"></div>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Patricio<span>Coding</span></a>
  <ul class="nav-links">
    <li><a href="#indicators">Indicators</a></li>
    <li><a href="https://linktr.ee/patriciocoding?utm_source=linktree_profile_share&ltsid=5b4acc1d-4658-46dc-b87d-c34e3528153a" target="_blank" class="linktree-link">LINKTREE</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-glow"></div>
  <p class="hero-tag" id="typedTag"></p>
  <h1 id="typedTitle"></h1>
  <p class="hero-sub">High-performance trading indicators designed to trade accurately in any market.</p>

  <!-- Redes Sociales con PNGs (debajo del texto) -->
  <div class="social-icons">
    <a href="https://t.me/algoritmoatros" target="_blank">
      <img src="Telegram.png" alt="Telegram" class="social-img">
    </a>
    <a href="https://www.youtube.com/@PatricioCoding" target="_blank">
      <img src="YouTube.png" alt="YouTube" class="social-img">
    </a>
    <!-- Agrega más si quieres -->
    <a href="hhttps://www.instagram.com/patriciocoding/" target="_blank">
      <img src="Instagram.png" alt="Instagram" class="social-img">
    </a>
  </div>

  <div class="hero-cta">
    <a href="#indicators" class="btn-primary">Ver Indicadores</a>
    <a href="https://hotmart.com" target="_blank" class="btn-ghost">Ir a la tienda</a>
  </div>
</div>

<!-- STATS -->
<div class="stats-bar">
  <div class="stat">
    <span class="stat-val">+20</span>
    <span class="stat-label">Open Source Projects</span>
  </div>
  <div class="stat">
    <span class="stat-val">TradingView</span>
    <span class="stat-label">Solutions Projects</span>
  </div>
  <div class="stat">
    <span class="stat-val">Pine Script</span>
    <span class="stat-label">Language</span>
  </div>
  <div class="stat">
    <span class="stat-val">24/7</span>
    <span class="stat-label">Support</span>
  </div>
</div>

<!-- INDICATORS -->
<section id="indicators">
  <div class="section-header">
    <span class="section-tag">// arsenal completo</span>
    <h2 class="section-title">Todos los <span class="hl">Indicadores</span></h2>
  </div>
  <div class="indicators-grid" id="gridContainer"></div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-brand">Patricio<span>Coding</span></div>
  <div class="footer-copy">© 2025 PatricioCoding — Fractality In Code</div>
</footer>

<!-- MODAL CORREGIDO -->
<div class="modal-overlay" id="modalOverlay">
  <div class="modal">
    <button class="modal-close" id="modalClose">✕</button>
    <div class="modal-num" id="modalNum"></div>
    <div class="modal-title" id="modalTitle"></div>
    <div class="modal-divider"></div>
    <div class="modal-body" id="modalBody"></div>
    <ul class="modal-features" id="modalFeatures"></ul>
    <div class="modal-actions" style="flex-direction: column; gap: 0.75rem;">
      <a id="modalYoutubeBtn" href="#" target="_blank" class="btn-youtube">Ver en YouTube</a>
      <a id="modalBuyBtn" href="#" target="_blank" class="btn-buy">BUY INDICATOR</a>
    </div>
  </div>
</div>

<script>
  // ── DATA DE INDICADORES (con youtubeUrl) ──
  const indicators = [
    {
      name: "Fractal Trend Engine",
      desc: "Detecta tendencias usando estructuras fractales multi-timeframe para identificar la dirección dominante del mercado.",
      tags: ["Tendencia", "Multi-TF"],
      badge: "pro",
      features: ["Análisis fractal en 3 timeframes", "Señales de entrada filtradas", "Compatible con todos los activos", "Alertas configurables"],
      youtubeUrl: "https://www.youtube.com/watch?v=GnJ4znpPgr8",
      buyUrl: "https://hotmart.com/es/producto/tu-enlace"
    }
  ];

  // Esperar a que el DOM esté completamente cargado
  document.addEventListener('DOMContentLoaded', function() {
    // Renderizar tarjetas
    const grid = document.getElementById('gridContainer');
    indicators.forEach((ind, i) => {
      const badgeLabel = ind.badge === 'premium' ? 'Premium' : 'Pro';
      const card = document.createElement('div');
      card.className = 'card';
      card.innerHTML = `
        <div class="card-top">
          <span class="card-num">// ${String(i+1).padStart(2,'0')}</span>
          <span class="card-badge ${ind.badge}">${badgeLabel}</span>
        </div>
        <div class="card-title">${ind.name}</div>
        <div class="card-desc">${ind.desc}</div>
        <div class="card-meta">
          ${ind.tags.map(t => `<span class="meta-pill">${t}</span>`).join('')}
        </div>
        <div class="card-actions">
          <button class="btn-view" onclick="openModal(${i})">View</button>
        </div>
      `;
      grid.appendChild(card);
    });

    // Definir funciones globales para que onclick las encuentre
    window.openModal = function(i) {
      const ind = indicators[i];
      const modalNum = document.getElementById('modalNum');
      const modalTitle = document.getElementById('modalTitle');
      const modalBody = document.getElementById('modalBody');
      const modalFeatures = document.getElementById('modalFeatures');
      const modalYoutubeBtn = document.getElementById('modalYoutubeBtn');
      const overlay = document.getElementById('modalOverlay');

      if (modalNum) modalNum.textContent = `// INDICATOR ${String(i+1).padStart(2,'0')}`;
      if (modalTitle) modalTitle.textContent = ind.name;
      if (modalBody) modalBody.textContent = ind.desc;
      if (modalFeatures) modalFeatures.innerHTML = ind.features.map(f => `<li>→ ${f}</li>`).join('');
      if (modalYoutubeBtn) modalYoutubeBtn.href = ind.youtubeUrl || "https://www.youtube.com/@PatricioCoding";
      if (overlay) {
        overlay.classList.add('open');
        document.body.style.overflow = 'hidden';
      }
    };

    window.closeModal = function() {
      const overlay = document.getElementById('modalOverlay');
      if (overlay) {
        overlay.classList.remove('open');
        document.body.style.overflow = '';
      }
    };

    // Asignar event listeners a los elementos del modal
    const overlay = document.getElementById('modalOverlay');
    const modalClose = document.getElementById('modalClose');

    if (modalClose) modalClose.addEventListener('click', window.closeModal);
    if (overlay) overlay.addEventListener('click', function(e) { if (e.target === overlay) window.closeModal(); });
    document.addEventListener('keydown', function(e) { if (e.key === 'Escape') window.closeModal(); });

    // Lógica del panel de opciones de compra
    const buyOptionsOverlay = document.getElementById('buyOptionsOverlay');
    const closeBuyPanel = document.getElementById('closeBuyPanel');
    const modalBuyBtn = document.getElementById('modalBuyBtn');

    function showBuyOptions() {
      if (buyOptionsOverlay) buyOptionsOverlay.classList.add('show');
    }
    function hideBuyOptions() {
      if (buyOptionsOverlay) buyOptionsOverlay.classList.remove('show');
    }

    if (modalBuyBtn) {
      modalBuyBtn.addEventListener('click', function(e) {
        e.preventDefault();
        showBuyOptions();
      });
    }
    if (closeBuyPanel) closeBuyPanel.addEventListener('click', hideBuyOptions);
    if (buyOptionsOverlay) {
      buyOptionsOverlay.addEventListener('click', function(e) {
        if (e.target === buyOptionsOverlay) hideBuyOptions();
      });
    }
    document.addEventListener('keydown', function(e) {
      if (e.key === 'Escape' && buyOptionsOverlay?.classList.contains('show')) hideBuyOptions();
    });
  });
</script>
<script>
  // ── TYPEWRITER EFFECT WITH INFINITE LOOP ──
  (function() {
    const tagElement = document.getElementById('typedTag');
    const titleElement = document.getElementById('typedTitle');
    
    const tagText = "// Trading Intelligence";
    const titlePrefix = "Patricio";
    const titleSuffix = "Coding";
    
    let state = "writingTag"; // states: writingTag, writingTitlePrefix, writingTitleSuffix, pausing, erasingTitle, erasingTag
    let i = 0, j = 0, k = 0;
    let timeoutId = null;
    let pauseTimeout = null;
    
    function clearTimeouts() {
      if (timeoutId) clearTimeout(timeoutId);
      if (pauseTimeout) clearTimeout(pauseTimeout);
    }
    
    function eraseText(element, length, callback) {
      let currentLength = length;
      function eraseStep() {
        if (currentLength > 0) {
          const text = element.innerHTML;
          // Remove last character, but preserve any inner span structure for title
          if (element === titleElement) {
            // Complex inner HTML, easier to rebuild
            const fullText = titleElement.innerText; // get plain text
            const newText = fullText.slice(0, -1);
            titleElement.innerHTML = newText; // this loses spans, but we'll reapply later
            // But we need to handle the hl span later. Simpler: use textContent for erasing
            // Actually, we can store as plain text and re-apply hl after rewrite? Better to manage with care.
            // Let's do a simpler approach: store the whole text as plain string and manipulate
          } else {
            // For tagElement, it's plain text
            element.innerHTML = text.slice(0, -1);
          }
          currentLength--;
          timeoutId = setTimeout(eraseStep, 50);
        } else {
          callback();
        }
      }
      eraseStep();
    }
    
    // Instead of complex DOM manipulation, we'll use a simpler method: store the raw strings and rebuild.
    // We'll keep separate strings for the current content of tag and title.
    let currentTagContent = "";
    let currentTitleContent = "";
    
    function updateTagDisplay() {
      tagElement.innerHTML = currentTagContent;
    }
    
    function updateTitleDisplay() {
      // Title display: either just the prefix or prefix+suffix, but suffix should be inside .hl span
      if (currentTitleContent.length <= titlePrefix.length) {
        titleElement.innerHTML = currentTitleContent;
      } else {
        const prefixPart = titlePrefix;
        const suffixPart = currentTitleContent.slice(titlePrefix.length);
        titleElement.innerHTML = prefixPart + `<span class="hl">${suffixPart}</span>`;
      }
    }
    
    function resetAndRestart() {
      currentTagContent = "";
      currentTitleContent = "";
      updateTagDisplay();
      updateTitleDisplay();
      i = 0; j = 0; k = 0;
      state = "writingTag";
      typeLoop();
    }
    
    function typeLoop() {
      clearTimeouts();
      
      if (state === "writingTag") {
        if (i < tagText.length) {
          currentTagContent += tagText[i];
          updateTagDisplay();
          i++;
          timeoutId = setTimeout(typeLoop, 50);
        } else {
          // Tag finished, add permanent cursor? But we'll remove on erase, so let's add a cursor that will be removed later.
          // Actually we can add a blinking cursor but it will be erased. Simpler: no cursor during loop, or add after each write.
          // To avoid extra complexity, we skip the permanent cursor in loop. But you wanted a cursor at the end of tag? In loop it will appear and disappear. I'll add a cursor span that we remove later.
          // Better: just move to next state without cursor, but the user expects a cursor? We can add a cursor that blinks and remove on erase.
          const cursor = document.createElement('span');
          cursor.className = 'cursor';
          cursor.id = 'tagCursor';
          cursor.innerHTML = ' ';
          tagElement.appendChild(cursor);
          state = "writingTitlePrefix";
          timeoutId = setTimeout(typeLoop, 200); // small pause before title
        }
      } 
      else if (state === "writingTitlePrefix") {
        if (j < titlePrefix.length) {
          currentTitleContent += titlePrefix[j];
          updateTitleDisplay();
          j++;
          timeoutId = setTimeout(typeLoop, 50);
        } else {
          state = "writingTitleSuffix";
          timeoutId = setTimeout(typeLoop, 50);
        }
      }
      else if (state === "writingTitleSuffix") {
        if (k < titleSuffix.length) {
          currentTitleContent += titleSuffix[k];
          updateTitleDisplay();
          k++;
          timeoutId = setTimeout(typeLoop, 50);
        } else {
          // Title complete, add cursor
          const titleCursor = document.createElement('span');
          titleCursor.className = 'cursor';
          titleCursor.id = 'titleCursor';
          titleCursor.innerHTML = ' ';
          titleElement.appendChild(titleCursor);
          state = "pausing";
          pauseTimeout = setTimeout(() => {
            state = "erasingTitle";
            typeLoop();
          }, 1250);
        }
      }
      else if (state === "erasingTitle") {
        if (currentTitleContent.length > 0) {
          // remove last character
          currentTitleContent = currentTitleContent.slice(0, -1);
          updateTitleDisplay();
          // also remove cursor if present
          const titleCursor = document.getElementById('titleCursor');
          if (titleCursor && currentTitleContent.length === 0) titleCursor.remove();
          timeoutId = setTimeout(typeLoop, 50);
        } else {
          // remove tag cursor
          const tagCursor = document.getElementById('tagCursor');
          if (tagCursor) tagCursor.remove();
          state = "erasingTag";
          timeoutId = setTimeout(typeLoop, 50);
        }
      }
      else if (state === "erasingTag") {
        if (currentTagContent.length > 0) {
          currentTagContent = currentTagContent.slice(0, -1);
          updateTagDisplay();
          timeoutId = setTimeout(typeLoop, 50);
        } else {
          // both erased, restart
          state = "writingTag";
          i = 0; j = 0; k = 0;
          timeoutId = setTimeout(typeLoop, 250);
        }
      }
    }
    
    // Start the loop
    window.addEventListener('DOMContentLoaded', () => {
      tagElement.innerHTML = '';
      titleElement.innerHTML = '';
      currentTagContent = '';
      currentTitleContent = '';
      i = 0; j = 0; k = 0;
      state = "writingTag";
      typeLoop();
    });
  })();
</script>

<!-- Panel de opciones de compra (inicialmente oculto) -->
<div id="buyOptionsOverlay" class="buy-options-overlay">
  <div class="buy-options-panel">
    <h4>⚡ Selecciona plataforma</h4>
    <div class="buy-options-buttons">
      <a href="https://hotmart.com" target="_blank" class="buy-option-btn" data-platform="hotmart">Hotmart [WebSite]</a>
      <a href="https://www.upwork.com" target="_blank" class="buy-option-btn" data-platform="upwork">Upwork [WebSite]</a>
      <a href="https://gumroad.com" target="_blank" class="buy-option-btn" data-platform="gumroad">Gumroad [WebSite]</a>
      <a href="https://t.me/tuusuario" target="_blank" class="buy-option-btn" data-platform="telegram">Telegram [10% OFF]</a>
    </div>
    <button class="close-buy-panel" id="closeBuyPanel">Cerrar</button>
  </div>
</div>

</body>
</html>
