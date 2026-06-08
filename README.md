
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WOTT 2〜6月 リード分析</title>
<style>
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: -apple-system, BlinkMacSystemFont, 'Hiragino Sans', 'Yu Gothic', sans-serif; background: #f5f4f0; color: #1a1a18; font-size: 14px; max-width: 480px; margin: 0 auto; }
  .header { background: #1a1a18; color: #fff; padding: 16px 16px 14px; }
  .header-title { font-size: 18px; font-weight: 700; margin-bottom: 3px; }
  .header-sub { font-size: 11px; color: #aaa; line-height: 1.7; }
  .section { padding: 12px 12px 0; }
  .section-label { font-size: 10px; font-weight: 700; color: #888; text-transform: uppercase; letter-spacing: 0.08em; margin-bottom: 8px; }
  .grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 8px; }
  .grid3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 6px; margin-bottom: 8px; }
  .grid4 { display: grid; grid-template-columns: 1fr 1fr 1fr 1fr; gap: 5px; margin-bottom: 8px; }
  .metric { background: #fff; border-radius: 10px; padding: 12px 10px; }
  .metric-label { font-size: 10px; color: #888; margin-bottom: 4px; line-height: 1.4; }
  .metric-value { font-size: 24px; font-weight: 700; color: #1a1a18; line-height: 1; }
  .metric-value.red { color: #e24b4a; }
  .metric-value.green { color: #1d9e75; }
  .metric-value.amber { color: #ba7517; }
  .metric-value.purple { color: #7f77dd; }
  .metric-value.sm { font-size: 18px; }
  .metric-sub { font-size: 10px; color: #aaa; margin-top: 3px; }
  .card { background: #fff; border-radius: 10px; padding: 12px; margin-bottom: 8px; }
  .card-title { font-size: 10px; font-weight: 700; color: #888; text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 10px; }
  .bar-row { display: flex; align-items: center; gap: 6px; margin-bottom: 6px; }
  .bar-label { width: 72px; font-size: 11px; color: #666; text-align: right; flex-shrink: 0; }
  .bar-track { flex: 1; background: #f0efe9; border-radius: 3px; height: 20px; overflow: hidden; }
  .bar-fill { height: 100%; border-radius: 3px; display: flex; align-items: center; padding-left: 6px; font-size: 10px; font-weight: 600; white-space: nowrap; overflow: hidden; }
  .bar-num { width: 28px; text-align: right; font-size: 11px; color: #888; flex-shrink: 0; }
  .month-block { margin-bottom: 6px; }
  .month-header { display: flex; justify-content: space-between; align-items: center; font-size: 12px; margin-bottom: 4px; color: #555; }
  .month-val { font-weight: 700; }
  .big-bar-track { background: #f0efe9; border-radius: 4px; height: 28px; overflow: hidden; }
  .big-bar-fill { height: 100%; border-radius: 4px; display: flex; align-items: center; padding-left: 10px; font-size: 12px; font-weight: 700; }
  .tag { display: inline-block; padding: 2px 7px; border-radius: 4px; font-size: 10px; font-weight: 600; }
  .tag-green { background: #e4f2d6; color: #3a6d10; }
  .tag-amber { background: #faeeda; color: #854f0b; }
  .tag-red { background: #fcebeb; color: #a32d2d; }
  .tag-blue { background: #e3f0fb; color: #185fa5; }
  .tag-purple { background: #eeedfe; color: #4a43b5; }
  .lead-item { padding: 9px 10px; background: #f8f7f3; border-radius: 7px; margin-bottom: 6px; }
  .lead-name { font-size: 12px; font-weight: 600; margin-bottom: 2px; }
  .lead-desc { font-size: 11px; color: #777; line-height: 1.4; }
  .divider { border: none; border-top: 0.5px solid #eee; margin: 10px 0; }
  .insight { background: #1a1a18; color: #fff; border-radius: 10px; padding: 13px 14px; margin-bottom: 8px; }
  .insight-title { font-size: 10px; font-weight: 700; color: #aaa; text-transform: uppercase; letter-spacing: 0.06em; margin-bottom: 8px; }
  .insight-item { display: flex; align-items: flex-start; gap: 8px; margin-bottom: 7px; font-size: 12px; line-height: 1.5; }
  .insight-item:last-child { margin-bottom: 0; }
  .dot { width: 6px; height: 6px; border-radius: 50%; flex-shrink: 0; margin-top: 5px; }
  .dot-green { background: #5dca97; }
  .dot-amber { background: #ef9f27; }
  .dot-red { background: #e24b4a; }
  .dot-blue { background: #6ab4f5; }
  .sep { height: 6px; background: #f5f4f0; margin: 4px 0; }
  .hl-green { background: #e4f2d6; border-radius: 8px; padding: 11px 13px; margin-bottom: 8px; }
  .hl-purple { background: #eeedfe; border-radius: 8px; padding: 11px 13px; margin-bottom: 8px; }
  .hl-dark { background: #1a1a18; border-radius: 8px; padding: 11px 13px; margin-bottom: 8px; }
  .hl-title { font-size: 11px; font-weight: 700; margin-bottom: 3px; }
  .hl-value { font-size: 22px; font-weight: 700; }
  .hl-sub { font-size: 11px; margin-top: 3px; line-height: 1.5; }
  table { width: 100%; border-collapse: collapse; font-size: 11px; }
  th { text-align: center; padding: 5px 4px; color: #888; font-weight: 600; font-size: 10px; border-bottom: 0.5px solid #e8e7e2; background: #fafaf7; }
  th:first-child { text-align: left; }
  td { padding: 7px 4px; border-bottom: 0.5px solid #f0efe9; text-align: center; color: #1a1a18; }
  td:first-child { text-align: left; font-weight: 600; }
  tr:last-child td { border-bottom: none; }
  .highlight-row td { background: #f0faf6; }
  .contract-row td { background: #eeedfe; }
  .footer { padding: 16px 12px 32px; text-align: center; font-size: 10px; color: #aaa; }
  .spacer { height: 8px; }

  /* SVGグラフ */
  .chart-container { width: 100%; margin-bottom: 4px; }
  svg { width: 100%; display: block; }
</style>
</head>
<body>

<div class="header">
  <div class="header-title">WOTT リード分析</div>
  <div class="header-sub">2026年2月〜6月8日　No.155〜326<br>成約3件達成 ／ 広告費 月¥500,000</div>
</div>

<!-- 最新成約 -->
<div class="section" style="padding-top:16px;">
  <div class="hl-dark">
    <div class="hl-title" style="color:#aaa;">🎉 成約 3件達成</div>
    <div style="display:flex; flex-direction:column; gap:6px; margin-top:6px;">
      <div style="display:flex; align-items:center; gap:8px;">
        <span style="background:#7f77dd; color:#fff; font-size:10px; font-weight:700; padding:2px 8px; border-radius:4px;">4月</span>
        <span style="color:#fff; font-size:13px; font-weight:700;">No.202 田倉美保</span>
        <span style="background:#1d9e75; color:#fff; font-size:10px; font-weight:700; padding:2px 8px; border-radius:4px;">成約</span>
      </div>
      <div style="display:flex; align-items:center; gap:8px;">
        <span style="background:#7f77dd; color:#fff; font-size:10px; font-weight:700; padding:2px 8px; border-radius:4px;">5月</span>
        <span style="color:#fff; font-size:13px; font-weight:700;">No.279 宇多川隆弘</span>
        <span style="background:#1d9e75; color:#fff; font-size:10px; font-weight:700; padding:2px 8px; border-radius:4px;">成約</span>
      </div>
      <div style="display:flex; align-items:center; gap:8px;">
        <span style="background:#7f77dd; color:#fff; font-size:10px; font-weight:700; padding:2px 8px; border-radius:4px;">5月</span>
        <span style="color:#fff; font-size:13px; font-weight:700;">No.297 長濱真吾</span>
        <span style="background:#1d9e75; color:#fff; font-size:10px; font-weight:700; padding:2px 8px; border-radius:4px;">成約</span>
      </div>
    </div>
  </div>
</div>

<!-- 累計KPI -->
<div class="section">
  <div class="section-label">2月〜6/8 累計</div>
  <div class="grid4">
    <div class="metric">
      <div class="metric-label">問合せ</div>
      <div class="metric-value purple">171+</div>
      <div class="metric-sub">〜6/8途中</div>
    </div>
    <div class="metric">
      <div class="metric-label">アポ獲得</div>
      <div class="metric-value green">約42</div>
      <div class="metric-sub">2〜4月</div>
    </div>
    <div class="metric">
      <div class="metric-label">アポ率</div>
      <div class="metric-value green">45%</div>
      <div class="metric-sub">過去最高水準</div>
    </div>
    <div class="metric">
      <div class="metric-label">成約</div>
      <div class="metric-value green">3件</div>
      <div class="metric-sub">4月・5月</div>
    </div>
  </div>
</div>

<!-- 月別アポ率 -->
<div class="section">
  <div class="section-label">月別 アポ獲得率</div>
  <div class="card">
    <div class="month-block">
      <div class="month-header">
        <span>2月（19件）</span>
        <span class="month-val" style="color:#ef9f27;">32%</span>
      </div>
      <div class="big-bar-track">
        <div class="big-bar-fill" style="width:32%; background:#ef9f27; color:#fff;">32%</div>
      </div>
    </div>
    <div style="height:8px;"></div>
    <div class="month-block">
      <div class="month-header">
        <span>3月（57件）</span>
        <span class="month-val" style="color:#1d9e75;">48%</span>
      </div>
      <div class="big-bar-track">
        <div class="big-bar-fill" style="width:48%; background:#1d9e75; color:#fff;">48%</div>
      </div>
    </div>
    <div style="height:8px;"></div>
    <div class="month-block">
      <div class="month-header">
        <span>4月（48件）<span class="tag tag-purple" style="margin-left:4px;">田倉美保 成約</span></span>
        <span class="month-val" style="color:#1d9e75;">41%</span>
      </div>
      <div class="big-bar-track">
        <div class="big-bar-fill" style="width:41%; background:#1d9e75; color:#fff;">41%</div>
      </div>
    </div>
    <div style="height:8px;"></div>
    <div class="month-block">
      <div class="month-header">
        <span>5月（41件）<span class="tag tag-purple" style="margin-left:4px;">宇多川隆弘 成約</span><span class="tag tag-purple" style="margin-left:4px;">長濱真吾 成約</span></span>
        <span class="month-val" style="color:#7f77dd;">41件</span>
      </div>
      <div class="big-bar-track">
        <div class="big-bar-fill" style="width:41%; background:#7f77dd; color:#fff;">41件</div>
      </div>
    </div>
    <div style="height:8px;"></div>
    <div class="month-block">
      <div class="month-header">
        <span>6月（6件 途中〜6/8）</span>
        <span class="month-val" style="color:#aaa;">集計中</span>
      </div>
      <div class="big-bar-track">
        <div class="big-bar-fill" style="width:10%; background:#b0aaee; color:#555; opacity:0.8;">途中</div>
      </div>
    </div>
    <div style="margin-top:10px; padding:9px 10px; background:#f0faf6; border-radius:7px; font-size:11px; color:#3a6d10; line-height:1.5;">
      3月〜5月に成約が集中。大兼・小林体制の後追いが実を結び、<strong>4月 田倉美保・5月 宇多川隆弘 / 長濱真吾</strong>の成約3件を達成。
    </div>
  </div>
</div>

<!-- CPA推移グラフ（SVG） -->
<div class="section">
  <div class="section-label">月別 CPA推移 × CV数（広告費 月¥500,000）</div>
  <div class="card">
    <div class="card-title">CPA推移（2〜4月確定 ／ 5月途中）</div>
    <!-- SVG棒グラフ: CPA -->
    <!-- 2月:26316 3月:8475 4月:21739 5月:途中 -->
    <!-- max=20万 scale=145/200000=0.000725 -->
    <!-- 2月: 26316*0.000725=19.1→h=19 y=141 / 3月: 8772*0.000725=6.4→h=6 y=154 / 4月: 10416*0.000725=7.6→h=8 y=152 / 5月: 166666*0.000725=120.8→h=121 y=39 -->
    <div class="chart-container">
      <svg viewBox="0 0 340 210" xmlns="http://www.w3.org/2000/svg">
        <line x1="45" y1="15" x2="45" y2="165" stroke="#e8e7e2" stroke-width="1"/>
        <line x1="45" y1="165" x2="320" y2="165" stroke="#e8e7e2" stroke-width="1"/>
        <line x1="45" y1="129" x2="320" y2="129" stroke="#f0efe9" stroke-width="1" stroke-dasharray="3,3"/>
        <line x1="45" y1="92"  x2="320" y2="92"  stroke="#f0efe9" stroke-width="1" stroke-dasharray="3,3"/>
        <line x1="45" y1="56"  x2="320" y2="56"  stroke="#f0efe9" stroke-width="1" stroke-dasharray="3,3"/>
        <text x="40" y="169" text-anchor="end" font-size="9" fill="#aaa">¥0</text>
        <text x="40" y="133" text-anchor="end" font-size="9" fill="#aaa">5万</text>
        <text x="40" y="96"  text-anchor="end" font-size="9" fill="#aaa">10万</text>
        <text x="40" y="60"  text-anchor="end" font-size="9" fill="#aaa">15万</text>

        <!-- 2月 CPA¥26,315 h=19 -->
        <rect x="60"  y="146" width="44" height="19" rx="4" fill="#ef9f27"/>
        <text x="82"  y="140" text-anchor="middle" font-size="9" font-weight="700" fill="#ef9f27">¥26,315</text>

        <!-- 3月 CPA¥8,771 h=6 ★最良 -->
        <rect x="128" y="159" width="44" height="6"  rx="4" fill="#1d9e75"/>
        <text x="150" y="153" text-anchor="middle" font-size="9" font-weight="700" fill="#1d9e75">¥8,771 ★</text>

        <!-- 4月 CPA¥10,416 h=8 成約 -->
        <rect x="196" y="157" width="44" height="8"  rx="4" fill="#7f77dd"/>
        <text x="218" y="151" text-anchor="middle" font-size="9" font-weight="700" fill="#7f77dd">¥10,416</text>

        <!-- 5月 CPA¥11,363 h=55 成約・途中 -->
        <rect x="264" y="110" width="44" height="55"  rx="4" fill="#7f77dd" opacity="0.7"/>
        <text x="286" y="104" text-anchor="middle" font-size="9" font-weight="700" fill="#7f77dd">¥11,363</text>

        <!-- 6月 CPA参考値 h=30 -->
        <rect x="265" y="135" width="44" height="30"  rx="4" fill="#e24b4a" opacity="0.5"/>
        <text x="287" y="129" text-anchor="middle" font-size="9" fill="#e24b4a">¥15,793</text>
        <text x="287" y="141" text-anchor="middle" font-size="8" fill="#e24b4a">参考</text>

        <text x="82"  y="181" text-anchor="middle" font-size="11" font-weight="600" fill="#555">2月</text>
        <text x="150" y="181" text-anchor="middle" font-size="11" font-weight="600" fill="#555">3月</text>
        <text x="219" y="181" text-anchor="middle" font-size="11" font-weight="600" fill="#555">4月</text>
        <text x="287" y="181" text-anchor="middle" font-size="11" font-weight="600" fill="#555">5月</text>
        <text x="287" y="193" text-anchor="middle" font-size="9" fill="#aaa">41件</text>
        <text x="333" y="181" text-anchor="middle" font-size="11" font-weight="600" fill="#555">6月</text>
        <text x="333" y="193" text-anchor="middle" font-size="9" fill="#e24b4a">途中</text>

        <!-- 成約バッジ -->
        <rect x="128" y="167" width="44" height="14" rx="3" fill="#7f77dd"/>
        <text x="150" y="177" text-anchor="middle" font-size="8" font-weight="700" fill="#fff">田倉美保</text>
        <rect x="197" y="167" width="44" height="14" rx="3" fill="#7f77dd"/>
        <text x="219" y="177" text-anchor="middle" font-size="8" font-weight="700" fill="#fff">宇多川隆弘</text>
      </svg>
    </div>

    <!-- CV数SVG -->
    <div class="card-title" style="margin-top:10px;">CV数推移</div>
    <div class="chart-container">
      <svg viewBox="0 0 340 150" xmlns="http://www.w3.org/2000/svg">
        <line x1="45" y1="10"  x2="45" y2="120" stroke="#e8e7e2" stroke-width="1"/>
        <line x1="45" y1="120" x2="320" y2="120" stroke="#e8e7e2" stroke-width="1"/>
        <line x1="45" y1="69"  x2="320" y2="69"  stroke="#f0efe9" stroke-width="1" stroke-dasharray="3,3"/>
        <text x="40" y="124" text-anchor="end" font-size="9" fill="#aaa">0</text>
        <text x="40" y="73"  text-anchor="end" font-size="9" fill="#aaa">30</text>
        <text x="40" y="24"  text-anchor="end" font-size="9" fill="#aaa">60</text>

        <!-- 塗りつぶし（4月まで実線、5月点線） -->
        <polygon points="82,72 150,21 218,40 218,120 150,120 82,120" fill="rgba(55,138,221,0.08)"/>
        <!-- 実線: 2〜4月 -->
        <polyline points="82,72 150,21 218,40" fill="none" stroke="#378add" stroke-width="2.5" stroke-linejoin="round"/>
        <!-- 5月は点線 -->
        <line x1="218" y1="40" x2="219" y2="38" stroke="#378add" stroke-width="2" stroke-dasharray="5,3"/>

        <circle cx="82"  cy="72"  r="5" fill="#ef9f27"/>
        <circle cx="150" cy="21"  r="5" fill="#1d9e75"/>
        <circle cx="218" cy="40"  r="5" fill="#7f77dd"/>
        <circle cx="219" cy="38"  r="5" fill="#7f77dd" stroke="#7f77dd" stroke-width="1.5" opacity="0.7"/>

        <text x="82"  y="63"  text-anchor="middle" font-size="11" font-weight="700" fill="#ef9f27">19</text>
        <text x="150" y="13"  text-anchor="middle" font-size="11" font-weight="700" fill="#1d9e75">57</text>
        <text x="218" y="35"  text-anchor="middle" font-size="11" font-weight="700" fill="#7f77dd">48</text>
        <text x="219" y="30"  text-anchor="middle" font-size="11" font-weight="700" fill="#7f77dd">41</text>
        

        <text x="82"  y="137" text-anchor="middle" font-size="11" font-weight="600" fill="#555">2月</text>
        <text x="150" y="137" text-anchor="middle" font-size="11" font-weight="600" fill="#555">3月</text>
        <text x="218" y="137" text-anchor="middle" font-size="11" font-weight="600" fill="#555">4月</text>
        <text x="219" y="137" text-anchor="middle" font-size="9" fill="#aaa" transform="translate(0,11)">—</text>
        <text x="287" y="137" text-anchor="middle" font-size="11" font-weight="600" fill="#555">5月</text>
        <text x="340" y="137" text-anchor="middle" font-size="11" font-weight="600" fill="#555">6月</text>
      </svg>
    </div>

    <!-- CPA/CV詳細テーブル -->
    <div style="overflow-x:auto; margin-top:8px;">
      <table style="min-width:260px;">
        <thead>
          <tr>
            <th>月</th>
            <th>CV数</th>
            <th>CPA</th>
            <th>成約</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>2月</td>
            <td>19件</td>
            <td style="color:#ba7517; font-weight:700;">¥26,316</td>
            <td style="color:#aaa;">—</td>
          </tr>
          <tr class="highlight-row">
            <td style="color:#1d9e75;">3月 ★</td>
            <td style="font-weight:700;">57件</td>
            <td style="color:#1d9e75; font-weight:700;">¥8,771</td>
            <td style="color:#aaa;">—</td>
          </tr>
          <tr class="contract-row">
            <td>4月</td>
            <td>48件</td>
            <td style="color:#7f77dd; font-weight:700;">¥10,416</td>
            <td><span class="tag tag-purple">田倉美保</span></td>
          </tr>
          <tr class="contract-row">
            <td>5月<small style="color:#aaa;"> 途中</small></td>
            <td style="color:#7f77dd; font-weight:700;">41件</td>
            <td style="color:#7f77dd; font-weight:700;">¥12,195</td>
            <td><span class="tag tag-purple">宇多川隆弘</span><br><span class="tag tag-purple" style="margin-top:3px;display:inline-block;">長濱真吾</span></td>
          </tr>
          <tr>
            <td>6月<small style="color:#aaa;"> 途中</small></td>
            <td style="color:#e24b4a; font-weight:700;">6件</td>
            <td style="color:#e24b4a; font-weight:700;">¥15,793</td>
            <td style="color:#aaa;">—</td>
          </tr>
          <tr style="border-top:1px solid #ddd; background:#f0faf6;">
            <td style="font-weight:700;">合計</td>
            <td style="font-weight:700;">171件+</td>
            <td style="font-weight:700; color:#1d9e75;">¥11,765</td>
            <td><span class="tag tag-green">3件</span></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div style="margin-top:8px; padding:9px 10px; background:#f0faf6; border-radius:7px; font-size:11px; color:#3a6d10; line-height:1.5;">
      3月LP（lp03）切替＋大兼・小林体制でCV 57件達成。CPA <strong>¥8,771</strong> は全期間最低水準。4月 田倉美保・5月 宇多川隆弘 / 長濱真吾 の成約3件を達成。<br>
      <span style="color:#555; font-size:11px;">※5月は44件（途中）。月末にかけてさらにCV積み上がり見込み。</span>
    </div>
  </div>
</div>

<div class="sep"></div>

<!-- 担当別 -->
<div class="section">
  <div class="section-label">担当別 件数（2〜4月）</div>
  <div class="card">
    <div class="bar-row">
      <div class="bar-label">大兼</div>
      <div class="bar-track"><div class="bar-fill" style="width:100%; background:#378add; color:#e6f1fb;">46件</div></div>
      <div class="bar-num">46</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">小林</div>
      <div class="bar-track"><div class="bar-fill" style="width:54%; background:#7f77dd; color:#eeedfe;">25件</div></div>
      <div class="bar-num">25</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">須田</div>
      <div class="bar-track"><div class="bar-fill" style="width:20%; background:#1d9e75; color:#e1f5ee;"></div></div>
      <div class="bar-num">9</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">大谷</div>
      <div class="bar-track"><div class="bar-fill" style="width:13%; background:#d85a30; color:#faece7;"></div></div>
      <div class="bar-num">6</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">その他</div>
      <div class="bar-track"><div class="bar-fill" style="width:9%; background:#888780;"></div></div>
      <div class="bar-num">4</div>
    </div>
    <hr class="divider">
    <div style="font-size:11px; color:#777; line-height:1.5;">大兼・小林の2名で <strong style="color:#1a1a18;">75%</strong> を担当。成約3件もこの体制から生まれた。</div>
  </div>
</div>

<!-- 地域別 -->
<div class="section">
  <div class="section-label">都道府県別 トップ8（2〜4月）</div>
  <div class="card">
    <div class="bar-row">
      <div class="bar-label">愛知県</div>
      <div class="bar-track"><div class="bar-fill" style="width:100%; background:#378add; color:#e6f1fb;">愛知</div></div>
      <div class="bar-num">11</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">北海道</div>
      <div class="bar-track"><div class="bar-fill" style="width:55%; background:#378add; color:#e6f1fb;"></div></div>
      <div class="bar-num">6</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">沖縄県</div>
      <div class="bar-track"><div class="bar-fill" style="width:45%; background:#7f77dd; color:#eeedfe;"></div></div>
      <div class="bar-num">5</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">神奈川県</div>
      <div class="bar-track"><div class="bar-fill" style="width:45%; background:#7f77dd; color:#eeedfe;"></div></div>
      <div class="bar-num">5</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">埼玉県</div>
      <div class="bar-track"><div class="bar-fill" style="width:36%; background:#1d9e75; color:#e1f5ee;"></div></div>
      <div class="bar-num">4</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">香川県</div>
      <div class="bar-track"><div class="bar-fill" style="width:36%; background:#1d9e75; color:#e1f5ee;"></div></div>
      <div class="bar-num">4</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">徳島県</div>
      <div class="bar-track"><div class="bar-fill" style="width:27%; background:#888780;"></div></div>
      <div class="bar-num">3</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">福岡県</div>
      <div class="bar-track"><div class="bar-fill" style="width:27%; background:#888780;"></div></div>
      <div class="bar-num">3</div>
    </div>
    <hr class="divider">
    <div style="font-size:11px; color:#777; line-height:1.5;"><strong style="color:#1a1a18;">愛知・北海道・沖縄</strong>など地方からの流入が拡大。エリアカバレッジは全国規模に。</div>
  </div>
</div>

<!-- 問い合わせ種別 -->
<div class="section">
  <div class="section-label">問い合わせ種別（2〜4月）</div>
  <div class="card">
    <div class="bar-row">
      <div class="bar-label">資料請求</div>
      <div class="bar-track"><div class="bar-fill" style="width:100%; background:#888780; color:#f1efe8;">資料請求</div></div>
      <div class="bar-num">62</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">デモ体験</div>
      <div class="bar-track"><div class="bar-fill" style="width:74%; background:#378add; color:#e6f1fb;">デモ</div></div>
      <div class="bar-num">46</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">代理店希望</div>
      <div class="bar-track"><div class="bar-fill" style="width:69%; background:#7f77dd; color:#eeedfe;">代理店</div></div>
      <div class="bar-num">43</div>
    </div>
    <div class="bar-row">
      <div class="bar-label">その他</div>
      <div class="bar-track"><div class="bar-fill" style="width:6%; background:#d85a30;"></div></div>
      <div class="bar-num">4</div>
    </div>
    <div style="margin-top:10px; padding:8px 10px; background:#f0eefe; border-radius:7px; font-size:11px; color:#534ab7; line-height:1.5;">
      代理店希望が <strong>46%</strong>（全期間30%比 +16pt）。WOTTパートナー制度の認知が急速に広がっている。
    </div>
  </div>
</div>

<!-- 月別詳細テーブル -->
<div class="section">
  <div class="section-label">月別 詳細サマリー</div>
  <div class="card">
    <table>
      <thead>
        <tr>
          <th>月</th>
          <th>件数</th>
          <th>アポ率</th>
          <th>成約</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>2月</td>
          <td>19</td>
          <td><span class="tag tag-amber">32%</span></td>
          <td style="color:#aaa;">—</td>
        </tr>
        <tr class="highlight-row">
          <td>3月</td>
          <td>57</td>
          <td><span class="tag tag-green">48%</span></td>
          <td style="color:#aaa;">—</td>
        </tr>
        <tr class="contract-row">
          <td>4月</td>
          <td>48</td>
          <td><span class="tag tag-green">41%</span></td>
          <td><span class="tag tag-purple">田倉美保</span></td>
        </tr>
        <tr class="contract-row">
          <td>5月<small style="color:#aaa;"> 途中</small></td>
          <td style="color:#e24b4a; font-weight:700;">3</td>
          <td style="color:#aaa;">—</td>
          <td><span class="tag tag-purple">宇多川隆弘</span></td>
        </tr>
        <tr style="border-top:1px solid #ddd; background:#f0faf6;">
          <td>合計</td>
          <td><strong>127</strong></td>
          <td><span class="tag tag-green">45%</span></td>
          <td><span class="tag tag-green">2件</span></td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<!-- インサイト -->
<div class="section">
  <div class="section-label">総括とアクション</div>
  <div class="insight">
    <div class="insight-title">ポジティブ</div>
    <div class="insight-item">
      <div class="dot dot-green"></div>
      <span>成約3件（田倉美保・宇多川隆弘・長濱真吾）を4〜5月で達成。アポ率45%（全期間平均22%の2倍超）が結果につながった。</span>
    </div>
    <div class="insight-item">
      <div class="dot dot-green"></div>
      <span>3月CPA¥8,771は全期間最低水準。lp03切替＋大兼・小林体制の組み合わせが効果を発揮。</span>
    </div>
    <div class="insight-item">
      <div class="dot dot-green"></div>
      <span>代理店希望が46%に急増。WOTTパートナー制度への関心が全国に拡大している。</span>
    </div>
    <div style="height:8px;"></div>
    <div class="insight-title">次のアクション</div>
    <div class="insight-item">
      <div class="dot dot-amber"></div>
      <span>4月48件・5月41件・6月6件（途中）。成約率4〜5%水準が維持できれば月1〜2件ペースが見込める。</span>
    </div>
    <div class="insight-item">
      <div class="dot dot-amber"></div>
      <span>ZOOM確定後の商談→契約転換率をトラッキングし、次のKPI（商談率・契約率）の管理を開始する段階。</span>
    </div>
    <div class="insight-item">
      <div class="dot dot-blue"></div>
      <span>5月問合せが少ない場合、3月に大量流入した57件の後追いリードを掘り起こすタイミング。</span>
    </div>
  </div>
</div>

<div class="spacer"></div>
<div class="footer">WOTT リード管理 ／ 2026年2月〜6月8日 ／ 更新 2026/6/8</div>

</body>
</html>
