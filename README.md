# Baseketball-web
<!DOCTYPE html>

<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lộ Trình Bóng Rổ — 12 Tuổi · 5 Giai Đoạn</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Oswald:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --orange: #FF6B35;
  --orange-light: #FF8C5A;
  --navy: #1B2A4A;
  --navy-light: #2D4270;
  --yellow: #FFD60A;
  --green: #2ECC71;
  --red: #E74C3C;
  --blue: #3498DB;
  --purple: #9B59B6;
  --bg: #F4F6FC;
  --white: #FFFFFF;
  --text: #1B2A4A;
  --gray: #8892A4;
  --light-border: #E2E8F0;
  --card-shadow: 0 4px 24px rgba(27,42,74,0.10);
  --radius: 18px;
  --radius-sm: 10px;
}

- { margin:0; padding:0; box-sizing:border-box; }

body {
background: var(–bg);
color: var(–text);
font-family: ‘Nunito’, sans-serif;
overflow-x: hidden;
}

/* ─── HEADER ─── */
.hero {
background: linear-gradient(135deg, var(–navy) 0%, var(–navy-light) 60%, #3a5a9a 100%);
padding: 48px 32px 80px;
position: relative;
overflow: hidden;
text-align: center;
}
.hero::before {
content: ‘🏀’;
position: absolute;
font-size: 300px;
opacity: 0.04;
top: -40px; right: -60px;
line-height: 1;
pointer-events: none;
}
.hero-badge {
display: inline-flex;
align-items: center;
gap: 8px;
background: rgba(255,107,53,0.18);
border: 1.5px solid rgba(255,107,53,0.5);
border-radius: 50px;
padding: 6px 18px;
font-size: 13px;
color: #FF8C5A;
font-weight: 700;
letter-spacing: 1px;
margin-bottom: 20px;
}
.hero h1 {
font-family: ‘Oswald’, sans-serif;
font-size: clamp(34px, 7vw, 64px);
color: #fff;
font-weight: 700;
line-height: 1.05;
margin-bottom: 12px;
letter-spacing: 0.5px;
}
.hero h1 span { color: var(–orange); }
.hero p {
color: rgba(255,255,255,0.65);
font-size: 15px;
max-width: 560px;
margin: 0 auto 32px;
line-height: 1.7;
}
.hero-stats {
display: flex;
justify-content: center;
gap: 24px;
flex-wrap: wrap;
}
.hstat {
background: rgba(255,255,255,0.08);
border: 1px solid rgba(255,255,255,0.12);
border-radius: var(–radius-sm);
padding: 14px 24px;
text-align: center;
min-width: 110px;
}
.hstat-num {
font-family: ‘Oswald’, sans-serif;
font-size: 30px;
color: var(–yellow);
line-height: 1;
}
.hstat-label { font-size: 11px; color: rgba(255,255,255,0.5); margin-top: 4px; font-weight: 700; letter-spacing: 0.5px; }

/* ─── NAV TABS ─── */
.nav-wrap {
background: var(–white);
border-bottom: 2px solid var(–light-border);
position: sticky;
top: 0;
z-index: 100;
box-shadow: 0 2px 12px rgba(0,0,0,0.07);
}
.nav-tabs {
display: flex;
overflow-x: auto;
padding: 0 16px;
gap: 4px;
scrollbar-width: none;
}
.nav-tabs::-webkit-scrollbar { display: none; }
.tab-btn {
flex-shrink: 0;
padding: 14px 18px;
border: none;
background: none;
cursor: pointer;
font-family: ‘Nunito’, sans-serif;
font-size: 13px;
font-weight: 800;
color: var(–gray);
border-bottom: 3px solid transparent;
transition: all 0.2s;
white-space: nowrap;
display: flex;
align-items: center;
gap: 6px;
}
.tab-btn:hover { color: var(–orange); }
.tab-btn.active { color: var(–orange); border-bottom-color: var(–orange); }

/* ─── MAIN CONTENT ─── */
.content-wrap { max-width: 1060px; margin: 0 auto; padding: 40px 20px 80px; }
.tab-panel { display: none; }
.tab-panel.active { display: block; }

/* ─── SECTION TITLE ─── */
.sec-title {
font-family: ‘Oswald’, sans-serif;
font-size: 28px;
font-weight: 700;
color: var(–navy);
margin-bottom: 6px;
letter-spacing: 0.3px;
}
.sec-sub {
font-size: 14px;
color: var(–gray);
margin-bottom: 28px;
font-weight: 600;
}
.sec-sub span { color: var(–orange); }

/* ─── PHASE HEADER ─── */
.phase-header {
background: linear-gradient(135deg, var(–navy) 0%, var(–navy-light) 100%);
border-radius: var(–radius);
padding: 32px;
margin-bottom: 28px;
display: flex;
align-items: flex-start;
gap: 24px;
position: relative;
overflow: hidden;
}
.phase-header::after {
content: ‘’;
position: absolute;
right: -30px; bottom: -30px;
width: 160px; height: 160px;
border-radius: 50%;
border: 2px solid rgba(255,255,255,0.06);
}
.phase-icon-big {
font-size: 56px;
flex-shrink: 0;
line-height: 1;
filter: drop-shadow(0 4px 8px rgba(0,0,0,0.3));
}
.phase-header h2 {
font-family: ‘Oswald’, sans-serif;
font-size: 26px;
color: #fff;
font-weight: 700;
margin-bottom: 6px;
}
.phase-header p { color: rgba(255,255,255,0.65); font-size: 14px; line-height: 1.6; }
.phase-meta {
display: flex;
gap: 12px;
margin-top: 14px;
flex-wrap: wrap;
}
.pmeta-tag {
background: rgba(255,255,255,0.1);
border-radius: 50px;
padding: 4px 14px;
font-size: 12px;
font-weight: 700;
color: rgba(255,255,255,0.85);
}
.pmeta-tag.orange { background: rgba(255,107,53,0.3); color: #FF8C5A; }

/* ─── SKILL BARS ─── */
.skill-row { margin-bottom: 12px; }
.skill-label { display: flex; justify-content: space-between; font-size: 13px; font-weight: 700; margin-bottom: 5px; }
.skill-label span:last-child { color: var(–orange); }
.skill-bar { height: 8px; background: var(–light-border); border-radius: 50px; overflow: hidden; }
.skill-fill { height: 100%; border-radius: 50px; background: linear-gradient(90deg, var(–orange), var(–yellow)); transition: width 1s ease; }

/* ─── CARDS ─── */
.card {
background: var(–white);
border-radius: var(–radius);
box-shadow: var(–card-shadow);
padding: 24px;
margin-bottom: 20px;
}
.card-title {
font-family: ‘Oswald’, sans-serif;
font-size: 18px;
font-weight: 600;
color: var(–navy);
margin-bottom: 16px;
display: flex;
align-items: center;
gap: 10px;
}
.card-title .icon { font-size: 22px; }

/* ─── GRID ─── */
.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
.grid-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 16px; }
.grid-auto { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }

/* ─── SCHEDULE TABLE ─── */
.schedule-wrap { overflow-x: auto; }
.schedule-table { width: 100%; border-collapse: collapse; font-size: 13px; }
.schedule-table th {
background: var(–navy);
color: #fff;
font-family: ‘Oswald’, sans-serif;
font-weight: 600;
padding: 10px 14px;
text-align: left;
font-size: 13px;
letter-spacing: 0.3px;
}
.schedule-table th:first-child { border-radius: var(–radius-sm) 0 0 0; }
.schedule-table th:last-child { border-radius: 0 var(–radius-sm) 0 0; }
.schedule-table td {
padding: 10px 14px;
border-bottom: 1px solid var(–light-border);
vertical-align: top;
line-height: 1.5;
}
.schedule-table tr:last-child td { border-bottom: none; }
.schedule-table tr:nth-child(even) td { background: #F8FAFE; }
.time-badge {
display: inline-block;
background: var(–navy);
color: #fff;
font-family: ‘Oswald’, sans-serif;
font-size: 12px;
padding: 2px 10px;
border-radius: 50px;
white-space: nowrap;
font-weight: 500;
}
.activity-name { font-weight: 800; color: var(–navy); margin-bottom: 2px; }
.activity-detail { color: var(–gray); font-size: 12px; }
.tag { display: inline-block; border-radius: 50px; padding: 2px 10px; font-size: 11px; font-weight: 800; }
.tag-skill { background: #EBF5FF; color: #2980B9; }
.tag-physical { background: #FFF0EB; color: #E74C3C; }
.tag-mental { background: #F0FBF4; color: #27AE60; }
.tag-rest { background: #F5F0FF; color: #8E44AD; }

/* ─── EXERCISE CARDS ─── */
.exercise-card {
background: var(–white);
border-radius: var(–radius);
box-shadow: var(–card-shadow);
padding: 20px;
border-left: 5px solid var(–orange);
transition: transform 0.2s;
}
.exercise-card:hover { transform: translateY(-2px); }
.exercise-card.blue { border-left-color: var(–blue); }
.exercise-card.green { border-left-color: var(–green); }
.exercise-card.purple { border-left-color: var(–purple); }
.exercise-card.yellow { border-left-color: var(–yellow); }
.ex-header { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; }
.ex-icon { font-size: 28px; }
.ex-title { font-family: ‘Oswald’, sans-serif; font-size: 16px; color: var(–navy); font-weight: 600; }
.ex-meta { font-size: 11px; color: var(–gray); font-weight: 700; }
.ex-body { font-size: 13px; color: #555; line-height: 1.7; }
.ex-steps { list-style: none; margin-top: 10px; }
.ex-steps li {
font-size: 12px;
color: #555;
line-height: 1.6;
padding: 4px 0 4px 20px;
position: relative;
border-bottom: 1px solid var(–light-border);
}
.ex-steps li:last-child { border-bottom: none; }
.ex-steps li::before {
content: counter(step-counter);
counter-increment: step-counter;
position: absolute;
left: 0;
font-family: ‘Oswald’, sans-serif;
font-size: 11px;
color: var(–orange);
font-weight: 700;
}
.ex-steps { counter-reset: step-counter; }
.ex-reps {
margin-top: 10px;
display: flex;
gap: 8px;
flex-wrap: wrap;
}
.rep-badge {
background: var(–bg);
border: 1.5px solid var(–light-border);
border-radius: 50px;
padding: 3px 12px;
font-size: 11px;
font-weight: 800;
color: var(–navy);
}

/* ─── WARNING / MISTAKE CARDS ─── */
.mistake-card {
background: #FFF5F5;
border: 1.5px solid #FDC5C5;
border-radius: var(–radius);
padding: 20px;
}
.mistake-card .m-header {
display: flex;
align-items: center;
gap: 10px;
margin-bottom: 10px;
}
.mistake-card .m-num {
background: var(–red);
color: #fff;
font-family: ‘Oswald’, sans-serif;
font-size: 16px;
width: 30px; height: 30px;
border-radius: 50%;
display: flex;
align-items: center;
justify-content: center;
flex-shrink: 0;
}
.mistake-card .m-title { font-weight: 800; color: var(–red); font-size: 14px; }
.mistake-card .m-body { font-size: 13px; color: #7B3B3B; line-height: 1.6; }
.mistake-card .m-fix {
margin-top: 10px;
background: #FEECEC;
border-radius: var(–radius-sm);
padding: 10px 14px;
font-size: 12px;
color: #C0392B;
font-weight: 700;
}
.mistake-card .m-fix::before { content: ’✅ Cách sửa: ’; }

/* ─── TIP CARDS ─── */
.tip-card {
background: linear-gradient(135deg, #F0FBF4, #E8F8EF);
border: 1.5px solid #A8E6C1;
border-radius: var(–radius);
padding: 16px 20px;
display: flex;
gap: 12px;
align-items: flex-start;
}
.tip-icon { font-size: 22px; flex-shrink: 0; }
.tip-text { font-size: 13px; color: #1A5C35; line-height: 1.6; }
.tip-text strong { display: block; font-size: 14px; margin-bottom: 4px; color: #145A2E; }

/* ─── DAY BREAKDOWN ─── */
.day-grid {
display: grid;
grid-template-columns: repeat(7, 1fr);
gap: 8px;
margin-bottom: 20px;
}
.day-card-mini {
background: var(–white);
border-radius: var(–radius-sm);
padding: 12px 8px;
text-align: center;
box-shadow: 0 2px 8px rgba(0,0,0,0.06);
border: 2px solid transparent;
transition: all 0.2s;
cursor: pointer;
}
.day-card-mini:hover { border-color: var(–orange); }
.day-card-mini.active { border-color: var(–orange); background: #FFF3EE; }
.day-card-mini.rest { background: #F5F0FF; }
.day-name { font-family: ‘Oswald’, sans-serif; font-size: 11px; color: var(–gray); font-weight: 600; margin-bottom: 4px; }
.day-emoji { font-size: 20px; display: block; margin-bottom: 4px; }
.day-type { font-size: 10px; font-weight: 800; }
.day-type.skill { color: var(–orange); }
.day-type.match { color: var(–blue); }
.day-type.physical { color: var(–red); }
.day-type.rest { color: var(–purple); }

/* ─── PROGRESS RING ─── */
.prog-ring-wrap {
display: flex;
flex-direction: column;
align-items: center;
gap: 8px;
}
.prog-ring { position: relative; width: 80px; height: 80px; }
.prog-ring svg { transform: rotate(-90deg); }
.prog-ring circle.bg { fill: none; stroke: #E2E8F0; stroke-width: 8; }
.prog-ring circle.fill { fill: none; stroke-width: 8; stroke-linecap: round; transition: stroke-dashoffset 1.2s ease; }
.prog-val {
position: absolute;
top: 50%; left: 50%;
transform: translate(-50%, -50%);
font-family: ‘Oswald’, sans-serif;
font-size: 18px;
font-weight: 700;
color: var(–navy);
}
.prog-label { font-size: 11px; font-weight: 800; color: var(–gray); text-align: center; }

/* ─── WEEKLY OVERVIEW ─── */
.week-block {
display: flex;
gap: 8px;
background: var(–white);
border-radius: var(–radius);
padding: 20px;
box-shadow: var(–card-shadow);
align-items: stretch;
}
.week-day-col {
flex: 1;
min-width: 0;
border-radius: var(–radius-sm);
padding: 12px 8px;
background: var(–bg);
display: flex;
flex-direction: column;
align-items: center;
gap: 6px;
text-align: center;
}
.week-day-col.highlight { background: linear-gradient(160deg, #FFF3EE, #FFE8DC); border: 1.5px solid #FFB899; }
.week-day-col.rest-day { background: #F5F0FF; }
.wday-name { font-family: ‘Oswald’, sans-serif; font-size: 12px; color: var(–navy); font-weight: 700; }
.wday-icon { font-size: 24px; }
.wday-focus { font-size: 10px; font-weight: 800; color: var(–orange); }
.wday-time { font-size: 10px; color: var(–gray); font-weight: 600; }

/* ─── CHECKLIST ─── */
.checklist { list-style: none; }
.checklist li {
display: flex;
align-items: flex-start;
gap: 10px;
padding: 8px 0;
border-bottom: 1px solid var(–light-border);
font-size: 13px;
line-height: 1.5;
}
.checklist li:last-child { border-bottom: none; }
.checklist li::before {
content: ‘✓’;
background: var(–green);
color: #fff;
font-size: 11px;
font-weight: 900;
width: 20px; height: 20px;
border-radius: 50%;
display: flex;
align-items: center;
justify-content: center;
flex-shrink: 0;
margin-top: 1px;
}

/* ─── NUTRITION ─── */
.meal-card {
background: var(–white);
border-radius: var(–radius);
box-shadow: var(–card-shadow);
overflow: hidden;
}
.meal-header {
padding: 14px 20px;
font-family: ‘Oswald’, sans-serif;
font-size: 15px;
font-weight: 600;
color: #fff;
display: flex;
align-items: center;
gap: 10px;
}
.meal-body { padding: 16px 20px; font-size: 13px; line-height: 1.7; color: #555; }

/* ─── OVERVIEW OVERVIEW ─── */
.overview-phases { display: grid; grid-template-columns: 1fr; gap: 12px; }
.op-card {
background: var(–white);
border-radius: var(–radius);
box-shadow: var(–card-shadow);
padding: 20px 24px;
display: flex;
align-items: center;
gap: 20px;
transition: transform 0.2s;
cursor: pointer;
border: 2px solid transparent;
}
.op-card:hover { transform: translateX(6px); border-color: var(–orange); }
.op-num {
font-family: ‘Oswald’, sans-serif;
font-size: 42px;
color: var(–light-border);
font-weight: 700;
line-height: 1;
flex-shrink: 0;
min-width: 48px;
}
.op-icon { font-size: 36px; flex-shrink: 0; }
.op-info { flex: 1; }
.op-title { font-family: ‘Oswald’, sans-serif; font-size: 18px; color: var(–navy); font-weight: 700; margin-bottom: 2px; }
.op-duration { font-size: 12px; color: var(–orange); font-weight: 800; margin-bottom: 4px; }
.op-desc { font-size: 13px; color: var(–gray); line-height: 1.5; }
.op-bar { height: 5px; background: var(–light-border); border-radius: 50px; margin-top: 10px; overflow: hidden; }
.op-bar-fill { height: 100%; border-radius: 50px; background: linear-gradient(90deg, var(–orange), var(–yellow)); }

/* ─── PROFILE CARD ─── */
.profile-card {
background: linear-gradient(135deg, var(–navy), var(–navy-light));
border-radius: var(–radius);
padding: 28px;
color: #fff;
display: flex;
gap: 24px;
align-items: flex-start;
margin-bottom: 28px;
}
.profile-avatar {
font-size: 70px;
line-height: 1;
flex-shrink: 0;
filter: drop-shadow(0 4px 8px rgba(0,0,0,0.3));
}
.profile-name {
font-family: ‘Oswald’, sans-serif;
font-size: 22px;
font-weight: 700;
margin-bottom: 6px;
}
.profile-tags { display: flex; gap: 8px; flex-wrap: wrap; margin-bottom: 14px; }
.profile-tag {
background: rgba(255,255,255,0.12);
border-radius: 50px;
padding: 4px 12px;
font-size: 11px;
font-weight: 700;
color: rgba(255,255,255,0.85);
}
.profile-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 12px; }
.pstat { text-align: center; background: rgba(255,255,255,0.07); border-radius: 10px; padding: 10px; }
.pstat-val { font-family: ‘Oswald’, sans-serif; font-size: 24px; color: var(–yellow); line-height: 1; }
.pstat-key { font-size: 10px; color: rgba(255,255,255,0.5); font-weight: 700; margin-top: 3px; }

/* ─── TIMELINE ─── */
.roadmap-visual {
position: relative;
padding: 20px 0 0;
}
.roadmap-line {
position: absolute;
left: 28px;
top: 20px; bottom: 0;
width: 3px;
background: linear-gradient(180deg, var(–orange), var(–yellow), var(–green));
border-radius: 3px;
}
.roadmap-item {
display: flex;
gap: 20px;
margin-bottom: 24px;
align-items: flex-start;
position: relative;
}
.roadmap-dot {
width: 58px;
height: 58px;
border-radius: 50%;
background: var(–white);
border: 3px solid var(–orange);
display: flex;
align-items: center;
justify-content: center;
font-size: 22px;
flex-shrink: 0;
box-shadow: 0 4px 12px rgba(255,107,53,0.25);
z-index: 2;
}
.roadmap-content {
flex: 1;
background: var(–white);
border-radius: var(–radius);
box-shadow: var(–card-shadow);
padding: 18px 20px;
border-left: 4px solid var(–orange);
}
.roadmap-content h3 {
font-family: ‘Oswald’, sans-serif;
font-size: 17px;
color: var(–navy);
font-weight: 700;
margin-bottom: 4px;
}
.roadmap-content p { font-size: 13px; color: var(–gray); line-height: 1.6; }
.roadmap-time {
display: inline-block;
background: var(–orange);
color: #fff;
font-size: 10px;
font-weight: 800;
padding: 2px 10px;
border-radius: 50px;
margin-bottom: 8px;
}

/* ─── BADGE ─── */
.badge { display: inline-flex; align-items: center; gap: 6px; border-radius: 50px; padding: 5px 14px; font-size: 12px; font-weight: 800; }
.badge-orange { background: #FFF0EB; color: var(–orange); }
.badge-green { background: #EAFAF1; color: #1E8449; }
.badge-blue { background: #EBF5FF; color: #2471A3; }
.badge-red { background: #FDEDEC; color: var(–red); }

/* ─── DIVIDER ─── */
.divider { height: 1px; background: var(–light-border); margin: 28px 0; }

/* ─── FOOTER ─── */
.footer-note {
background: var(–navy);
color: rgba(255,255,255,0.5);
text-align: center;
padding: 24px;
font-size: 12px;
font-weight: 600;
letter-spacing: 0.5px;
}
.footer-note span { color: var(–orange); }

/* ─── RESPONSIVE ─── */
@media (max-width: 700px) {
.grid-2, .grid-3 { grid-template-columns: 1fr; }
.day-grid { grid-template-columns: repeat(4, 1fr); }
.week-block { flex-wrap: wrap; }
.week-day-col { min-width: calc(50% - 4px); }
.profile-card { flex-direction: column; gap: 16px; }
.profile-stats { grid-template-columns: repeat(3, 1fr); }
.phase-header { flex-direction: column; }
}

/* Animation */
@keyframes fadeInUp {
from { opacity: 0; transform: translateY(20px); }
to { opacity: 1; transform: translateY(0); }
}
.tab-panel.active > * { animation: fadeInUp 0.4s ease forwards; }
</style>

</head>
<body>

<!-- ═══════════ HERO ═══════════ -->

<div class="hero">
  <div class="hero-badge">🏀 Chương Trình Cá Nhân Hóa</div>
  <h1>LỘ TRÌNH<br><span>BÓNG RỔ ĐỈNH CAO</span></h1>
  <p>Được thiết kế riêng cho bé <strong style="color:#fff">12 tuổi · 4 năm kinh nghiệm</strong> — từng ngày, từng bài tập, từng lỗi cần tránh để bứt phá lên top.</p>
  <div class="hero-stats">
    <div class="hstat"><div class="hstat-num">5</div><div class="hstat-label">GIAI ĐOẠN</div></div>
    <div class="hstat"><div class="hstat-num">22+</div><div class="hstat-label">THÁNG</div></div>
    <div class="hstat"><div class="hstat-num">7</div><div class="hstat-label">NGÀY/TUẦN</div></div>
    <div class="hstat"><div class="hstat-num">50+</div><div class="hstat-label">BÀI TẬP</div></div>
  </div>
</div>

<!-- ═══════════ NAV TABS ═══════════ -->

<div class="nav-wrap">
  <div class="nav-tabs">
    <button class="tab-btn active" onclick="switchTab('overview')">🗺️ Tổng quan</button>
    <button class="tab-btn" onclick="switchTab('phase1')">⚡ Giai đoạn 1</button>
    <button class="tab-btn" onclick="switchTab('phase2')">🔥 Giai đoạn 2</button>
    <button class="tab-btn" onclick="switchTab('phase3')">🧠 Giai đoạn 3</button>
    <button class="tab-btn" onclick="switchTab('phase4')">🏆 Giai đoạn 4</button>
    <button class="tab-btn" onclick="switchTab('phase5')">👑 Giai đoạn 5</button>
    <button class="tab-btn" onclick="switchTab('mistakes')">⚠️ Sai lầm</button>
    <button class="tab-btn" onclick="switchTab('nutrition')">🥗 Dinh dưỡng</button>
  </div>
</div>

<div class="content-wrap">

<!-- ══════════════════════════════════════
     TAB: OVERVIEW
══════════════════════════════════════ -->

<div id="tab-overview" class="tab-panel active">

  <!-- Profile -->

  <div class="profile-card">
    <div class="profile-avatar">🧒</div>
    <div style="flex:1">
      <div class="profile-name">Cầu Thủ Trẻ · Cấp Độ Nâng Cao</div>
      <div class="profile-tags">
        <span class="profile-tag">📅 12 tuổi</span>
        <span class="profile-tag">⏱️ 4 năm kinh nghiệm</span>
        <span class="profile-tag">🎯 Mục tiêu: Elite</span>
        <span class="profile-tag">💪 Nền tảng: Tốt</span>
      </div>
      <div class="profile-stats">
        <div class="pstat"><div class="pstat-val">70%</div><div class="pstat-key">NỀN TẢNG KỸ THUẬT</div></div>
        <div class="pstat"><div class="pstat-val">55%</div><div class="pstat-key">THỂ LỰC</div></div>
        <div class="pstat"><div class="pstat-val">45%</div><div class="pstat-key">IQ BÓNG RỔ</div></div>
      </div>
    </div>
  </div>

  <!-- Roadmap visual -->

  <div class="sec-title">🗺️ Lộ Trình Tổng Thể</div>
  <div class="sec-sub">5 giai đoạn · <span>22+ tháng</span> · từ "khá" lên "xuất sắc"</div>

  <div class="overview-phases">
    <div class="op-card" onclick="switchTab('phase1')">
      <div class="op-num">01</div>
      <div class="op-icon">⚡</div>
      <div class="op-info">
        <div class="op-title">NÂNG CẤP NỀN TẢNG</div>
        <div class="op-duration">Tháng 1 – 4 · 16 tuần</div>
        <div class="op-desc">Sửa cơ học chuyển động, củng cố dribble, shooting form và footwork. Bé đã có nền rồi — giờ là lúc nâng lên tầm cao hơn.</div>
        <div class="op-bar"><div class="op-bar-fill" style="width:30%"></div></div>
      </div>
    </div>
    <div class="op-card" onclick="switchTab('phase2')">
      <div class="op-num">02</div>
      <div class="op-icon">🔥</div>
      <div class="op-info">
        <div class="op-title">XÂY KHO KỸ THUẬT</div>
        <div class="op-duration">Tháng 5 – 10 · 24 tuần</div>
        <div class="op-desc">Học combo moves, finishing layers, mid-range game và defensive skills chuyên nghiệp. Xây kho vũ khí không ai đoán được.</div>
        <div class="op-bar"><div class="op-bar-fill" style="width:50%"></div></div>
      </div>
    </div>
    <div class="op-card" onclick="switchTab('phase3')">
      <div class="op-num">03</div>
      <div class="op-icon">🧠</div>
      <div class="op-info">
        <div class="op-title">IQ BÓNG RỔ</div>
        <div class="op-duration">Tháng 11 – 15 · 20 tuần</div>
        <div class="op-desc">Đọc trận, đọc đối thủ, đưa ra quyết định nhanh. Đây là cấp độ phân biệt "chơi được" và "chơi thông minh".</div>
        <div class="op-bar"><div class="op-bar-fill" style="width:65%"></div></div>
      </div>
    </div>
    <div class="op-card" onclick="switchTab('phase4')">
      <div class="op-num">04</div>
      <div class="op-icon">🏆</div>
      <div class="op-info">
        <div class="op-title">THI ĐẤU & ÁP LỰC</div>
        <div class="op-duration">Tháng 16 – 20 · 20 tuần</div>
        <div class="op-desc">Thi đấu nhiều hơn, học cách xử lý áp lực, clutch moments và team leadership. Biến tập luyện thành kết quả thật.</div>
        <div class="op-bar"><div class="op-bar-fill" style="width:80%"></div></div>
      </div>
    </div>
    <div class="op-card" onclick="switchTab('phase5')">
      <div class="op-num">05</div>
      <div class="op-icon">👑</div>
      <div class="op-info">
        <div class="op-title">ELITE — KHÔNG CÓ ĐÍCH ĐẾN</div>
        <div class="op-duration">Tháng 21+ · Cả đời</div>
        <div class="op-desc">Trở thành cầu thủ không thể sao chép. Phong cách riêng, tư duy riêng, hành trình riêng. Không bao giờ ngừng học.</div>
        <div class="op-bar"><div class="op-bar-fill" style="width:95%"></div></div>
      </div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Weekly rhythm overview -->

  <div class="sec-title">📅 Nhịp Điệu Tuần Chuẩn</div>
  <div class="sec-sub">Áp dụng xuyên suốt tất cả giai đoạn, điều chỉnh cường độ theo từng phase</div>

  <div class="week-block">
    <div class="week-day-col">
      <div class="wday-name">THỨ 2</div>
      <div class="wday-icon">⚡</div>
      <div class="wday-focus">KỸ THUẬT</div>
      <div class="wday-time">90 phút</div>
    </div>
    <div class="week-day-col highlight">
      <div class="wday-name">THỨ 3</div>
      <div class="wday-icon">💪</div>
      <div class="wday-focus">THỂ LỰC</div>
      <div class="wday-time">60 phút</div>
    </div>
    <div class="week-day-col">
      <div class="wday-name">THỨ 4</div>
      <div class="wday-icon">🏀</div>
      <div class="wday-focus">KỸ THUẬT</div>
      <div class="wday-time">90 phút</div>
    </div>
    <div class="week-day-col highlight">
      <div class="wday-name">THỨ 5</div>
      <div class="wday-icon">🎯</div>
      <div class="wday-focus">SHOOTING</div>
      <div class="wday-time">75 phút</div>
    </div>
    <div class="week-day-col rest-day">
      <div class="wday-name">THỨ 6</div>
      <div class="wday-icon">😌</div>
      <div class="wday-focus" style="color:#8E44AD">NGHỈ NHẸ</div>
      <div class="wday-time">Kéo giãn</div>
    </div>
    <div class="week-day-col highlight">
      <div class="wday-name">THỨ 7</div>
      <div class="wday-icon">🏟️</div>
      <div class="wday-focus">SCRIMMAGE</div>
      <div class="wday-time">2 tiếng</div>
    </div>
    <div class="week-day-col rest-day">
      <div class="wday-name">CN</div>
      <div class="wday-icon">🛌</div>
      <div class="wday-focus" style="color:#8E44AD">NGHỈ NGƠI</div>
      <div class="wday-time">Recovery</div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- Skill radar summary -->

  <div class="sec-title">📊 Các Kỹ Năng Cần Phát Triển</div>
  <div class="sec-sub">Baseline tại thời điểm bắt đầu — mục tiêu sau 22 tháng</div>
  <div class="card">
    <div style="max-width:520px">
      <div class="skill-row"><div class="skill-label"><span>🏀 Ball Handling</span><span>70% → 95%</span></div><div class="skill-bar"><div class="skill-fill" style="width:70%"></div></div></div>
      <div class="skill-row"><div class="skill-label"><span>🎯 Shooting Form</span><span>60% → 90%</span></div><div class="skill-bar"><div class="skill-fill" style="width:60%"></div></div></div>
      <div class="skill-row"><div class="skill-label"><span>👟 Footwork</span><span>55% → 92%</span></div><div class="skill-bar"><div class="skill-fill" style="width:55%"></div></div></div>
      <div class="skill-row"><div class="skill-label"><span>🛡️ Defense</span><span>50% → 88%</span></div><div class="skill-bar"><div class="skill-fill" style="width:50%"></div></div></div>
      <div class="skill-row"><div class="skill-label"><span>🧠 Basketball IQ</span><span>45% → 90%</span></div><div class="skill-bar"><div class="skill-fill" style="width:45%"></div></div></div>
      <div class="skill-row"><div class="skill-label"><span>💪 Thể lực / Sức bền</span><span>55% → 90%</span></div><div class="skill-bar"><div class="skill-fill" style="width:55%"></div></div></div>
      <div class="skill-row"><div class="skill-label"><span>🏆 Thi đấu / Clutch</span><span>40% → 85%</span></div><div class="skill-bar"><div class="skill-fill" style="width:40%"></div></div></div>
    </div>
  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: PHASE 1
══════════════════════════════════════ -->

<div id="tab-phase1" class="tab-panel">

  <div class="phase-header">
    <div class="phase-icon-big">⚡</div>
    <div>
      <h2>GIAI ĐOẠN 1 — NÂNG CẤP NỀN TẢNG</h2>
      <p>Bé đã chơi 4 năm nên có nhiều thói quen tốt, nhưng cũng có nhiều "bad habits" ăn sâu. Giai đoạn này tập trung phá vỡ giới hạn cũ và xây lại đúng hơn, mạnh hơn.</p>
      <div class="phase-meta">
        <span class="pmeta-tag">📅 Tháng 1–4</span>
        <span class="pmeta-tag">⏱️ 16 tuần</span>
        <span class="pmeta-tag orange">90 phút/buổi · 5 buổi/tuần</span>
      </div>
    </div>
  </div>

  <!-- Daily schedule school day -->

  <div class="sec-title">📋 Lịch Ngày Học (Thứ 2–6)</div>
  <div class="sec-sub">Chia thành buổi sáng ngắn + buổi chiều chính — phù hợp lịch học</div>

  <div class="card">
    <div class="card-title"><span class="icon">🌅</span> Buổi Sáng — Trước Khi Đi Học (15 phút)</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Thời gian</th><th>Bài tập</th><th>Chi tiết</th><th>Loại</th></tr>
        <tr>
          <td><span class="time-badge">6:00–6:05</span></td>
          <td><div class="activity-name">🌊 Uống nước + Activation</div></td>
          <td><div class="activity-detail">Uống 300ml nước, vươn vai 2 phút</div></td>
          <td><span class="tag tag-rest">Khởi động</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">6:05–6:15</span></td>
          <td><div class="activity-name">🏀 Visualization</div></td>
          <td><div class="activity-detail">Nhắm mắt tưởng tượng 10 cú ném hoàn hảo + 5 pha dribble — não bộ kích hoạt neural pathway</div></td>
          <td><span class="tag tag-mental">Tâm lý</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">6:15–6:20</span></td>
          <td><div class="activity-name">⚡ Jumping rope</div></td>
          <td><div class="activity-detail">Nhảy dây 5 phút liên tục — xây fast-twitch muscle fiber và phản xạ chân</div></td>
          <td><span class="tag tag-physical">Thể lực</span></td>
        </tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-title"><span class="icon">🌇</span> Buổi Chiều — Tập Chính (90 phút · 15:30–17:00)</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Thời gian</th><th>Bài tập</th><th>Reps / Sets</th><th>Loại</th></tr>
        <tr>
          <td><span class="time-badge">15:30–15:40</span></td>
          <td><div class="activity-name">🔥 Dynamic Warm-up</div><div class="activity-detail">High knees, butt kicks, lateral shuffle, arm circles</div></td>
          <td>2 vòng × 20m mỗi bài</td>
          <td><span class="tag tag-physical">Warm-up</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">15:40–16:00</span></td>
          <td><div class="activity-name">🏀 Dribble Foundation</div><div class="activity-detail">Stationary dribble: thấp – cao – crossover – between legs – behind back. Tập tay yếu (tay trái) 70% thời gian.</div></td>
          <td>3 sets × 30 giây mỗi kiểu</td>
          <td><span class="tag tag-skill">Kỹ thuật</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">16:00–16:20</span></td>
          <td><div class="activity-name">🎯 Shooting Mechanics</div><div class="activity-detail">Form shooting cận rổ (1–2m): tập BEEF — Balance, Eyes, Elbow, Follow-through. Quay video nhìn lại mỗi 10 cú.</div></td>
          <td>100 cú · tracking mỗi cú</td>
          <td><span class="tag tag-skill">Ném bóng</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">16:20–16:40</span></td>
          <td><div class="activity-name">👟 Footwork Drills</div><div class="activity-detail">Pivot drills (front + reverse), jab step, drop step, close-out footwork. Dùng cones để đánh dấu vị trí chân.</div></td>
          <td>4 bài × 3 phút</td>
          <td><span class="tag tag-skill">Kỹ thuật</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">16:40–16:55</span></td>
          <td><div class="activity-name">🏃 Conditioning</div><div class="activity-detail">Suicide runs (từ vạch end-line), lateral shuffle tốc độ, defensive slides</div></td>
          <td>5 × suicide · 90 giây nghỉ</td>
          <td><span class="tag tag-physical">Thể lực</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">16:55–17:00</span></td>
          <td><div class="activity-name">🧘 Cool-down + Ghi chú</div><div class="activity-detail">Kéo giãn tĩnh. Viết 3 điều học được hôm nay vào sổ tập.</div></td>
          <td>5 phút</td>
          <td><span class="tag tag-rest">Recovery</span></td>
        </tr>
      </table>
    </div>
  </div>

  <div class="card">
    <div class="card-title"><span class="icon">🏟️</span> Thứ 7 — Buổi Tập Dài (120 phút)</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Thời gian</th><th>Bài tập</th><th>Ghi chú</th><th>Loại</th></tr>
        <tr>
          <td><span class="time-badge">8:00–8:15</span></td>
          <td><div class="activity-name">🔥 Warm-up đầy đủ</div></td>
          <td>Chạy nhẹ 3 vòng sân + dynamic stretching</td>
          <td><span class="tag tag-physical">Warm-up</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">8:15–9:00</span></td>
          <td><div class="activity-name">🏀 Full Skill Session</div><div class="activity-detail">Dribble → Shooting → Footwork kết hợp với nhau thành combo</div></td>
          <td>Tập thực tế có chuyển động, không đứng yên</td>
          <td><span class="tag tag-skill">Kỹ thuật</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">9:00–9:45</span></td>
          <td><div class="activity-name">🏟️ Scrimmage 3v3 / 5v5</div><div class="activity-detail">Thi đấu thật sự. Áp dụng tất cả những gì đã tập trong tuần.</div></td>
          <td>Chú ý áp dụng footwork và dribble đúng kỹ thuật</td>
          <td><span class="tag tag-mental">Thi đấu</span></td>
        </tr>
        <tr>
          <td><span class="time-badge">9:45–10:00</span></td>
          <td><div class="activity-name">📹 Film Review + Cool-down</div></td>
          <td>Xem lại video tập, chỉ ra 1 điều tốt + 1 điều cần sửa</td>
          <td><span class="tag tag-mental">Phân tích</span></td>
        </tr>
      </table>
    </div>
  </div>

  <!-- Key exercises phase 1 -->

  <div class="sec-title">🏋️ Bài Tập Chi Tiết — Giai Đoạn 1</div>
  <div class="sec-sub">Những bài quan trọng nhất cần thực hiện đúng kỹ thuật</div>

  <div class="grid-2">
    <div class="exercise-card">
      <div class="ex-header">
        <span class="ex-icon">🏀</span>
        <div>
          <div class="ex-title">Two-Ball Dribble</div>
          <div class="ex-meta">⏱️ 5 phút · Tập hằng ngày</div>
        </div>
      </div>
      <div class="ex-body">Dribble 2 bóng cùng lúc — một bóng lên thì bóng kia xuống (alternating), sau đó cùng lúc (simultaneous). Bài này buộc não phải phối hợp 2 tay đồng đều.</div>
      <ol class="ex-steps">
        <li>Đứng rộng bằng vai, gối hơi cúi</li>
        <li>Alternating: trái xuống khi phải lên — 30 giây</li>
        <li>Simultaneous: 2 bóng cùng xuống — 30 giây</li>
        <li>Di chuyển tiến/lùi trong khi dribble — 60 giây</li>
      </ol>
      <div class="ex-reps">
        <span class="rep-badge">3 sets</span>
        <span class="rep-badge">2 phút/set</span>
        <span class="rep-badge">Tay yếu ưu tiên</span>
      </div>
    </div>

```
<div class="exercise-card blue">
  <div class="ex-header">
    <span class="ex-icon">🎯</span>
    <div>
      <div class="ex-title">Form Shooting Wall</div>
      <div class="ex-meta">⏱️ 10 phút · Tập hằng ngày</div>
    </div>
  </div>
  <div class="ex-body">Đứng cách tường 30cm, ném bóng lên tường và bắt lại. Tập BEEF thuần túy mà không lo bóng vào rổ hay không — chỉ tập form.</div>
  <ol class="ex-steps">
    <li>Một tay (tay ném) giữ bóng ở ear level</li>
    <li>Khuỷu tay vuông góc, thẳng hàng với rổ</li>
    <li>Ném lên tường, follow-through ngón tay chỉ xuống</li>
    <li>Bắt bóng, không để bóng chạm tay kia</li>
  </ol>
  <div class="ex-reps">
    <span class="rep-badge">100 lần/ngày</span>
    <span class="rep-badge">Slow-motion</span>
    <span class="rep-badge">Quay video</span>
  </div>
</div>

<div class="exercise-card green">
  <div class="ex-header">
    <span class="ex-icon">👟</span>
    <div>
      <div class="ex-title">Pivot Master Drill</div>
      <div class="ex-meta">⏱️ 8 phút · 3 lần/tuần</div>
    </div>
  </div>
  <div class="ex-body">Pivot là nền tảng của mọi offensive move. Bài này train front pivot và reverse pivot cho cả 2 chân trụ, giúp tạo góc ném và thoát áp lực phòng thủ.</div>
  <ol class="ex-steps">
    <li>Đứng với bóng, chọn chân trụ (phải hoặc trái)</li>
    <li>Front pivot: quay về phía trước 180° không nhấc chân trụ</li>
    <li>Reverse pivot: quay về phía sau 180°</li>
    <li>Kết hợp: bắt bóng → pivot → jab step → ném hoặc drive</li>
  </ol>
  <div class="ex-reps">
    <span class="rep-badge">20 lần mỗi kiểu</span>
    <span class="rep-badge">Cả 2 chân trụ</span>
  </div>
</div>

<div class="exercise-card purple">
  <div class="ex-header">
    <span class="ex-icon">⚡</span>
    <div>
      <div class="ex-title">Defensive Slide Circuit</div>
      <div class="ex-meta">⏱️ 6 phút · 3 lần/tuần</div>
    </div>
  </div>
  <div class="ex-body">Phòng thủ tốt bắt đầu từ footwork phòng thủ. Bài này train defensive stance và lateral movement — điều mà 90% cầu thủ trẻ bỏ qua.</div>
  <ol class="ex-steps">
    <li>Defensive stance: gối cúi, lưng thẳng, tay rộng</li>
    <li>Trượt ngang 5 bước trái → 5 bước phải × 10 lần</li>
    <li>Drop step: khi đối thủ vượt qua, xoay người đuổi theo</li>
    <li>Close-out drill: chạy đến cầu thủ ném, hất tay lên</li>
  </ol>
  <div class="ex-reps">
    <span class="rep-badge">4 sets</span>
    <span class="rep-badge">90 giây/set</span>
    <span class="rep-badge">Không chéo chân</span>
  </div>
</div>
```

  </div>

  <div class="divider"></div>

  <!-- Tips phase 1 -->

  <div class="sec-title">💡 Điểm Quan Trọng — Giai Đoạn 1</div>
  <div style="display:grid;gap:12px">
    <div class="tip-card"><span class="tip-icon">📸</span><div class="tip-text"><strong>Quay video mỗi buổi tập</strong>Đặt điện thoại góc 45° và quay lại bản thân. Xem lại sau tập — đây là cách duy nhất để thấy lỗi mà mình không cảm nhận được khi đang tập.</div></div>
    <div class="tip-card"><span class="tip-icon">📔</span><div class="tip-text"><strong>Sổ nhật ký tập luyện</strong>Mỗi buổi ghi: 1 điều làm tốt hôm nay + 1 điều cần sửa ngày mai + số bóng vào. Sau 4 tháng nhìn lại sẽ thấy tiến bộ rõ ràng.</div></div>
    <div class="tip-card"><span class="tip-icon">⏰</span><div class="tip-text"><strong>Chất lượng hơn số lượng</strong>90 phút tập tập trung 100% tốt hơn 3 tiếng tập mà đầu óc để đi chỗ khác. Nếu mệt quá, dừng lại — đừng tập sai kỹ thuật để đủ quota.</div></div>
    <div class="tip-card"><span class="tip-icon">🤚</span><div class="tip-text"><strong>Tay yếu = tay quan trọng nhất</strong>Dành 60–70% bài dribble và tập finishing cho tay trái (nếu thuận phải). Đây là vũ khí bí mật mà đối thủ không chuẩn bị phòng thủ.</div></div>
  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: PHASE 2
══════════════════════════════════════ -->

<div id="tab-phase2" class="tab-panel">

  <div class="phase-header">
    <div class="phase-icon-big">🔥</div>
    <div>
      <h2>GIAI ĐOẠN 2 — XÂY KHO KỸ THUẬT</h2>
      <p>Nền tảng đã vững, giờ là lúc xây thêm vũ khí. Mục tiêu: có ít nhất 5 moves khác nhau để vào rổ, một signature move và defensive skills đủ để "lock down" đối thủ.</p>
      <div class="phase-meta">
        <span class="pmeta-tag">📅 Tháng 5–10</span>
        <span class="pmeta-tag">⏱️ 24 tuần</span>
        <span class="pmeta-tag orange">100 phút/buổi · 5 buổi/tuần</span>
      </div>
    </div>
  </div>

  <div class="sec-title">📋 Lịch Tuần Chi Tiết — Giai Đoạn 2</div>

  <div class="card">
    <div class="card-title"><span class="icon">📅</span> Phân Bố Tuần — Thứ 2 đến Chủ Nhật</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Ngày</th><th>Focus chính</th><th>Thời lượng</th><th>Bài tập trọng tâm</th></tr>
        <tr>
          <td><strong>Thứ 2</strong></td>
          <td><span class="badge badge-orange">Offensive Skills</span></td>
          <td>100 phút</td>
          <td>Dribble combos, Euro step, Hesitation move</td>
        </tr>
        <tr>
          <td><strong>Thứ 3</strong></td>
          <td><span class="badge badge-red">Thể lực + Nhảy</span></td>
          <td>75 phút</td>
          <td>Squat jumps, box jumps, agility ladder, suicide</td>
        </tr>
        <tr>
          <td><strong>Thứ 4</strong></td>
          <td><span class="badge badge-orange">Shooting Zones</span></td>
          <td>100 phút</td>
          <td>Mid-range, corner 3, catch-and-shoot, off-dribble</td>
        </tr>
        <tr>
          <td><strong>Thứ 5</strong></td>
          <td><span class="badge badge-blue">Defense Mastery</span></td>
          <td>90 phút</td>
          <td>On-ball defense, help defense, boxing out, steal</td>
        </tr>
        <tr>
          <td><strong>Thứ 6</strong></td>
          <td><span class="tag tag-rest">Nghỉ nhẹ / Yoga</span></td>
          <td>30 phút</td>
          <td>Kéo giãn, yoga, đi bộ nhẹ</td>
        </tr>
        <tr>
          <td><strong>Thứ 7</strong></td>
          <td><span class="badge badge-green">Game Speed + Scrimmage</span></td>
          <td>120 phút</td>
          <td>Tốc độ game thật, thi đấu 3v3 / 5v5</td>
        </tr>
        <tr>
          <td><strong>Chủ nhật</strong></td>
          <td><span class="tag tag-rest">Nghỉ hoàn toàn</span></td>
          <td>—</td>
          <td>Xem phim NBA · Đọc sách · Ngủ sớm</td>
        </tr>
      </table>
    </div>
  </div>

  <!-- Key moves to learn -->

  <div class="sec-title">🎯 5 Moves Cần Học Trong Giai Đoạn 2</div>
  <div class="sec-sub">Học theo thứ tự — mỗi move nắm chắc trước khi qua cái tiếp theo</div>

  <div class="grid-2">
    <div class="exercise-card">
      <div class="ex-header"><span class="ex-icon">🏃</span><div><div class="ex-title">Move 1: Euro Step</div><div class="ex-meta">🗓️ Tuần 1–3 của phase 2</div></div></div>
      <div class="ex-body">Bước đổi hướng để qua người phòng thủ khi drive vào lane. Cực kỳ hiệu quả và khó phòng thủ khi thực hiện đúng.</div>
      <ol class="ex-steps">
        <li>Drive thẳng vào lane ở tốc độ cao</li>
        <li>Bước bên phải (step 1) — người phòng thủ bị lừa</li>
        <li>Bước bên trái (step 2) — vòng qua người phòng thủ</li>
        <li>Lay-up bằng tay trái (hoặc tay phải tùy hướng)</li>
      </ol>
      <div class="ex-reps"><span class="rep-badge">20 lần/buổi</span><span class="rep-badge">Cả 2 bên</span><span class="rep-badge">Tốc độ dần</span></div>
    </div>

```
<div class="exercise-card blue">
  <div class="ex-header"><span class="ex-icon">⏸️</span><div><div class="ex-title">Move 2: Hesitation (Hesi)</div><div class="ex-meta">🗓️ Tuần 4–6</div></div></div>
  <div class="ex-body">Dừng đột ngột khi đang drive để làm người phòng thủ đứng lại, sau đó vụt qua hoặc dừng pull-up jumper. Cực kỳ hiệu quả ở tốc độ cao.</div>
  <ol class="ex-steps">
    <li>Drive về phía rổ ở tốc độ vừa–nhanh</li>
    <li>Hesi: kéo bóng về sát thân — pause 0.3 giây</li>
    <li>Đọc xem người phòng thủ phản ứng thế nào</li>
    <li>Option A: vụt qua nếu họ dừng lại</li>
    <li>Option B: pull-up jumper nếu họ lùi</li>
  </ol>
  <div class="ex-reps"><span class="rep-badge">15 lần/buổi</span><span class="rep-badge">Cả 2 tay</span></div>
</div>

<div class="exercise-card green">
  <div class="ex-header"><span class="ex-icon">🔄</span><div><div class="ex-title">Move 3: Step-Back Jumper</div><div class="ex-meta">🗓️ Tuần 7–10</div></div></div>
  <div class="ex-body">Bước lùi để tạo không gian rồi ném. Đây là signature move của James Harden — cực kỳ khó phòng thủ khi thực hiện nhanh và quyết đoán.</div>
  <ol class="ex-steps">
    <li>Attack close-out của người phòng thủ</li>
    <li>Bước lùi 2 bước ra xa — tạo khoảng cách</li>
    <li>Đứng cân bằng ngay sau bước lùi</li>
    <li>Ném jumper với balance hoàn hảo</li>
  </ol>
  <div class="ex-reps"><span class="rep-badge">20 lần/buổi</span><span class="rep-badge">Từ mid-range</span></div>
</div>

<div class="exercise-card purple">
  <div class="ex-header"><span class="ex-icon">🏀</span><div><div class="ex-title">Move 4: Off-Screen Shooting</div><div class="ex-meta">🗓️ Tuần 11–16</div></div></div>
  <div class="ex-body">Bắt bóng sau khi chạy qua screen và ném ngay lập tức. Đây là cách các shooters chuyên nghiệp tạo ra open shot trong team offense.</div>
  <ol class="ex-steps">
    <li>Chạy vào screen (người đặt chắn) tốc độ cao</li>
    <li>Curl hoặc fade tùy theo người phòng thủ bám thế nào</li>
    <li>Bắt bóng trong tư thế sẵn sàng ném (feet set)</li>
    <li>Ném trong 1 giây sau khi bắt bóng</li>
  </ol>
  <div class="ex-reps"><span class="rep-badge">30 lần/buổi</span><span class="rep-badge">Cả 2 hướng</span></div>
</div>
```

  </div>

  <div class="tip-card" style="margin-top:16px">
    <span class="tip-icon">⭐</span>
    <div class="tip-text">
      <strong>Move 5: Signature Move cá nhân</strong>
      Sau khi học 4 moves trên (tuần 17–24), hãy tạo ra 1 move kết hợp từ các thứ đã học mà phù hợp nhất với thân hình, tốc độ và style của bé. Đây sẽ là "trademark" — cầu thủ nào cũng biết bé có nó nhưng không chặn được.
    </div>
  </div>

  <!-- Physical training phase 2 -->

  <div class="divider"></div>
  <div class="sec-title">💪 Chương Trình Thể Lực — Thứ 3 mỗi tuần</div>

  <div class="card">
    <div class="card-title"><span class="icon">🏋️</span> Circuit Training (75 phút · 12 tuổi = Bodyweight only, KHÔNG tạ nặng)</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Bài tập</th><th>Reps / Thời gian</th><th>Sets</th><th>Nghỉ giữa</th></tr>
        <tr><td><div class="activity-name">🦵 Squat Jump</div><div class="activity-detail">Ngồi xuống như squat, bật nhảy cao nhất có thể, hạ xuống nhẹ nhàng</div></td><td>15 reps</td><td>3</td><td>60 giây</td></tr>
        <tr><td><div class="activity-name">📦 Box Jump</div><div class="activity-detail">Nhảy lên ghế/bục cao 40–50cm, hạ xuống nhẹ — không nhảy xuống mạnh</div></td><td>10 reps</td><td>3</td><td>90 giây</td></tr>
        <tr><td><div class="activity-name">🏃 Agility Ladder</div><div class="activity-detail">In-in-out-out, icky shuffle, hopscotch qua thang nhanh nhất có thể</div></td><td>3 kiểu × 2 vòng</td><td>3</td><td>60 giây</td></tr>
        <tr><td><div class="activity-name">💪 Push-up Variations</div><div class="activity-detail">Standard → Wide → Diamond → Clap push-up (nếu có thể)</div></td><td>10–15 reps mỗi loại</td><td>2</td><td>45 giây</td></tr>
        <tr><td><div class="activity-name">🦵 Lateral Bound</div><div class="activity-detail">Nhảy sang ngang từng chân, giữ thăng bằng khi tiếp đất — train lateral power</div></td><td>10 lần mỗi bên</td><td>3</td><td>60 giây</td></tr>
        <tr><td><div class="activity-name">🏀 Medicine Ball Slam</div><div class="activity-detail">Nâng bóng lên đầu, đập xuống đất mạnh nhất có thể, bắt lại</div></td><td>15 reps</td><td>3</td><td>60 giây</td></tr>
      </table>
    </div>
  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: PHASE 3
══════════════════════════════════════ -->

<div id="tab-phase3" class="tab-panel">

  <div class="phase-header">
    <div class="phase-icon-big">🧠</div>
    <div>
      <h2>GIAI ĐOẠN 3 — IQ BÓNG RỔ</h2>
      <p>Kỹ thuật tốt nhưng không đọc được trận thì vẫn chưa hoàn chỉnh. Giai đoạn này dạy bé cách "nhìn" bóng rổ khác đi — đọc người phòng thủ, đọc đồng đội, và ra quyết định nhanh.</p>
      <div class="phase-meta">
        <span class="pmeta-tag">📅 Tháng 11–15</span>
        <span class="pmeta-tag">⏱️ 20 tuần</span>
        <span class="pmeta-tag orange">Film study 3 lần/tuần</span>
      </div>
    </div>
  </div>

  <div class="sec-title">📋 Lịch Học IQ Bóng Rổ</div>
  <div class="card">
    <div class="card-title"><span class="icon">📺</span> Film Study Schedule — 3 Lần / Tuần (30 phút mỗi lần)</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Buổi</th><th>Nội dung xem</th><th>Câu hỏi cần trả lời</th><th>Ghi chú</th></tr>
        <tr>
          <td><strong>Thứ 2</strong><br><span class="time-badge">8:00–8:30 tối</span></td>
          <td><div class="activity-name">📹 Xem trận mình thi đấu</div></td>
          <td>Tôi ra quyết định sai ở đâu? Có open teammate nào tôi không thấy?</td>
          <td>Tắt âm thanh, chỉ nhìn movement</td>
        </tr>
        <tr>
          <td><strong>Thứ 4</strong><br><span class="time-badge">8:00–8:30 tối</span></td>
          <td><div class="activity-name">📺 Xem 1 trận NBA · Focus vào 1 vị trí</div></td>
          <td>Cầu thủ đó đọc người phòng thủ thế nào? Di chuyển không bóng như thế nào?</td>
          <td>Chọn cầu thủ cùng vị trí với bé</td>
        </tr>
        <tr>
          <td><strong>Thứ 6</strong><br><span class="time-badge">8:00–8:30 tối</span></td>
          <td><div class="activity-name">🗂️ Phân tích đối thủ sắp gặp</div></td>
          <td>Đối thủ thường attack bên nào? Điểm yếu của họ ở đâu? Cách phòng thủ họ?</td>
          <td>Xem 2–3 trận gần nhất của đối thủ</td>
        </tr>
      </table>
    </div>
  </div>

  <div class="sec-title">🧠 Các Concept IQ Cần Học</div>
  <div class="grid-2">
    <div class="card">
      <div class="card-title"><span class="icon">👁️</span> Soft Eyes — Nhìn Rộng</div>
      <p style="font-size:13px;color:#555;line-height:1.7;margin-bottom:14px">Thay vì nhìn chằm chằm vào bóng hoặc rổ, hãy nhìn "mờ" — để peripheral vision (tầm nhìn ngoại vi) tự động thu thập thông tin về cả sân. Đây là bí quyết của các point guard giỏi nhất.</p>
      <div class="tip-card">
        <span class="tip-icon">🏋️</span>
        <div class="tip-text"><strong>Cách tập:</strong>Khi dribble, nhìn vào một điểm trên tường phía xa. Cố gắng "thấy" bóng trong tầm nhìn mà không nhìn trực tiếp. Tập 10 phút mỗi buổi.</div>
      </div>
    </div>

```
<div class="card">
  <div class="card-title"><span class="icon">🗺️</span> Court Mapping — Biết Mình Đứng Đâu</div>
  <p style="font-size:13px;color:#555;line-height:1.7;margin-bottom:14px">Cầu thủ elite luôn biết mình đứng ở đâu trên sân mà không cần nhìn xuống đất. Họ cảm nhận khoảng cách đến đường 3 điểm, đến góc sân, đến rổ.</p>
  <div class="tip-card">
    <span class="tip-icon">🏋️</span>
    <div class="tip-text"><strong>Cách tập:</strong>Nhắm mắt, đứng ngẫu nhiên, sau đó đoán mình đang đứng ở đâu. Mở mắt kiểm tra. Làm 20 lần mỗi buổi — khả năng định vị sân sẽ tự động hóa.</div>
  </div>
</div>

<div class="card">
  <div class="card-title"><span class="icon">⚡</span> Read and React — Đọc → Phản Ứng</div>
  <p style="font-size:13px;color:#555;line-height:1.7;margin-bottom:14px">Học đọc "tín hiệu" từ người phòng thủ: hướng bàn chân, trọng tâm cơ thể, vị trí tay. Từ đó biết trước họ sẽ làm gì và phản ứng trước.</p>
  <ul class="checklist" style="margin-top:10px">
    <li>Chân người phòng thủ lệch trái → drive sang phải</li>
    <li>Trọng tâm về sau → pull-up jumper</li>
    <li>Tay giơ cao → body fake, rồi drive</li>
    <li>Họ bám sát → backdoor cut</li>
  </ul>
</div>

<div class="card">
  <div class="card-title"><span class="icon">🔄</span> Off-Ball Movement — Chuyển Động Không Bóng</div>
  <p style="font-size:13px;color:#555;line-height:1.7;margin-bottom:14px">80% thời gian không có bóng trong tay — nhưng đây là lúc quyết định bé sẽ nhận bóng ở đâu và tạo cơ hội thế nào. Đây là thứ HLV tìm kiếm nhất ở cầu thủ trẻ.</p>
  <ul class="checklist" style="margin-top:10px">
    <li>Luôn di chuyển — không đứng yên khi không có bóng</li>
    <li>Set screen cho đồng đội khi có cơ hội</li>
    <li>V-cut và L-cut để thoát người phòng thủ nhận bóng</li>
    <li>Backdoor cut khi người phòng thủ overplay</li>
  </ul>
</div>
```

  </div>

  <!-- Decision making drills -->

  <div class="divider"></div>
  <div class="sec-title">🎮 Bài Tập Ra Quyết Định Nhanh</div>

  <div class="card">
    <div class="card-title"><span class="icon">⚡</span> 3-Second Decision Drill</div>
    <p style="font-size:13px;color:#555;line-height:1.8;margin-bottom:14px">HLV đứng ở các vị trí khác nhau cầm bóng. Khi tung bóng lên, cầu thủ phải quyết định trong 3 giây: drive, ném, hay pass? Không được do dự.</p>
    <div class="grid-3">
      <div style="background:#FFF3EE;border-radius:10px;padding:14px;text-align:center">
        <div style="font-size:28px;margin-bottom:6px">🏃</div>
        <div style="font-weight:800;font-size:13px;color:#FF6B35">DRIVE</div>
        <div style="font-size:11px;color:#888;margin-top:4px">Người phòng thủ lùi hoặc off-balance</div>
      </div>
      <div style="background:#EBF5FF;border-radius:10px;padding:14px;text-align:center">
        <div style="font-size:28px;margin-bottom:6px">🎯</div>
        <div style="font-weight:800;font-size:13px;color:#2471A3">SHOOT</div>
        <div style="font-size:11px;color:#888;margin-top:4px">Khoảng trống đủ, bàn chân set, tự tin</div>
      </div>
      <div style="background:#EAFAF1;border-radius:10px;padding:14px;text-align:center">
        <div style="font-size:28px;margin-bottom:6px">🤝</div>
        <div style="font-weight:800;font-size:13px;color:#1E8449">PASS</div>
        <div style="font-size:11px;color:#888;margin-top:4px">Đồng đội open, defense collapse về phía mình</div>
      </div>
    </div>
  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: PHASE 4
══════════════════════════════════════ -->

<div id="tab-phase4" class="tab-panel">

  <div class="phase-header">
    <div class="phase-icon-big">🏆</div>
    <div>
      <h2>GIAI ĐOẠN 4 — THI ĐẤU & ÁP LỰC</h2>
      <p>Kỹ năng và IQ đã có, nhưng thi đấu thật dưới áp lực là thứ khác hoàn toàn. Giai đoạn này train bé chơi tốt ngay cả khi sợ, mệt, hay đội đang thua.</p>
      <div class="phase-meta">
        <span class="pmeta-tag">📅 Tháng 16–20</span>
        <span class="pmeta-tag">⏱️ 20 tuần</span>
        <span class="pmeta-tag orange">Thi đấu ≥ 2 lần/tuần</span>
      </div>
    </div>
  </div>

  <div class="sec-title">🧠 Xây Dựng Tâm Lý Thi Đấu</div>
  <div class="grid-2">
    <div class="card">
      <div class="card-title"><span class="icon">🎯</span> Pre-Game Routine (30 phút trước thi đấu)</div>
      <div class="schedule-wrap">
        <table class="schedule-table">
          <tr><th>Thời gian</th><th>Hoạt động</th></tr>
          <tr><td><span class="time-badge">30 phút trước</span></td><td><div class="activity-name">🎧 Nghe nhạc tạo năng lượng</div><div class="activity-detail">Playlist cá nhân đã chọn sẵn — tạo trạng thái tâm lý nhất quán</div></td></tr>
          <tr><td><span class="time-badge">20 phút trước</span></td><td><div class="activity-name">🏃 Warm-up cơ thể</div><div class="activity-detail">Chạy nhẹ, dynamic stretch, lateral slides, form shooting nhẹ</div></td></tr>
          <tr><td><span class="time-badge">10 phút trước</span></td><td><div class="activity-name">🧘 Visualization</div><div class="activity-detail">Nhắm mắt 3 phút — hình dung 5 pha chơi đẹp nhất của mình trong trận hôm nay</div></td></tr>
          <tr><td><span class="time-badge">5 phút trước</span></td><td><div class="activity-name">🔥 Affirmation + Focus word</div><div class="activity-detail">Chọn 1 từ cho trận hôm nay: "AGGRESSIVE" / "CALM" / "DEFEND" / "SHOOT"</div></td></tr>
        </table>
      </div>
    </div>

```
<div class="card">
  <div class="card-title"><span class="icon">📊</span> Post-Game Review (Sau thi đấu)</div>
  <ul class="checklist">
    <li><strong>Điều tốt nhất tôi làm hôm nay là gì?</strong> (Tìm ít nhất 3 điều — không phụ thuộc vào thắng thua)</li>
    <li><strong>Quyết định nào tôi hối hận nhất?</strong> (1 điều — không tự trách nhiều)</li>
    <li><strong>Tôi đã áp dụng được kỹ thuật đã tập không?</strong></li>
    <li><strong>Tâm lý tôi thế nào khi bị thua hoặc bị áp lực?</strong></li>
    <li><strong>Tuần tới tôi sẽ tập gì để cải thiện?</strong></li>
  </ul>
</div>
```

  </div>

  <!-- Pressure drills -->

  <div class="sec-title">⚡ Bài Tập Áp Lực Cao</div>
  <div class="grid-2">
    <div class="exercise-card">
      <div class="ex-header"><span class="ex-icon">⏰</span><div><div class="ex-title">Last-Second Free Throw</div><div class="ex-meta">Tập clutch moment</div></div></div>
      <div class="ex-body">Sau khi chạy suicide 5 lần (mệt hết sức), bước vào vạch ném phạt và ném 2 quả. Simulate tình huống thi đấu thật khi cơ thể mệt nhưng phải thực hiện tốt.</div>
      <div class="ex-reps"><span class="rep-badge">5 sets</span><span class="rep-badge">Sau conditioning</span><span class="rep-badge">Track tỷ lệ %</span></div>
    </div>

```
<div class="exercise-card blue">
  <div class="ex-header"><span class="ex-icon">🎰</span><div><div class="ex-title">Random Drill Challenge</div><div class="ex-meta">Quyết định dưới áp lực</div></div></div>
  <div class="ex-body">HLV hoặc bạn tập gọi ngẫu nhiên: "LEFT!" "3-POINTER!" "EURO!" và cầu thủ phải thực hiện ngay trong 2 giây. Train phản xạ không cần suy nghĩ.</div>
  <div class="ex-reps"><span class="rep-badge">10 phút/buổi</span><span class="rep-badge">Tốc độ cao</span><span class="rep-badge">Không được dừng</span></div>
</div>
```

  </div>

  <div class="divider"></div>
  <div class="sec-title">🏟️ Kế Hoạch Thi Đấu — Giai Đoạn 4</div>
  <div class="card">
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Loại thi đấu</th><th>Tần suất</th><th>Mục tiêu</th></tr>
        <tr><td><div class="activity-name">🏀 Pickup game / Sân mở</div></td><td>2–3 lần/tuần</td><td>Thử moves mới không sợ thất bại</td></tr>
        <tr><td><div class="activity-name">🏟️ Giải đấu học sinh</div></td><td>1–2 giải/học kỳ</td><td>Trải nghiệm áp lực thật sự</td></tr>
        <tr><td><div class="activity-name">⭐ Chơi vs người lớn hơn</div></td><td>1 lần/tuần</td><td>Bị thử thách — học từ người giỏi hơn</td></tr>
        <tr><td><div class="activity-name">🤝 3v3 competitive</div></td><td>Cuối tuần</td><td>Decision making nhanh trong không gian nhỏ</td></tr>
      </table>
    </div>
  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: PHASE 5
══════════════════════════════════════ -->

<div id="tab-phase5" class="tab-panel">

  <div class="phase-header">
    <div class="phase-icon-big">👑</div>
    <div>
      <h2>GIAI ĐOẠN 5 — ELITE · KHÔNG CÓ ĐÍCH ĐẾN</h2>
      <p>Đây không phải giai đoạn kết thúc — đây là nơi hành trình thật sự bắt đầu. Cầu thủ elite không bao giờ nghĩ mình đã đủ giỏi.</p>
      <div class="phase-meta">
        <span class="pmeta-tag">📅 Tháng 21+</span>
        <span class="pmeta-tag">⏱️ Cả đời</span>
        <span class="pmeta-tag orange">Cá nhân hóa hoàn toàn</span>
      </div>
    </div>
  </div>

  <div class="sec-title">👑 Đặc Điểm Của Cầu Thủ Elite Cùng Tuổi</div>
  <div class="grid-3">
    <div style="background:var(--white);border-radius:var(--radius);box-shadow:var(--card-shadow);padding:24px;text-align:center">
      <div style="font-size:40px;margin-bottom:12px">📚</div>
      <div style="font-family:'Oswald',sans-serif;font-size:16px;color:var(--navy);margin-bottom:8px">STUDENT OF THE GAME</div>
      <div style="font-size:12px;color:var(--gray);line-height:1.7">Luôn học. Xem phim, đọc sách, hỏi HLV. Không bao giờ nói "Tôi biết rồi" — luôn hỏi "Còn cách nào tốt hơn không?"</div>
    </div>
    <div style="background:var(--white);border-radius:var(--radius);box-shadow:var(--card-shadow);padding:24px;text-align:center">
      <div style="font-size:40px;margin-bottom:12px">🤝</div>
      <div style="font-family:'Oswald',sans-serif;font-size:16px;color:var(--navy);margin-bottom:8px">TEAM LEADER</div>
      <div style="font-size:12px;color:var(--gray);line-height:1.7">Encourage đồng đội. Dạy lại người mới những gì mình biết. Cầu thủ giỏi nhất thường là người cổ vũ nhiệt tình nhất cho đồng đội.</div>
    </div>
    <div style="background:var(--white);border-radius:var(--radius);box-shadow:var(--card-shadow);padding:24px;text-align:center">
      <div style="font-size:40px;margin-bottom:12px">🔄</div>
      <div style="font-family:'Oswald',sans-serif;font-size:16px;color:var(--navy);margin-bottom:8px">CONTINUOUS EVOLUTION</div>
      <div style="font-size:12px;color:var(--gray);line-height:1.7">Mỗi mùa giải thêm 1 kỹ năng mới vào "kho vũ khí". Không bao giờ hài lòng — nhưng cũng không quên ăn mừng những tiến bộ đã đạt được.</div>
    </div>
  </div>

  <div class="divider"></div>
  <div class="sec-title">📅 Lịch Hàng Năm — Phase Elite</div>
  <div class="card">
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Giai đoạn năm</th><th>Focus</th><th>Hoạt động chính</th></tr>
        <tr><td><strong>Mùa hè</strong><br>(Jun–Aug)</td><td><span class="badge badge-orange">Phát triển kỹ năng</span></td><td>Tập luyện cường độ cao · Skill camps · Summer league · Thêm 1 kỹ năng mới</td></tr>
        <tr><td><strong>Pre-season</strong><br>(Sep–Oct)</td><td><span class="badge badge-blue">Chuẩn bị</span></td><td>Team practice · Conditioning peak · Chiến thuật · Scrimmages</td></tr>
        <tr><td><strong>Mùa giải</strong><br>(Nov–Mar)</td><td><span class="badge badge-green">Thi đấu</span></td><td>Maintain skills · Recovery ưu tiên · Film study · Thi đấu tốt nhất</td></tr>
        <tr><td><strong>Off-season</strong><br>(Apr–May)</td><td><span class="tag tag-rest">Recovery + Đánh giá</span></td><td>Nghỉ ngơi · Xem lại năm qua · Lên kế hoạch cho năm tới · Cross-sport training</td></tr>
      </table>
    </div>
  </div>

  <div class="tip-card" style="margin-top:20px">
    <span class="tip-icon">🌟</span>
    <div class="tip-text">
      <strong>Triết lý của elite 12 tuổi</strong>
      Ở tuổi 12, mục tiêu không phải là trở thành NBA player ngay — mà là yêu bóng rổ đủ để kiên trì 10 năm tiếp theo. Cầu thủ tốt nhất ở tuổi 22 là người vui vẻ và đam mê nhất lúc 12 tuổi, không nhất thiết là người giỏi nhất lúc đó.
    </div>
  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: MISTAKES
══════════════════════════════════════ -->

<div id="tab-mistakes" class="tab-panel">

  <div class="sec-title">⚠️ 12 Sai Lầm Hay Mắc Nhất</div>
  <div class="sec-sub">Của cầu thủ trẻ 10–14 tuổi · Đọc kỹ để tránh lặp lại</div>

  <div class="grid-2">
    <div class="mistake-card">
      <div class="m-header"><div class="m-num">1</div><div class="m-title">Nhìn xuống bóng khi dribble</div></div>
      <div class="m-body">Đây là sai lầm #1 của hầu hết cầu thủ trẻ. Khi nhìn bóng, bé mù hoàn toàn với phần còn lại của sân, đồng đội và người phòng thủ.</div>
      <div class="m-fix">Dán một tờ giấy lên kính hoặc nhìn vào mắt người đứng đối diện khi dribble. Tập cho đến khi cảm giác bóng nằm trong tay không cần nhìn.</div>
    </div>

```
<div class="mistake-card">
  <div class="m-header"><div class="m-num">2</div><div class="m-title">Khuỷu tay mở ra khi ném</div></div>
  <div class="m-body">Khuỷu tay "chicken wing" — mở ra bên ngoài thay vì thẳng hướng về rổ — là nguyên nhân ném lệch trái hoặc phải nhất quán.</div>
  <div class="m-fix">Đặt một chiếc sách mỏng kẹp vào nách tay ném trong khi tập. Nếu sách rơi là khuỷu tay đang mở sai. Tập form shooting 100 lần/ngày với sách.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">3</div><div class="m-title">Tập toàn tay mạnh, bỏ qua tay yếu</div></div>
  <div class="m-body">90% cầu thủ trẻ drive, dribble và ném toàn bằng tay thuận. Người phòng thủ học được điều này trong 5 phút và ép bé về phía tay yếu mọi lúc.</div>
  <div class="m-fix">Quy tắc 70/30: 70% thời gian dribbling tập tay yếu, 30% tay mạnh. Đây là quy tắc cứng trong ít nhất 6 tháng đầu.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">4</div><div class="m-title">Không follow-through khi ném</div></div>
  <div class="m-body">"Gà bới" — ném bóng xong tay thu về ngay lập tức thay vì giữ pose. Thiếu follow-through làm giảm backspin và accuracy cực kỳ nhiều.</div>
  <div class="m-fix">Sau mỗi cú ném, giữ tay ở vị trí follow-through (ngón tay chỉ xuống như đang "nhúng tay vào rổ") cho đến khi bóng chạm rổ hoặc bảng.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">5</div><div class="m-title">Đứng yên khi không có bóng</div></div>
  <div class="m-body">Khi đồng đội cầm bóng, bé đứng xem. Đây là điều tệ nhất có thể làm — người phòng thủ không cần để ý đến bé, team mất 1 người tạo cơ hội.</div>
  <div class="m-fix">Quy tắc "2 giây không bóng": sau 2 giây không có bóng trong tay, BẮT BUỘC phải di chuyển. V-cut, L-cut, set screen, hoặc ít nhất là đổi vị trí.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">6</div><div class="m-title">Phòng thủ thiếu tập trung</div></div>
  <div class="m-body">Nhiều cầu thủ trẻ chỉ muốn tấn công, coi phòng thủ là "công việc buồn chán". Nhưng HLV giỏi chọn cầu thủ defensive trước tiên.</div>
  <div class="m-fix">Mỗi buổi tập, dành ít nhất 20 phút chỉ cho defensive drills. Tập defensive slides, on-ball defense, và boxing out. Track xem mình block được bao nhiêu shot hoặc steal được bao nhiêu bóng.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">7</div><div class="m-title">Tập quá nhiều không nghỉ đủ</div></div>
  <div class="m-body">Cơ thể 12 tuổi đang phát triển — tập 7 ngày/7 liên tục không chỉ không hiệu quả mà còn gây chấn thương xương khớp nghiêm trọng.</div>
  <div class="m-fix">1–2 ngày nghỉ hoàn toàn mỗi tuần là bắt buộc. Sleep 9–10 tiếng mỗi đêm. Nếu có đau xương hoặc gân, nghỉ ngay và gặp bác sĩ thể thao.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">8</div><div class="m-title">Ném quá xa so với sức</div></div>
  <div class="m-body">Cố ném 3 điểm khi cơ thể chưa đủ mạnh → form bị méo, bóng thiếu arc, xây thói quen xấu. Phổ biến nhất ở độ tuổi 10–13.</div>
  <div class="m-fix">Xác định "shooting range" hiện tại — khoảng cách xa nhất mà form vẫn đẹp. Chỉ tập từ đó trở vào. Mỗi tháng thêm 30–50cm sau khi nắm chắc.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">9</div><div class="m-title">Không học từ sai lầm trong thi đấu</div></div>
  <div class="m-body">Thua trận rồi quên. Không review lại, không phân tích tại sao thua, không rút ra bài học. Tiếp tục lặp lại sai lầm cũ.</div>
  <div class="m-fix">Sau mỗi trận (thắng hay thua), viết ít nhất 3 điều vào sổ. Xem lại video nếu có thể. Tập luyện tuần sau phải address ít nhất 1 điểm yếu đã phát hiện.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">10</div><div class="m-title">So sánh mình với người khác</div></div>
  <div class="m-body">Thấy bạn khác cao hơn, nhanh hơn, ném tốt hơn → nản lòng → bỏ tập. So sánh với người khác phá hủy động lực dài hạn.</div>
  <div class="m-fix">Chỉ so sánh với bản thân 1 tháng trước. Câu hỏi duy nhất: "Tháng này tôi giỏi hơn tháng trước không?" Nếu có → đang đi đúng đường.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">11</div><div class="m-title">Bỏ qua khởi động và kéo giãn</div></div>
  <div class="m-body">Nhảy vào tập ngay không khởi động. Kết thúc tập không kéo giãn. Ở tuổi 12, gân và cơ chưa hoàn thiện — chấn thương có thể ảnh hưởng cả sự nghiệp.</div>
  <div class="m-fix">10 phút dynamic warm-up BẮT BUỘC trước tập. 5–10 phút static stretching BẮT BUỘC sau tập. Đặc biệt chú ý đầu gối, mắt cá chân và cổ tay.</div>
</div>

<div class="mistake-card">
  <div class="m-header"><div class="m-num">12</div><div class="m-title">Mất bình tĩnh khi thi đấu</div></div>
  <div class="m-body">Bị foul, bị chê, đội đang thua → nổi giận, chơi liều, mất kiểm soát. Tâm lý bất ổn phá hủy tất cả kỹ thuật đã tập.</div>
  <div class="m-fix">Học "reset routine": khi cảm thấy tức giận, hít thở sâu 3 lần, nói với mình "next play" và focus vào pha bóng tiếp theo. Tập ritual này trong luyện tập hằng ngày.</div>
</div>
```

  </div>

</div>

<!-- ══════════════════════════════════════
     TAB: NUTRITION
══════════════════════════════════════ -->

<div id="tab-nutrition" class="tab-panel">

  <div class="sec-title">🥗 Dinh Dưỡng Cho Cầu Thủ 12 Tuổi</div>
  <div class="sec-sub">Cơ thể đang phát triển cần nhiên liệu đúng — ăn uống ảnh hưởng 30% hiệu suất tập luyện</div>

  <div class="tip-card" style="margin-bottom:24px">
    <span class="tip-icon">⚠️</span>
    <div class="tip-text">
      <strong>Lưu ý quan trọng cho phụ huynh</strong>
      Ở tuổi 12, KHÔNG cần supplement protein, creatine hay bất kỳ thực phẩm chức năng nào. Cơ thể phát triển tự nhiên qua thức ăn thật. Tập trung vào bữa ăn cân bằng và ngủ đủ giấc.
    </div>
  </div>

  <div class="grid-2">
    <div class="meal-card">
      <div class="meal-header" style="background:linear-gradient(135deg,#FF8C00,#FFB347)">🌅 Bữa Sáng (Trước Khi Đi Học)</div>
      <div class="meal-body">
        <strong style="color:#333">Ngày có tập chiều:</strong><br>
        🍚 Cơm hoặc bánh mì nguyên cám (carbs cho năng lượng) · 🥚 2–3 trứng (protein) · 🥛 1 ly sữa · 🍌 1 quả chuối<br><br>
        <strong style="color:#333">Ngày không tập:</strong><br>
        🍜 Phở hoặc cháo · 🥛 Sữa · 🍊 Trái cây theo mùa<br><br>
        <span style="color:#FF6B35;font-weight:800">⏰ Ăn ít nhất 60 phút trước khi vận động mạnh</span>
      </div>
    </div>

```
<div class="meal-card">
  <div class="meal-header" style="background:linear-gradient(135deg,#27AE60,#2ECC71)">☀️ Bữa Trưa (Ở Trường)</div>
  <div class="meal-body">
    🍚 Cơm (1.5–2 chén) · 🍗 Thịt gà/cá/thịt heo nạc · 🥦 Rau xanh đa dạng · 🍜 Canh<br><br>
    <strong style="color:#333">Tránh:</strong><br>
    ❌ Đồ chiên nhiều dầu vào ngày tập · ❌ Nước ngọt có gas · ❌ Ăn quá nhiều khiến uể oải chiều<br><br>
    <span style="color:#27AE60;font-weight:800">💧 Uống 500ml nước sau bữa trưa</span>
  </div>
</div>

<div class="meal-card">
  <div class="meal-header" style="background:linear-gradient(135deg,#2471A3,#3498DB)">⚡ Snack Trước Tập (60–90 phút trước)</div>
  <div class="meal-body">
    Bữa nhỏ để cung cấp năng lượng cho buổi tập chiều:<br><br>
    🍌 Chuối + 🥜 1 nắm hạt (hạnh nhân/điều) — lý tưởng nhất<br>
    🍞 Bánh mì nguyên cám + 🥜 Bơ đậu phộng<br>
    🍚 Cơm nhỏ + 🥩 Một chút thịt<br><br>
    <span style="color:#2471A3;font-weight:800">❌ KHÔNG ăn thức ăn nhiều dầu mỡ trước tập</span>
  </div>
</div>

<div class="meal-card">
  <div class="meal-header" style="background:linear-gradient(135deg,#8E44AD,#9B59B6)">🌙 Bữa Tối (Sau Tập — Recovery Meal)</div>
  <div class="meal-body">
    Đây là bữa quan trọng nhất cho recovery — ăn trong 45 phút sau tập:<br><br>
    🍗 Protein: Thịt gà/cá/tôm (bắt buộc — giúp cơ bắp phục hồi)<br>
    🍚 Carbs: Cơm hoặc khoai lang<br>
    🥦 Rau xanh và trái cây nhiều màu sắc<br>
    🥛 1 ly sữa trước khi ngủ<br><br>
    <span style="color:#8E44AD;font-weight:800">😴 Ngủ 9–10 tiếng — đây là "supplement" tốt nhất</span>
  </div>
</div>
```

  </div>

  <div class="divider"></div>
  <div class="sec-title">💧 Hydration — Uống Nước Đúng Cách</div>
  <div class="card">
    <div class="card-title"><span class="icon">💧</span> Lịch Uống Nước Trong Ngày Tập</div>
    <div class="schedule-wrap">
      <table class="schedule-table">
        <tr><th>Thời điểm</th><th>Lượng nước</th><th>Ghi chú</th></tr>
        <tr><td>🌅 Ngay khi thức dậy</td><td>300–400ml</td><td>Bổ sung nước mất trong đêm</td></tr>
        <tr><td>☀️ Suốt buổi sáng ở trường</td><td>500–700ml</td><td>Mang bình nước 750ml đến trường</td></tr>
        <tr><td>⚡ 30 phút trước tập</td><td>300–400ml</td><td>Pre-hydrate trước khi vận động</td></tr>
        <tr><td>🏀 Trong khi tập</td><td>150–200ml mỗi 20 phút</td><td>Uống từng ngụm nhỏ, không uống nhiều 1 lần</td></tr>
        <tr><td>🏁 Sau tập</td><td>400–600ml</td><td>Bù lại nước đã mất qua mồ hôi</td></tr>
        <tr><td>🌙 Trước khi ngủ</td><td>200ml</td><td>Không uống quá nhiều gây thức giấc ban đêm</td></tr>
      </table>
    </div>
    <div class="tip-card" style="margin-top:16px">
      <span class="tip-icon">💡</span>
      <div class="tip-text"><strong>Kiểm tra màu nước tiểu</strong>Vàng nhạt = đủ nước ✅ · Vàng đậm = thiếu nước ❌ · Trong như nước = uống hơi nhiều (hiếm khi cần lo) · Ăn muối điện giải sau tập dài &gt; 90 phút hoặc đổ mồ hôi nhiều.</div>
    </div>
  </div>

</div>

</div><!-- end content-wrap -->

<div class="footer-note">
  🏀 Lộ Trình Bóng Rổ · <span>12 Tuổi · 4 Năm Kinh Nghiệm</span> · Được thiết kế bởi AI Coach · Tham khảo thêm ý kiến HLV chuyên nghiệp
</div>

<script>
function switchTab(id) {
  document.querySelectorAll('.tab-btn').forEach((btn, i) => {
    const ids = ['overview','phase1','phase2','phase3','phase4','phase5','mistakes','nutrition'];
    btn.classList.toggle('active', ids[i] === id);
  });
  document.querySelectorAll('.tab-panel').forEach(p => {
    p.classList.remove('active');
  });
  document.getElementById('tab-' + id).classList.add('active');
  window.scrollTo({ top: document.querySelector('.nav-wrap').offsetTop, behavior: 'smooth' });
}
</script>

</body>
</html>