<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="theme-color" content="#fff5f7">
  <meta name="description" content="Shravani Karad — fashion, personal style, and a plot twist in embedded technology.">
  <title>Shravani Karad — Style first. Plot twist: I code.</title>
  <style>
    :root {
      color-scheme: light;
      --paper: #fff7f7;
      --ink: #38232d;
      --muted: #806872;
      --line: #f0dce2;
      --red: #d7507a;
      --acid: #ffd4e3;
      --blue: #f6dce6;
      --serif: Georgia, "Times New Roman", serif;
      --sans: "Helvetica Neue", Helvetica, Arial, sans-serif;
      --mono: "SFMono-Regular", Consolas, "Liberation Mono", monospace;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      background: var(--paper);
      color: var(--ink);
      font-family: var(--sans);
      -webkit-font-smoothing: antialiased;
    }
    a { color: inherit; }
    a:focus-visible {
      outline: 2px solid var(--red);
      outline-offset: 4px;
    }
    .shell {
      width: min(1320px, calc(100% - 64px));
      margin: 0 auto;
    }
    .eyebrow, .tag, .nav, .meta, .number, .footer-note {
      font-family: var(--mono);
      text-transform: uppercase;
      letter-spacing: .08em;
    }
    .eyebrow {
      color: var(--red);
      font-size: 11px;
      line-height: 1.6;
    }
    .topbar {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      border-bottom: 1px solid var(--line);
    }
    .wordmark {
      font-family: var(--mono);
      font-size: 11px;
      letter-spacing: .045em;
      text-decoration: none;
    }
    .wordmark span { color: var(--red); }
    .nav {
      display: flex;
      gap: 28px;
      font-size: 10px;
    }
    .nav a { text-decoration: none; }
    .nav a:hover { color: var(--red); }
    .hero {
      min-height: 650px;
      display: grid;
      grid-template-columns: minmax(0, 1.15fr) minmax(320px, .85fr);
      align-items: center;
      gap: 4vw;
      padding: 76px 0 86px;
    }
    .hero-copy { position: relative; z-index: 1; }
    h1, h2, h3, p { margin-top: 0; }
    h1 {
      max-width: 800px;
      margin: 22px 0 25px;
      font-family: var(--serif);
      font-size: clamp(64px, 8.5vw, 122px);
      font-weight: 400;
      letter-spacing: -.075em;
      line-height: .91;
    }
    h1 em {
      color: var(--red);
      font-weight: 400;
    }
    .hero-intro {
      max-width: 470px;
      color: var(--muted);
      font-size: 16px;
      line-height: 1.65;
    }
    .hero-links {
      display: flex;
      align-items: center;
      gap: 24px;
      margin-top: 33px;
    }
    .button {
      display: inline-flex;
      min-height: 48px;
      align-items: center;
      justify-content: center;
      padding: 0 20px;
      background: var(--ink);
      color: var(--paper);
      font-size: 12px;
      text-decoration: none;
      transition: background .2s ease, color .2s ease;
    }
    .button:hover { background: var(--red); }
    .text-link {
      font-family: var(--mono);
      font-size: 10px;
      text-decoration-thickness: 1px;
      text-underline-offset: 5px;
      text-transform: uppercase;
    }
    .hero-art {
      position: relative;
      width: min(100%, 500px);
      min-height: 480px;
      justify-self: end;
      overflow: hidden;
      background: var(--blue);
      color: var(--paper);
    }
    .hero-art::before {
      position: absolute;
      top: 48px;
      left: 50%;
      width: 290px;
      height: 290px;
      border: 1px solid rgba(243, 239, 230, .55);
      border-radius: 50%;
      content: "";
      transform: translateX(-50%);
    }
    .hero-art::after {
      position: absolute;
      top: 98px;
      left: 50%;
      width: 190px;
      height: 190px;
      border: 1px solid rgba(243, 239, 230, .48);
      border-radius: 50%;
      content: "";
      transform: translateX(-50%);
    }
    .orbit {
      position: absolute;
      top: 74px;
      left: 50%;
      width: 240px;
      height: 240px;
      border: 1px dashed rgba(243, 239, 230, .5);
      border-radius: 50%;
      transform: translateX(-50%) rotate(-32deg) scaleY(.56);
    }
    .orbit::before, .orbit::after {
      position: absolute;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--acid);
      content: "";
    }
    .orbit::before { top: 32px; left: 26px; }
    .orbit::after { right: 24px; bottom: 30px; }
    .core {
      position: absolute;
      top: 145px;
      left: 50%;
      width: 96px;
      height: 96px;
      display: grid;
      place-items: center;
      border: 1px solid var(--acid);
      border-radius: 50%;
      color: var(--acid);
      font-family: var(--serif);
      font-size: 38px;
      transform: translateX(-50%);
    }
    .art-label {
      position: absolute;
      top: 33px;
      left: 28px;
      color: var(--acid);
    }
    .art-caption {
      position: absolute;
      right: 28px;
      bottom: 28px;
      left: 28px;
      display: flex;
      align-items: end;
      justify-content: space-between;
      border-top: 1px solid rgba(243, 239, 230, .45);
      padding-top: 15px;
    }
    .art-caption strong {
      max-width: 180px;
      font-family: var(--serif);
      font-size: 24px;
      font-weight: 400;
      line-height: 1;
    }
    .art-caption span { color: var(--acid); }
    .intro-strip {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 40px;
      padding: 32px 0;
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
    }
    .intro-strip p {
      max-width: 750px;
      margin: 0;
      font-family: var(--serif);
      font-size: clamp(22px, 3vw, 36px);
      letter-spacing: -.025em;
      line-height: 1.25;
    }
    section.content-section { padding: 105px 0; }
    .section-heading {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 40px;
      margin-bottom: 52px;
    }
    .section-heading h2 {
      max-width: 750px;
      margin: 0;
      font-family: var(--serif);
      font-size: clamp(40px, 6vw, 72px);
      font-weight: 400;
      letter-spacing: -.06em;
      line-height: .98;
    }
    .section-heading p {
      max-width: 500px;
      align-self: end;
      margin: 0;
      color: var(--muted);
      font-size: 14px;
      line-height: 1.7;
    }
    .project-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 18px;
    }
    .project {
      min-height: 340px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 28px;
      border: 1px solid var(--line);
      text-decoration: none;
      transition: border-color .2s ease, transform .2s ease;
    }
    .project:hover {
      border-color: var(--red);
      transform: translateY(-3px);
    }
    .project:first-child {
      grid-row: span 2;
      min-height: 698px;
      background: var(--acid);
      border-color: var(--acid);
    }
    .project-top {
      display: flex;
      justify-content: space-between;
      gap: 16px;
    }
    .number { font-size: 11px; }
    .project h3 {
      max-width: 550px;
      margin: 20px 0 12px;
      font-family: var(--serif);
      font-size: clamp(30px, 4vw, 49px);
      font-weight: 400;
      letter-spacing: -.045em;
      line-height: 1;
    }
    .project p {
      max-width: 530px;
      margin-bottom: 20px;
      color: var(--muted);
      font-size: 13px;
      line-height: 1.65;
    }
    .project:first-child p { color: #484a31; }
    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
      margin-top: 20px;
    }
    .tag {
      border: 1px solid currentColor;
      border-radius: 20px;
      padding: 6px 9px;
      font-size: 9px;
    }
    .project-diagram {
      position: relative;
      min-height: 260px;
      margin: 28px 0 6px;
      display: grid;
      place-items: center;
    }
    .ring {
      position: relative;
      width: 198px;
      height: 198px;
      display: grid;
      place-items: center;
      border: 1px solid rgba(34, 34, 30, .55);
      border-radius: 50%;
    }
    .ring::before, .ring::after {
      position: absolute;
      border: 1px solid rgba(34, 34, 30, .4);
      border-radius: 50%;
      content: "";
    }
    .ring::before { inset: 17px; }
    .ring::after { inset: 40px; }
    .ring-core {
      width: 18px;
      height: 18px;
      border-radius: 50%;
      background: var(--red);
    }
    .ring-caption {
      position: absolute;
      top: 14px;
      right: 0;
      font-family: var(--mono);
      font-size: 9px;
      line-height: 1.7;
      text-transform: uppercase;
    }
    .work-list { border-top: 1px solid var(--line); }
    .work-row {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 40px;
      padding: 26px 0;
      border-bottom: 1px solid var(--line);
    }
    .work-row h3 {
      margin: 0 0 8px;
      font-family: var(--serif);
      font-size: 28px;
      font-weight: 400;
      letter-spacing: -.03em;
    }
    .work-row p {
      max-width: 700px;
      margin: 0;
      color: var(--muted);
      font-size: 13px;
      line-height: 1.7;
    }
    .meta {
      color: var(--muted);
      font-size: 10px;
      line-height: 1.7;
    }
    .two-column {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
    }
    .note-card {
      min-height: 270px;
      padding: 28px;
      border: 1px solid var(--line);
    }
    .note-card.accent { background: var(--red); color: var(--paper); }
    .note-card h3 {
      max-width: 450px;
      margin: 35px 0 13px;
      font-family: var(--serif);
      font-size: clamp(30px, 4vw, 46px);
      font-weight: 400;
      letter-spacing: -.05em;
      line-height: 1;
    }
    .note-card p {
      max-width: 520px;
      margin: 0;
      color: var(--muted);
      font-size: 13px;
      line-height: 1.7;
    }
    .note-card.accent p { color: #f1d7d0; }
    .contact {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 40px;
      align-items: end;
      padding: 65px 0 78px;
      border-top: 1px solid var(--line);
    }
    .contact h2 {
      max-width: 650px;
      margin: 15px 0 0;
      font-family: var(--serif);
      font-size: clamp(48px, 7vw, 86px);
      font-weight: 400;
      letter-spacing: -.065em;
      line-height: .95;
    }
    .contact-links {
      display: flex;
      flex-direction: column;
      gap: 13px;
      align-items: start;
      justify-self: end;
    }
    .contact-links a {
      font-family: var(--mono);
      font-size: 12px;
      text-underline-offset: 5px;
    }
    footer {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      padding: 18px 0 25px;
      border-top: 1px solid var(--line);
      color: var(--muted);
    }
    .footer-note { font-size: 9px; }

    :root {
      --pink: #e55383;
      --deep-pink: #a9325d;
      --soft-pink: #ffe5ed;
      --lilac: #eee4fb;
      --butter: #fff0bf;
      --leaf: #71826a;
    }
    body {
      background:
        radial-gradient(ellipse at 92% 5%, rgba(255, 221, 232, .68), transparent 25rem),
        var(--paper);
    }
    .shell { width: min(1320px, calc(100% - 72px)); }
    .eyebrow { color: var(--deep-pink); }
    .topbar { border-color: var(--line); }
    .wordmark { font-family: var(--sans); font-weight: 700; letter-spacing: .09em; }
    .wordmark span { color: var(--pink); }
    .nav { font-family: var(--sans); font-weight: 700; letter-spacing: .04em; }
    .nav a:hover { color: var(--pink); }
    .hero { min-height: 665px; gap: 5vw; }
    h1 { font-family: var(--sans); font-size: clamp(62px, 8.2vw, 110px); font-weight: 800; letter-spacing: -.085em; line-height: .93; }
    h1 em { color: var(--pink); font-family: var(--serif); font-weight: 400; }
    .hero-intro { color: var(--muted); }
    .button {
      border-radius: 999px;
      background: var(--pink);
      color: white;
      font-weight: 700;
      box-shadow: 0 7px 18px rgba(190, 61, 105, .15);
    }
    .button:hover { background: var(--deep-pink); }
    .text-link { color: var(--deep-pink); }
    .hero-art {
      min-height: 490px;
      border: 1px solid #f4cbd7;
      border-radius: 240px 240px 24px 24px;
      background:
        radial-gradient(ellipse at 48% 42%, #fff8fa 0 23%, transparent 23.5%),
        radial-gradient(ellipse at 48% 44%, #f7b9cd 0 35%, transparent 35.5%),
        linear-gradient(150deg, #ffe9ef, #f4c2d2 72%, #edafc4);
      box-shadow: 0 24px 55px rgba(173, 85, 111, .11);
      color: var(--deep-pink);
    }
    .hero-art::before {
      top: 90px;
      width: 320px;
      height: 330px;
      border: 0;
      border-radius: 48% 52% 45% 55%;
      background: radial-gradient(circle at 48% 44%, rgba(255,255,255,.75), rgba(255,255,255,.22) 69%, transparent 70%);
      transform: translateX(-50%) rotate(-9deg);
    }
    .hero-art::after { display: none; }
    .orbit, .core { display: none; }
    .fashion-illustration {
      position: absolute;
      top: 76px;
      left: 15%;
      width: 70%;
      height: 66%;
      overflow: visible;
      filter: drop-shadow(0 12px 13px rgba(143, 58, 87, .12));
    }
    .art-label { color: var(--deep-pink); }
    .art-caption { border-color: rgba(169, 50, 93, .35); }
    .art-caption strong { font-family: var(--sans); font-size: 22px; font-weight: 700; }
    .art-caption span { color: var(--deep-pink); }
    .intro-strip { border-color: var(--line); }
    .intro-strip p { font-family: var(--sans); font-size: clamp(21px, 2.5vw, 31px); font-weight: 500; letter-spacing: -.04em; }
    section.content-section { padding: 92px 0; }
    .section-heading h2 { font-family: var(--sans); font-weight: 750; letter-spacing: -.065em; }
    .section-heading p { color: var(--muted); }
    .lookbook-grid {
      display: grid;
      grid-template-columns: 1.15fr 1fr 1fr;
      gap: 16px;
    }
    .look-card {
      position: relative;
      min-height: 370px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      overflow: hidden;
      padding: 19px;
      border: 1px solid rgba(169, 50, 93, .13);
      border-radius: 14px;
      color: var(--ink);
      text-decoration: none;
      isolation: isolate;
      transition: transform .2s ease, box-shadow .2s ease;
    }
    .look-card:hover { transform: translateY(-5px) rotate(-.4deg); box-shadow: 0 14px 26px rgba(158, 73, 102, .13); }
    .look-card::before {
      position: absolute;
      z-index: -1;
      inset: 0;
      background: radial-gradient(ellipse at 50% 44%, rgba(255,255,255,.62), transparent 45%);
      content: "";
    }
    .look-card.pink-look { background: linear-gradient(145deg, #f8b8cc, #f7d7df 62%, #fff0e5); }
    .look-card.dresden-look { background: linear-gradient(150deg, #e4def8, #f6dbe6 56%, #fff0d3); }
    .look-card.garba-look { background: linear-gradient(145deg, #e58d80, #f1b29a 52%, #f9d38b); }
    .look-card.saree-look { background: linear-gradient(145deg, #f4c6d3, #f9e6bc 54%, #d9e1cb); }
    .look-card.city-look { background: linear-gradient(155deg, #c9dce0, #eee0df 56%, #f5d2dd); }
    .look-stamp {
      align-self: start;
      border: 1px solid rgba(89, 44, 60, .36);
      border-radius: 999px;
      padding: 7px 10px;
      background: rgba(255, 248, 248, .65);
      color: var(--deep-pink);
      font-family: var(--mono);
      font-size: 9px;
      letter-spacing: .08em;
      text-transform: uppercase;
    }
    .look-doodle {
      position: absolute;
      inset: 68px 22px 68px;
      display: grid;
      place-items: center;
      color: rgba(169, 50, 93, .8);
      font-family: var(--serif);
      font-size: clamp(78px, 10vw, 132px);
      line-height: 1;
      text-shadow: 0 10px 25px rgba(146, 62, 88, .13);
      transform: rotate(-8deg);
    }
    .look-doodle span { position: absolute; font-family: var(--sans); font-size: 26px; }
    .look-doodle span:first-child { top: 8%; right: 12%; }
    .look-doodle span:last-child { bottom: 7%; left: 12%; }
    .look-footer { display: flex; align-items: end; justify-content: space-between; gap: 10px; }
    .look-footer strong { max-width: 220px; font-family: var(--serif); font-size: 25px; font-weight: 400; line-height: 1.05; }
    .look-footer span { color: var(--deep-pink); font-size: 18px; }
    .lookbook-note { margin: 18px 0 0; color: var(--muted); font-size: 12px; line-height: 1.6; }
    .project-grid { gap: 16px; }
    .project {
      border-color: var(--line);
      border-radius: 14px;
      background: rgba(255, 255, 255, .5);
    }
    .project:hover { border-color: var(--pink); }
    .project:first-child {
      background: var(--soft-pink);
      border-color: #f7d5df;
    }
    .project:first-child p { color: #76525e; }
    .project h3 { font-family: var(--sans); font-size: clamp(27px, 3.4vw, 40px); font-weight: 700; letter-spacing: -.055em; }
    .project p, .work-row p, .note-card p { color: var(--muted); }
    .tag { border-radius: 999px; color: var(--deep-pink); }
    .work-list, .work-row { border-color: var(--line); }
    .work-row h3 { font-family: var(--sans); font-size: 22px; font-weight: 700; }
    .note-card { border-color: var(--line); border-radius: 14px; background: rgba(255,255,255,.42); }
    .note-card.accent { background: var(--pink); color: white; }
    .note-card.accent p { color: #fff0f4; }
    .note-card h3 { font-family: var(--sans); font-weight: 700; letter-spacing: -.055em; }
    .contact { border-color: var(--line); }
    .contact h2 { font-family: var(--sans); font-weight: 750; letter-spacing: -.065em; }
    .contact-links a { color: var(--deep-pink); }
    footer { border-color: var(--line); }
    .footer-note { font-family: var(--sans); letter-spacing: .08em; }

    @media (max-width: 760px) {
      .shell { width: min(100% - 36px, 600px); }
      .topbar { min-height: 66px; }
      .nav { gap: 13px; font-size: 9px; }
      .nav a:first-child { display: none; }
      .hero {
        min-height: auto;
        grid-template-columns: 1fr;
        gap: 38px;
        padding: 65px 0;
      }
      h1 { font-size: clamp(61px, 15vw, 100px); }
      .hero-art {
        width: 100%;
        min-height: 360px;
      }
      .hero-art::before { top: 28px; width: 250px; height: 250px; }
      .hero-art::after { top: 68px; width: 170px; height: 170px; }
      .orbit { top: 48px; width: 210px; height: 210px; }
      .core { top: 102px; width: 86px; height: 86px; }
      .intro-strip, .section-heading, .work-row, .contact {
        grid-template-columns: 1fr;
        gap: 18px;
      }
      section.content-section { padding: 74px 0; }
      .section-heading { margin-bottom: 34px; }
      .project-grid, .two-column { grid-template-columns: 1fr; }
      .project:first-child {
        grid-row: auto;
        min-height: 580px;
      }
      .project { min-height: 300px; }
      .contact-links { justify-self: start; }
      .lookbook-grid { grid-template-columns: repeat(2, minmax(0, 1fr)); }
      .look-card { min-height: 300px; }
      .look-card:first-child { grid-row: span 2; min-height: 616px; }
      footer { flex-direction: column; }
    }
    @media (max-width: 480px) {
      .shell { width: calc(100% - 32px); }
      .wordmark { font-size: 9px; }
      .nav { gap: 12px; font-size: 8px; }
      .nav a:nth-child(2) { display: none; }
      .lookbook-grid { grid-template-columns: 1fr; }
      .look-card, .look-card:first-child { grid-row: auto; min-height: 340px; }
    }
    @media (prefers-reduced-motion: reduce) {
      html { scroll-behavior: auto; }
      *, *::before, *::after { transition-duration: .01ms !important; }
    }
  </style>
</head>
<body>
  <header class="shell topbar">
    <a class="wordmark" href="#top">SHRAVANI <span> / </span> STYLE &amp; STEM</a>
    <nav class="nav" aria-label="Main navigation">
      <a href="#style">Style diary</a>
      <a href="#work">The plot twist</a>
      <a href="#contact">Contact ↗</a>
    </nav>
  </header>

  <main id="top">
    <div class="shell hero">
      <div class="hero-copy">
        <div class="eyebrow">Shravani Karad · a little style, a lot of curiosity</div>
        <h1>Outfit<br>repeater.<br><em>Code writer.</em></h1>
        <p class="hero-intro">A pink-loving fashion person with a B.Tech, an M.Sc. in embedded systems, and a soft spot for outfits with a story. Scroll for the wardrobe; stay for the plot twist.</p>
        <div class="hero-links">
          <a class="button" href="#style">Come see the looks <span aria-hidden="true">&nbsp;♡</span></a>
          <a class="text-link" href="#work">Wait, you code?</a>
        </div>
      </div>
      <div class="hero-art" role="img" aria-label="Pink fashion-inspired artwork for Shravani's personal style portfolio">
        <div class="art-label eyebrow">Chemnitz ↔ Mumbai · outfit notes</div>
        <svg class="fashion-illustration" viewBox="0 0 320 360" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <path d="M160 36c0-15 11-25 25-25 11 0 18 7 18 16 0 8-5 13-14 17" stroke="#A9325D" stroke-width="4" stroke-linecap="round"/>
          <path d="M55 78 160 43l105 35-105 31L55 78Z" fill="#FFF7F7" stroke="#A9325D" stroke-width="3" stroke-linejoin="round"/>
          <path d="m102 98 35 16 23-13 23 13 35-16 30 36-33 25 5 153H100l5-153-33-25 30-35Z" fill="#E95C89" stroke="#A9325D" stroke-width="4" stroke-linejoin="round"/>
          <path d="m137 114 23 34 23-34m-46 0 23 34 23-34" stroke="#FFF7F7" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="m104 160 56 18 56-18m-112 60 112 0m-113 60h114" stroke="#FFCDDC" stroke-width="3" stroke-linecap="round"/>
          <path d="M123 189c17 11 57 11 74 0m-72 60c19 12 51 12 70 0" stroke="#A9325D" stroke-width="2" stroke-dasharray="2 8" stroke-linecap="round"/>
          <path d="m77 43 5 12 12 5-12 5-5 12-5-12-12-5 12-5 5-12Zm180 87 4 9 9 4-9 4-4 9-4-9-9-4 9-4 4-9Z" fill="#FFF7F7" stroke="#A9325D" stroke-width="2" stroke-linejoin="round"/>
          <path d="M45 208c0-12 10-22 22-22s22 10 22 22-10 22-22 22-22-10-22-22Z" fill="#FFE7EF" stroke="#D7507A" stroke-width="2"/>
          <path d="M67 194v28m-14-14h28m-24-10 20 20m0-20-20 20" stroke="#D7507A" stroke-width="2" stroke-linecap="round"/>
        </svg>
        <div class="art-caption">
          <strong>Personal style,<br>with a little plot twist.</strong>
          <span class="eyebrow">Style × STEM</span>
        </div>
      </div>
    </div>

    <div class="shell intro-strip">
      <div class="eyebrow">My kind of moodboard</div>
      <p>Pink looks, Indian wear, city walks, and the confidence to bring a little of home wherever I go. Clothes are how I tell the story; curiosity is what happens next.</p>
    </div>

    <section class="shell content-section" id="style">
      <div class="section-heading">
        <div class="eyebrow">01 / The style diary</div>
        <h2>A little desi.<br>A little Dresden.<br>Always me.</h2>
        <p>My Instagram is where the outfits, occasions, and Chemnitz-and-Dresden life live. A few favorite chapters—straight from my own style diary.</p>
      </div>
      <div class="lookbook-grid">
        <a class="look-card pink-look" href="https://www.instagram.com/shravani_karad04/p/DcoApKZDJWM/" target="_blank" rel="noreferrer" aria-label="Open Pink jasmine look on Instagram">
          <span class="look-stamp">The pink edit · 01</span>
          <span class="look-doodle" aria-hidden="true">✿<span>♡</span><span>✧</span></span>
          <span class="look-footer"><strong>Felt like a pink jasmine 🎀</strong><span aria-hidden="true">↗</span></span>
        </a>
        <a class="look-card dresden-look" href="https://www.instagram.com/shravani_karad04/p/Deq8ea9DKo2/" target="_blank" rel="noreferrer" aria-label="Open Dresden diaries on Instagram">
          <span class="look-stamp">Out &amp; about · 02</span>
          <span class="look-doodle" aria-hidden="true">⌂<span>✧</span><span>♡</span></span>
          <span class="look-footer"><strong>Dresden diaries</strong><span aria-hidden="true">↗</span></span>
        </a>
        <a class="look-card garba-look" href="https://www.instagram.com/shravani_karad04/p/DeoMpRLk4w-/" target="_blank" rel="noreferrer" aria-label="Open Garba night look on Instagram">
          <span class="look-stamp">After dark · 03</span>
          <span class="look-doodle" aria-hidden="true">✺<span>✧</span><span>✦</span></span>
          <span class="look-footer"><strong>Garba night, no sleep</strong><span aria-hidden="true">↗</span></span>
        </a>
        <a class="look-card saree-look" href="https://www.instagram.com/shravani_karad04/stories/highlights/17928943562900607/" target="_blank" rel="noreferrer" aria-label="Open Saree highlight on Instagram">
          <span class="look-stamp">A love letter · 04</span>
          <span class="look-doodle" aria-hidden="true">❀<span>♡</span><span>✧</span></span>
          <span class="look-footer"><strong>Saree? Always.</strong><span aria-hidden="true">↗</span></span>
        </a>
        <a class="look-card city-look" href="https://www.instagram.com/shravani_karad04/p/DeukcglE3_c/" target="_blank" rel="noreferrer" aria-label="Open cute Dresden days on Instagram">
          <span class="look-stamp">Little moments · 05</span>
          <span class="look-doodle" aria-hidden="true">☼<span>♡</span><span>✿</span></span>
          <span class="look-footer"><strong>Cute days in Germany</strong><span aria-hidden="true">↗</span></span>
        </a>
      </div>
      <p class="lookbook-note">These are illustrated placeholders for now; tap any card to see the original photo or carousel on Instagram.</p>
    </section>

    <section class="shell content-section" id="work">
      <div class="section-heading">
        <div class="eyebrow">02 / The plot twist</div>
        <h2>Yes, I’m a techie too.</h2>
        <p>Behind the outfit posts: an electronics engineer who writes Python, builds with sensors, and is doing an M.Sc. in Embedded Systems at TU Chemnitz. Fashion tech is where those two sides meet.</p>
      </div>
      <div class="project-grid">
        <article class="project">
          <div>
            <div class="project-top">
              <span class="number">01 / Wearable tech</span>
            </div>
            <div class="project-diagram" role="img" aria-label="Abstract line drawing of a sensor ring">
              <div class="ring"><div class="ring-core"></div></div>
              <div class="ring-caption">IMU / BLE<br>Real-time signal</div>
            </div>
            <h3>RT-Ring<br>Tremor Analysis Device</h3>
            <p>A finger-worn device I helped develop to measure hand tremor in real time. My work spans the 6-axis IMU, miniaturized PCB, Bluetooth Low Energy data streaming, and an app-to-cloud pipeline. Tiny wearable, genuinely useful data.</p>
          </div>
          <div class="tags">
            <span class="tag">Wearables</span>
            <span class="tag">Embedded systems</span>
            <span class="tag">BLE</span>
            <span class="tag">Human-centred design</span>
          </div>
        </article>

        <article class="project">
          <div>
            <div class="project-top">
              <span class="number">02 / Wearable research</span>
            </div>
            <h3>Smart glasses for multimeter applications</h3>
            <p>My 2025 conference publication explores a hands-free, wearable approach to working with multimeter information.</p>
          </div>
          <div class="tags"><span class="tag">Wearable interface</span><span class="tag">Research</span></div>
        </article>

        <article class="project">
          <div>
            <div class="project-top">
              <span class="number">03 / Connected device</span>
            </div>
            <h3>Meter Specs</h3>
            <p>An ESP32-based monitoring system that reads current and voltage, displays measurements on an OLED, and shares data wirelessly between boards using ESP-NOW.</p>
          </div>
          <div class="tags"><span class="tag">ESP32</span><span class="tag">Sensors</span><span class="tag">IoT</span></div>
        </article>
      </div>
    </section>

    <section class="shell content-section" id="about">
      <div class="section-heading">
        <div class="eyebrow">03 / The engineering behind it</div>
        <h2>Engineering, tested beyond the slide deck.</h2>
        <p>Hands-on roles have taught me to move between experiments, electronics, prototypes, and clear communication across a team.</p>
      </div>
      <div class="work-list">
        <article class="work-row">
          <div>
            <h3>Research Engineer</h3>
            <div class="meta">IIT Bombay · Research</div>
          </div>
          <p>Used Python and MATLAB for data analysis, experimental validation, and research. Also modelled a 1 kW PEM fuel-cell system in MATLAB/Simulink using real datasheet parameters.</p>
        </article>
        <article class="work-row">
          <div>
            <h3>Research Engineer</h3>
            <div class="meta">Ksolare Pvt. Ltd. · Solar &amp; power electronics</div>
          </div>
          <p>Worked across inverter PCBs, embedded monitoring and control, EV charger development, hardware testing, and troubleshooting in solar-energy systems.</p>
        </article>
        <article class="work-row">
          <div>
            <h3>M.Sc. Embedded Systems</h3>
            <div class="meta">TU Chemnitz · Germany</div>
          </div>
          <p>Building on a B.Tech in Electronics &amp; Telecommunication Engineering from Sardar Patel Institute of Technology, Mumbai.</p>
        </article>
      </div>
    </section>

    <section class="shell content-section">
      <div class="section-heading">
        <div class="eyebrow">04 / A bit more about me</div>
        <h2>Different worlds.<br>Same attention to detail.</h2>
        <p>Engineering gives me the tools to make things work; style, dance, and people give me ideas for what is worth making.</p>
      </div>
      <div class="two-column">
        <article class="note-card accent">
          <div class="eyebrow">The technical toolkit</div>
          <h3>Python by day. Outfit planning also by day.</h3>
          <p>Python · C · C++ · embedded systems · sensors and IMUs · Bluetooth Low Energy · ESP32 · MATLAB/Simulink · signal processing. Currently studying Embedded Systems at TU Chemnitz after my B.Tech in Electronics &amp; Telecommunication Engineering at S.P.I.T.</p>
        </article>
        <article class="note-card">
          <div class="eyebrow">A practice beyond engineering</div>
          <h3>Bharatanatyam</h3>
          <p>Bharatanatyam has been part of my life since childhood. Years of training in movement, rhythm, expression, and costume give me another way to think about how fashion feels and moves.</p>
        </article>
      </div>
    </section>

    <section class="shell contact" id="contact">
      <div>
        <div class="eyebrow">05 / Say hi</div>
        <h2>Let’s make technology feel more human.</h2>
      </div>
      <div class="contact-links">
        <a href="mailto:snkarad2004@gmail.com">snkarad2004@gmail.com ↗</a>
        <a href="https://www.linkedin.com/in/shravani-karad-136269257/" target="_blank" rel="noreferrer">LinkedIn ↗</a>
        <a href="https://www.instagram.com/shravani_karad04/" target="_blank" rel="noreferrer">Style diary on Instagram ↗</a>
        <span class="meta">Open to fashion-tech, wearable-tech &amp; product internships</span>
      </div>
    </section>
  </main>

  <footer class="shell">
    <span class="footer-note">Shravani Karad · 2026</span>
    <span class="footer-note">Pink on the outside. Python on the inside. ♡</span>
  </footer>
</body>
</html>
