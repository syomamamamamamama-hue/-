[axenor_preview_fixed (2).html](https://github.com/user-attachments/files/22735603/axenor_preview_fixed.2.html)
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Axenor – 信念と美学でデジタルを創る</title>
  <meta name="description" content="Axenor｜信念と美学でデジタルを創る。クリエイティブ制作・Webマーケティング・AI導入支援。理念から成果まで伴走。" />
  <style>
    :root{--bg:#f7f8fc;--ink:#131a2a;--muted:#5b6478;--brand:#306CFF;--brand2:#6BD1FF;--gold:#d1b563;--dark:#0f1528;--line:rgba(15,25,45,.12);--card:#fff;--shadow:0 12px 36px rgba(10,20,40,.08);--anim:.6s}
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{margin:0;font-family:'Noto Sans JP',system-ui,-apple-system,'Segoe UI',sans-serif;background:var(--bg);color:var(--ink);position:relative}

    /* 背景の柔らかな動き */
    body::before{content:'';position:fixed;inset:-20vmax;z-index:-1;background:
      radial-gradient(60vmax 60vmax at 110% 120%, rgba(209,181,99,.08),transparent 60%),
      radial-gradient(40vmax 40vmax at -10% -20%, rgba(209,181,99,.06),transparent 60%);
      animation:bgfloat 14s ease-in-out infinite alternate}
    @keyframes bgfloat{from{transform:translate3d(0,0,0)}to{transform:translate3d(2vw,-2vh,0)}}
    @media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}body::before{animation:none}}

    /* Header */
    header{position:sticky;top:0;z-index:60;background:rgba(255,255,255,.85);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
    .nav{display:flex;justify-content:space-between;align-items:center;padding:.9rem 5%}
    .brand{font-weight:900;font-size:1.2rem;letter-spacing:.1em;color:var(--gold)}
    .links{display:flex;gap:1.2rem}
    .links a{color:var(--ink);text-decoration:none;font-weight:700}

    /* Mobile menu */
    .menu-btn{display:none}
    @media (max-width:860px){
      .links{display:none}
      .menu-btn{display:block;border:0;background:transparent;font-size:1.4rem}
      .drawer{position:fixed;inset:0 0 0 auto;width:min(78%,360px);background:#fff;box-shadow:var(--shadow);transform:translateX(100%);transition:transform .35s ease;z-index:70;padding:18px}
      .drawer a{display:block;padding:12px 6px;color:#222;text-decoration:none;border-bottom:1px solid #eee}
      .drawer.show{transform:none}
      .scrim{position:fixed;inset:0;background:rgba(0,0,0,.35);backdrop-filter:blur(2px);opacity:0;pointer-events:none;transition:.3s}
      .scrim.show{opacity:1;pointer-events:auto}
    }

    .wrap{width:min(1200px,92%);margin:auto}

    /* Buttons */
    .btn{display:inline-block;border:0;padding:12px 22px;border-radius:12px;font-weight:800;text-decoration:none}
    .btn-grad{background:linear-gradient(135deg,var(--brand),var(--brand2));color:#fff;box-shadow:0 10px 24px rgba(48,108,255,.25)}
    .btn-ghost{border:1px solid var(--line);background:#fff;color:#1b2333}

    /* Floating contact */
    .floating-contact{position:fixed;right:16px;bottom:16px;z-index:55}
    .floating-contact .btn{padding:14px 18px;border-radius:999px}

    /* HERO */
    .hero{position:relative;isolation:isolate;color:#fff;padding:148px 0 170px;overflow:hidden}
    .hero::before{content:'';position:absolute;inset:0;background:url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?q=80&w=2000&auto=format&fit=crop') center/cover no-repeat;filter:saturate(.95) contrast(1.02)}
    .hero::after{content:'';position:absolute;inset:0;background:linear-gradient(180deg,rgba(12,16,32,.55),rgba(12,16,32,.35));mix-blend:multiply}
    .hero .inner{position:relative;z-index:1;width:min(1200px,92%);margin:auto}
    .hero h1{font-size:clamp(54px,9vw,112px);font-weight:900;letter-spacing:.04em;margin:0 0 10px;background:linear-gradient(90deg,#fff,var(--gold));-webkit-background-clip:text;background-clip:text;color:transparent;animation:titleflow 10s linear infinite}
    @keyframes titleflow{from{background-position:0 0}to{background-position:300% 0}}
    .hero .lead{color:#f7f9ff;max-width:760px;line-height:1.9;text-shadow:0 2px 18px rgba(0,0,0,.45)}

    /* Sections */
    section{padding:92px 0}
    .section-title{font-size:clamp(22px,3.2vw,36px);text-align:center;color:var(--brand);margin:0 0 10px}
    .section-lead{text-align:center;color:var(--muted);max-width:900px;margin:0 auto 28px}

    /* ABOUT */
    .about-grid{display:grid;gap:28px;align-items:center}
    @media(min-width:980px){.about-grid{grid-template-columns:1.1fr .9fr}}
    .about-visual{border-radius:14px;overflow:hidden;border:1px solid var(--line);box-shadow:var(--shadow)}
    .about-visual img{width:100%;aspect-ratio:16/11;object-fit:cover;display:block}

    /* Services summary (Home) */
    .svc-summary{background:#fff;border-top:1px solid var(--line);border-bottom:1px solid var(--line)}
    .svc-list{max-width:1000px;margin:12px auto 0;display:grid;gap:20px}
    .svc-item{display:grid;grid-template-columns:1fr auto;align-items:center;gap:18px;padding:20px;border:1px solid var(--line);border-radius:14px;background:#f9fafc;box-shadow:0 8px 20px rgba(10,20,40,.05)}
    .svc-item h3{margin:.2rem 0 .4rem}
    .svc-item p{margin:0;color:#5b6478}
    .svc-tags{margin-top:10px;display:flex;flex-wrap:wrap;gap:8px}
    .svc-tag{font-size:.78rem;background:#eaeef7;border:1px solid #d9e0f2;border-radius:999px;padding:6px 10px;color:#39435a}
    .svc-go{display:inline-flex;align-items:center;justify-content:center;width:42px;height:42px;border-radius:999px;border:1px solid var(--line);background:#fff;color:#6b748a;text-decoration:none}
    .svc-go:hover{transform:translateY(-1px)}

    /* Services (detail) – alternation */
    .service-stack{max-width:1000px;margin:0 auto;display:grid;gap:56px}
    .svc-row{display:flex;gap:40px;align-items:center;flex-wrap:wrap}
    .svc-row:nth-child(even){flex-direction:row-reverse}
    .svc-row img{width:48%;min-width:320px;border-radius:14px;box-shadow:var(--shadow)}
    .svc-text{flex:1;min-width:300px}
    .svc-text h3{margin:.2rem 0 .6rem}
    .svc-bullets{margin:.2rem 0 1rem;padding-left:18px;color:#5b6478;line-height:1.9}

    /* Works */
    .works{background:linear-gradient(180deg,#f9fafc,#f1f3f8);border-top:1px solid var(--line);border-bottom:1px solid var(--line);text-align:center}

    /* Company */
    .table{border-collapse:collapse;width:100%}
    .table th,.table td{border-bottom:1px solid var(--line);padding:10px 6px;text-align:left}

    /* Contact band */
    .band{background:var(--dark);color:#fff;text-align:center;padding:56px 0}

    /* Reveal motion */
    .reveal{opacity:0;transform:translateY(14px);transition:opacity var(--anim) ease,transform var(--anim) ease}
    .reveal.show{opacity:1;transform:none}

    /* Footer – legal small, brand emphasized */
    footer{background:var(--dark);color:#cfcfd6;text-align:center;padding:36px 0;border-top:1px solid rgba(255,255,255,.05)}
    footer .brand-footer{display:block;font-size:1.08rem;color:#fff;font-weight:800;margin-bottom:6px}
    footer a{color:#cfcfd6;text-decoration:underline;margin:0 8px;font-size:.86rem}

    /* Legal pages text smaller */
    .legal-wrap{max-width:860px;margin:0 auto;line-height:1.85;color:#333;font-size:.9rem}
  </style>
</head>
<body>
  <header>
    <div class="nav">
      <div class="brand">Axenor</div>
      <nav class="links">
        <a href="#/home">Home</a>
        <a href="#/services">Services</a>
        <a href="#/works">Works</a>
        <a href="#/company">Company</a>
        <a href="#/contact">Contact</a>
      </nav>
      <button class="menu-btn" aria-label="menu" onclick="toggleMenu()">☰</button>
    </div>
  </header>
  <div class="scrim" id="scrim" onclick="toggleMenu(false)"></div>
  <aside class="drawer" id="drawer">
    <a href="#/home" onclick="toggleMenu(false)">Home</a>
    <a href="#/services" onclick="toggleMenu(false)">Services</a>
    <a href="#/works" onclick="toggleMenu(false)">Works</a>
    <a href="#/company" onclick="toggleMenu(false)">Company</a>
    <a href="#/contact" onclick="toggleMenu(false)">Contact</a>
  </aside>

  <!-- Floating contact button -->
  <div class="floating-contact"><a class="btn btn-grad" href="#/contact">お問い合わせ</a></div>

  <!-- ============== HOME ============== -->
  <main id="page-home">
    <section class="hero">
      <div class="inner">
        <h1 class="reveal">Axenor</h1>
        <p class="lead reveal" style="transition-delay:.08s">信念と美学で、デジタルの未来をデザインする。</p>
        <div class="reveal" style="margin-top:18px;display:flex;gap:10px"><a class="btn btn-grad" href="#/contact">無料相談</a><a class="btn btn-ghost" href="#/services">サービスを見る</a></div>
      </div>
    </section>

    <section id="philosophy" class="reveal">
      <div class="wrap about-grid">
        <div>
          <h2 class="section-title" style="text-align:left">Philosophy</h2>
          <h3>信念を軸に、未来を創る。</h3>
          <p>私たちAxenorは「美学とテクノロジーの融合」をテーマに、企業や個人が持つ“コア”をデザインを通じて可視化します。表面的な装飾ではなく、理念や想いを軸にしたブランドづくりを大切にします。</p>
          <p>言語化・情報設計・体験設計まで一気通貫。信頼・誠実・美意識をもって、理念から成果まで伴走します。</p>
        </div>
        <div class="about-visual"><img loading="lazy" src="https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1600&auto=format&fit=crop" alt="Workspace"></div>
      </div>
    </section>

    <!-- Services summary only (カードの概要) -->
    <section id="services-summary" class="svc-summary reveal">
      <div class="wrap">
        <h2 class="section-title">Services</h2>
        <p class="section-lead">クリエイティブ制作・Webマーケティング・AI導入支援。理念に基づく設計で、成果へつなげます。</p>
        <div class="svc-list">
          <div class="svc-item">
            <div>
              <h3>クリエイティブ制作</h3>
              <p>ホームページ制作・LP制作・ロゴ/ビジュアルなど、統一された世界観で魅せる表現を。</p>
              <div class="svc-tags"><span class="svc-tag">Web/LP</span><span class="svc-tag">ブランド設計</span><span class="svc-tag">ロゴ/バナー</span></div>
            </div>
            <a class="svc-go" href="#/services" aria-label="go">→</a>
          </div>
          <div class="svc-item">
            <div>
              <h3>Webマーケティング</h3>
              <p>SEO・広告・SNS運用・アクセス分析で、データ起点の成長を設計します。</p>
              <div class="svc-tags"><span class="svc-tag">SEO/GA4</span><span class="svc-tag">広告運用</span><span class="svc-tag">SNS戦略</span></div>
            </div>
            <a class="svc-go" href="#/services" aria-label="go">→</a>
          </div>
          <div class="svc-item">
            <div>
              <h3>AI導入支援</h3>
              <p>ChatGPT活用・自動化・プロンプト設計など、業務効率と品質向上を両立。</p>
              <div class="svc-tags"><span class="svc-tag">ChatGPT</span><span class="svc-tag">自動化</span><span class="svc-tag">運用ガイド</span></div>
            </div>
            <a class="svc-go" href="#/services" aria-label="go">→</a>
          </div>
        </div>
      </div>
    </section>

    <section class="works reveal" id="home-works">
      <div class="wrap">
        <h2 class="section-title">Works</h2>
        <p class="section-lead">実績は現在準備中です。Coming Soon…</p>
        <img loading="lazy" src="https://images.unsplash.com/photo-1529101091764-c3526daf38fe?q=80&w=1600&auto=format&fit=crop" alt="work visual" style="max-width:960px;width:92%;margin:18px auto;border-radius:12px;border:1px solid var(--line);box-shadow:0 8px 24px rgba(10,20,40,.08);display:block">
      </div>
    </section>

    <section id="company" class="reveal">
      <div class="wrap" style="padding-top:8px">
        <h2 class="section-title" style="text-align:left">Company</h2>
        <div class="about-grid">
          <div class="about-visual"><img loading="lazy" src="https://images.unsplash.com/photo-1529336953121-eef04f6b733c?q=80&w=1600&auto=format&fit=crop" alt="office"></div>
          <div>
            <table class="table">
              <tr><th>会社名</th><td>株式会社Axenor（アクセノール）</td></tr>
              <tr><th>代表者</th><td>臼木 翔麻</td></tr>
              <tr><th>事業内容</th><td>クリエイティブ制作／Webマーケティング／AI導入支援／各種デザイン</td></tr>
              <tr><th>所在地</th><td>非掲載（契約書類にて通知）</td></tr>
              <tr><th>設立</th><td>2025年</td></tr>
            </table>
          </div>
        </div>
      </div>
    </section>

    <section class="band reveal" id="home-contact">
      <div class="wrap">
        <h2>Contact</h2>
        <p>ご相談・お見積りはメールでお気軽に。</p>
        <a class="btn btn-grad" href="mailto:info@axenor.jp?subject=%5BAxenor%5D%20お問い合わせ">info@axenor.jp にメールする</a>
      </div>
    </section>
  </main>

  <!-- ============== SERVICES（独立ページ） ============== -->
  <main id="page-services" class="page" style="display:none">
    <section class="hero"><div class="inner"><h1>Services</h1><p class="lead">想いを、デザインと技術で形にする。<br>美学・戦略・テクノロジーの力で、価値の伝わる仕組みをつくります。</p></div></section>
    <section>
      <div class="wrap service-stack">
        <div class="svc-row reveal">
          <img loading="lazy" src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?q=80&w=1600&auto=format&fit=crop" alt="Creative">
          <div class="svc-text"><h3>🎨 クリエイティブ制作</h3>
            <ul class="svc-bullets"><li>ホームページ／LP構成・デザイン・実装</li><li>ブランド・ロゴ・トーン設計</li><li>写真・動画・サムネイル・広告クリエイティブ</li></ul>
            <p>ブランドの“本質”を、形にする。見た目の美しさだけでなく、理念や世界観を可視化するデザインを。WebサイトやLP、ロゴ・ビジュアル制作を通じて、伝えたい“軸”を設計します。美学と情報設計の両面から、見る人の記憶に残る体験を創出。</p>
          </div>
        </div>
        <div class="svc-row reveal">
          <img loading="lazy" src="https://images.unsplash.com/photo-1551281044-8d8d0d8f1ee1?q=80&w=1600&auto=format&fit=crop" alt="Marketing">
          <div class="svc-text"><h3>🌐 Webマーケティング</h3>
            <ul class="svc-bullets"><li>SEO／アクセス分析</li><li>SNS戦略・広告運用</li><li>コンテンツ／LP改善・ファネル設計</li></ul>
            <p>戦略から設計まで、“伝わる仕組み”を。ブランドの想いをデータと戦略で支え、必要な人に確実に届く導線を構築します。感性とロジックの両立で、成果に直結するマーケティングを。</p>
          </div>
        </div>
        <div class="svc-row reveal">
          <img loading="lazy" src="https://images.unsplash.com/photo-1555255707-c07966088b7b?q=80&w=1600&auto=format&fit=crop" alt="AI">
          <div class="svc-text"><h3>🤖 AI導入支援</h3>
            <ul class="svc-bullets"><li>ChatGPT運用支援・プロンプト設計</li><li>自動化</li><li>社内AI教育・運用ガイドライン整備</li></ul>
            <p>創造性と効率を、共存させる。AIは代替ではなく“拡張”のための技術。業務やブランドに最適化して導入し、日々の作業を洗練された体験へ変える仕組み化をデザインします。</p>
          </div>
        </div>
      </div>
    </section>
    <section class="band"><div class="wrap"><a class="btn btn-grad" href="#/contact">お問い合わせはこちら</a></div></section>
  </main>

  <!-- ============== LEGAL & CONTACT（文字小さめ） ============== -->
  <main id="page-privacy" class="page" style="display:none">
    <section class="hero"><div class="inner"><h1>Privacy</h1><p class="lead">個人情報の取り扱い方針について。</p></div></section>
    <section><div class="legal-wrap"><h3>1. 利用目的</h3><p>お問い合わせ対応、業務連絡、サービス提供のため。</p><h3>2. 管理</h3><p>不正アクセス・漏洩・改ざん防止のための安全対策を講じます。</p><h3>3. 第三者提供</h3><p>法令に基づく場合を除き、本人同意なく第三者提供は行いません。</p><h3>4. 開示・訂正・削除</h3><p>要請に応じ適切に対応します。</p><h3>5. 窓口</h3><p>Axenor／<a href="mailto:info@axenor.jp">info@axenor.jp</a></p></div></section>
  </main>

  <main id="page-terms" class="page" style="display:none">
    <section class="hero"><div class="inner"><h1>Terms</h1><p class="lead">サービス利用条件（標準版）。</p></div></section>
    <section><div class="legal-wrap"><h3>第1条（適用）</h3><p>当社提供のすべてのサービスに適用します。</p><h3>第2条（禁止事項）</h3><ul><li>法令・公序良俗に反する行為</li><li>権利侵害・虚偽の情報提供</li><li>運営妨害</li></ul><h3>第3条（変更）</h3><p>事前通知なく内容を変更または中止する場合があります。</p><h3>第4条（免責）</h3><p>提供に際し生じた損害について責任を負いません。</p><h3>第5条（知的財産）</h3><p>コンテンツの権利は当社または権利者に帰属します。</p><h3>第6条（個人情報）</h3><p><a href="#/privacy">プライバシーポリシー</a>に従います。</p></div></section>
  </main>

  <main id="page-disclosure" class="page" style="display:none">
    <section class="hero"><div class="inner"><h1>Electronic Disclosure</h1><p class="lead">登記・法務に関する公告を掲載します。</p></div></section>
    <section class="wrap legal-wrap" style="max-width:960px"><table class="table"><thead><tr><th style="width:180px">掲載日</th><th>内容</th><th style="width:160px">ファイル</th></tr></thead><tbody><tr><td colspan="3" style="color:#7b8597;text-align:center">現在、公告すべき事項はありません。</td></tr></tbody></table></section>
  </main>

  <main id="page-contact" class="page" style="display:none">
    <section class="hero"><div class="inner"><h1>Contact</h1><p class="lead">お仕事・提携・取材のご相談はメールで。</p></div></section>
    <section class="band"><div class="wrap"><a class="btn btn-grad" href="mailto:info@axenor.jp?subject=%5BAxenor%5D%20お問い合わせ">info@axenor.jp にメールする</a></div></section>
  </main>

  <footer>
    <span class="brand-footer">© 2025 Axenor Inc.</span>
    <a href="#/terms">利用規約</a> | <a href="#/privacy">プライバシーポリシー</a> | <a href="#/disclosure">電子公告</a>
  </footer>

  <script>
    // Router（/works・/companyはホーム内スクロール）
    const pages = {
      '/home':'page-home',
      '/services':'page-services',
      '/privacy':'page-privacy',
      '/terms':'page-terms',
      '/disclosure':'page-disclosure',
      '/contact':'page-contact',
      '/works':'page-home',
      '/company':'page-home'
    };

    function route(){
      const key=(location.hash||'#/home').replace('#','');
      document.querySelectorAll('main').forEach(m=>m.style.display='none');
      if(key==='/works' || key==='/company'){
        document.getElementById('page-home').style.display='';
        const sel = (key==='/works') ? '#home-works' : '#company';
        const el = document.querySelector(sel);
        if(el){ window.scrollTo({ top: el.getBoundingClientRect().top + window.scrollY - 80, behavior:'smooth' }); }
      }else{
        const target = document.getElementById(pages[key]) || document.getElementById('page-home');
        target.style.display='';
        window.scrollTo(0,0);
      }
      revealRun();
    }
    addEventListener('hashchange',route);
    addEventListener('load',()=>{ route(); try{ runTests(); }catch(e){} });

    // Reveal motion
    function revealRun(){
      const io=new IntersectionObserver(ents=>{ents.forEach(e=>{if(e.isIntersecting){e.target.classList.add('show');io.unobserve(e.target);}})},{threshold:.1});
      document.querySelectorAll('.reveal').forEach(el=>io.observe(el));
    }

    // Mobile menu toggle
    function toggleMenu(force){
      const d=document.getElementById('drawer');
      const s=document.getElementById('scrim');
      const show = typeof force==='boolean'? force : !d.classList.contains('show');
      d.classList.toggle('show',show); s.classList.toggle('show',show);
    }

    // Tests (routing visible) — 最低限の表示確認
    function runTests(){
      const vis=id=>{const el=document.getElementById(id);return !!el && el.style.display!=='none'};
      const h=location.hash;
      const cases=[
        {hash:'#/home',expect:'page-home'},
        {hash:'#/services',expect:'page-services'},
        {hash:'#/privacy',expect:'page-privacy'},
        {hash:'#/terms',expect:'page-terms'},
        {hash:'#/disclosure',expect:'page-disclosure'},
        {hash:'#/contact',expect:'page-contact'},
        {hash:'#/works',expect:'page-home'},
        {hash:'#/company',expect:'page-home'}
      ];
      cases.forEach(t=>{location.hash=t.hash;route();console.assert(vis(t.expect),'Route test failed',t)});
      location.hash=h||'#/home';route();
    }
  </script>
</body>
</html>
