
<!DOCTYPE html>
<html lang="rw">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#123c32">
  <meta name="description" content="HANGA-AKAZI: shakisha amahirwe y'akazi, kwihangira imirimo n'amahugurwa.">
  <title>HANGA-AKAZI | Amahirwe yawe</title>

  <style>
    :root {
      --green: #123c32;
      --green-light: #e8f4ed;
      --lime: #c9f36b;
      --ink: #1e2b27;
      --muted: #68766f;
      --bg: #f5f7f4;
      --white: #ffffff;
      --border: #e0e7e1;
      --radius: 18px;
      --shadow: 0 8px 25px rgba(18, 60, 50, 0.07);
    }

    * {
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      background: var(--bg);
      color: var(--ink);
      font-family: Arial, Helvetica, sans-serif;
      line-height: 1.6;
    }

    button, input, select {
      font: inherit;
    }

    button, a, select {
      -webkit-tap-highlight-color: transparent;
    }

    a {
      color: inherit;
    }

    .container {
      width: min(1100px, 92%);
      margin: 0 auto;
    }

    header {
      background: var(--green);
      color: var(--white);
      padding: 15px 0;
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      flex-wrap: wrap;
    }

    .brand {
      font-size: 1.3rem;
      font-weight: 800;
      letter-spacing: -0.5px;
    }

    .brand span {
      color: var(--lime);
    }

    .nav-links {
      display: flex;
      gap: 17px;
      flex-wrap: wrap;
    }

    .nav-links a {
      text-decoration: none;
      color: #e5eee9;
      font-size: 0.92rem;
    }

    .hero {
      background: var(--green);
      color: var(--white);
      padding: 42px 0 56px;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.5fr 1fr;
      gap: 28px;
      align-items: center;
    }

    .eyebrow {
      color: var(--lime);
      font-weight: 700;
      font-size: 0.83rem;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    h1 {
      font-size: clamp(2rem, 5vw, 3.4rem);
      line-height: 1.12;
      margin: 12px 0;
      letter-spacing: -1.5px;
    }

    .hero p {
      color: #d7e6dd;
      max-width: 580px;
    }

    .primary-button {
      display: inline-block;
      border: 0;
      background: var(--lime);
      color: var(--green);
      font-weight: 800;
      text-decoration: none;
      border-radius: 12px;
      padding: 12px 18px;
      cursor: pointer;
    }

    .hero-note {
      background: rgba(255,255,255,0.08);
      border: 1px solid rgba(255,255,255,0.16);
      padding: 22px;
      border-radius: var(--radius);
    }

    .hero-note strong {
      display: block;
      font-size: 1.6rem;
      color: var(--lime);
    }

    .hero-note small {
      color: #d7e6dd;
    }

    main {
      padding: 32px 0 50px;
    }

    .section {
      margin-bottom: 34px;
      scroll-margin-top: 20px;
    }

    .section-heading {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 12px;
      margin-bottom: 17px;
    }

    h2 {
      margin: 0;
      font-size: 1.55rem;
      letter-spacing: -0.5px;
    }

    .subtext {
      color: var(--muted);
      margin: 5px 0 0;
      font-size: 0.94rem;
    }

    .stats-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 14px;
    }

    .stat-card, .panel, .opportunity-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }

    .stat-card {
      padding: 19px;
    }

    .stat-label {
      color: var(--muted);
      font-size: 0.85rem;
    }

    .stat-value {
      display: block;
      font-size: 1.8rem;
      font-weight: 800;
      margin: 8px 0 3px;
      color: var(--green);
    }

    .stat-foot {
      font-size: 0.78rem;
      color: var(--muted);
    }

    .source-note {
      background: #edf2ed;
      border-radius: 12px;
      padding: 14px 16px;
      margin-top: 14px;
      color: #46574d;
      font-size: 0.86rem;
    }

    .source-note a {
      font-weight: 700;
    }

    .panel {
      padding: 22px;
    }

    .search-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 15px;
    }

    .field label {
      display: block;
      font-size: 0.88rem;
      font-weight: 700;
      margin-bottom: 6px;
    }

    .field input, .field select {
      width: 100%;
      min-height: 47px;
      border: 1px solid #cfd9d1;
      border-radius: 10px;
      padding: 10px 12px;
      background: #fff;
      color: var(--ink);
    }

    .field input:focus, .field select:focus {
      outline: 2px solid #83b99a;
      outline-offset: 1px;
    }

    .search-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 17px;
    }

    .button {
      min-height: 44px;
      border: 0;
      border-radius: 10px;
      padding: 10px 16px;
      font-weight: 700;
      cursor: pointer;
    }

    .button-green {
      background: var(--green);
      color: var(--white);
    }

    .button-light {
      background: var(--green-light);
      color: var(--green);
    }

    .results-top {
      display: flex;
      justify-content: space-between;
      gap: 10px;
      align-items: center;
      margin: 22px 0 13px;
      flex-wrap: wrap;
    }

    #resultCount {
      color: var(--muted);
      font-size: 0.9rem;
    }

    .opportunity-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 16px;
    }

    .opportunity-card {
      padding: 20px;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    .card-top {
      display: flex;
      justify-content: space-between;
      align-items: start;
      gap: 10px;
    }

    .tag {
      display: inline-block;
      padding: 5px 9px;
      border-radius: 20px;
      background: var(--green-light);
      color: var(--green);
      font-size: 0.76rem;
      font-weight: 700;
    }

    .demo-tag {
      background: #fff2d9;
      color: #7b4c00;
    }

    .opportunity-card h3 {
      margin: 0;
      font-size: 1.1rem;
      line-height: 1.35;
    }

    .meta {
      color: var(--muted);
      font-size: 0.86rem;
    }

    .description {
      margin: 0;
      font-size: 0.92rem;
    }

    .details {
      border-top: 1px solid var(--border);
      padding-top: 12px;
      color: #48584f;
      font-size: 0.9rem;
    }

    .details[hidden] {
      display: none;
    }

    .card-actions {
      display: flex;
      gap: 8px;
      flex-wrap: wrap;
      margin-top: auto;
      padding-top: 4px;
    }

    .empty-state {
      text-align: center;
      padding: 30px 15px;
      background: white;
      border: 1px dashed #b9c9bd;
      border-radius: var(--radius);
      color: var(--muted);
    }

    .how-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
    }

    .how-card {
      padding: 18px;
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: var(--radius);
    }

    .how-number {
      display: inline-grid;
      place-items: center;
      width: 35px;
      height: 35px;
      background: var(--green-light);
      color: var(--green);
      border-radius: 50%;
      font-weight: 800;
      margin-bottom: 8px;
    }

    .how-card h3 {
      margin: 4px 0;
      font-size: 1rem;
    }

    .how-card p {
      color: var(--muted);
      font-size: 0.9rem;
      margin-bottom: 0;
    }

    footer {
      background: #102f28;
      color: #d7e6dd;
      padding: 25px 0;
      font-size: 0.86rem;
    }

    footer p {
      margin: 6px 0;
    }

    .footer-brand {
      font-weight: 800;
      color: var(--white);
    }

    @media (max-width: 760px) {
      .hero-grid {
        grid-template-columns: 1fr;
      }

      .stats-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .opportunity-grid {
        grid-template-columns: 1fr;
      }

      .how-grid {
        grid-template-columns: 1fr;
      }

      .hero {
        padding: 32px 0 38px;
      }

      .panel {
        padding: 16px;
      }
    }

    @media (max-width: 420px) {
      .search-grid {
        grid-template-columns: 1fr;
      }

      .nav-links {
        gap: 11px;
      }

      .nav-links a {
        font-size: 0.84rem;
      }

      .stat-card {
        padding: 14px;
      }

      .stat-value {
        font-size: 1.5rem;
      }
    }
  </style>
</head>

<body>
  <header>
    <div class="container nav">
      <a class="brand" href="#" style="text-decoration:none">
        HANGA-<span>AKAZI</span>
      </a>

      <nav class="nav-links" aria-label="Imiyoborere">
        <a href="#dashboard">Dashboard</a>
        <a href="#search">Shakisha</a>
        <a href="#about">Uko ikora</a>
      </nav>
    </div>
  </header>

  <section class="hero">
    <div class="container hero-grid">
      <div>
        <div class="eyebrow">Ubumenyi bwawe. Amahirwe yawe.</div>
        <h1>Shaka amahirwe.<br>Hanga ejo hazaza.</h1>
        <p>
          HANGA-AKAZI igamije gufasha urubyiruko kubona amahirwe
          ajyanye n'ubumenyi, akazi, kwihangira imirimo n'amahugurwa.
        </p>
        <a class="primary-button" href="#search">Tangira gushakisha →</a>
      </div>

      <div class="hero-note">
        <strong>Ubumenyi + Amahirwe</strong>
        <p>
          Intego ni uguhuza abantu n'amahirwe abafasha gukoresha
          ibyo bazi no kongera ubumenyi bafite.
        </p>
        <small>Prototype y'igerageza — verisiyo ya mbere</small>
      </div>
    </div>
  </section>

  <main class="container">
    <section class="section" id="dashboard">
      <div class="section-heading">
        <div>
          <h2>Dashboard y'imibare</h2>
          <p class="subtext">Imibare ifasha gusobanukirwa ikibazo cy'akazi mu Rwanda.</p>
        </div>
      </div>

      <div class="stats-grid">
        <article class="stat-card">
          <span class="stat-label">Urubyiruko rwa NEET</span>
          <strong class="stat-value">24.5%</strong>
          <span class="stat-foot">Imyaka 16–30, raporo ya 2025</span>
        </article>

        <article class="stat-card">
          <span class="stat-label">Abagore ba NEET</span>
          <strong class="stat-value">30.5%</strong>
          <span class="stat-foot">Imibare ya raporo ya 2025</span>
        </article>

        <article class="stat-card">
          <span class="stat-label">Abagabo ba NEET</span>
          <strong class="stat-value">18.3%</strong>
          <span class="stat-foot">Imibare ya raporo ya 2025</span>
        </article>

        <article class="stat-card">
          <span class="stat-label">Abatuye mu cyaro ba NEET</span>
          <strong class="stat-value">26.7%</strong>
          <span class="stat-foot">Imibare ya raporo ya 2025</span>
        </article>
      </div>

      <div class="source-note">
        <strong>NEET bisobanura iki?</strong>
        Ni urubyiruko rutari mu kazi, amashuri cyangwa amahugurwa.
        Iyi mibare ni iyo muri raporo ya NISR ya Labour Force Survey 2025;
        ntabwo ari imibare ibarwa n'iyi porogaramu.
        <br>
        <a href="https://www.statistics.gov.rw/sites/default/files/documents/2026-03/Annual%20LFS%202025%20Report..pdf"
           target="_blank" rel="noopener noreferrer">
          Fungura raporo y'umwimerere ya NISR
        </a>
      </div>
    </section>

    <section class="section" id="search">
      <div class="section-heading">
        <div>
          <h2>Shakisha amahirwe</h2>
          <p class="subtext">
            Hitamo ubumenyi, aho ushaka amahirwe n'ubwoko bw'ibyo ushaka.
          </p>
        </div>
      </div>

      <div class="panel">
        <form id="searchForm">
          <div class="search-grid">
            <div class="field">
              <label for="keyword">Ijambo ushakisha</label>
              <input id="keyword" type="search"
                     placeholder="Urugero: English, ubuhinzi...">
            </div>

            <div class="field">
              <label for="skill">Ubumenyi ufite cyangwa wifuza</label>
              <select id="skill">
                <option value="">Ubumenyi bwose</option>
                <option value="English">English</option>
                <option value="Kiswahili">Kiswahili</option>
                <option value="ICT">ICT / Ikoranabuhanga</option>
                <option value="Ubuhinzi">Ubuhinzi</option>
                <option value="Ubucuruzi">Ubucuruzi</option>
                <option value="Ubudozi">Ubudozi</option>
                <option value="Ubukanishi">Ubukanishi</option>
              </select>
            </div>

            <div class="field">
              <label for="district">Akarere</label>
              <select id="district">
                <option value="">Uturere twose</option>
                <option value="Nyagatare">Nyagatare</option>
                <option value="Kigali">Kigali</option>
                <option value="Huye">Huye</option>
                <option value="Musanze">Musanze</option>
                <option value="Rubavu">Rubavu</option>
              </select>
            </div>

            <div class="field">
              <label for="type">Ubwoko bw'amahirwe</label>
              <select id="type">
                <option value="">Ubwoko bwose</option>
                <option value="Akazi">Akazi</option>
                <option value="Kwihangira imirimo">Kwihangira imirimo</option>
                <option value="Amahugurwa">Amahugurwa</option>
              </select>
            </div>
          </div>

          <div class="search-actions">
            <button class="button button-green" type="submit">
              Shakisha amahirwe
            </button>
            <button class="button button-light" type="reset">
              Siba ibyo wahisemo
            </button>
          </div>
        </form>
      </div>

      <div class="results-top">
        <h2 style="font-size:1.2rem">Amahirwe aboneka</h2>
        <span id="resultCount" aria-live="polite">Turategura amahirwe...</span>
      </div>

      <div class="opportunity-grid" id="opportunityList"></div>
      <div class="empty-state" id="emptyState" hidden>
        <strong>Nta mahirwe ahuye n'ibyo washakishije.</strong>
        <p>Gerageza guhindura ubumenyi, akarere cyangwa ubwoko bw'amahirwe.</p>
      </div>
    </section>

    <section class="section" id="about">
      <div class="section-heading">
        <div>
          <h2>Uko HANGA-AKAZI ikora</h2>
          <p class="subtext">Iyi ni intangiriro; ibindi bice bizongerwaho nyuma.</p>
        </div>
      </div>

      <div class="how-grid">
        <article class="how-card">
          <span class="how-number">1</span>
          <h3>Shakisha</h3>
          <p>Hitamo ubumenyi, akarere n'ubwoko bw'amahirwe ukeneye.</p>
        </article>

        <article class="how-card">
          <span class="how-number">2</span>
          <h3>Reba ibisobanuro</h3>
          <p>Soma ibyo amahirwe asaba n'icyo ashobora kugufasha kugeraho.</p>
        </article>

        <article class="how-card">
          <span class="how-number">3</span>
          <h3>Fata intambwe</h3>
          <p>Mu verisiyo zizakurikiraho, tuzongeramo amakuru yizewe yo gusaba amahirwe.</p>
        </article>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <p class="footer-brand">HANGA-AKAZI</p>
      <p>Prototype igamije gufasha urubyiruko guhuza ubumenyi n'amahirwe.</p>
      <p>
        Iyi verisiyo ntirahuza n'ububiko bw'amakuru kandi nta mahirwe
        y'akazi yemejwe itangaza.
      </p>
      <p>© <span id="year"></span> HANGA-AKAZI — Verisiyo ya mbere.</p>
    </div>
  </footer>

  <script>
    // Aya ni amakuru y'icyitegererezo yo kugerageza prototype.
    // Ntabwo ari imyanya y'akazi cyangwa amahugurwa yemejwe.
    const opportunities = [
      {
        id: 1,
        title: "Gufasha mu masomo y'English",
        type: "Kwihangira imirimo",
        district: "Nyagatare",
        skills: ["English"],
        format: "Mu gace utuyemo",
        description: "Icyitegererezo cy'igitekerezo cyo gutanga amasomo y'inyongera.",
        details: "Gerageza kumenya amashuri cyangwa imiryango ikeneye ubufasha mu masomo. Iyi card ni demo gusa; nta mukiriya wemejwe ihagarariye."
      },
      {
        id: 2,
        title: "Amahugurwa y'ibanze ya ICT",
        type: "Amahugurwa",
        district: "Kigali",
        skills: ["ICT"],
        format: "Amahugurwa",
        description: "Icyitegererezo cy'amahirwe yo kongera ubumenyi mu ikoranabuhanga.",
        details: "Mbere yo kwiyandikisha mu mahugurwa nyayo, genzura uyatanga, ikiguzi, igihe n'ibyangombwa bisabwa."
      },
      {
        id: 3,
        title: "Igitekerezo cy'umushinga w'ubuhinzi",
        type: "Kwihangira imirimo",
        district: "Nyagatare",
        skills: ["Ubuhinzi", "Ubucuruzi"],
        format: "Kwihangira imirimo",
        description: "Icyitegererezo cyo gutekereza ku buhinzi n'uburyo bwo kugera ku bakiriya.",
        details: "Kora ubushakashatsi ku isoko ry'aho utuye, ibikoresho bikenewe n'abaguzi bashobora kuboneka mbere yo gushora amafaranga."
      },
      {
        id: 4,
        title: "Gufasha mu bucuruzi no kwamamaza",
        type: "Akazi",
        district: "Huye",
        skills: ["Ubucuruzi", "ICT"],
        format: "Akazi",
        description: "Icyitegererezo cy'umwanya usaba kumenya ubucuruzi n'ikoranabuhanga.",
        details: "Iyi si vacancy nyayo. Ni urugero rwo kwerekana uburyo amakuru y'akazi ashobora kugaragara muri app."
      },
      {
        id: 5,
        title: "Amahugurwa y'ubudozi",
        type: "Amahugurwa",
        district: "Musanze",
        skills: ["Ubudozi"],
        format: "Amahugurwa",
        description: "Icyitegererezo cy'amahirwe yo kwiga ubudozi no guteza imbere ubuhanga.",
        details: "Shaka ikigo cy'amahugurwa cyemewe kandi ugenzure igihe, ikiguzi n'ibyangombwa mbere yo kwiyandikisha."
      },
      {
        id: 6,
        title: "Serivisi z'ubukanishi",
        type: "Kwihangira imirimo",
        district: "Rubavu",
        skills: ["Ubukanishi", "Ubucuruzi"],
        format: "Kwihangira imirimo",
        description: "Icyitegererezo cy'uburyo umuntu ufite ubuhanga mu bukaniishi yakora serivisi.",
        details: "Suzuma ibyo abakiriya bo mu gace kawe bakeneye, ibikoresho n'ibyangombwa bisabwa. Iyi si serivisi yemejwe."
      },
      {
        id: 7,
        title: "Gufasha mu rurimi rwa Kiswahili",
        type: "Kwihangira imirimo",
        district: "Kigali",
        skills: ["Kiswahili"],
        format: "Gutanga amasomo",
        description: "Icyitegererezo cyo gutanga ubufasha mu rurimi rwa Kiswahili.",
        details: "Menya niba hari abakeneye amasomo, utegure gahunda y'amasomo kandi ugenzure uko wakorana n'abakiriya."
      },
      {
        id: 8,
        title: "Kwamamaza ibicuruzwa kuri internet",
        type: "Amahugurwa",
        district: "Huye",
        skills: ["ICT", "Ubucuruzi"],
        format: "Amahugurwa",
        description: "Icyitegererezo cyo kwiga kwamamaza no kumenyekanisha ibicuruzwa kuri internet.",
        details: "Shaka amahugurwa yizewe kandi urebe niba yigisha ubumenyi ushaka. Iyi card ntabwo itanga uburenganzira bwo kwiyandikisha."
      }
    ];

    const form = document.getElementById("searchForm");
    const keywordInput = document.getElementById("keyword");
    const skillSelect = document.getElementById("skill");
    const districtSelect = document.getElementById("district");
    const typeSelect = document.getElementById("type");
    const list = document.getElementById("opportunityList");
    const resultCount = document.getElementById("resultCount");
    const emptyState = document.getElementById("emptyState");

    function escapeHTML(value) {
      return String(value).replace(/[&<>"']/g, function (character) {
        const entities = {
          "&": "&amp;",
          "<": "&lt;",
          ">": "&gt;",
          '"': "&quot;",
          "'": "&#39;"
        };
        return entities[character];
      });
    }

    function getFilteredOpportunities() {
      const keyword = keywordInput.value.trim().toLowerCase();
      const skill = skillSelect.value;
      const district = districtSelect.value;
      const type = typeSelect.value;

      return opportunities.filter(function (item) {
        const searchableText = [
          item.title,
          item.type,
          item.district,
          item.description,
          item.details,
          item.format,
          ...item.skills
        ].join(" ").toLowerCase();

        const matchesKeyword = !keyword || searchableText.includes(keyword);
        const matchesSkill = !skill || item.skills.includes(skill);
        const matchesDistrict = !district || item.district === district;
        const matchesType = !type || item.type === type;

        return matchesKeyword && matchesSkill &&
               matchesDistrict && matchesType;
      });
    }

    function renderOpportunities() {
      const results = getFilteredOpportunities();

      resultCount.textContent =
        results.length + (results.length === 1
          ? " amahirwe y'icyitegererezo"
          : " amahirwe y'icyitegererezo");

      emptyState.hidden = results.length !== 0;
      list.innerHTML = "";

      results.forEach(function (item) {
        const card = document.createElement("article");
        card.className = "opportunity-card";

        card.innerHTML = `
          <div class="card-top">
            <span class="tag">${escapeHTML(item.type)}</span>
            <span class="tag demo-tag">DEMO</span>
          </div>

          <h3>${escapeHTML(item.title)}</h3>

          <div class="meta">
            📍 ${escapeHTML(item.district)}
            &nbsp; · &nbsp;
            ${escapeHTML(item.format)}
          </div>

          <p class="description">${escapeHTML(item.description)}</p>

          <div>
            ${item.skills.map(function (skill) {
              return `<span class="tag">${escapeHTML(skill)}</span>`;
            }).join(" ")}
          </div>

          <div class="details" id="details-${item.id}" hidden>
            ${escapeHTML(item.details)}
          </div>

          <div class="card-actions">
            <button class="button button-light details-button"
                    type="button"
                    aria-expanded="false"
                    aria-controls="details-${item.id}"
                    data-id="${item.id}">
              Reba ibisobanuro
            </button>
          </div>
        `;

        list.appendChild(card);
      });
    }

    form.addEventListener("submit", function (event) {
      event.preventDefault();
      renderOpportunities();
    });

    form.addEventListener("reset", function () {
      setTimeout(renderOpportunities, 0);
    });

    // Guhindura filter bihita bivugurura ibisubizo.
    [keywordInput, skillSelect, districtSelect, typeSelect]
      .forEach(function (control) {
        control.addEventListener("input", renderOpportunities);
        control.addEventListener("change", renderOpportunities);
      });

    list.addEventListener("click", function (event) {
      const button = event.target.closest(".details-button");
      if (!button) return;

      const details = document.getElementById(
        "details-" + button.dataset.id
      );

      const willOpen = details.hidden;
      details.hidden = !willOpen;
      button.setAttribute("aria-expanded", String(willOpen));
      button.textContent = willOpen
        ? "Hisha ibisobanuro"
        : "Reba ibisobanuro";
    });

    document.getElementById("year").textContent =
      new Date().getFullYear();

    renderOpportunities();
  </script>
</body>
</html>
