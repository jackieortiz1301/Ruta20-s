# Ruta-20-s
Nuestra herramienta ayudará a los universitarios a tener un mejor control de sus finanzas personales
<!DOCTYPE html>

<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FinanceU — Tu Plan Financiero Universitario</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">
<style>
  :root {
    --bg:       #F0F6FF;
    --surface:  #ffffff;
    --navy:     #0C2D6B;
    --blue:     #1A6FD4;
    --teal:     #0AAEA0;
    --green:    #22C55E;
    --amber:    #F59E0B;
    --rose:     #EF4444;
    --indigo:   #6366F1;
    --text:     #0F1F3D;
    --muted:    #5A718A;
    --border:   #D4E2F5;
  }

- { margin: 0; padding: 0; box-sizing: border-box; }

body {
font-family: ‘DM Sans’, sans-serif;
background: var(–bg);
color: var(–text);
min-height: 100vh;
overflow-x: hidden;
}

/* ── BACKGROUND ── */
body::before {
content: ‘’;
position: fixed; inset: 0;
background:
radial-gradient(ellipse 70% 50% at 5% 10%, rgba(26,111,212,0.09) 0%, transparent 60%),
radial-gradient(ellipse 60% 45% at 95% 85%, rgba(10,174,160,0.08) 0%, transparent 60%),
radial-gradient(ellipse 50% 40% at 50% 50%, rgba(99,102,241,0.04) 0%, transparent 70%);
pointer-events: none; z-index: 0;
}

/* ── HEADER ── */
header {
position: relative; z-index: 10;
padding: 1.5rem 2.5rem 1.2rem;
display: flex; align-items: center; justify-content: space-between;
background: var(–surface);
border-bottom: 1px solid var(–border);
box-shadow: 0 1px 8px rgba(12,45,107,0.06);
}

.logo {
font-family: ‘Syne’, sans-serif;
font-weight: 800; font-size: 1.6rem;
letter-spacing: -0.5px;
color: var(–navy);
}
.logo span { color: var(–teal); }

.tagline {
font-size: 0.8rem; color: var(–muted);
font-style: italic; letter-spacing: 0.5px;
}

/* ── HERO ── */
.hero {
position: relative; z-index: 5;
text-align: center;
padding: 3rem 2rem 2rem;
}

.hero h1 {
font-family: ‘Syne’, sans-serif;
font-size: clamp(2rem, 5vw, 3.2rem);
font-weight: 800;
line-height: 1.1;
margin-bottom: 0.8rem;
color: var(–navy);
}

.hero h1 em {
font-style: normal;
background: linear-gradient(90deg, var(–blue), var(–teal));
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
}

.hero p {
color: var(–muted);
font-size: 1rem; max-width: 480px; margin: 0 auto;
line-height: 1.7;
}

/* ── NAV PILLS ── */
.nav-pills {
position: relative; z-index: 5;
display: flex; flex-wrap: wrap; gap: 0.6rem;
justify-content: center;
padding: 1.5rem 2rem 0;
}

.pill {
font-family: ‘Syne’, sans-serif;
font-size: 0.78rem; font-weight: 600;
padding: 0.5rem 1.1rem;
border-radius: 999px;
border: 1.5px solid var(–border);
background: var(–surface);
color: var(–muted);
cursor: pointer;
transition: all 0.2s ease;
letter-spacing: 0.3px;
box-shadow: 0 1px 4px rgba(12,45,107,0.05);
}
.pill:hover { border-color: var(–blue); color: var(–blue); background: rgba(26,111,212,0.06); }
.pill.active { background: var(–navy); border-color: var(–navy); color: #ffffff; box-shadow: 0 2px 8px rgba(12,45,107,0.2); }

/* ── MAIN CONTENT ── */
main {
position: relative; z-index: 5;
max-width: 900px; margin: 0 auto;
padding: 2rem 1.5rem 4rem;
}

.section { display: none; animation: fadeUp 0.4s ease; }
.section.active { display: block; }

@keyframes fadeUp {
from { opacity: 0; transform: translateY(16px); }
to   { opacity: 1; transform: translateY(0); }
}

/* ── SECTION HEADER ── */
.section-header {
display: flex; align-items: center; gap: 1rem;
margin-bottom: 1.8rem;
}
.section-icon {
width: 52px; height: 52px; border-radius: 14px;
display: flex; align-items: center; justify-content: center;
font-size: 1.5rem; flex-shrink: 0;
}
.section-header h2 {
font-family: ‘Syne’, sans-serif;
font-size: 1.6rem; font-weight: 800;
color: var(–navy);
}
.section-header p { color: var(–muted); font-size: 0.9rem; margin-top: 0.2rem; }

/* ── CARDS ── */
.cards-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
gap: 1rem; margin-bottom: 1.5rem;
}

.card {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 16px; padding: 1.4rem;
transition: all 0.2s ease;
box-shadow: 0 2px 8px rgba(12,45,107,0.05);
}
.card:hover { box-shadow: 0 6px 20px rgba(12,45,107,0.10); transform: translateY(-2px); }

.card-label {
font-family: ‘Syne’, sans-serif;
font-size: 0.7rem; font-weight: 700;
letter-spacing: 1.5px; text-transform: uppercase;
margin-bottom: 0.5rem; color: var(–muted);
}
.card h3 {
font-family: ‘Syne’, sans-serif;
font-size: 1.05rem; font-weight: 700;
margin-bottom: 0.6rem; color: var(–navy);
}
.card p, .card li {
font-size: 0.88rem; color: var(–muted);
line-height: 1.65;
}
.card ul { padding-left: 1.1rem; }
.card li { margin-bottom: 0.3rem; }

.card .big-num {
font-family: ‘Syne’, sans-serif;
font-size: 2.8rem; font-weight: 800;
line-height: 1; margin-bottom: 0.3rem;
}

/* accent borders */
.card.teal  { border-left: 4px solid var(–teal); }
.card.coral { border-left: 4px solid var(–rose); }
.card.gold  { border-left: 4px solid var(–amber); }
.card.lav   { border-left: 4px solid var(–indigo); }
.card.sky   { border-left: 4px solid var(–blue); }

/* ── INFO BOX ── */
.info-box {
background: rgba(26,111,212,0.06);
border: 1px solid rgba(26,111,212,0.18);
border-radius: 14px; padding: 1.2rem 1.4rem;
margin-bottom: 1.2rem;
font-size: 0.9rem; line-height: 1.7;
color: var(–navy);
}

/* ── STEPS ── */
.steps { display: flex; flex-direction: column; gap: 0.9rem; }
.step {
display: flex; gap: 1rem; align-items: flex-start;
background: var(–surface);
border: 1px solid var(–border);
border-radius: 14px; padding: 1.1rem 1.2rem;
box-shadow: 0 1px 6px rgba(12,45,107,0.05);
}
.step-num {
font-family: ‘Syne’, sans-serif;
font-size: 1.4rem; font-weight: 800;
min-width: 36px; line-height: 1;
}
.step h4 {
font-family: ‘Syne’, sans-serif;
font-size: 0.95rem; font-weight: 700; margin-bottom: 0.25rem;
color: var(–navy);
}
.step p { font-size: 0.85rem; color: var(–muted); line-height: 1.6; }

/* ── GLOSSARY ── */
.glossary { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 0.8rem; }
.gloss-item {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 12px; padding: 1rem 1.1rem;
cursor: pointer; transition: all 0.2s;
box-shadow: 0 1px 4px rgba(12,45,107,0.04);
}
.gloss-item:hover { border-color: var(–indigo); box-shadow: 0 4px 14px rgba(99,102,241,0.12); }
.gloss-item h4 {
font-family: ‘Syne’, sans-serif;
font-size: 0.95rem; font-weight: 700; margin-bottom: 0.4rem;
color: var(–indigo);
}
.gloss-item p { font-size: 0.83rem; color: var(–muted); line-height: 1.55; }

/* ── CALCULATOR ── */
.calc-wrapper {
background: var(–surface);
border: 1px solid var(–border);
border-radius: 20px; padding: 1.8rem;
box-shadow: 0 2px 12px rgba(12,45,107,0.07);
}

.calc-wrapper h3 {
font-family: ‘Syne’, sans-serif;
font-size: 1.1rem; font-weight: 700;
margin-bottom: 1.2rem; color: var(–navy);
}

.input-group { margin-bottom: 1rem; }
.input-group label {
display: block; font-size: 0.82rem;
color: var(–muted);
margin-bottom: 0.4rem; font-weight: 500;
}
.input-group input {
width: 100%; padding: 0.7rem 1rem;
background: var(–bg);
border: 1.5px solid var(–border);
border-radius: 10px; color: var(–text);
font-family: ‘DM Sans’, sans-serif; font-size: 1rem;
outline: none; transition: border 0.2s;
}
.input-group input:focus { border-color: var(–blue); }
.input-group input::placeholder { color: #aab4c4; }

.calc-btn {
width: 100%; padding: 0.85rem;
background: var(–navy); border: none;
border-radius: 12px; color: #ffffff;
font-family: ‘Syne’, sans-serif; font-size: 1rem; font-weight: 700;
cursor: pointer; transition: all 0.2s; margin-top: 0.5rem;
}
.calc-btn:hover { background: var(–blue); transform: translateY(-1px); box-shadow: 0 4px 14px rgba(26,111,212,0.3); }

.calc-results {
display: none; margin-top: 1.5rem;
animation: fadeUp 0.3s ease;
}
.calc-results.show { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.8rem; }

.result-card {
border-radius: 14px; padding: 1rem;
text-align: center;
}
.result-card .pct {
font-family: ‘Syne’, sans-serif;
font-size: 1.8rem; font-weight: 800; line-height: 1;
}
.result-card .label { font-size: 0.75rem; margin-top: 0.3rem; color: var(–muted); }
.result-card .amount {
font-family: ‘Syne’, sans-serif;
font-size: 1.1rem; font-weight: 700; margin-top: 0.4rem;
color: var(–navy);
}

.rc-teal  { background: rgba(10,174,160,0.08);  border: 1px solid rgba(10,174,160,0.25); }
.rc-coral { background: rgba(239,68,68,0.07);   border: 1px solid rgba(239,68,68,0.22); }
.rc-gold  { background: rgba(245,158,11,0.08);  border: 1px solid rgba(245,158,11,0.25); }

/* ── TIPS ── */
.tip-list { display: flex; flex-direction: column; gap: 0.9rem; }
.tip {
display: flex; gap: 1rem; align-items: flex-start;
padding: 1.1rem 1.2rem;
background: var(–surface);
border: 1px solid var(–border);
border-radius: 14px;
box-shadow: 0 1px 5px rgba(12,45,107,0.05);
}
.tip-num {
font-family: ‘Syne’, sans-serif; font-size: 1rem; font-weight: 800;
color: var(–amber); min-width: 28px;
}
.tip h4 { font-family: ‘Syne’, sans-serif; font-size: 0.95rem; font-weight: 700; margin-bottom: 0.3rem; color: var(–navy); }
.tip p  { font-size: 0.85rem; color: var(–muted); line-height: 1.6; }

/* ── BENEFITS ── */
.benefit-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 1rem; }
.benefit-card {
border-radius: 16px; padding: 1.3rem;
border: 1px solid var(–border);
background: var(–surface);
transition: all 0.2s;
box-shadow: 0 2px 8px rgba(12,45,107,0.05);
}
.benefit-card:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(12,45,107,0.10); }
.benefit-icon { font-size: 2rem; margin-bottom: 0.6rem; }
.benefit-card h4 {
font-family: ‘Syne’, sans-serif; font-size: 0.95rem; font-weight: 700;
margin-bottom: 0.4rem; color: var(–navy);
}
.benefit-card p { font-size: 0.83rem; color: var(–muted); line-height: 1.55; }

/* ── FOOTER NOTE ── */
.section-note {
margin-top: 1.8rem;
padding: 1rem 1.3rem;
background: rgba(245,158,11,0.07);
border: 1px solid rgba(245,158,11,0.25);
border-radius: 12px;
font-size: 0.85rem; color: #7C5C00;
font-style: italic; line-height: 1.6;
}

/* ── ENHANCED CALCULATOR ── */
.calc-results {
display: none; margin-top: 1.5rem;
animation: fadeUp 0.3s ease;
}
.calc-results.show { display: grid; grid-template-columns: repeat(3, 1fr); gap: 0.8rem; }

.budget-bar {
display: flex; border-radius: 12px; overflow: hidden;
height: 14px; margin-top: 1rem; gap: 3px;
}
.bar-segment { height: 100%; border-radius: 6px; transition: width 0.5s ease; }
.bar-teal  { background: var(–teal); }
.bar-coral { background: var(–rose); }
.bar-gold  { background: var(–amber); }

.budget-table-section { margin-top: 2rem; }

.table-header-row {
display: flex; justify-content: space-between; align-items: center;
margin-bottom: 0.6rem;
}
.table-header-row h4 {
font-family: ‘Syne’, sans-serif; font-size: 1rem; font-weight: 700; color: var(–navy);
}

.add-btn {
font-family: ‘Syne’, sans-serif; font-size: 0.8rem; font-weight: 700;
padding: 0.45rem 1rem; border-radius: 999px;
border: 1.5px solid var(–blue); color: var(–blue);
background: rgba(26,111,212,0.06); cursor: pointer; transition: all 0.2s;
}
.add-btn:hover { background: var(–blue); color: #fff; }

.budget-table-wrap { overflow-x: auto; margin-bottom: 1.5rem; }

.budget-table {
width: 100%; border-collapse: collapse;
font-size: 0.88rem;
}
.budget-table thead tr {
background: var(–bg); border-bottom: 2px solid var(–border);
}
.budget-table th {
padding: 0.65rem 0.8rem; text-align: left;
font-family: ‘Syne’, sans-serif; font-size: 0.75rem; font-weight: 700;
letter-spacing: 0.8px; text-transform: uppercase; color: var(–muted);
}
.budget-table td {
padding: 0.55rem 0.8rem; border-bottom: 1px solid var(–border);
vertical-align: middle;
}
.budget-table tbody tr:hover { background: rgba(26,111,212,0.03); }

.budget-table input[type=“text”],
.budget-table input[type=“number”] {
width: 100%; padding: 0.4rem 0.6rem;
border: 1.5px solid var(–border); border-radius: 8px;
font-family: ‘DM Sans’, sans-serif; font-size: 0.88rem;
color: var(–text); background: var(–surface); outline: none;
transition: border 0.2s;
}
.budget-table input:focus { border-color: var(–blue); }

.budget-table select {
width: 100%; padding: 0.4rem 0.6rem;
border: 1.5px solid var(–border); border-radius: 8px;
font-family: ‘DM Sans’, sans-serif; font-size: 0.88rem;
color: var(–text); background: var(–surface); outline: none;
cursor: pointer; transition: border 0.2s;
}
.budget-table select:focus { border-color: var(–blue); }
.budget-table select.cat-50 { border-left: 3px solid var(–teal); }
.budget-table select.cat-30 { border-left: 3px solid var(–rose); }
.budget-table select.cat-20 { border-left: 3px solid var(–amber); }

.del-btn {
background: none; border: none; cursor: pointer;
color: var(–muted); font-size: 1rem; padding: 0.2rem 0.4rem;
border-radius: 6px; transition: all 0.15s;
}
.del-btn:hover { color: var(–rose); background: rgba(239,68,68,0.08); }

.table-summary {
display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
gap: 0.9rem; margin-top: 0.5rem;
}
.summary-block {
border-radius: 14px; padding: 1rem 1.1rem;
border: 1px solid var(–border); background: var(–surface);
}
.sb-label {
font-family: ‘Syne’, sans-serif; font-size: 0.78rem; font-weight: 700;
text-transform: uppercase; letter-spacing: 0.8px; margin-bottom: 0.5rem;
color: var(–muted);
}
.sb-vals {
display: flex; justify-content: space-between;
font-size: 0.82rem; color: var(–muted); margin-bottom: 0.5rem;
flex-wrap: wrap; gap: 0.2rem;
}
.sb-vals strong { color: var(–navy); }
.sb-bar-wrap {
height: 8px; background: var(–bg); border-radius: 999px; overflow: hidden;
margin-bottom: 0.5rem;
}
.sb-bar { height: 100%; border-radius: 999px; transition: width 0.4s ease; width: 0%; }
.sb-bar-teal  { background: var(–teal); }
.sb-bar-coral { background: var(–rose); }
.sb-bar-gold  { background: var(–amber); }
.sb-status { font-size: 0.78rem; font-weight: 600; min-height: 1.1em; }
.status-ok   { color: #16a34a; }
.status-warn { color: var(–amber); }
.status-over { color: var(–rose); }

/* scrollbar */
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: transparent; }
::-webkit-scrollbar-thumb { background: var(–border); border-radius: 3px; }

@media (max-width: 600px) {
header { flex-direction: column; gap: 0.3rem; text-align: center; }
.calc-results.show { grid-template-columns: 1fr; }
.table-summary { grid-template-columns: 1fr; }
}
</style>

</head>
<body>

<header>
  <div class="logo">Finance<span>U</span></div>
  <div class="tagline">Ruta 20's · Innovación sostenible</div>
</header>

<div class="hero">
  <h1>Tu dinero,<br><em>tu futuro.</em></h1>
  <p>Una guía práctica para que como universitario tomes el control de tus finanzas desde hoy.</p>
</div>

<nav class="nav-pills">
  <button class="pill active" onclick="show('regla')">📊 Regla 50-30-20</button>
  <button class="pill" onclick="show('hormiga')">🐜 Gastos Hormiga</button>
  <button class="pill" onclick="show('tarjetas')">💳 Tarjetas de Crédito</button>
  <button class="pill" onclick="show('presupuesto')">📋 Presupuesto</button>
  <button class="pill" onclick="show('inversion')">📈 Inversión</button>
  <button class="pill" onclick="show('consejos')">💡 Consejos</button>
  <button class="pill" onclick="show('conceptos')">📚 Conceptos Clave</button>
  <button class="pill" onclick="show('beneficios')">🎓 Beneficios</button>
</nav>

<main>

  <!-- ── REGLA 50-30-20 ── -->

  <section class="section active" id="regla">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(10,174,160,0.12);">📊</div>
      <div>
        <h2>Regla 50-30-20</h2>
        <p>Divide tus ingresos en tres partes con una lógica simple y efectiva.</p>
      </div>
    </div>

```
<div class="info-box">
  Es un método sencillo para gestionar tus finanzas personales. El objetivo es dividir tus ingresos de manera equilibrada entre <strong>gastos básicos</strong>, <strong>deudas o gastos personales</strong>, y <strong>ahorro o inversión</strong>.
</div>

<div class="cards-grid">
  <div class="card teal">
    <div class="big-num" style="color:var(--teal)">50%</div>
    <h3>Gastos básicos</h3>
    <ul>
      <li>Vivienda / renta</li>
      <li>Servicios (luz, agua, gas, internet)</li>
      <li>Alimentación (super, no restaurantes)</li>
      <li>Transporte esencial</li>
      <li>Seguros</li>
      <li>Pagos mínimos de deudas</li>
    </ul>
    <p style="margin-top:0.6rem;font-size:0.8rem;opacity:0.6;">Si superas este porcentaje, considera reducir costos.</p>
  </div>
  <div class="card coral">
    <div class="big-num" style="color:var(--coral)">30%</div>
    <h3>Deudas y otros gastos</h3>
    <ul>
      <li>Salidas con amigos, restaurantes</li>
      <li>Streaming, música, gimnasio</li>
      <li>Hobbies y entretenimiento</li>
      <li>Ropa no esencial</li>
      <li>Viajes y escapadas</li>
      <li>Pago de tarjeta de crédito</li>
    </ul>
    <p style="margin-top:0.6rem;font-size:0.8rem;opacity:0.6;">Gastos que forman parte de tu estilo de vida.</p>
  </div>
  <div class="card gold">
    <div class="big-num" style="color:var(--gold)">20%</div>
    <h3>Ahorro e inversión</h3>
    <ul>
      <li>Fondo de emergencia</li>
      <li>Ahorro para metas a largo plazo</li>
      <li>Inversión (CETES, fondos)</li>
    </ul>
    <p style="margin-top:0.6rem;font-size:0.8rem;opacity:0.6;">Clave para tu estabilidad financiera futura.</p>
  </div>
</div>

<!-- CALCULADORA MEJORADA -->
<div class="calc-wrapper">
  <h3>🧮 Calculadora 50-30-20</h3>
  <div class="input-group">
    <label>¿Cuánto recibes al mes? (beca, trabajo, apoyo familiar…)</label>
    <input type="number" id="ingreso" placeholder="ej. 5000" min="0" oninput="calcular()">
  </div>

  <div class="calc-results" id="resultados">
    <div class="result-card rc-teal">
      <div class="pct" style="color:var(--teal)">50%</div>
      <div class="label">Gastos básicos</div>
      <div class="amount" id="r50"></div>
    </div>
    <div class="result-card rc-coral">
      <div class="pct" style="color:var(--rose)">30%</div>
      <div class="label">Otros gastos</div>
      <div class="amount" id="r30"></div>
    </div>
    <div class="result-card rc-gold">
      <div class="pct" style="color:var(--amber)">20%</div>
      <div class="label">Ahorro</div>
      <div class="amount" id="r20"></div>
    </div>
  </div>

  <div class="budget-bar" id="budgetBar" style="display:none">
    <div class="bar-segment bar-teal"  id="bar50" style="width:50%"></div>
    <div class="bar-segment bar-coral" id="bar30" style="width:30%"></div>
    <div class="bar-segment bar-gold"  id="bar20" style="width:20%"></div>
  </div>

  <div class="budget-table-section" id="tableSection" style="display:none">
    <div class="table-header-row">
      <h4>📋 Clasifica tus gastos</h4>
      <button class="add-btn" onclick="addRow()">+ Agregar gasto</button>
    </div>
    <p style="font-size:0.82rem;color:var(--muted);margin-bottom:1rem;">Escribe cada gasto, el monto y selecciona a qué categoría pertenece. El resumen se actualiza automáticamente.</p>

    <div class="budget-table-wrap">
      <table class="budget-table" id="budgetTable">
        <thead>
          <tr>
            <th>Gasto</th>
            <th>Monto ($)</th>
            <th>Categoría</th>
            <th></th>
          </tr>
        </thead>
        <tbody id="tableBody"></tbody>
      </table>
    </div>

    <div class="table-summary" id="tableSummary">
      <div class="summary-block sb-teal">
        <div class="sb-label">Gastos básicos (50%)</div>
        <div class="sb-vals">
          <span>Usado: <strong id="used50">$0</strong></span>
          <span>Límite: <strong id="lim50">—</strong></span>
        </div>
        <div class="sb-bar-wrap"><div class="sb-bar sb-bar-teal" id="prog50"></div></div>
        <div class="sb-status" id="st50"></div>
      </div>
      <div class="summary-block sb-coral">
        <div class="sb-label">Otros gastos (30%)</div>
        <div class="sb-vals">
          <span>Usado: <strong id="used30">$0</strong></span>
          <span>Límite: <strong id="lim30">—</strong></span>
        </div>
        <div class="sb-bar-wrap"><div class="sb-bar sb-bar-coral" id="prog30"></div></div>
        <div class="sb-status" id="st30"></div>
      </div>
      <div class="summary-block sb-gold">
        <div class="sb-label">Ahorro (20%)</div>
        <div class="sb-vals">
          <span>Asignado: <strong id="used20">$0</strong></span>
          <span>Meta: <strong id="lim20">—</strong></span>
        </div>
        <div class="sb-bar-wrap"><div class="sb-bar sb-bar-gold" id="prog20"></div></div>
        <div class="sb-status" id="st20"></div>
      </div>
    </div>
  </div>
</div>
```

  </section>

  <!-- ── GASTOS HORMIGA ── -->

  <section class="section" id="hormiga">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(239,68,68,0.10);">🐜</div>
      <div>
        <h2>Gastos Hormiga</h2>
        <p>Pequeños gastos que se van sin que te des cuenta.</p>
      </div>
    </div>

```
<div class="cards-grid">
  <div class="card coral">
    <div class="card-label">¿Qué son?</div>
    <p>Son pequeños gastos diarios que parecen insignificantes, pero al acumularse afectan mucho tu presupuesto. No son las compras grandes las que arruinan las finanzas, sino las pequeñas y constantes.</p>
  </div>
  <div class="card sky">
    <div class="card-label">Ejemplos comunes</div>
    <ul>
      <li>Comprar café todos los días ☕</li>
      <li>Pedir comida constantemente 🍔</li>
      <li>Compras impulsivas en línea 📱</li>
      <li>Snacks entre clases 🍿</li>
      <li>Suscripciones que ya no usas</li>
    </ul>
  </div>
  <div class="card lav">
    <div class="card-label">¿Cómo evitarlos?</div>
    <ul>
      <li>Lleva un registro diario de gastos</li>
      <li>Pregúntate: ¿lo necesito o lo quiero?</li>
      <li>Usa apps de control de gastos</li>
      <li>Establece un límite semanal de "antojos"</li>
      <li>Prepara comida en casa</li>
    </ul>
  </div>
</div>

<div class="section-note">
  💡 <strong>Dato:</strong> Si gastas $50 diarios en café, al mes son $1,500. Al año: $18,000. Ese dinero podría ir a tu fondo de inversión.
</div>
```

  </section>

  <!-- ── TARJETAS DE CRÉDITO ── -->

  <section class="section" id="tarjetas">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(26,111,212,0.10);">💳</div>
      <div>
        <h2>Tarjetas de Crédito</h2>
        <p>Úsalas a tu favor, no en tu contra.</p>
      </div>
    </div>

```
<div class="info-box">
  Muchos estudiantes comienzan a usar tarjetas para cubrir gastos personales, emergencias o compras escolares. Sin embargo, si no se administran bien, pueden generar deudas difíciles de pagar.
</div>

<div class="cards-grid">
  <div class="card teal">
    <div class="card-label">✅ Ventajas</div>
    <ul>
      <li>Cubrir emergencias</li>
      <li>Compras necesarias sin efectivo</li>
      <li>Construir historial crediticio</li>
      <li>Compras en línea seguras</li>
    </ul>
  </div>
  <div class="card coral">
    <div class="card-label">⚠️ Riesgos</div>
    <ul>
      <li>Gastar más de lo que puedes pagar</li>
      <li>Intereses muy altos</li>
      <li>Deudas acumuladas que crecen rápido</li>
    </ul>
  </div>
  <div class="card gold">
    <div class="card-label">💡 Consejos de oro</div>
    <ul>
      <li>Úsala solo para gastos importantes</li>
      <li>No gastes más de lo que puedes pagar</li>
      <li>Paga a tiempo, siempre</li>
      <li>Evita usarla para "antojos"</li>
    </ul>
  </div>
</div>

<div class="section-note">
  🚨 Una tarjeta de crédito <strong>no es dinero extra</strong>. Es dinero prestado que tendrás que devolver con intereses si no pagas a tiempo.
</div>
```

  </section>

  <!-- ── PRESUPUESTO ── -->

  <section class="section" id="presupuesto">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(245,158,11,0.10);">📋</div>
      <div>
        <h2>Cómo hacer tu Presupuesto</h2>
        <p>El presupuesto no te limita; te da libertad de gastar con inteligencia.</p>
      </div>
    </div>

```
<div class="info-box">
  Un buen presupuesto estudiantil asegura que tu inversión en educación llegue a buen puerto, sin sorpresas a mitad del semestre.
</div>

<div class="steps">
  <div class="step">
    <div class="step-num" style="color:var(--teal)">01</div>
    <div>
      <h4>Identifica tus ingresos</h4>
      <p>Suma todo lo que recibes: beca, mesada, trabajo de medio tiempo, apoyo familiar. Sé realista con el total mensual.</p>
    </div>
  </div>
  <div class="step">
    <div class="step-num" style="color:var(--sky)">02</div>
    <div>
      <h4>Clasifica tus gastos</h4>
      <p>Separa gastos fijos (renta, transporte) de variables (salidas, ropa). Esto te ayuda a ver dónde puedes recortar.</p>
    </div>
  </div>
  <div class="step">
    <div class="step-num" style="color:var(--coral)">03</div>
    <div>
      <h4>Estima gastos académicos</h4>
      <p>Considera inscripción, libros, materiales, impresiones. Muchos no los incluyen y luego se quedan cortos.</p>
    </div>
  </div>
  <div class="step">
    <div class="step-num" style="color:var(--lavender)">04</div>
    <div>
      <h4>Limita el entretenimiento</h4>
      <p>Asigna una cantidad fija semanal para salidas y diversión. Cuando se acabe, ¡se acabó! Sin culpas.</p>
    </div>
  </div>
  <div class="step">
    <div class="step-num" style="color:var(--gold)">05</div>
    <div>
      <h4>Crea tu fondo de ahorro</h4>
      <p>Aunque sea un porcentaje pequeño, ahorra antes de gastar. Trátalo como un gasto obligatorio, no opcional.</p>
    </div>
  </div>
  <div class="step">
    <div class="step-num" style="color:var(--teal)">06</div>
    <div>
      <h4>Revisa y ajusta quincenalmente</h4>
      <p>Tu presupuesto no es estático. Revísalo cada dos semanas y ajusta según lo que haya pasado.</p>
    </div>
  </div>
</div>
```

  </section>

  <!-- ── INVERSIÓN ── -->

  <section class="section" id="inversion">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(10,174,160,0.12);">📈</div>
      <div>
        <h2>Invierte tu Dinero</h2>
        <p>Haz que tu dinero trabaje para ti, incluso siendo estudiante.</p>
      </div>
    </div>

```
<div class="cards-grid">
  <div class="card teal" style="grid-column: 1 / -1;">
    <div class="card-label">🇲🇽 CETES — La opción más accesible</div>
    <h3>Certificados de la Tesorería de la Federación</h3>
    <p>Son instrumentos de deuda emitidos por el Gobierno Federal de México desde 1978. Al invertir en CETES, en términos simples, <strong>le prestas dinero al gobierno</strong>, quien se compromete a devolverte tu inversión más un rendimiento al término de un plazo establecido.</p>
    <br>
    <ul>
      <li>✅ Puedes invertir desde <strong>$100 pesos</strong></li>
      <li>✅ Muy seguro (respaldo del gobierno)</li>
      <li>✅ Plazos desde 28 días</li>
      <li>✅ Disponible en <strong>cetesdirecto.com</strong></li>
    </ul>
  </div>
  <div class="card sky">
    <div class="card-label">📦 Fondos de inversión</div>
    <h3>¿Qué son?</h3>
    <p>Grupos de inversionistas que juntan su dinero para diversificar. Puedes entrar con poco capital a través de plataformas como GBM+, Flink o Kueski.</p>
  </div>
  <div class="card lav">
    <div class="card-label">🛡️ Fondo de emergencia</div>
    <h3>Primero lo primero</h3>
    <p>Antes de invertir, construye un fondo de 3 meses de gastos básicos en una cuenta de ahorro separada. Es tu red de seguridad.</p>
  </div>
</div>

<div class="section-note">
  🌱 El mejor momento para empezar a invertir fue ayer. El segundo mejor momento es hoy. Aunque sean $200 al mes, los hábitos tempranos hacen una diferencia enorme a largo plazo.
</div>
```

  </section>

  <!-- ── CONSEJOS ── -->

  <section class="section" id="consejos">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(245,158,11,0.10);">💡</div>
      <div>
        <h2>Consejos Prácticos</h2>
        <p>Tips reales que hacen diferencia en tu bolsillo.</p>
      </div>
    </div>

```
<div class="tip-list">
  <div class="tip">
    <div class="tip-num">01</div>
    <div>
      <h4>Evita pagar precio completo por libros de texto</h4>
      <p>Busca libros de segunda mano en Facebook Marketplace, chats universitarios o librerías locales. También puedes rentar o comprar versiones digitales en Amazon, Chegg, AbeBooks o BookFinder.com.</p>
    </div>
  </div>
  <div class="tip">
    <div class="tip-num">02</div>
    <div>
      <h4>Come en casa con más frecuencia</h4>
      <p>El estadounidense promedio gastó casi $4,000 USD en comer fuera en 2024. Cocinar en casa puede liberar ese dinero para cosas como la matrícula, los libros u otros gastos escolares.</p>
    </div>
  </div>
  <div class="tip">
    <div class="tip-num">03</div>
    <div>
      <h4>Limita tus suscripciones</h4>
      <p>Las suscripciones se acumulan rápido, especialmente las automáticas. Revisa cuáles usas realmente y si alguna ofrece descuento para estudiantes antes de cancelarla.</p>
    </div>
  </div>
  <div class="tip">
    <div class="tip-num">04</div>
    <div>
      <h4>Usa apps de finanzas personales</h4>
      <p>Aplicaciones como Finerio, Wallet o YNAB te ayudan a ver exactamente a dónde va tu dinero. Lo que se mide, se puede mejorar.</p>
    </div>
  </div>
  <div class="tip">
    <div class="tip-num">05</div>
    <div>
      <h4>Compara precios antes de comprar</h4>
      <p>Antes de cualquier compra mayor, dedica 5 minutos a comparar precios en línea. Google Shopping, Mercado Libre y Amazon son buenos puntos de partida.</p>
    </div>
  </div>
</div>
```

  </section>

  <!-- ── CONCEPTOS CLAVE ── -->

  <section class="section" id="conceptos">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(99,102,241,0.10);">📚</div>
      <div>
        <h2>Conceptos Clave</h2>
        <p>El vocabulario financiero básico que todo universitario debe conocer.</p>
      </div>
    </div>

```
<div class="glossary">
  <div class="gloss-item">
    <h4>💰 Ingreso</h4>
    <p>Todo el dinero que recibes: beca, trabajo, mesada. Es tu punto de partida para cualquier plan financiero.</p>
  </div>
  <div class="gloss-item">
    <h4>💸 Gasto</h4>
    <p>El dinero que sale de tu bolsillo. Puede ser fijo (renta) o variable (salidas, ropa).</p>
  </div>
  <div class="gloss-item">
    <h4>📉 Deuda</h4>
    <p>Dinero que debes a alguien. No toda deuda es mala, pero debe gestionarse con cuidado.</p>
  </div>
  <div class="gloss-item">
    <h4>📊 Tasa de interés</h4>
    <p>El costo de pedir dinero prestado, o la ganancia por invertirlo. Se expresa en porcentaje anual.</p>
  </div>
  <div class="gloss-item">
    <h4>🏦 Crédito</h4>
    <p>Capacidad de obtener dinero prestado con el compromiso de devolverlo. Se construye con buen historial.</p>
  </div>
  <div class="gloss-item">
    <h4>📋 Historial crediticio</h4>
    <p>Tu "calificación" financiera. Resume cómo has manejado tus deudas y pagos a lo largo del tiempo.</p>
  </div>
</div>

<div class="section-note">
  🎯 Conocer estos términos te da poder. Cuando entiendas de qué hablan los bancos y las aplicaciones financieras, podrás tomar mejores decisiones.
</div>
```

  </section>

  <!-- ── BENEFICIOS ESTUDIANTILES ── -->

  <section class="section" id="beneficios">
    <div class="section-header">
      <div class="section-icon" style="background:rgba(26,111,212,0.10);">🎓</div>
      <div>
        <h2>Beneficios Estudiantiles</h2>
        <p>Ser estudiante tiene ventajas económicas que muchas veces no aprovechamos.</p>
      </div>
    </div>

```
<div class="info-box">
  Existen descuentos, promociones y apoyos especiales que te ayudan a ahorrar dinero y administrar mejor tus gastos. ¡Aprovéchalos!
</div>

<div class="benefit-grid">
  <div class="benefit-card" style="border-top:3px solid #0AAEA0">
    <div class="benefit-icon">🪪</div>
    <h4>Credencial estudiantil</h4>
    <p>Con tu credencial puedes acceder a descuentos en museos, cines, teatros y muchos comercios. Siempre pregunta si hay precio de estudiante.</p>
  </div>
  <div class="benefit-card" style="border-top:3px solid #EF4444">
    <div class="benefit-icon">🚌</div>
    <h4>Transporte</h4>
    <p>Muchas ciudades tienen tarifas reducidas en transporte público para estudiantes. Infórmate sobre la tarjeta universitaria de tu ciudad.</p>
  </div>
  <div class="benefit-card" style="border-top:3px solid #6366F1">
    <div class="benefit-icon">📱</div>
    <h4>Plataformas digitales</h4>
    <p>Spotify, Apple Music, YouTube Premium, Adobe, Microsoft 365 y más ofrecen planes estudiantiles con hasta 50% de descuento.</p>
  </div>
  <div class="benefit-card" style="border-top:3px solid #F59E0B">
    <div class="benefit-icon">🍎</div>
    <h4>Alimentos</h4>
    <p>Muchas universidades tienen comedores subsidiados o convenios con restaurantes cercanos. Explora las opciones de tu campus.</p>
  </div>
</div>

<div class="section-note">
  ✨ Ser estudiante no solo implica gastos; también ofrece oportunidades de ahorro que pueden mejorar tu economía si aprendes a aprovecharlas.
</div>
```

  </section>

</main>

<script>
  /* ── NAVIGATION ── */
  function show(id) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.querySelectorAll('.pill').forEach(p => p.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    const pills = document.querySelectorAll('.pill');
    const map = ['regla','hormiga','tarjetas','presupuesto','inversion','consejos','conceptos','beneficios'];
    pills[map.indexOf(id)].classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  /* ── CALCULATOR ── */
  const fmt = n => '$' + n.toLocaleString('es-MX', { minimumFractionDigits: 2, maximumFractionDigits: 2 });
  let rowCount = 0;

  function calcular() {
    const val = parseFloat(document.getElementById('ingreso').value);
    if (!val || val <= 0) {
      document.getElementById('resultados').classList.remove('show');
      document.getElementById('budgetBar').style.display = 'none';
      document.getElementById('tableSection').style.display = 'none';
      return;
    }

    // Cards
    document.getElementById('r50').textContent = fmt(val * 0.5);
    document.getElementById('r30').textContent = fmt(val * 0.3);
    document.getElementById('r20').textContent = fmt(val * 0.2);
    document.getElementById('resultados').classList.add('show');

    // Bar
    document.getElementById('budgetBar').style.display = 'flex';

    // Limits in summary
    document.getElementById('lim50').textContent = fmt(val * 0.5);
    document.getElementById('lim30').textContent = fmt(val * 0.3);
    document.getElementById('lim20').textContent = fmt(val * 0.2);

    // Show table section
    document.getElementById('tableSection').style.display = 'block';

    // Add first row if empty
    if (rowCount === 0) addRow();

    updateSummary();
  }

  function addRow() {
    const tbody = document.getElementById('tableBody');
    rowCount++;
    const id = rowCount;
    const tr = document.createElement('tr');
    tr.id = 'row-' + id;
    tr.innerHTML = `
      <td><input type="text" placeholder="ej. Renta, Netflix…" oninput="updateSummary()"></td>
      <td><input type="number" placeholder="0.00" min="0" step="0.01" oninput="updateSummary()" style="max-width:110px"></td>
      <td>
        <select onchange="updateSelectStyle(this); updateSummary()">
          <option value="">— Elegir —</option>
          <option value="50">50% · Básico</option>
          <option value="30">30% · Personal</option>
          <option value="20">20% · Ahorro</option>
        </select>
      </td>
      <td><button class="del-btn" onclick="deleteRow(${id})" title="Eliminar">✕</button></td>
    `;
    tbody.appendChild(tr);
  }

  function deleteRow(id) {
    const row = document.getElementById('row-' + id);
    if (row) { row.remove(); updateSummary(); }
  }

  function updateSelectStyle(sel) {
    sel.className = '';
    if (sel.value === '50') sel.classList.add('cat-50');
    else if (sel.value === '30') sel.classList.add('cat-30');
    else if (sel.value === '20') sel.classList.add('cat-20');
  }

  function updateSummary() {
    const ingreso = parseFloat(document.getElementById('ingreso').value) || 0;
    const lim = { '50': ingreso * 0.5, '30': ingreso * 0.3, '20': ingreso * 0.2 };
    const used = { '50': 0, '30': 0, '20': 0 };

    document.querySelectorAll('#tableBody tr').forEach(row => {
      const amtInput = row.querySelectorAll('input')[1];
      const sel = row.querySelector('select');
      const amt = parseFloat(amtInput?.value) || 0;
      const cat = sel?.value;
      if (cat && used[cat] !== undefined) used[cat] += amt;
    });

    ['50','30','20'].forEach(cat => {
      const u = used[cat], l = lim[cat];
      const pct = l > 0 ? Math.min((u / l) * 100, 100) : 0;
      const over = l > 0 && u > l;
      const idSuf = cat;

      document.getElementById('used' + idSuf).textContent = fmt(u);
      document.getElementById('prog' + idSuf).style.width = pct + '%';

      const stEl = document.getElementById('st' + idSuf);
      if (ingreso <= 0) { stEl.textContent = ''; return; }
      if (u === 0) { stEl.textContent = ''; stEl.className = 'sb-status'; }
      else if (over) {
        const exc = u - l;
        stEl.textContent = `⚠️ Te pasas por ${fmt(exc)}`;
        stEl.className = 'sb-status status-over';
      } else {
        const rem = l - u;
        stEl.textContent = `✅ Te quedan ${fmt(rem)}`;
        stEl.className = 'sb-status status-ok';
      }
    });
  }
</script>

</body>
</html>
