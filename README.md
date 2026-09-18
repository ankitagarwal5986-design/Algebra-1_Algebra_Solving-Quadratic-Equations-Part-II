<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Algebra • Solving Quadratic Equations, Part II: 20-Problem Mastery Suite</title>

  <!-- MathJax Configuration & Loader -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)'], ['$', '$']],
        displayMath: [['\\[', '\\]'], ['$$', '$$']],
        processEscapes: true
      },
      svg: { fontCache: 'global' }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --navy-dark: #0f172a;
      --brand-blue: #2563eb;
      --accent-cyan: #0284c7;
      --bg-tint: #f8fafc;
      --card-surf: #ffffff;
      --border-accent: #93c5fd;
      --border-soft: #cbd5e1;
      --green-ok: #059669;
      --green-surf: #d1fae5;
      --red-fail: #dc2626;
      --red-surf: #fee2e2;
      --brand-gold: #f59e0b;
      --gold-dark: #d97706;
      --gold-surf: #fef3c7;
      --text-main: #0f172a;
      --text-muted: #475569;

      /* High-Contrast Clear Light Yellow Options Palette */
      --opt-yellow-bg: #fefce8;
      --opt-yellow-border: #fef08a;
      --opt-yellow-hover: #fef9c3;
      --opt-yellow-active: #fde047;
      --opt-yellow-text: #713f12;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-tint);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: var(--navy-dark);
      color: #fff;
      padding: 14px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 12px rgba(15, 23, 42, 0.2);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .logo-badge {
      width: 44px;
      height: 44px;
      background: #ffffff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.25);
    }

    .brand-title h1 {
      font-size: 1.15rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .brand-title p {
      font-size: 0.78rem;
      color: #38bdf8;
      font-weight: 500;
    }

    .header-controls {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .chip {
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid rgba(255, 255, 255, 0.25);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.88rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .chip strong {
      color: #ffffff;
      font-weight: 800;
      letter-spacing: 0.3px;
    }

    .btn-icon {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.3);
      color: #fff;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
    }

    nav {
      background: #ffffff;
      border-bottom: 1px solid var(--border-soft);
      display: flex;
      justify-content: center;
      gap: 8px;
      padding: 8px 16px;
      flex-wrap: wrap;
    }

    nav button {
      background: none;
      border: none;
      outline: none;
      padding: 10px 20px;
      font-size: 0.92rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
    }

    nav button.active {
      background: #eff6ff;
      color: var(--brand-blue);
      border-bottom: 3px solid var(--brand-blue);
    }

    main {
      flex: 1;
      padding: 24px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .view {
      display: none;
    }

    .view.active {
      display: block;
    }

    #loginGateView {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(15, 23, 42, 0.94);
      backdrop-filter: blur(6px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .login-box {
      background: #fff;
      padding: 36px;
      border-radius: 16px;
      width: 100%;
      max-width: 480px;
      text-align: center;
      box-shadow: 0 14px 35px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      font-size: 1.45rem;
      color: var(--navy-dark);
      margin-bottom: 6px;
    }

    .login-box p {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 20px;
      line-height: 1.5;
    }

    .resume-alert {
      display: none;
      background: #eff6ff;
      border: 1px solid var(--border-accent);
      border-radius: 8px;
      padding: 10px 14px;
      margin-bottom: 16px;
      font-size: 0.86rem;
      color: var(--navy-dark);
      text-align: left;
    }

    .login-box input {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      font-size: 1rem;
      margin-bottom: 16px;
      outline: none;
    }

    .btn-primary {
      background: var(--brand-blue);
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      width: 100%;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: #1d4ed8;
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 9px 18px;
      font-size: 0.88rem;
      font-weight: 600;
      border-radius: 6px;
      cursor: pointer;
      width: 100%;
      margin-top: 10px;
    }

    .btn-secondary:hover {
      background: var(--bg-tint);
    }

    .sheet-grid {
      display: grid;
      grid-template-columns: 1fr 340px;
      gap: 24px;
    }

    @media (max-width: 990px) {
      .sheet-grid {
        grid-template-columns: 1fr;
      }
    }

    .topic-integrated-banner {
      background: #ffffff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 22px;
      margin-bottom: 22px;
      box-shadow: 0 2px 8px rgba(15, 23, 42, 0.04);
    }

    .topic-integrated-banner h3 {
      color: var(--navy-dark);
      font-size: 1.25rem;
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 8px;
    }

    .paul-notes-container {
      background: #f0fdf4;
      border: 1px solid #bbf7d0;
      border-radius: 10px;
      padding: 16px 18px;
      margin: 14px 0;
    }

    .paul-notes-container h4 {
      color: #166534;
      font-size: 0.98rem;
      display: flex;
      align-items: center;
      gap: 6px;
      margin-bottom: 8px;
    }

    .paul-notes-body {
      font-size: 0.9rem;
      line-height: 1.65;
      color: #14532d;
    }

    .paul-notes-body ul {
      margin-left: 20px;
      margin-top: 6px;
      margin-bottom: 6px;
    }

    .formula-box {
      background: #f8fafc;
      border-left: 4px solid var(--brand-blue);
      border-radius: 0 6px 6px 0;
      padding: 10px 14px;
      margin: 12px 0;
    }

    .question-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 26px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .concept-tag {
      display: inline-block;
      padding: 4px 10px;
      border-radius: 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      margin-bottom: 8px;
      background: #e0f2fe;
      color: #0369a1;
      border: 1px solid #7dd3fc;
    }

    .hint-container {
      margin: 14px 0;
    }

    .btn-hint-toggle {
      background: #fffbeb;
      border: 1px solid #fde68a;
      color: #b45309;
      font-size: 0.86rem;
      font-weight: 600;
      padding: 7px 14px;
      border-radius: 6px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s ease;
    }

    .btn-hint-toggle:hover {
      background: #fef3c7;
      border-color: #f59e0b;
    }

    .hint-box {
      display: none;
      background: #fffbeb;
      border-left: 4px solid #f59e0b;
      border-radius: 0 8px 8px 0;
      padding: 12px 16px;
      margin-top: 8px;
      font-size: 0.9rem;
      color: #92400e;
      line-height: 1.6;
    }

    /* Step Box Structure - Sequential Strict Reveal */
    .step-unit {
      margin-top: 18px;
      padding: 18px;
      background: #f8fafc;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      animation: fadeIn 0.3s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .step-unit.completed {
      border-color: #86efac;
      background: #f0fdf4;
    }

    .step-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
    }

    .step-title {
      font-size: 0.98rem;
      font-weight: 700;
      color: var(--navy-dark);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .step-badge {
      font-size: 0.75rem;
      font-weight: 700;
      padding: 2px 8px;
      border-radius: 10px;
      background: #e2e8f0;
      color: #475569;
    }

    .step-badge.resolved {
      background: #dcfce7;
      color: #166534;
    }

    .mcq-container {
      display: grid;
      grid-template-columns: 1fr;
      gap: 10px;
      margin: 12px 0;
    }

    /* High-Visibility Light Yellow Options with Proper Word Spacing */
    .mcq-option-btn {
      background: var(--opt-yellow-bg);
      border: 2px solid var(--opt-yellow-border);
      border-radius: 10px;
      padding: 13px 18px;
      text-align: left;
      font-size: 0.96rem;
      line-height: 1.5;
      color: var(--opt-yellow-text);
      cursor: pointer;
      transition: all 0.15s ease;
      display: flex;
      align-items: center;
      gap: 14px;
      box-shadow: 0 2px 4px rgba(254, 240, 138, 0.25);
    }

    .mcq-option-btn:hover:not(:disabled) {
      background: var(--opt-yellow-hover);
      border-color: var(--opt-yellow-active);
      transform: translateY(-1px);
    }

    .mcq-option-btn.selected-correct {
      background: var(--green-surf) !important;
      border-color: var(--green-ok) !important;
      color: var(--green-ok) !important;
      font-weight: 700;
      box-shadow: none;
    }

    .mcq-option-btn.selected-wrong {
      background: var(--red-surf) !important;
      border-color: var(--red-fail) !important;
      color: var(--red-fail) !important;
      box-shadow: none;
    }

    .opt-letter {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #ffffff;
      border: 2px solid var(--opt-yellow-active);
      font-weight: 800;
      color: var(--opt-yellow-text);
      flex-shrink: 0;
    }

    .opt-text-content {
      display: inline-block;
      white-space: normal;
      word-spacing: 0.05em;
    }

    .attempts-badge {
      font-size: 0.8rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 12px;
      background: #f1f5f9;
      color: #64748b;
      margin-left: 6px;
    }

    .step-feedback-box {
      margin-top: 12px;
      padding: 12px 14px;
      border-radius: 8px;
      font-size: 0.9rem;
      line-height: 1.6;
      display: block;
      animation: fadeIn 0.25s ease-in;
    }

    .step-feedback-box.correct {
      background: #ecfdf5;
      border-left: 4px solid var(--green-ok);
      color: #065f46;
    }

    .step-feedback-box.incorrect {
      background: #fef2f2;
      border-left: 4px solid var(--red-fail);
      color: #991b1b;
    }

    .btn-reveal-step {
      background: var(--brand-gold);
      color: #fff;
      border: none;
      padding: 6px 12px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.82rem;
      cursor: pointer;
      margin-top: 8px;
    }

    .btn-reveal-step:hover {
      background: var(--gold-dark);
    }

    .svg-container {
      display: flex;
      justify-content: center;
      margin: 16px 0;
      padding: 16px;
      background: var(--bg-tint);
      border-radius: 8px;
      border: 1px solid var(--border-soft);
      overflow-x: auto;
    }

    .nav-toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid var(--border-soft);
    }

    .nav-btn-group {
      display: flex;
      gap: 10px;
    }

    .btn-nav-action {
      background: #f8fafc;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 8px 18px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s;
    }

    .btn-nav-action:hover:not(:disabled) {
      background: var(--bg-tint);
      border-color: var(--brand-blue);
    }

    .btn-nav-action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    .btn-skip {
      border-color: var(--brand-gold);
      color: var(--gold-dark);
      background: var(--gold-surf);
    }

    .btn-skip:hover {
      background: #fde68a;
    }

    .palette-box {
      background: #fff;
      border: 1px solid var(--border-soft);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 20px;
    }

    .palette-filters {
      display: flex;
      gap: 6px;
      margin-bottom: 12px;
      flex-wrap: wrap;
    }

    .btn-filter {
      flex: 1 1 45%;
      padding: 6px 4px;
      font-size: 0.78rem;
      font-weight: 700;
      border: 1px solid var(--border-soft);
      background: #f8fafc;
      border-radius: 6px;
      cursor: pointer;
      color: var(--text-muted);
    }

    .btn-filter.active {
      background: var(--brand-blue);
      color: #fff;
      border-color: var(--brand-blue);
    }

    .palette-legend {
      display: flex;
      justify-content: space-between;
      font-size: 0.72rem;
      margin: 8px 0 12px 0;
      padding: 6px 8px;
      background: var(--bg-tint);
      border-radius: 6px;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 4px;
      font-weight: 600;
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }

    .palette-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 6px;
      margin-bottom: 12px;
      max-height: 380px;
      overflow-y: auto;
      padding-right: 4px;
    }

    .palette-btn {
      aspect-ratio: 1;
      border: 1px solid var(--border-soft);
      background: var(--bg-tint);
      border-radius: 6px;
      font-weight: 700;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      transition: all 0.15s;
      font-size: 0.82rem;
      color: var(--navy-dark);
    }

    .palette-btn.active {
      border: 2px solid var(--navy-dark) !important;
      background: #bfdbfe;
      color: #1e3a8a;
    }

    .palette-btn.completed {
      background: var(--green-ok) !important;
      color: #fff !important;
      border-color: var(--green-ok) !important;
    }

    .palette-btn.partial {
      background: var(--brand-gold) !important;
      color: #fff !important;
      border-color: var(--gold-dark) !important;
    }

    .theory-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      margin-bottom: 24px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    }

    .theory-card h3 {
      color: var(--navy-dark);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 1.25rem;
    }

    .compendium-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      margin: 16px 0;
    }

    .comp-card {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      box-shadow: 0 2px 6px rgba(15, 23, 42, 0.04);
    }

    .comp-card h4 {
      color: var(--navy-dark);
      border-bottom: 2px solid var(--border-soft);
      padding-bottom: 8px;
      margin-bottom: 12px;
      font-size: 1.05rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .recap-body {
      font-size: 0.92rem;
      line-height: 1.65;
      color: var(--text-main);
    }

    .hero-score-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 28px;
      text-align: center;
      margin-bottom: 24px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.03);
    }

    .student-badge {
      display: inline-block;
      background: var(--bg-tint);
      border: 1px solid var(--border-accent);
      padding: 6px 18px;
      border-radius: 20px;
      font-size: 1rem;
      margin-bottom: 14px;
      color: var(--navy-dark);
    }

    .student-badge strong {
      color: var(--brand-blue);
    }

    .score-badge {
      font-size: 3rem;
      font-weight: 800;
      color: var(--brand-blue);
      margin: 8px 0;
    }

    .progress-bar-wrap {
      width: 100%;
      height: 12px;
      background: #e2e8f0;
      border-radius: 6px;
      overflow: hidden;
      margin: 16px 0;
    }

    .progress-bar-fill {
      height: 100%;
      background: var(--green-ok);
      width: 0%;
      transition: width 0.3s ease;
    }

    .toast {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      display: none;
      z-index: 1000;
    }

    @media print {
      header, nav, .palette-box, .btn-primary, #loginGateView, .nav-toolbar, .btn-hint-toggle {
        display: none !important;
      }
      body { background: #fff; }
      main { width: 100%; max-width: 100%; padding: 0; }
      .sheet-grid { display: block; }
      .view { display: block !important; }
    }
  </style>
</head>
<body>

  <header>
    <div class="brand-wrap">
      <div class="logo-badge">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none">
          <circle cx="50" cy="50" r="44" stroke="#2563eb" stroke-width="7"/>
          <path d="M 28 65 Q 50 15 72 65" stroke="#0284c7" stroke-width="6" fill="none"/>
          <circle cx="50" cy="40" r="5" fill="#f59e0b"/>
        </svg>
      </div>
      <div class="brand-title">
        <h1>Algebra • Solving Quadratic Equations, Part II</h1>
        <p>Completing the Square &amp; Quadratic Formula • Lamar University 20-Problem Master Suite</p>
      </div>
    </div>
    <div class="header-controls">
      <div class="chip" id="timerChip">⏱️ 00:00</div>
      <div class="chip" id="userPill"><strong>Student: Guest</strong></div>
      <button class="btn-icon" id="audioToggleBtn" title="Toggle Audio">🔊</button>
    </div>
  </header>

  <nav>
    <button class="tab-btn active" id="tabPracticeBtn" onclick="switchMainTab('practice')">
      🎯 Interactive Practice Workstation (20 Problems)
    </button>
    <button class="tab-btn" id="tabTheoryBtn" onclick="switchMainTab('theory')">
      📖 Completing the Square &amp; Quadratic Formula Compendium
    </button>
    <button class="tab-btn" id="tabScorecardBtn" onclick="switchMainTab('scorecard')">
      📊 Master Scorecard &amp; Solutions
    </button>
  </nav>

  <!-- Login Modal with Session Persistence -->
  <div id="loginGateView">
    <div class="login-box">
      <h2>Quadratic Equations II Practice Portal</h2>
      <p>Algebra • Completing the Square, Discriminant Analysis &amp; The Quadratic Formula</p>
      
      <div id="resumeAlertBox" class="resume-alert">
        <strong>Saved Session Found!</strong><br>
        <span id="savedSessionDetails"></span>
      </div>

      <input type="text" id="studentNameInput" placeholder="Enter Student Name" />
      <button class="btn-primary" id="startSessionBtn" onclick="initDirectLogin(false)">Start Learning Session</button>
      <button class="btn-secondary" id="resumeSessionBtn" style="display:none;" onclick="initDirectLogin(true)">Resume Saved Session</button>
    </div>
  </div>

  <main>
    <!-- View 1: Unified Interactive Learning Stream -->
    <div id="viewPractice" class="view active">
      <div class="sheet-grid">
        <div>
          <!-- Unified Header Card: Synchronized Notes directly above active problem -->
          <div class="topic-integrated-banner" id="topicBannerContainer"></div>

          <!-- Question Workstation Card -->
          <div class="question-card" id="activeQuestionCard"></div>
        </div>

        <aside>
          <div class="palette-box">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px;">
              <h4 id="paletteHeaderTitle">All 20 Problems</h4>
              <span style="font-size:0.8rem; color:var(--text-muted);" id="paletteCount">0 / 20 Solved</span>
            </div>

            <div class="palette-filters">
              <button class="btn-filter active" id="filterAllBtn" onclick="filterPalette('all')">All (20)</button>
              <button class="btn-filter" id="filterP1Btn" onclick="filterPalette('p1')">Practice (8)</button>
              <button class="btn-filter" id="filterP2Btn" onclick="filterPalette('p2')">Assign (8)</button>
              <button class="btn-filter" id="filterTutBtn" onclick="filterPalette('tut')">Tutorial (4)</button>
            </div>

            <div class="palette-legend">
              <div class="legend-item"><span class="legend-dot" style="background:var(--green-ok);"></span> Completed</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f59e0b;"></span> In Progress</div>
              <div class="legend-item"><span class="legend-dot" style="background:#bfdbfe;"></span> Active</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f0f9ff; border:1px solid #bae6fd;"></span> Unseen</div>
            </div>
            
            <div class="palette-grid" id="paletteGrid"></div>
            
            <button class="btn-primary" style="margin-top: 10px; background: var(--navy-dark);" onclick="switchMainTab('scorecard')">
              📊 View Evaluation Scorecard
            </button>
            <button class="btn-secondary" style="margin-top: 8px; border-color: #cbd5e1;" onclick="resetStudentProgress()">
              🔄 Reset All Progress
            </button>
          </div>

          <div class="palette-box" style="background: #f8fafc;">
            <h4 style="font-size: 0.92rem; margin-bottom: 8px; color: var(--navy-dark);">Strict Step-Gating Rules</h4>
            <p style="font-size: 0.82rem; line-height: 1.6; color: var(--text-muted);">
              • <strong>Sequential Lock:</strong> Step 2 remains completely hidden until Step 1 is verified.<br/>
              • <strong>Proper Word Spacing:</strong> Standard text is separated cleanly from LaTeX math symbols.<br/>
              • <strong>Balanced Options:</strong> Correct answers are distributed across (A), (B), (C), and (D).<br/>
              • Click <strong>💡 Need a Hint?</strong> to reveal tailored calculation hints.<br/>
              • You get <strong>2 attempts</strong> per step. If unresolved after 2 attempts, the <strong>Reveal Step Solution</strong> button unlocks.
            </p>
          </div>
        </aside>
      </div>
    </div>

    <!-- View 2: Compendium Guide -->
    <div id="viewTheory" class="view">
      <div class="theory-card">
        <h3>📐 Paul's Online Notes: Solving Quadratic Equations, Part II Compendium</h3>
        <p class="theory-intro-text">
          When a quadratic equation cannot be easily factored, or when finding exact radical and complex roots is required, two universal methods exist: <strong>Completing the Square</strong> and the <strong>Quadratic Formula</strong>.
        </p>

        <div class="compendium-grid">
          <div class="comp-card">
            <h4>1. Completing the Square Method</h4>
            <div class="recap-body">
              <p>Transforms any quadratic equation into a binomial square:</p>
              <div class="formula-box">
                \[x^2 + bx = -c \implies x^2 + bx + \left(\frac{b}{2}\right)^2 = -c + \left(\frac{b}{2}\right)^2\]
                \[\left(x + \frac{b}{2}\right)^2 = \frac{b^2 - 4c}{4} \implies x + \frac{b}{2} = \pm\sqrt{\frac{b^2 - 4c}{4}}\]
                <p>If \(a \ne 1\), always divide the entire equation by \(a\) before computing \(\left(\frac{b}{2a}\right)^2\).</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>2. The Quadratic Formula</h4>
            <div class="recap-body">
              <p>For any quadratic equation in standard form \(ax^2 + bx + c = 0\):</p>
              <div class="formula-box">
                \[x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\]
                <p><strong>Common Pitfall:</strong> The fraction bar must extend under the entire numerator, including \(-b\).</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>3. The Discriminant (\(D = b^2 - 4ac\))</h4>
            <div class="recap-body">
              <p>The radicand \(b^2 - 4ac\) determines the nature of the roots:</p>
              <div class="formula-box">
                <p>• \(D > 0\): Two distinct real roots.</p>
                <p>• \(D = 0\): Exactly one repeated real root.</p>
                <p>• \(D < 0\): Two complex conjugate roots (\(u \pm vi\)).</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- View 3: Complete Scorecard & Master Solutions -->
    <div id="viewScorecard" class="view">
      <div class="hero-score-card">
        <h2>Quadratic Equations Part II Diagnostic Scorecard</h2>
        <div class="student-badge" id="reportStudentBadge"><strong>Student: Guest</strong></div>
        <div class="score-badge" id="scoreValue">0 / 20</div>
        <div class="progress-bar-wrap">
          <div class="progress-bar-fill" id="progressBarFill"></div>
        </div>
        <p id="scoreSubtitle" style="font-size:1.02rem; font-weight:600; color:var(--navy-dark); margin-top:8px;">
          Review all 20 problem solutions, step evaluations, and derivations below.
        </p>
        <button class="btn-primary" style="margin-top: 14px; max-width: 240px;" onclick="window.print()">🖨️ Print Final Scorecard</button>
      </div>

      <div id="completeSolutionsContainer"></div>
    </div>
  </main>

  <div class="toast" id="toastMessage"></div>

  <script>
    /* ==========================================================================
       COMPLETE 20-PROBLEM DATASET (8 PRACTICE + 8 ASSIGNMENT + 4 TUTORIAL)
       Every option contains proper text & math delimiters for clean readability.
       ========================================================================== */
    const PROBLEMS_DATA = [
      // ---------- PART 1: PRACTICE PROBLEMS (1 TO 8) ----------
      {
        id: 1,
        set: "p1",
        setName: "Practice Problems",
        title: "Completing the Square: Monic Real Radical",
        prompt: "Solve the equation by completing the square: \\[x^2 - 8x + 9 = 0\\]",
        hint: "Isolate constants: \\(x^2 - 8x = -9\\). Add \\((-8/2)^2 = (-4)^2 = 16\\) to both sides.",
        svg: `<svg width="100%" height="180" viewBox="0 0 360 160" style="max-width:360px;">
          <rect width="360" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <line x1="20" y1="100" x2="340" y2="100" stroke="#64748b" stroke-width="1.5"/>
          <line x1="80" y1="15" x2="80" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <path d="M 60,20 Q 180,160 300,20" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="120" cy="100" r="4.5" fill="#059669"/>
          <text x="95" y="120" font-size="10" font-weight="bold" fill="#059669">4 − √7</text>
          <circle cx="240" cy="100" r="4.5" fill="#059669"/>
          <text x="230" y="120" font-size="10" font-weight="bold" fill="#059669">4 + √7</text>
          <circle cx="180" cy="135" r="4" fill="#0284c7"/>
          <text x="165" y="150" font-size="9" fill="#0284c7">Vertex: (4, −7)</text>
        </svg>`,
        steps: [
          {
            title: "Step 1: Isolate Constants and Complete the Square",
            prompt: "What is added to both sides to complete the square?",
            options: [
              { label: "A", text: "Add 64 to both sides of the equation" },
              { label: "B", text: "Add 16 to both sides, resulting in \\((x - 4)^2 = 7\\)" },
              { label: "C", text: "Add 8 to both sides, resulting in \\((x - 4)^2 = 17\\)" },
              { label: "D", text: "Add 4 to both sides, resulting in \\((x - 2)^2 = 7\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x^2 - 8x = -9\\). Add \\((-4)^2 = 16\\): \\(x^2 - 8x + 16 = -9 + 16 \\implies (x - 4)^2 = 7\\)."
          },
          {
            title: "Step 2: Apply Square Root Property and Solve",
            prompt: "Solve \\((x - 4)^2 = 7\\) for \\(x\\).",
            options: [
              { label: "A", text: "\\(x = -4 \\pm \\sqrt{7}\\)" },
              { label: "B", text: "\\(x = 4 \\pm 7\\)" },
              { label: "C", text: "\\(x = \\pm \\sqrt{7}\\)" },
              { label: "D", text: "\\(x = 4 \\pm \\sqrt{7}\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x - 4 = \\pm\\sqrt{7} \\implies x = 4 \\pm \\sqrt{7}\\)."
          }
        ]
      },
      {
        id: 2,
        set: "p1",
        setName: "Practice Problems",
        title: "Completing the Square: Monic Complex Roots",
        prompt: "Solve the equation by completing the square: \\[x^2 + 10x + 26 = 0\\]",
        hint: "Subtract 26 to the right. Add \\((10/2)^2 = 25\\) to both sides. Notice that \\(-26 + 25 = -1\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Form the Perfect Square Trinomial",
            prompt: "What equation results from adding 25 to both sides?",
            options: [
              { label: "A", text: "\\((x + 5)^2 = 1\\)" },
              { label: "B", text: "\\((x + 10)^2 = -1\\)" },
              { label: "C", text: "\\((x + 5)^2 = -1\\)" },
              { label: "D", text: "\\((x - 5)^2 = -1\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x^2 + 10x = -26\\). Add 25: \\(x^2 + 10x + 25 = -26 + 25 \\implies (x + 5)^2 = -1\\)."
          },
          {
            title: "Step 2: Solve with Imaginary Unit",
            prompt: "Solve \\((x + 5)^2 = -1\\) for \\(x\\).",
            options: [
              { label: "A", text: "\\(x = -5 \\pm i\\)" },
              { label: "B", text: "\\(x = 5 \\pm i\\)" },
              { label: "C", text: "\\(x = -5 \\pm 1\\)" },
              { label: "D", text: "\\(x = -10 \\pm i\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x + 5 = \\pm\\sqrt{-1} = \\pm i \\implies x = -5 \\pm i\\)."
          }
        ]
      },
      {
        id: 3,
        set: "p1",
        setName: "Practice Problems",
        title: "Completing the Square: Non-Monic Real Fraction",
        prompt: "Solve the equation by completing the square: \\[2x^2 + 5x - 4 = 0\\]",
        hint: "Divide by 2 first: \\(x^2 + \\frac{5}{2}x = 2\\). Half of \\(5/2\\) is \\(5/4\\); square it to get \\(25/16\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Divide by 2 and Complete Square",
            prompt: "What is the resulting equation after adding \\((5/4)^2 = 25/16\\) to both sides?",
            options: [
              { label: "A", text: "\\(\\left(x + \\frac{5}{2}\\right)^2 = \\frac{57}{16}\\)" },
              { label: "B", text: "\\(\\left(x + \\frac{5}{4}\\right)^2 = \\frac{33}{16}\\)" },
              { label: "C", text: "\\(\\left(x + \\frac{5}{4}\\right)^2 = \\frac{57}{16}\\)" },
              { label: "D", text: "\\(\\left(x - \\frac{5}{4}\\right)^2 = \\frac{57}{16}\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x^2 + \\frac{5}{2}x = 2\\). Add \\(\\frac{25}{16}\\): \\(2 + \\frac{25}{16} = \\frac{32 + 25}{16} = \\frac{57}{16} \\implies \\left(x + \\frac{5}{4}\\right)^2 = \\frac{57}{16}\\)."
          },
          {
            title: "Step 2: Solve for x",
            prompt: "Isolate \\(x\\) and express the exact roots.",
            options: [
              { label: "A", text: "\\(x = \\frac{5 \\pm \\sqrt{57}}{4}\\)" },
              { label: "B", text: "\\(x = \\frac{-5 \\pm \\sqrt{57}}{4}\\)" },
              { label: "C", text: "\\(x = -5 \\pm \\sqrt{57}\\)" },
              { label: "D", text: "\\(x = \\frac{-5 \\pm \\sqrt{33}}{4}\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x + \\frac{5}{4} = \\pm\\frac{\\sqrt{57}}{4} \\implies x = \\frac{-5 \\pm \\sqrt{57}}{4}\\)."
          }
        ]
      },
      {
        id: 4,
        set: "p1",
        setName: "Practice Problems",
        title: "Completing the Square: Radical Fraction Reduction",
        prompt: "Solve the equation by completing the square: \\[3x^2 - 6x + 1 = 0\\]",
        hint: "Divide by 3: \\(x^2 - 2x = -1/3\\). Add \\((-1)^2 = 1\\) to both sides: \\(-1/3 + 1 = 2/3\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Complete the Square",
            prompt: "What is the equation after completing the square?",
            options: [
              { label: "A", text: "\\((x - 1)^2 = \\frac{2}{3}\\)" },
              { label: "B", text: "\\((x - 2)^2 = \\frac{2}{3}\\)" },
              { label: "C", text: "\\((x - 1)^2 = -\\frac{1}{3}\\)" },
              { label: "D", text: "\\((x + 1)^2 = \\frac{4}{3}\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x^2 - 2x = -\\frac{1}{3}\\). Add 1: \\(x^2 - 2x + 1 = -\\frac{1}{3} + 1 = \\frac{2}{3} \\implies (x - 1)^2 = \\frac{2}{3}\\)."
          },
          {
            title: "Step 2: Rationalize and Solve for x",
            prompt: "Solve \\(x - 1 = \\pm\\sqrt{2/3}\\).",
            options: [
              { label: "A", text: "\\(x = 1 \\pm \\sqrt{6}\\)" },
              { label: "B", text: "\\(x = \\frac{1 \\pm \\sqrt{6}}{3}\\)" },
              { label: "C", text: "\\(x = \\frac{3 \\pm \\sqrt{6}}{3} \\quad \\text{or} \\quad 1 \\pm \\frac{\\sqrt{6}}{3}\\)" },
              { label: "D", text: "\\(x = 3 \\pm \\sqrt{2}\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x - 1 = \\pm\\frac{\\sqrt{2}}{\\sqrt{3}} = \\pm\\frac{\\sqrt{6}}{3} \\implies x = 1 \\pm \\frac{\\sqrt{6}}{3} = \\frac{3 \\pm \\sqrt{6}}{3}\\)."
          }
        ]
      },
      {
        id: 5,
        set: "p1",
        setName: "Practice Problems",
        title: "Quadratic Formula: Simplifiable Radical",
        prompt: "Use the quadratic formula to solve: \\[x^2 + 4x - 8 = 0\\]",
        hint: "Identify \\(a = 1, b = 4, c = -8\\). The discriminant is \\(b^2 - 4ac = 16 - 4(1)(-8) = 48\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute the Discriminant",
            prompt: "What is the value of \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(-16\\)" },
              { label: "B", text: "\\(48\\)" },
              { label: "C", text: "\\(32\\)" },
              { label: "D", text: "\\(24\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(b^2 - 4ac = 4^2 - 4(1)(-8) = 16 + 32 = 48\\)."
          },
          {
            title: "Step 2: Evaluate and Simplify the Formula",
            prompt: "Simplify \\(x = \\frac{-4 \\pm \\sqrt{48}}{2}\\).",
            options: [
              { label: "A", text: "\\(x = -2 \\pm 2\\sqrt{3}\\)" },
              { label: "B", text: "\\(x = -4 \\pm 4\\sqrt{3}\\)" },
              { label: "C", text: "\\(x = -2 \\pm 4\\sqrt{3}\\)" },
              { label: "D", text: "\\(x = -2 \\pm \\sqrt{12}\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(\\sqrt{48} = 4\\sqrt{3}\\). Thus \\(x = \\frac{-4 \\pm 4\\sqrt{3}}{2} = -2 \\pm 2\\sqrt{3}\\)."
          }
        ]
      },
      {
        id: 6,
        set: "p1",
        setName: "Practice Problems",
        title: "Quadratic Formula: Rational Roots",
        prompt: "Use the quadratic formula to solve: \\[2x^2 - 7x + 3 = 0\\]",
        hint: "Calculate \\(b^2 - 4ac = (-7)^2 - 4(2)(3) = 49 - 24 = 25\\). Since 25 is a perfect square, solutions will be rational.",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute the Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(73\\)" },
              { label: "B", text: "\\(-25\\)" },
              { label: "C", text: "\\(25\\)" },
              { label: "D", text: "\\(1\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\((-7)^2 - 4(2)(3) = 49 - 24 = 25\\)."
          },
          {
            title: "Step 2: Evaluate Roots",
            prompt: "Compute \\(x = \\frac{7 \\pm 5}{4}\\).",
            options: [
              { label: "A", text: "\\(x = 6 \\quad \\text{and} \\quad x = 1\\)" },
              { label: "B", text: "\\(x = -3 \\quad \\text{and} \\quad x = -1/2\\)" },
              { label: "C", text: "\\(x = 3 \\quad \\text{and} \\quad x = 1/2\\)" },
              { label: "D", text: "\\(x = 4 \\quad \\text{and} \\quad x = 2\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x = \\frac{7 + 5}{4} = 3\\) and \\(x = \\frac{7 - 5}{4} = \\frac{2}{4} = \\frac{1}{2}\\)."
          }
        ]
      },
      {
        id: 7,
        set: "p1",
        setName: "Practice Problems",
        title: "Quadratic Formula: Negative Discriminant",
        prompt: "Use the quadratic formula to solve: \\[x^2 - 6x + 13 = 0\\]",
        hint: "Discriminant is \\((-6)^2 - 4(1)(13) = 36 - 52 = -16\\). Express \\(\\sqrt{-16} = 4i\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute the Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(-16\\)" },
              { label: "B", text: "\\(16\\)" },
              { label: "C", text: "\\(-88\\)" },
              { label: "D", text: "\\(88\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\((-6)^2 - 4(1)(13) = 36 - 52 = -16\\)."
          },
          {
            title: "Step 2: State the Complex Solutions",
            prompt: "Evaluate \\(x = \\frac{6 \\pm 4i}{2}\\).",
            options: [
              { label: "A", text: "\\(x = 3 \\pm 4i\\)" },
              { label: "B", text: "\\(x = 3 \\pm 2i\\)" },
              { label: "C", text: "\\(x = 6 \\pm 2i\\)" },
              { label: "D", text: "\\(x = -3 \\pm 2i\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x = \\frac{6 \\pm 4i}{2} = 3 \\pm 2i\\)."
          }
        ]
      },
      {
        id: 8,
        set: "p1",
        setName: "Practice Problems",
        title: "Quadratic Formula: Zero Discriminant (Repeated Root)",
        prompt: "Use the quadratic formula to solve: \\[9x^2 + 12x + 4 = 0\\]",
        hint: "Calculate \\(b^2 - 4ac = 12^2 - 4(9)(4) = 144 - 144 = 0\\). A zero discriminant yields one repeated rational root.",
        svg: `<svg width="100%" height="180" viewBox="0 0 360 160" style="max-width:360px;">
          <rect width="360" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <line x1="20" y1="120" x2="340" y2="120" stroke="#64748b" stroke-width="1.5"/>
          <line x1="180" y1="15" x2="180" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <path d="M 60,20 Q 140,120 220,20" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="140" cy="120" r="5" fill="#059669"/>
          <text x="100" y="140" font-size="10" font-weight="bold" fill="#059669">Tangent Root: x = −2/3</text>
          <text x="210" y="70" font-size="10" font-weight="bold" fill="#0284c7">D = 0 (Repeated)</text>
        </svg>`,
        steps: [
          {
            title: "Step 1: Compute the Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(288\\)" },
              { label: "B", text: "\\(72\\)" },
              { label: "C", text: "\\(0\\)" },
              { label: "D", text: "\\(-144\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(12^2 - 4(9)(4) = 144 - 144 = 0\\)."
          },
          {
            title: "Step 2: Find the Single Repeated Solution",
            prompt: "Evaluate \\(x = \\frac{-12 \\pm 0}{18}\\).",
            options: [
              { label: "A", text: "\\(x = -3/2\\)" },
              { label: "B", text: "\\(x = 2/3\\)" },
              { label: "C", text: "\\(x = -4/3\\)" },
              { label: "D", text: "\\(x = -2/3\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x = \\frac{-12}{18} = -\\frac{2}{3}\\)."
          }
        ]
      },

      // ---------- PART 2: ASSIGNMENT PROBLEMS (9 TO 16) ----------
      {
        id: 9,
        set: "p2",
        setName: "Assignment Problems",
        title: "Completing the Square: Radical Simplification",
        prompt: "Solve the equation by completing the square: \\[x^2 - 6x - 3 = 0\\]",
        hint: "Isolate: \\(x^2 - 6x = 3\\). Add \\((-3)^2 = 9\\) to both sides.",
        svg: null,
        steps: [
          {
            title: "Step 1: Complete the Square",
            prompt: "What is the factored square equation?",
            options: [
              { label: "A", text: "\\((x - 3)^2 = 6\\)" },
              { label: "B", text: "\\((x - 3)^2 = 12\\)" },
              { label: "C", text: "\\((x + 3)^2 = 12\\)" },
              { label: "D", text: "\\((x - 6)^2 = 39\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x^2 - 6x = 3\\). Add 9: \\(x^2 - 6x + 9 = 3 + 9 \\implies (x - 3)^2 = 12\\)."
          },
          {
            title: "Step 2: Solve and Simplify Radical",
            prompt: "Solve \\((x - 3)^2 = 12\\).",
            options: [
              { label: "A", text: "\\(x = 3 \\pm 2\\sqrt{3}\\)" },
              { label: "B", text: "\\(x = -3 \\pm 2\\sqrt{3}\\)" },
              { label: "C", text: "\\(x = 3 \\pm 3\\sqrt{2}\\)" },
              { label: "D", text: "\\(x = 3 \\pm \\sqrt{12}\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x - 3 = \\pm\\sqrt{12} = \\pm 2\\sqrt{3} \\implies x = 3 \\pm 2\\sqrt{3}\\)."
          }
        ]
      },
      {
        id: 10,
        set: "p2",
        setName: "Assignment Problems",
        title: "Completing the Square: Pure Imaginary Component",
        prompt: "Solve the equation by completing the square: \\[x^2 + 8x + 25 = 0\\]",
        hint: "Isolate: \\(x^2 + 8x = -25\\). Add \\(4^2 = 16\\) to both sides.",
        svg: null,
        steps: [
          {
            title: "Step 1: Complete the Square",
            prompt: "What is the resulting equation?",
            options: [
              { label: "A", text: "\\((x + 4)^2 = 9\\)" },
              { label: "B", text: "\\((x + 8)^2 = -9\\)" },
              { label: "C", text: "\\((x + 4)^2 = -9\\)" },
              { label: "D", text: "\\((x - 4)^2 = -9\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x^2 + 8x = -25\\). Add 16: \\(x^2 + 8x + 16 = -25 + 16 \\implies (x + 4)^2 = -9\\)."
          },
          {
            title: "Step 2: Solve for x",
            prompt: "State the complex roots.",
            options: [
              { label: "A", text: "\\(x = 4 \\pm 3i\\)" },
              { label: "B", text: "\\(x = -4 \\pm 3i\\)" },
              { label: "C", text: "\\(x = -4 \\pm 9i\\)" },
              { label: "D", text: "\\(x = -4 \\pm 3\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x + 4 = \\pm\\sqrt{-9} = \\pm 3i \\implies x = -4 \\pm 3i\\)."
          }
        ]
      },
      {
        id: 11,
        set: "p2",
        setName: "Assignment Problems",
        title: "Completing the Square: Fractional Linear Coefficient",
        prompt: "Solve the equation by completing the square: \\[2x^2 + 7x - 2 = 0\\]",
        hint: "Divide by 2: \\(x^2 + \\frac{7}{2}x = 1\\). Half of \\(7/2\\) is \\(7/4\\); square is \\(49/16\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Complete the Square",
            prompt: "What is the equation after adding \\(49/16\\) to both sides?",
            options: [
              { label: "A", text: "\\(\\left(x + \\frac{7}{2}\\right)^2 = \\frac{65}{16}\\)" },
              { label: "B", text: "\\(\\left(x + \\frac{7}{4}\\right)^2 = \\frac{33}{16}\\)" },
              { label: "C", text: "\\(\\left(x - \\frac{7}{4}\\right)^2 = \\frac{65}{16}\\)" },
              { label: "D", text: "\\(\\left(x + \\frac{7}{4}\\right)^2 = \\frac{65}{16}\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x^2 + \\frac{7}{2}x = 1\\). Add \\(\\frac{49}{16}\\): \\(1 + \\frac{49}{16} = \\frac{65}{16} \\implies \\left(x + \\frac{7}{4}\\right)^2 = \\frac{65}{16}\\)."
          },
          {
            title: "Step 2: State Solutions",
            prompt: "Isolate \\(x\\).",
            options: [
              { label: "A", text: "\\(x = \\frac{-7 \\pm \\sqrt{65}}{4}\\)" },
              { label: "B", text: "\\(x = \\frac{7 \\pm \\sqrt{65}}{4}\\)" },
              { label: "C", text: "\\(x = -7 \\pm \\sqrt{65}\\)" },
              { label: "D", text: "\\(x = \\frac{-7 \\pm \\sqrt{65}}{2}\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x + \\frac{7}{4} = \\pm\\frac{\\sqrt{65}}{4} \\implies x = \\frac{-7 \\pm \\sqrt{65}}{4}\\)."
          }
        ]
      },
      {
        id: 12,
        set: "p2",
        setName: "Assignment Problems",
        title: "Completing the Square: Higher Leading Coefficient",
        prompt: "Solve the equation by completing the square: \\[4x^2 - 8x + 1 = 0\\]",
        hint: "Divide by 4: \\(x^2 - 2x = -1/4\\). Add \\((-1)^2 = 1\\) to both sides: \\(-1/4 + 1 = 3/4\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Complete the Square",
            prompt: "What is the resulting equation?",
            options: [
              { label: "A", text: "\\((x - 2)^2 = \\frac{3}{4}\\)" },
              { label: "B", text: "\\((x - 1)^2 = \\frac{3}{4}\\)" },
              { label: "C", text: "\\((x - 1)^2 = \\frac{5}{4}\\)" },
              { label: "D", text: "\\((x + 1)^2 = \\frac{3}{4}\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x^2 - 2x = -\\frac{1}{4}\\). Add 1: \\(x^2 - 2x + 1 = -\\frac{1}{4} + 1 = \\frac{3}{4} \\implies (x - 1)^2 = \\frac{3}{4}\\)."
          },
          {
            title: "Step 2: Solve for x",
            prompt: "Isolate \\(x\\).",
            options: [
              { label: "A", text: "\\(x = 1 \\pm \\sqrt{3}\\)" },
              { label: "B", text: "\\(x = \\frac{1 \\pm \\sqrt{3}}{2}\\)" },
              { label: "C", text: "\\(x = 2 \\pm \\sqrt{3}\\)" },
              { label: "D", text: "\\(x = \\frac{2 \\pm \\sqrt{3}}{2} \\quad \\text{or} \\quad 1 \\pm \\frac{\\sqrt{3}}{2}\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x - 1 = \\pm\\frac{\\sqrt{3}}{2} \\implies x = 1 \\pm \\frac{\\sqrt{3}}{2} = \\frac{2 \\pm \\sqrt{3}}{2}\\)."
          }
        ]
      },
      {
        id: 13,
        set: "p2",
        setName: "Assignment Problems",
        title: "Quadratic Formula: Radical Reduction",
        prompt: "Use the quadratic formula to solve: \\[x^2 + 6x - 1 = 0\\]",
        hint: "\\(a = 1, b = 6, c = -1\\). Discriminant: \\(6^2 - 4(1)(-1) = 36 + 4 = 40\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(32\\)" },
              { label: "B", text: "\\(-40\\)" },
              { label: "C", text: "\\(40\\)" },
              { label: "D", text: "\\(37\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(6^2 - 4(1)(-1) = 36 + 4 = 40\\)."
          },
          {
            title: "Step 2: Simplify Roots",
            prompt: "Simplify \\(x = \\frac{-6 \\pm \\sqrt{40}}{2}\\).",
            options: [
              { label: "A", text: "\\(x = -3 \\pm 2\\sqrt{10}\\)" },
              { label: "B", text: "\\(x = -3 \\pm \\sqrt{10}\\)" },
              { label: "C", text: "\\(x = -6 \\pm 2\\sqrt{10}\\)" },
              { label: "D", text: "\\(x = 3 \\pm \\sqrt{10}\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(\\sqrt{40} = 2\\sqrt{10}\\). \\(x = \\frac{-6 \\pm 2\\sqrt{10}}{2} = -3 \\pm \\sqrt{10}\\)."
          }
        ]
      },
      {
        id: 14,
        set: "p2",
        setName: "Assignment Problems",
        title: "Quadratic Formula: Fractional Denominator",
        prompt: "Use the quadratic formula to solve: \\[3x^2 - 8x + 2 = 0\\]",
        hint: "\\(a = 3, b = -8, c = 2\\). Discriminant: \\((-8)^2 - 4(3)(2) = 64 - 24 = 40\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(88\\)" },
              { label: "B", text: "\\(-40\\)" },
              { label: "C", text: "\\(24\\)" },
              { label: "D", text: "\\(40\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\((-8)^2 - 4(3)(2) = 64 - 24 = 40\\)."
          },
          {
            title: "Step 2: State Simplified Roots",
            prompt: "Simplify \\(x = \\frac{8 \\pm \\sqrt{40}}{6}\\).",
            options: [
              { label: "A", text: "\\(x = \\frac{4 \\pm \\sqrt{10}}{3}\\)" },
              { label: "B", text: "\\(x = \\frac{8 \\pm 2\\sqrt{10}}{3}\\)" },
              { label: "C", text: "\\(x = \\frac{4 \\pm 2\\sqrt{10}}{3}\\)" },
              { label: "D", text: "\\(x = \\frac{-4 \\pm \\sqrt{10}}{3}\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x = \\frac{8 \\pm 2\\sqrt{10}}{6} = \\frac{4 \\pm \\sqrt{10}}{3}\\)."
          }
        ]
      },
      {
        id: 15,
        set: "p2",
        setName: "Assignment Problems",
        title: "Quadratic Formula: Complex Radical",
        prompt: "Use the quadratic formula to solve: \\[2x^2 - 4x + 7 = 0\\]",
        hint: "Discriminant: \\((-4)^2 - 4(2)(7) = 16 - 56 = -40\\). Express \\(\\sqrt{-40} = 2i\\sqrt{10}\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(40\\)" },
              { label: "B", text: "\\(-40\\)" },
              { label: "C", text: "\\(-72\\)" },
              { label: "D", text: "\\(72\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\((-4)^2 - 4(2)(7) = 16 - 56 = -40\\)."
          },
          {
            title: "Step 2: State Complex Roots",
            prompt: "Evaluate and reduce \\(x = \\frac{4 \\pm 2i\\sqrt{10}}{4}\\).",
            options: [
              { label: "A", text: "\\(x = 2 \\pm i\\sqrt{10}\\)" },
              { label: "B", text: "\\(x = 1 \\pm 2i\\sqrt{10}\\)" },
              { label: "C", text: "\\(x = 1 \\pm \\frac{\\sqrt{10}}{2}i \\quad \\text{or} \\quad \\frac{2 \\pm i\\sqrt{10}}{2}\\)" },
              { label: "D", text: "\\(x = -1 \\pm \\frac{\\sqrt{10}}{2}i\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x = \\frac{4 \\pm 2i\\sqrt{10}}{4} = \\frac{2 \\pm i\\sqrt{10}}{2} = 1 \\pm \\frac{\\sqrt{10}}{2}i\\)."
          }
        ]
      },
      {
        id: 16,
        set: "p2",
        setName: "Assignment Problems",
        title: "Quadratic Formula: Perfect Square Trinomial",
        prompt: "Use the quadratic formula to solve: \\[16x^2 - 24x + 9 = 0\\]",
        hint: "Discriminant: \\((-24)^2 - 4(16)(9) = 576 - 576 = 0\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(0\\)" },
              { label: "B", text: "\\(576\\)" },
              { label: "C", text: "\\(-576\\)" },
              { label: "D", text: "\\(24\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\((-24)^2 - 4(16)(9) = 576 - 576 = 0\\)."
          },
          {
            title: "Step 2: Evaluate Root",
            prompt: "Find the single repeated root.",
            options: [
              { label: "A", text: "\\(x = -3/4\\)" },
              { label: "B", text: "\\(x = 4/3\\)" },
              { label: "C", text: "\\(x = 3/2\\)" },
              { label: "D", text: "\\(x = 3/4\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x = \\frac{24 \\pm 0}{32} = \\frac{24}{32} = \\frac{3}{4}\\)."
          }
        ]
      },

      // ---------- PART 3: TUTORIAL HIGHLIGHTS (17 TO 20) ----------
      {
        id: 17,
        set: "tut",
        setName: "Tutorial Highlights",
        title: "Lamar Example 1b: CTS with Leading Coefficient 2",
        prompt: "Solve by completing the square: \\[2x^2 + 6x - 7 = 0\\]",
        hint: "Divide by 2: \\(x^2 + 3x = 7/2\\). Add \\((3/2)^2 = 9/4\\) to both sides: \\(7/2 + 9/4 = 23/4\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Divide and Complete the Square",
            prompt: "What is the perfect square equation?",
            options: [
              { label: "A", text: "\\((x + 3)^2 = \\frac{23}{4}\\)" },
              { label: "B", text: "\\(\\left(x - \\frac{3}{2}\\right)^2 = \\frac{23}{4}\\)" },
              { label: "C", text: "\\(\\left(x + \\frac{3}{2}\\right)^2 = \\frac{23}{4}\\)" },
              { label: "D", text: "\\(\\left(x + \\frac{3}{2}\\right)^2 = 4\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x^2 + 3x = \\frac{7}{2}\\). Add \\(\\frac{9}{4}\\): \\(\\frac{14}{4} + \\frac{9}{4} = \\frac{23}{4} \\implies \\left(x + \\frac{3}{2}\\right)^2 = \\frac{23}{4}\\)."
          },
          {
            title: "Step 2: Solve for x",
            prompt: "Isolate \\(x\\).",
            options: [
              { label: "A", text: "\\(x = \\frac{3 \\pm \\sqrt{23}}{2}\\)" },
              { label: "B", text: "\\(x = \\frac{-3 \\pm \\sqrt{23}}{2}\\)" },
              { label: "C", text: "\\(x = -3 \\pm \\sqrt{23}\\)" },
              { label: "D", text: "\\(x = \\frac{-3 \\pm 23}{2}\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\(x + \\frac{3}{2} = \\pm\\frac{\\sqrt{23}}{2} \\implies x = \\frac{-3 \\pm \\sqrt{23}}{2}\\)."
          }
        ]
      },
      {
        id: 18,
        set: "tut",
        setName: "Tutorial Highlights",
        title: "Lamar Example 1c: CTS Yielding Complex Roots",
        prompt: "Solve by completing the square: \\[3x^2 - 2x + 6 = 0\\]",
        hint: "Divide by 3: \\(x^2 - \\frac{2}{3}x = -2\\). Add \\((-1/3)^2 = 1/9\\) to both sides: \\(-2 + 1/9 = -17/9\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Form the Squared Binomial",
            prompt: "What is the equation after completing the square?",
            options: [
              { label: "A", text: "\\(\\left(x - \\frac{1}{3}\\right)^2 = \\frac{17}{9}\\)" },
              { label: "B", text: "\\(\\left(x - \\frac{2}{3}\\right)^2 = -\\frac{17}{9}\\)" },
              { label: "C", text: "\\(\\left(x + \\frac{1}{3}\\right)^2 = -\\frac{17}{9}\\)" },
              { label: "D", text: "\\(\\left(x - \\frac{1}{3}\\right)^2 = -\\frac{17}{9}\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x^2 - \\frac{2}{3}x = -2\\). Add \\(\\frac{1}{9}\\): \\(-2 + \\frac{1}{9} = -\\frac{17}{9} \\implies \\left(x - \\frac{1}{3}\\right)^2 = -\\frac{17}{9}\\)."
          },
          {
            title: "Step 2: Solve with Imaginary Unit",
            prompt: "State the complex roots.",
            options: [
              { label: "A", text: "\\(x = \\frac{1 \\pm \\sqrt{17}i}{3} \\quad \\text{or} \\quad \\frac{1}{3} \\pm \\frac{\\sqrt{17}}{3}i\\)" },
              { label: "B", text: "\\(x = \\frac{-1 \\pm \\sqrt{17}i}{3}\\)" },
              { label: "C", text: "\\(x = 1 \\pm \\frac{\\sqrt{17}}{3}i\\)" },
              { label: "D", text: "\\(x = \\frac{1 \\pm 17i}{3}\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x - \\frac{1}{3} = \\pm\\frac{\\sqrt{17}i}{3} \\implies x = \\frac{1 \\pm \\sqrt{17}i}{3}\\)."
          }
        ]
      },
      {
        id: 19,
        set: "tut",
        setName: "Tutorial Highlights",
        title: "Lamar Example 2b: QF Non-Factorable Real",
        prompt: "Use the quadratic formula to solve: \\[2x^2 - 3x - 4 = 0\\]",
        hint: "\\(a = 2, b = -3, c = -4\\). Discriminant: \\((-3)^2 - 4(2)(-4) = 9 + 32 = 41\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(-23\\)" },
              { label: "B", text: "\\(41\\)" },
              { label: "C", text: "\\(23\\)" },
              { label: "D", text: "\\(-41\\)" }
            ],
            correctIndex: 1, // B
            explanation: "\\((-3)^2 - 4(2)(-4) = 9 + 32 = 41\\)."
          },
          {
            title: "Step 2: State Roots",
            prompt: "What are the exact roots?",
            options: [
              { label: "A", text: "\\(x = \\frac{-3 \\pm \\sqrt{41}}{4}\\)" },
              { label: "B", text: "\\(x = \\frac{3 \\pm \\sqrt{41}}{2}\\)" },
              { label: "C", text: "\\(x = \\frac{3 \\pm \\sqrt{41}}{4}\\)" },
              { label: "D", text: "\\(x = 3 \\pm \\sqrt{41}\\)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x = \\frac{-(-3) \\pm \\sqrt{41}}{2(2)} = \\frac{3 \\pm \\sqrt{41}}{4}\\)."
          }
        ]
      },
      {
        id: 20,
        set: "tut",
        setName: "Tutorial Highlights",
        title: "Lamar Example 2c: QF Exact Complex Conjugates",
        prompt: "Use the quadratic formula to solve: \\[x^2 - 4x + 13 = 0\\]",
        hint: "\\(a = 1, b = -4, c = 13\\). Discriminant: \\(16 - 52 = -36\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Compute Discriminant",
            prompt: "What is \\(b^2 - 4ac\\)?",
            options: [
              { label: "A", text: "\\(-36\\)" },
              { label: "B", text: "\\(36\\)" },
              { label: "C", text: "\\(-68\\)" },
              { label: "D", text: "\\(68\\)" }
            ],
            correctIndex: 0, // A
            explanation: "\\((-4)^2 - 4(1)(13) = 16 - 52 = -36\\)."
          },
          {
            title: "Step 2: Solve and Reduce",
            prompt: "Evaluate \\(x = \\frac{4 \\pm 6i}{2}\\).",
            options: [
              { label: "A", text: "\\(x = 4 \\pm 3i\\)" },
              { label: "B", text: "\\(x = -2 \\pm 3i\\)" },
              { label: "C", text: "\\(x = 2 \\pm 6i\\)" },
              { label: "D", text: "\\(x = 2 \\pm 3i\\)" }
            ],
            correctIndex: 3, // D
            explanation: "\\(x = \\frac{4 \\pm 6i}{2} = 2 \\pm 3i\\)."
          }
        ]
      }
    ];

    /* ==========================================================================
       PERSISTENCE & STATE MANAGEMENT ENGINE
       ========================================================================== */
    const STORAGE_KEY = "algebra_solve_quadratic_II_v2";

    let currentStudentName = "Guest";
    let activeProblemId = 1;
    let currentPaletteFilter = "all";

    let stepProgress = {};

    let audioMuted = false;
    let totalSeconds = 0;
    let timerInterval = null;

    function saveSessionProgress() {
      try {
        const payload = {
          studentName: currentStudentName,
          activeProblemId: activeProblemId,
          totalSeconds: totalSeconds,
          stepProgress: stepProgress
        };
        localStorage.setItem(STORAGE_KEY, JSON.stringify(payload));
      } catch (e) {
        console.warn("Storage save error", e);
      }
    }

    function checkSavedSession() {
      try {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (!raw) return;
        const data = JSON.parse(raw);
        if (data && data.studentName) {
          const alertBox = document.getElementById('resumeAlertBox');
          const detailsSpan = document.getElementById('savedSessionDetails');
          const resumeBtn = document.getElementById('resumeSessionBtn');
          const startBtn = document.getElementById('startSessionBtn');
          const input = document.getElementById('studentNameInput');

          input.value = data.studentName;
          let completedSteps = 0;
          Object.keys(data.stepProgress || {}).forEach(k => {
            if (data.stepProgress[k].resolved) completedSteps++;
          });
          detailsSpan.innerText = `Student: ${data.studentName} • ${completedSteps}/40 Steps Completed • Time: ${Math.floor(data.totalSeconds / 60)}m ${data.totalSeconds % 60}s`;
          alertBox.style.display = 'block';
          resumeBtn.style.display = 'inline-block';
          startBtn.innerText = 'Start Fresh Session';
        }
      } catch (e) {
        console.warn("Session check error", e);
      }
    }

    const AudioEngine = {
      ctx: null,
      init() {
        if (!this.ctx) {
          this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
      },
      playTone(freq, type, duration, delay = 0) {
        if (audioMuted || !this.ctx) return;
        setTimeout(() => {
          try {
            const osc = this.ctx.createOscillator();
            const gain = this.ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
            gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);
            osc.connect(gain);
            gain.connect(this.ctx.destination);
            osc.start();
            osc.stop(this.ctx.currentTime + duration);
          } catch (e) {
            console.warn(e);
          }
        }, delay * 1000);
      },
      correct() {
        this.init();
        this.playTone(659.25, 'sine', 0.15, 0);
        this.playTone(880.00, 'sine', 0.25, 0.12);
      },
      incorrect() {
        this.init();
        this.playTone(196.00, 'triangle', 0.2, 0);
        this.playTone(146.83, 'triangle', 0.3, 0.12);
      }
    };

    function startTimer() {
      if (timerInterval) clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        totalSeconds++;
        const mins = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const secs = String(totalSeconds % 60).padStart(2, '0');
        document.getElementById('timerChip').innerText = `⏱️ ${mins}:${secs}`;
        saveSessionProgress();
      }, 1000);
    }

    function showToast(msg) {
      const t = document.getElementById('toastMessage');
      t.innerText = msg;
      t.style.display = 'block';
      setTimeout(() => { t.style.display = 'none'; }, 2600);
    }

    function initDirectLogin(isResume = false) {
      const nameInput = document.getElementById('studentNameInput').value.trim() || 'Student';
      
      if (isResume) {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (raw) {
          const data = JSON.parse(raw);
          currentStudentName = data.studentName || nameInput;
          activeProblemId = data.activeProblemId || 1;
          totalSeconds = data.totalSeconds || 0;
          stepProgress = data.stepProgress || {};
          showToast(`Welcome back, ${currentStudentName}!`);
        }
      } else {
        currentStudentName = nameInput;
        totalSeconds = 0;
        activeProblemId = 1;
        stepProgress = {};
        saveSessionProgress();
      }

      document.getElementById('userPill').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;
      document.getElementById('loginGateView').style.display = 'none';
      
      AudioEngine.init();
      startTimer();
      renderPalette();
      loadProblem(activeProblemId);
    }

    function resetStudentProgress() {
      if (confirm("Reset all 20 problem attempts and scorecard progress?")) {
        localStorage.removeItem(STORAGE_KEY);
        location.reload();
      }
    }

    function switchMainTab(tab) {
      document.getElementById('tabPracticeBtn').classList.toggle('active', tab === 'practice');
      document.getElementById('tabTheoryBtn').classList.toggle('active', tab === 'theory');
      document.getElementById('tabScorecardBtn').classList.toggle('active', tab === 'scorecard');

      document.getElementById('viewPractice').classList.toggle('active', tab === 'practice');
      document.getElementById('viewTheory').classList.toggle('active', tab === 'theory');
      document.getElementById('viewScorecard').classList.toggle('active', tab === 'scorecard');

      if (tab === 'scorecard') {
        renderScorecard();
      } else if (tab === 'practice') {
        renderPalette();
        loadProblem(activeProblemId);
      }

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function filterPalette(mode) {
      currentPaletteFilter = mode;
      document.getElementById('filterAllBtn').classList.toggle('active', mode === 'all');
      document.getElementById('filterP1Btn').classList.toggle('active', mode === 'p1');
      document.getElementById('filterP2Btn').classList.toggle('active', mode === 'p2');
      document.getElementById('filterTutBtn').classList.toggle('active', mode === 'tut');
      renderPalette();
    }

    function renderAlignedTopicBanner() {
      const banner = document.getElementById('topicBannerContainer');
      banner.innerHTML = `
        <h3>📚 Solving Quadratic Equations, Part II: Core Reference</h3>
        <p style="font-size:0.94rem; color:var(--text-main); line-height:1.6;">
          When factoring by inspection is not straightforward, we turn to <strong>Completing the Square</strong> or the universal <strong>Quadratic Formula</strong>. Both methods handle non-real complex conjugate roots as naturally as real roots.
        </p>
        
        <div class="formula-box">
          <strong>The Two Universal Quadratic Methods:</strong>
          \\[\\text{Completing the Square: } x^2 + bx + \\left(\\frac{b}{2}\\right)^2 = -c + \\left(\\frac{b}{2}\\right)^2 \\qquad \\text{and} \\qquad x = \\frac{-b \\pm \\sqrt{b^2 - 4ac}}{2a}\\]
        </div>

        <div class="paul-notes-container">
          <h4>📖 Paul's Online Notes: Core Rules &amp; Frequent Pitfalls</h4>
          <div class="paul-notes-body">
            <ul>
              <li><strong>Leading Coefficient in Completing the Square:</strong> You <em>must</em> divide by \\(a\\) first if \\(a \\ne 1\\) before adding \\(\\left(\\frac{b}{2a}\\right)^2\\). Adding half the linear coefficient to a leading term like \\(2x^2\\) or \\(3x^2\\) will fail!</li>
              <li><strong>Negative Discriminant:</strong> When \\(b^2 - 4ac < 0\\), do not stop and write 'no solution'. Factor out \\(i = \\sqrt{-1}\\) to produce exact complex conjugate solutions.</li>
              <li><strong>Common Division Trap:</strong> When reducing \\(\\frac{-b \\pm \\sqrt{D}}{2a}\\), factor a common number out of the entire numerator first before canceling with the denominator.</li>
            </ul>
          </div>
        </div>
      `;
    }

    function toggleHint(pId) {
      const hintBox = document.getElementById(`hintBox_${pId}`);
      if (hintBox) {
        const isHidden = hintBox.style.display === 'none' || hintBox.style.display === '';
        hintBox.style.display = isHidden ? 'block' : 'none';
      }
    }

    function renderPalette() {
      const grid = document.getElementById('paletteGrid');
      grid.innerHTML = '';

      let completedProblems = 0;

      let filteredList = PROBLEMS_DATA;
      if (currentPaletteFilter === 'p1') filteredList = PROBLEMS_DATA.filter(p => p.set === 'p1');
      if (currentPaletteFilter === 'p2') filteredList = PROBLEMS_DATA.filter(p => p.set === 'p2');
      if (currentPaletteFilter === 'tut') filteredList = PROBLEMS_DATA.filter(p => p.set === 'tut');

      PROBLEMS_DATA.forEach((prob) => {
        let allResolved = true;
        prob.steps.forEach((_, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (!sp || !sp.resolved) allResolved = false;
        });
        if (allResolved) completedProblems++;
      });

      filteredList.forEach((prob) => {
        let allResolved = true;
        let anyResolved = false;

        prob.steps.forEach((_, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (sp && sp.resolved) anyResolved = true;
          else allResolved = false;
        });

        const btn = document.createElement('button');
        let stateClass = '';
        if (prob.id === activeProblemId) stateClass = 'active';
        else if (allResolved) stateClass = 'completed';
        else if (anyResolved) stateClass = 'partial';

        btn.className = `palette-btn ${stateClass}`;
        btn.innerHTML = `<span>${prob.id}</span>`;
        btn.title = `Problem ${prob.id}: ${prob.title}`;
        btn.onclick = () => loadProblem(prob.id);
        grid.appendChild(btn);
      });

      document.getElementById('paletteCount').innerText = `${completedProblems} / ${PROBLEMS_DATA.length} Solved`;
    }

    function loadProblem(pId) {
      activeProblemId = pId;
      saveSessionProgress();
      renderPalette();

      const prob = PROBLEMS_DATA.find(p => p.id === pId);
      const card = document.getElementById('activeQuestionCard');

      renderAlignedTopicBanner();

      let stepsHtml = '';

      // STRICT STEP GATING:
      // Step k is ONLY rendered if Step k-1 is resolved!
      prob.steps.forEach((step, sIdx) => {
        const key = `${prob.id}_${sIdx}`;
        const sp = stepProgress[key] || { attempts: 0, selectedIndex: null, resolved: false, correct: false };

        let canShow = false;
        if (sIdx === 0) {
          canShow = true;
        } else {
          const prevKey = `${prob.id}_${sIdx - 1}`;
          const prevSp = stepProgress[prevKey];
          if (prevSp && prevSp.resolved) {
            canShow = true;
          }
        }

        if (!canShow) return;

        let optionsHtml = '';
        step.options.forEach((opt, optIdx) => {
          let optClass = '';
          if (sp.resolved) {
            if (optIdx === step.correctIndex) {
              optClass = 'selected-correct';
            } else if (sp.selectedIndex === optIdx) {
              optClass = 'selected-wrong';
            }
          }

          optionsHtml += `
            <button class="mcq-option-btn ${optClass}" 
              onclick="handleStepSelect(${prob.id}, ${sIdx}, ${optIdx})"
              ${sp.resolved ? 'disabled' : ''}>
              <span class="opt-letter">(${opt.label})</span>
              <span class="opt-text-content">${opt.text}</span>
            </button>
          `;
        });

        let feedbackHtml = '';
        if (sp.resolved) {
          feedbackHtml = `
            <div class="step-feedback-box ${sp.correct ? 'correct' : 'incorrect'}">
              <strong>${sp.correct ? '✓ Step Completed' : '✗ Solution Revealed'}</strong> (Correct Choice: Option ${step.options[step.correctIndex].label})<br/>
              <div style="margin-top: 6px;">${step.explanation}</div>
            </div>
          `;
        }

        stepsHtml += `
          <div class="step-unit ${sp.resolved ? 'completed' : ''}">
            <div class="step-header">
              <div class="step-title">
                <span>${step.title}</span>
                ${sp.resolved ? '<span class="step-badge resolved">Finished</span>' : `<span class="step-badge">Active Step</span>`}
              </div>
              <span class="attempts-badge">Attempts: ${sp.attempts}/2</span>
            </div>
            <div style="font-size: 0.95rem; line-height: 1.6; margin-bottom: 10px;">${step.prompt}</div>
            <div class="mcq-container">${optionsHtml}</div>
            
            ${!sp.resolved && sp.attempts >= 2 ? `
              <button class="btn-reveal-step" onclick="revealStepSolution(${prob.id},${sIdx})">
                Reveal Step Solution &amp; Continue
              </button>
            ` : ''}

            ${feedbackHtml}
          </div>
        `;
      });

      const pIdx = PROBLEMS_DATA.findIndex(p => p.id === prob.id);
      const prevDisabled = pIdx === 0 ? 'disabled' : '';
      const nextDisabled = pIdx === PROBLEMS_DATA.length - 1 ? 'disabled' : '';

      card.innerHTML = `
        <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap;">
          <span class="concept-tag">${prob.setName}</span>
          <span style="font-size:0.82rem; color:var(--text-muted);">Algebra: Solving Quadratic Equations II</span>
        </div>
        
        <h2 style="color:var(--navy-dark); margin: 6px 0 10px 0;">Problem ${prob.id}: ${prob.title}</h2>
        <div style="margin-top: 8px; line-height: 1.65; font-size:1.02rem;">${prob.prompt}</div>
        
        <div class="hint-container">
          <button class="btn-hint-toggle" onclick="toggleHint(${prob.id})">
            💡 Need a Hint? Click to View / Hide
          </button>
          <div class="hint-box" id="hintBox_${prob.id}">
            <strong>Pedagogical Hint:</strong> ${prob.hint}
          </div>
        </div>

        ${prob.svg ? `<div class="svg-container">${prob.svg}</div>` : ''}
        
        <div style="margin-top: 18px;">${stepsHtml}</div>

        <div class="nav-toolbar">
          <button class="btn-nav-action" onclick="navigateProblem(-1)" ${prevDisabled}>
            ⏮ Previous Problem
          </button>
          <div class="nav-btn-group">
            <button class="btn-nav-action btn-skip" onclick="skipProblem(${prob.id})">
              ⏭ Skip Problem
            </button>
            <button class="btn-nav-action" onclick="navigateProblem(1)" ${nextDisabled}>
              Next Problem ❯
            </button>
          </div>
        </div>
      `;

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function handleStepSelect(pId, sIdx, optIdx) {
      const prob = PROBLEMS_DATA.find(p => p.id === pId);
      const step = prob.steps[sIdx];
      const key = `${pId}_${sIdx}`;

      if (!stepProgress[key]) {
        stepProgress[key] = { attempts: 0, selectedIndex: null, resolved: false, correct: false };
      }
      const sp = stepProgress[key];
      if (sp.resolved) return;

      sp.selectedIndex = optIdx;
      sp.attempts++;

      if (optIdx === step.correctIndex) {
        sp.resolved = true;
        sp.correct = true;
        AudioEngine.correct();
        showToast(`Step ${sIdx + 1} Completed! Next step unlocked.`);
      } else {
        AudioEngine.incorrect();
        if (sp.attempts >= 2) {
          showToast(`2 attempts reached. Click 'Reveal Step Solution' to unlock next step.`);
        } else {
          showToast(`Incorrect option. 1 attempt remaining!`);
        }
      }

      saveSessionProgress();
      renderPalette();
      loadProblem(pId);
    }

    function revealStepSolution(pId, sIdx) {
      const key = `${pId}_${sIdx}`;
      if (!stepProgress[key]) {
        stepProgress[key] = { attempts: 2, selectedIndex: null, resolved: false, correct: false };
      }
      const sp = stepProgress[key];
      sp.resolved = true;
      sp.correct = false;
      AudioEngine.incorrect();
      showToast(`Step ${sIdx + 1} solution revealed. Next step unlocked.`);
      saveSessionProgress();
      renderPalette();
      loadProblem(pId);
    }

    function navigateProblem(delta) {
      const pIdx = PROBLEMS_DATA.findIndex(p => p.id === activeProblemId);
      const target = pIdx + delta;
      if (target >= 0 && target < PROBLEMS_DATA.length) {
        loadProblem(PROBLEMS_DATA[target].id);
      }
    }

    function skipProblem(pId) {
      showToast(`Problem ${pId} skipped.`);
      navigateProblem(1);
    }

    function renderScorecard() {
      const container = document.getElementById('completeSolutionsContainer');
      let fullySolvedProblems = 0;
      let totalSteps = 0;
      let correctSteps = 0;

      PROBLEMS_DATA.forEach(p => {
        let probComplete = true;
        p.steps.forEach((_, sIdx) => {
          totalSteps++;
          const key = `${p.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (sp && sp.correct) {
            correctSteps++;
          } else {
            probComplete = false;
          }
        });
        if (probComplete) fullySolvedProblems++;
      });

      const percentage = Math.round((correctSteps / totalSteps) * 100);

      document.getElementById('scoreValue').innerText = `${fullySolvedProblems} / ${PROBLEMS_DATA.length}`;
      document.getElementById('progressBarFill').style.width = `${percentage}%`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong> (${correctSteps}/${totalSteps} Steps Correct • ${percentage}%)`;

      let html = '';
      PROBLEMS_DATA.forEach(prob => {
        let probStepsHtml = prob.steps.map((step, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key] || { attempts: 0, selectedIndex: null, resolved: false, correct: false };
          
          let badge = `<span style="color:var(--text-muted); font-weight:bold;">Unattempted</span>`;
          if (sp.resolved) {
            badge = sp.correct 
              ? `<span style="color:var(--green-ok); font-weight:bold;">✓ Correct (Attempt ${sp.attempts})</span>` 
              : `<span style="color:var(--red-fail); font-weight:bold;">✗ Solution Revealed</span>`;
          }

          const userChoiceText = (sp.selectedIndex !== null && step.options[sp.selectedIndex]) 
            ? `(${step.options[sp.selectedIndex].label}) ${step.options[sp.selectedIndex].text}` 
            : 'None';

          return `
            <div style="background:#f8fafc; border-left:4px solid var(--brand-blue); padding:12px; margin-top:10px; border-radius:0 6px 6px 0;">
              <div style="display:flex; justify-content:space-between; margin-bottom:4px;">
                <strong>${step.title}</strong>
                ${badge}
              </div>
              <p style="font-size:0.9rem; margin-bottom:4px;"><strong>Target:</strong> ${step.prompt}</p>
              <p style="font-size:0.88rem;"><strong>Your Choice:</strong> ${userChoiceText}</p>
              <p style="font-size:0.88rem;"><strong>Correct Option:</strong> (${step.options[step.correctIndex].label}) ${step.options[step.correctIndex].text}</p>
              <p style="font-size:0.86rem; color:var(--text-muted); margin-top:4px;">${step.explanation}</p>
            </div>
          `;
        }).join('');

        html += `
          <div class="theory-card" style="margin-bottom:20px;">
            <div style="display:flex; justify-content:space-between; align-items:center;">
              <span class="concept-tag">${prob.setName}</span>
              <span style="font-size:0.85rem; color:var(--text-muted);">Problem ${prob.id} of ${PROBLEMS_DATA.length}</span>
            </div>
            <h3 style="margin-top:6px;">Problem ${prob.id}: ${prob.title}</h3>
            <div style="margin: 8px 0; font-size:0.95rem;">${prob.prompt}</div>
            ${prob.svg ? `<div class="svg-container" style="max-width:320px; margin:12px 0;">${prob.svg}</div>` : ''}
            <div>${probStepsHtml}</div>
          </div>
        `;
      });

      container.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    document.getElementById('audioToggleBtn').onclick = () => {
      audioMuted = !audioMuted;
      document.getElementById('audioToggleBtn').innerText = audioMuted ? '🔇' : '🔊';
    };

    window.addEventListener('DOMContentLoaded', checkSavedSession);
  </script>
</body>
</html>
