<style>
  :root{
    --bg: #0b1020;
    --panel: rgba(255,255,255,.06);
    --panel2: rgba(255,255,255,.09);
    --text: rgba(255,255,255,.92);
    --muted: rgba(255,255,255,.72);
    --line: rgba(255,255,255,.12);
    --shadow: 0 20px 60px rgba(0,0,0,.35);
    --radius: 18px;
  }
  .wrap{
    color: var(--text);
    background: radial-gradient(1200px 600px at 20% 0%, rgba(99,102,241,.22), transparent 60%),
                radial-gradient(1000px 600px at 80% 10%, rgba(16,185,129,.14), transparent 60%),
                linear-gradient(180deg, #070a16, var(--bg));
    border: 1px solid var(--line);
    border-radius: 22px;
    padding: 18px;
    box-shadow: var(--shadow);
    font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
  }
  .hero{
    display:flex;
    justify-content:space-between;
    gap:16px;
    align-items:flex-start;
    padding: 16px;
    border-radius: var(--radius);
    background: linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.04));
    border: 1px solid var(--line);
    margin-bottom: 14px;
  }
  .title{ display:flex; gap:12px; align-items:center; }
  .emoji{ font-size: 34px; }
  .hero h1{
    margin:0;
    font-size: 22px;
    letter-spacing: .2px;
  }
  .subtitle{
    margin: 4px 0 0 0;
    color: var(--muted);
    font-size: 13px;
  }
  .meta{ display:flex; flex-wrap:wrap; gap:8px; justify-content:flex-end; }
  .chip{
    background: rgba(255,255,255,.06);
    border: 1px solid var(--line);
    padding: 8px 10px;
    border-radius: 999px;
    font-size: 12.5px;
    color: var(--muted);
    white-space: nowrap;
  }
  .cards{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin: 12px 0 14px;
  }
  @media (max-width: 860px){
    .hero{ flex-direction: column; }
    .meta{ justify-content:flex-start; }
    .cards{ grid-template-columns: 1fr; }
  }
  .card{
    background: rgba(255,255,255,.05);
    border: 1px solid var(--line);
    border-radius: var(--radius);
    padding: 12px 12px;
  }
  .card-h{
    font-weight: 700;
    font-size: 13px;
    color: rgba(255,255,255,.88);
    margin-bottom: 6px;
    letter-spacing: .2px;
  }
  .card-b{
    color: var(--muted);
    font-size: 13px;
    line-height: 1.5;
  }

  .table-shell{
    border: 1px solid var(--line);
    border-radius: var(--radius);
    overflow: hidden;
    background: rgba(255,255,255,.04);
  }
  .table-title{
    padding: 12px 14px;
    font-weight: 800;
    letter-spacing: .2px;
    border-bottom: 1px solid var(--line);
    background: rgba(255,255,255,.06);
  }
  .table-scroll{
    overflow:auto;
    max-height: 72vh;
  }
  table.plan{
    width: 100%;
    border-collapse: separate;
    border-spacing: 0;
    min-width: 880px;
  }
  table.plan th, table.plan td{
    padding: 10px 12px;
    border-bottom: 1px solid var(--line);
    font-size: 13.5px;
  }
  table.plan th{
    position: sticky;
    top: 0;
    z-index: 2;
    background: rgba(17,24,39,.95);
    color: rgba(255,255,255,.92);
    text-align: left;
    font-weight: 700;
    letter-spacing: .25px;
    white-space: nowrap;
    border-bottom: 1px solid rgba(255,255,255,.16);
  }
  table.plan tbody tr:nth-child(odd){ background: rgba(255,255,255,.02); }
  table.plan tbody tr:hover{ background: rgba(99,102,241,.12); }
  table.plan td.section{ max-width: 520px; }
  table.plan td.right, table.plan th.right{ text-align: right; }
  table.plan td.num, table.plan th.num{ width: 56px; text-align: right; }
  table.plan tr.is-off td{ background-image: linear-gradient(90deg, rgba(245,158,11,.10), transparent 60%); }
  .pill{
    display:inline-flex;
    align-items:center;
    gap:6px;
    padding: 4px 10px;
    border-radius: 999px;
    border: 1px solid rgba(255,255,255,.16);
    background: rgba(255,255,255,.05);
    font-size: 12px;
    font-weight: 700;
    color: rgba(255,255,255,.88);
    white-space: nowrap;
  }
  .pill[data-kind="status"]{
    background: rgba(99,102,241,.18);
    border-color: rgba(99,102,241,.35);
  }
  .pill[data-kind="off"]{
    background: rgba(245,158,11,.16);
    border-color: rgba(245,158,11,.38);
  }
  .hint{
    padding: 10px 14px;
    color: var(--muted);
    font-size: 12.5px;
    border-top: 1px solid var(--line);
  }
  details.fallback{
    margin-top: 14px;
    padding: 12px 14px;
    border-radius: var(--radius);
    border: 1px dashed rgba(255,255,255,.20);
    background: rgba(255,255,255,.03);
    color: var(--muted);
  }
  details.fallback summary{
    cursor: pointer;
    font-weight: 700;
    color: rgba(255,255,255,.88);
    margin-bottom: 8px;
  }
  code{
    background: rgba(255,255,255,.08);
    padding: 2px 6px;
    border-radius: 8px;
    border: 1px solid rgba(255,255,255,.10);
  }
</style>

<div class="wrap">
  <div class="hero">
    <div class="title">
      <div class="emoji">📚</div>
      <div>
        <h1>AWS SAA Study Plan</h1>
        <p class="subtitle">Tracker • Styled Markdown (HTML + CSS)</p>
      </div>
    </div>
    <div class="meta">
      <div class="chip">📅 Range: <strong>Feb 1 → Feb 28, 2026</strong></div>
      <div class="chip">🧩 Sections: <strong>33</strong></div>
      <div class="chip">🕒 Updated: <strong>Feb 16, 2026</strong></div>
    </div>
  </div>

  <div class="cards">
    <div class="card">
      <div class="card-h">Legend</div>
      <div class="card-b">
        <span class="pill" data-kind="status">Status</span> = তোমার tracker অনুযায়ী সংখ্যা<br/>
        <span class="pill" data-kind="off">**Off Day**</span> = rest / revision / light day
      </div>
    </div>
    <div class="card">
      <div class="card-h">Note</div>
      <div class="card-b">
        ✅ <strong>Content unchanged</strong> — শুধু outlook সুন্দর করা হয়েছে।<br/>
        ⚠️ কিছু জায়গায় (যেমন GitHub) <code>&lt;style&gt;</code> strip হতে পারে। তখন নিচের fallback table ব্যবহার করবে।
      </div>
    </div>
  </div>

  <div class="table-shell">
    <div class="table-title">📅 Plan Table</div>
    <div class="table-scroll">
      <table class="plan" aria-label="AWS SAA Study Plan Table">
        <thead>
          <tr>
            <th class="num">#</th>
            <th>Section</th>
            <th class="right">Duration</th>
            <th class="right">Remaining</th>
            <th class="right">Status</th>
            <th class="right">Date</th>
            <th>Day</th>
            <th>Off?</th>
          </tr>
        </thead>
        <tbody>
          <tr class="">
        <td class="num">1</td>
        <td class="section">Introduction</td>
        <td class="right">15 min</td>
        <td class="right">27 hr 18 min</td>
        <td class="right"><span class="pill" data-kind="status">1</span></td>
        <td class="right">Feb 1</td>
        <td>Sunday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">2</td>
        <td class="section">Code & Slides Download</td>
        <td class="right">1 min</td>
        <td class="right">27 hr 3 min</td>
        <td class="right"><span class="pill" data-kind="status">1</span></td>
        <td class="right">Feb 1</td>
        <td>Sunday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">3</td>
        <td class="section">Getting started with AWS</td>
        <td class="right">13 min</td>
        <td class="right">27 hr 2 min</td>
        <td class="right"><span class="pill" data-kind="status">1</span></td>
        <td class="right">Feb 1</td>
        <td>Sunday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">4</td>
        <td class="section">IAM & AWS CLI</td>
        <td class="right">57 min</td>
        <td class="right">26 hr 49 min</td>
        <td class="right"><span class="pill" data-kind="status">2</span></td>
        <td class="right">Feb 2</td>
        <td>Monday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">5</td>
        <td class="section">EC2 Fundamentals</td>
        <td class="right">1 hr 39 min</td>
        <td class="right">25 hr 52 min</td>
        <td class="right"><span class="pill" data-kind="status">2</span></td>
        <td class="right">Feb 2</td>
        <td>Monday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">6</td>
        <td class="section">EC2 – SA Level</td>
        <td class="right">34 min</td>
        <td class="right">24 hr 13 min</td>
        <td class="right"><span class="pill" data-kind="status">2</span></td>
        <td class="right">Feb 2</td>
        <td>Monday</td>
        <td>—</td>
      </tr><tr class="is-off">
        <td class="num">7</td>
        <td class="section">EC2 Instance Storage</td>
        <td class="right">59 min</td>
        <td class="right">23 hr 39 min</td>
        <td class="right"><span class="pill" data-kind="status">5</span></td>
        <td class="right">Feb 5</td>
        <td>Thursday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="">
        <td class="num">8</td>
        <td class="section">ELB & ASG</td>
        <td class="right">1 hr 34 min</td>
        <td class="right">22 hr 40 min</td>
        <td class="right"><span class="pill" data-kind="status">5</span></td>
        <td class="right">Feb 16</td>
        <td>Monday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">9</td>
        <td class="section">RDS + Aurora + ElastiCache</td>
        <td class="right">1 hr 10 min</td>
        <td class="right">21 hr 6 min</td>
        <td class="right"><span class="pill" data-kind="status">6</span></td>
        <td class="right">Feb 17</td>
        <td>Tuesday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">10</td>
        <td class="section">Route 53</td>
        <td class="right">1 hr 26 min</td>
        <td class="right">19 hr 56 min</td>
        <td class="right"><span class="pill" data-kind="status">6</span></td>
        <td class="right">Feb 18</td>
        <td>Wednesday</td>
        <td>—</td>
      </tr><tr class="is-off">
        <td class="num">11</td>
        <td class="section">Classic Architectures</td>
        <td class="right">43 min</td>
        <td class="right">18 hr 30 min</td>
        <td class="right"><span class="pill" data-kind="status">7</span></td>
        <td class="right">Feb 19</td>
        <td>Thursday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="">
        <td class="num">12</td>
        <td class="section">S3 Introduction</td>
        <td class="right">50 min</td>
        <td class="right">17 hr 47 min</td>
        <td class="right"><span class="pill" data-kind="status">8</span></td>
        <td class="right">Feb 19</td>
        <td>Thursday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">13</td>
        <td class="section">Advanced S3</td>
        <td class="right">30 min</td>
        <td class="right">16 hr 57 min</td>
        <td class="right"><span class="pill" data-kind="status">8</span></td>
        <td class="right">Feb 20</td>
        <td>Friday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">14</td>
        <td class="section">S3 Security</td>
        <td class="right">53 min</td>
        <td class="right">16 hr 27 min</td>
        <td class="right"><span class="pill" data-kind="status">8</span></td>
        <td class="right">Feb 20</td>
        <td>Friday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">15</td>
        <td class="section">CloudFront & GA</td>
        <td class="right">33 min</td>
        <td class="right">15 hr 34 min</td>
        <td class="right"><span class="pill" data-kind="status">8</span></td>
        <td class="right">Feb 20</td>
        <td>Friday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">16</td>
        <td class="section">Storage Extras</td>
        <td class="right">38 min</td>
        <td class="right">15 hr 1 min</td>
        <td class="right"><span class="pill" data-kind="status">9</span></td>
        <td class="right">Feb 20</td>
        <td>Friday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">17</td>
        <td class="section">SQS, SNS, Kinesis</td>
        <td class="right">1 hr 21 min</td>
        <td class="right">14 hr 23 min</td>
        <td class="right"><span class="pill" data-kind="status">9</span></td>
        <td class="right">Feb 21</td>
        <td>Saturday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">18</td>
        <td class="section">Containers on AWS</td>
        <td class="right">56 min</td>
        <td class="right">13 hr 2 min</td>
        <td class="right"><span class="pill" data-kind="status">9</span></td>
        <td class="right">Feb 21</td>
        <td>Saturday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">19</td>
        <td class="section">Serverless Overview</td>
        <td class="right">1 hr 23 min</td>
        <td class="right">12 hr 6 min</td>
        <td class="right"><span class="pill" data-kind="status">10</span></td>
        <td class="right">Feb 22</td>
        <td>Sunday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">20</td>
        <td class="section">Serverless Architecture</td>
        <td class="right">16 min</td>
        <td class="right">10 hr 43 min</td>
        <td class="right"><span class="pill" data-kind="status">10</span></td>
        <td class="right">Feb 22</td>
        <td>Sunday</td>
        <td>—</td>
      </tr><tr class="is-off">
        <td class="num">21</td>
        <td class="section">Databases in AWS</td>
        <td class="right">26 min</td>
        <td class="right">10 hr 27 min</td>
        <td class="right"><span class="pill" data-kind="status">11</span></td>
        <td class="right">Feb 23</td>
        <td>Monday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">22</td>
        <td class="section">Data & Analytics</td>
        <td class="right">48 min</td>
        <td class="right">10 hr 1 min</td>
        <td class="right"><span class="pill" data-kind="status">11</span></td>
        <td class="right">Feb 23</td>
        <td>Monday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">23</td>
        <td class="section">Machine Learning</td>
        <td class="right">26 min</td>
        <td class="right">9 hr 13 min</td>
        <td class="right"><span class="pill" data-kind="status">11</span></td>
        <td class="right">Feb 23</td>
        <td>Monday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">24</td>
        <td class="section">Monitoring & Audit</td>
        <td class="right">1 hr 15 min</td>
        <td class="right">8 hr 47 min</td>
        <td class="right"><span class="pill" data-kind="status">12</span></td>
        <td class="right">Feb 24</td>
        <td>Tuesday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">25</td>
        <td class="section">IAM – Advanced</td>
        <td class="right">49 min</td>
        <td class="right">7 hr 32 min</td>
        <td class="right"><span class="pill" data-kind="status">13</span></td>
        <td class="right">Feb 25</td>
        <td>Wednesday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">26</td>
        <td class="section">Security & Encryption</td>
        <td class="right">1 hr 25 min</td>
        <td class="right">6 hr 43 min</td>
        <td class="right"><span class="pill" data-kind="status">13</span></td>
        <td class="right">Feb 26</td>
        <td>Thursday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">27</td>
        <td class="section">Networking – VPC</td>
        <td class="right">2 hr 38 min</td>
        <td class="right">5 hr 18 min</td>
        <td class="right"><span class="pill" data-kind="status">14</span></td>
        <td class="right">Feb 27</td>
        <td>Friday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="">
        <td class="num">28</td>
        <td class="section">DR & Migrations</td>
        <td class="right">44 min</td>
        <td class="right">2 hr 40 min</td>
        <td class="right"><span class="pill" data-kind="status">15</span></td>
        <td class="right">Feb 28</td>
        <td>Saturday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">29</td>
        <td class="section">More Architectures</td>
        <td class="right">27 min</td>
        <td class="right">1 hr 56 min</td>
        <td class="right"><span class="pill" data-kind="status">15</span></td>
        <td class="right">Feb 28</td>
        <td>Saturday</td>
        <td>—</td>
      </tr><tr class="">
        <td class="num">30</td>
        <td class="section">Other Services</td>
        <td class="right">48 min</td>
        <td class="right">1 hr 29 min</td>
        <td class="right"><span class="pill" data-kind="status">15</span></td>
        <td class="right">Feb 28</td>
        <td>Saturday</td>
        <td>—</td>
      </tr><tr class="is-off">
        <td class="num">31</td>
        <td class="section">WhitePapers</td>
        <td class="right">15 min</td>
        <td class="right">41 min</td>
        <td class="right"><span class="pill" data-kind="status">16</span></td>
        <td class="right">Feb 28</td>
        <td>Saturday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">32</td>
        <td class="section">Exam + Practice</td>
        <td class="right">17 min</td>
        <td class="right">26 min</td>
        <td class="right"><span class="pill" data-kind="status">16</span></td>
        <td class="right">Feb 28</td>
        <td>Saturday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr><tr class="is-off">
        <td class="num">33</td>
        <td class="section">Congratulations</td>
        <td class="right">9 min</td>
        <td class="right">9 min</td>
        <td class="right"><span class="pill" data-kind="status">16</span></td>
        <td class="right">Feb 28</td>
        <td>Saturday</td>
        <td><span class="pill" data-kind="off">**Off Day**</span></td>
      </tr>
        </tbody>
      </table>
    </div>
    <div class="hint">Tip: Desktop-এ best দেখাবে। Mobile-এ horizontally scroll করো।</div>
  </div>

  <details class="fallback">
    <summary>🔁 Fallback (Pure Markdown Table) — যদি HTML/CSS না দেখায়</summary>
    
| Index | Section | Duration | Remaining Time | Status | Date | Day | Off Day or Not |
|------:|--------|----------|----------------|-------:|------|-----|----------------|
| 1 | Introduction | 15 min | 27 hr 18 min | 1 | Feb 1 | Sunday |   |
| 2 | Code & Slides Download | 1 min | 27 hr 3 min | 1 | Feb 1 | Sunday |   |
| 3 | Getting started with AWS | 13 min | 27 hr 2 min | 1 | Feb 1 | Sunday |   |
| 4 | IAM & AWS CLI | 57 min | 26 hr 49 min | 2 | Feb 2 | Monday |   |
| 5 | EC2 Fundamentals | 1 hr 39 min | 25 hr 52 min | 2 | Feb 2 | Monday |   |
| 6 | EC2 – SA Level | 34 min | 24 hr 13 min | 2 | Feb 2 | Monday |   |
| 7 | EC2 Instance Storage | 59 min | 23 hr 39 min | 5 | Feb 5 | Thursday | **Off Day** |
| 8 | ELB & ASG | 1 hr 34 min | 22 hr 40 min | 5 | Feb 16 | Monday |   |
| 9 | RDS + Aurora + ElastiCache | 1 hr 10 min | 21 hr 6 min | 6 | Feb 17 | Tuesday |   |
| 10 | Route 53 | 1 hr 26 min | 19 hr 56 min | 6 | Feb 18 | Wednesday |   |
| 11 | Classic Architectures | 43 min | 18 hr 30 min | 7 | Feb 19 | Thursday | **Off Day** |
| 12 | S3 Introduction | 50 min | 17 hr 47 min | 8 | Feb 19 | Thursday |   |
| 13 | Advanced S3 | 30 min | 16 hr 57 min | 8 | Feb 20 | Friday |   |
| 14 | S3 Security | 53 min | 16 hr 27 min | 8 | Feb 20 | Friday |   |
| 15 | CloudFront & GA | 33 min | 15 hr 34 min | 8 | Feb 20 | Friday |   |
| 16 | Storage Extras | 38 min | 15 hr 1 min | 9 | Feb 20 | Friday |   |
| 17 | SQS, SNS, Kinesis | 1 hr 21 min | 14 hr 23 min | 9 | Feb 21 | Saturday |   |
| 18 | Containers on AWS | 56 min | 13 hr 2 min | 9 | Feb 21 | Saturday |   |
| 19 | Serverless Overview | 1 hr 23 min | 12 hr 6 min | 10 | Feb 22 | Sunday |   |
| 20 | Serverless Architecture | 16 min | 10 hr 43 min | 10 | Feb 22 | Sunday |   |
| 21 | Databases in AWS | 26 min | 10 hr 27 min | 11 | Feb 23 | Monday | **Off Day** |
| 22 | Data & Analytics | 48 min | 10 hr 1 min | 11 | Feb 23 | Monday | **Off Day** |
| 23 | Machine Learning | 26 min | 9 hr 13 min | 11 | Feb 23 | Monday | **Off Day** |
| 24 | Monitoring & Audit | 1 hr 15 min | 8 hr 47 min | 12 | Feb 24 | Tuesday | **Off Day** |
| 25 | IAM – Advanced | 49 min | 7 hr 32 min | 13 | Feb 25 | Wednesday | **Off Day** |
| 26 | Security & Encryption | 1 hr 25 min | 6 hr 43 min | 13 | Feb 26 | Thursday | **Off Day** |
| 27 | Networking – VPC | 2 hr 38 min | 5 hr 18 min | 14 | Feb 27 | Friday | **Off Day** |
| 28 | DR & Migrations | 44 min | 2 hr 40 min | 15 | Feb 28 | Saturday |   |
| 29 | More Architectures | 27 min | 1 hr 56 min | 15 | Feb 28 | Saturday |   |
| 30 | Other Services | 48 min | 1 hr 29 min | 15 | Feb 28 | Saturday |   |
| 31 | WhitePapers | 15 min | 41 min | 16 | Feb 28 | Saturday | **Off Day** |
| 32 | Exam + Practice | 17 min | 26 min | 16 | Feb 28 | Saturday | **Off Day** |
| 33 | Congratulations | 9 min | 9 min | 16 | Feb 28 | Saturday | **Off Day** |
  </details>
</div>
