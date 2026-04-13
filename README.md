# Technical
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IB JIO Tier 2 – Complete Master Study Guide</title>
<link href="https://fonts.googleapis.com/css2?family=Rajdhani:wght@600;700&family=Nunito:wght@400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --navy: #0d1b3e; --gold: #f5a623; --accent: #e63946;
    --card: #162040; --text: #d6e0ff; --sub: #8fa4d8;
    --green: #2ecc71; --border: #1e305c; --white: #fff;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body { font-family: 'Nunito', sans-serif; background: var(--navy); color: var(--text); min-height: 100vh; }

  header {
    background: linear-gradient(135deg, #0d1b3e, #1a2e5a);
    border-bottom: 3px solid var(--gold);
    padding: 13px 16px 9px; text-align: center;
    position: sticky; top: 0; z-index: 100;
    box-shadow: 0 4px 20px rgba(0,0,0,0.5);
  }
  header h1 { font-family: 'Rajdhani',sans-serif; font-size: 1.4rem; color: var(--white); }
  header h1 span { color: var(--gold); }
  header p { font-size: 0.7rem; color: var(--sub); margin-top: 1px; }

  .tabs {
    display: flex; overflow-x: auto; gap: 5px;
    padding: 9px 12px; background: #0b1630;
    border-bottom: 1px solid var(--border); scrollbar-width: none;
  }
  .tabs::-webkit-scrollbar { display: none; }
  .tab-btn {
    flex-shrink: 0; background: #1a2a50; border: 1.5px solid #2a3f70;
    color: var(--sub); border-radius: 20px; padding: 6px 13px;
    font-size: 0.74rem; font-weight: 700; font-family: 'Nunito',sans-serif;
    cursor: pointer; white-space: nowrap; transition: all 0.2s;
  }
  .tab-btn.active, .tab-btn:hover { background: var(--gold); color: var(--navy); border-color: var(--gold); }

  .section { display: none; padding: 12px 13px 90px; animation: fadeIn 0.3s ease; }
  .section.active { display: block; }
  @keyframes fadeIn { from{opacity:0;transform:translateY(6px)} to{opacity:1;transform:translateY(0)} }

  .sec-title {
    font-family: 'Rajdhani',sans-serif; font-size: 1.25rem; color: var(--gold);
    margin-bottom: 13px; padding-bottom: 7px; border-bottom: 2px solid var(--border);
  }

  /* ACCORDION */
  .topic-card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; margin-bottom: 9px; overflow: hidden; }
  .topic-header { display: flex; justify-content: space-between; align-items: center; padding: 12px 14px; cursor: pointer; transition: background 0.2s; }
  .topic-header:hover { background: #1a2a50; }
  .topic-header-left { display: flex; align-items: center; gap: 9px; }
  .topic-num { background: var(--gold); color: var(--navy); font-weight: 700; font-size: 0.67rem; border-radius: 50%; width: 22px; height: 22px; line-height: 22px; text-align: center; flex-shrink: 0; }
  .topic-name { font-family: 'Rajdhani',sans-serif; font-size: 0.98rem; color: var(--gold); }
  .arrow { color: var(--sub); font-size: 0.9rem; transition: transform 0.3s; }
  .arrow.open { transform: rotate(180deg); }
  .topic-body { display: none; padding: 0 14px 14px; border-top: 1px solid var(--border); }
  .topic-body.open { display: block; }

  /* CONTENT */
  .cb { margin-top: 11px; }
  .cb h4 { font-family: 'Rajdhani',sans-serif; font-size: 0.95rem; color: var(--white); margin-bottom: 5px; margin-top: 11px; padding-left: 8px; border-left: 3px solid var(--gold); }
  .cb p { font-size: 0.81rem; line-height: 1.62; color: #b8c8f0; margin-bottom: 5px; }
  .cb ul { padding-left: 16px; margin-bottom: 5px; }
  .cb ul li { font-size: 0.81rem; line-height: 1.65; color: #b8c8f0; margin-bottom: 3px; }
  .cb ul li strong { color: var(--gold); }
  .cb ul li code { background: #0d2040; padding: 1px 5px; border-radius: 4px; font-size: 0.78rem; color: #7dd3fc; }

  /* TABLE */
  .tbl { width: 100%; border-collapse: collapse; margin: 10px 0; font-size: 0.78rem; }
: .tbl th { background: #1a2a50; color: var(--gold); padding: 7px 9px; text-align: left; font-family: 'Rajdhani',sans-serif; font-size: 0.85rem; }
  .tbl td { padding: 7px 9px; border-bottom: 1px solid #1e305c; color: #b8c8f0; }
  .tbl tr:last-child td { border-bottom: none; }
  .tbl code { background: #0d2040; padding: 1px 5px; border-radius: 4px; color: #7dd3fc; }

  /* CMD BOX */
  .cmd-box { background: #060f20; border: 1px solid #2a3f70; border-radius: 8px; padding: 10px 12px; margin: 8px 0; font-family: monospace; font-size: 0.78rem; color: #7dd3fc; line-height: 1.8; overflow-x: auto; }
  .cmd-box .prompt { color: #f5a623; }
  .cmd-box .comment { color: #4a6090; }
  .cmd-box .output { color: #8fa4d8; }

  /* KEY POINT */
  .kp { background: #0d2040; border: 1px solid var(--border); border-left: 3px solid var(--green); border-radius: 8px; padding: 9px 11px; margin-top: 9px; font-size: 0.79rem; color: #b8c8f0; line-height: 1.58; }
  .kp strong { color: var(--green); }
  .warn { border-left-color: var(--accent); }
  .warn strong { color: var(--accent); }

  /* TAGS */
  .tag-row { display: flex; flex-wrap: wrap; gap: 5px; margin-top: 9px; }
  .tag { background: #1a2a50; border: 1px solid #2a3f70; color: var(--sub); border-radius: 20px; padding: 2px 9px; font-size: 0.68rem; font-weight: 700; }

  /* COMPARE CARD */
  .compare-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin: 8px 0; }
  .compare-card { background: #0b1630; border: 1px solid var(--border); border-radius: 8px; padding: 9px 10px; }
  .compare-card h5 { font-family: 'Rajdhani',sans-serif; color: var(--gold); font-size: 0.88rem; margin-bottom: 5px; }
  .compare-card p { font-size: 0.75rem; color: #b8c8f0; line-height: 1.5; }

  /* QUIZ */
  .score-bar { background: #0b1630; border: 1px solid var(--border); border-radius: 10px; padding: 11px 15px; margin-bottom: 13px; display: flex; justify-content: space-between; align-items: center; }
  .score-bar span { color: var(--sub); font-size: 0.81rem; }
  .score-val { color: var(--gold); font-weight: 700; font-size: 1.05rem; font-family: 'Rajdhani',sans-serif; }
  .qcard { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 15px; margin-bottom: 11px; }
  .qnum { font-size: 0.68rem; color: var(--sub); margin-bottom: 3px; }
  .qtext { font-size: 0.87rem; font-weight: 700; color: var(--white); margin-bottom: 11px; line-height: 1.5; }
  .opt { display: block; width: 100%; background: #1a2a50; border: 1.5px solid #2a3f70; color: #b8c8f0; border-radius: 8px; padding: 9px 12px; text-align: left; font-size: 0.8rem; font-family: 'Nunito',sans-serif; cursor: pointer; margin-bottom: 6px; transition: all 0.2s; }
  .opt:hover:not(:disabled) { background: #243660; border-color: var(--gold); color: var(--white); }
  .opt.correct { background: #1a4a2e; border-color: var(--green); color: var(--green); }
  .opt.wrong { background: #4a1a1a; border-color: var(--accent); color: var(--accent); }
  .opt:disabled { cursor: not-allowed; }
  .exp-box { display: none; background: #0d2040; border: 1px solid var(--border); border-radius: 8px; padding: 9px 11px; font-size: 0.78rem; color: var(--sub); margin-top: 4px; line-height: 1.5; }
  .exp-box.show { display: block; }

  /* BOTTOM NAV */
  .bnav { position: fixed; bottom: 0; left: 0; right: 0; background: #0b1630; border-top: 2px solid var(--gold); display: flex; z-index: 200; overflow-x: auto; }
  .bnav-btn { flex: 1; min-width: 60px; padding: 8px 0 6px; background: none; border: none; color: #4a6090; font-size: 0.52rem; font-family: 'Nunito',sans-serif; font-weight: 700; cursor: pointer; display: flex; flex-direction: column; align-items: center; gap: 2px; transition: color 0.2s; white-space: nowrap; }
  .bnav-btn.active, .bnav-btn:hover { color: var(--gold); }
  .bnav-btn svg { width: 17px; height: 17px; }
</style>
</head>
<body>

<header>
  <h1>IB JIO <span>Tier 2</span> – Master Study Guide</h1>
  <p>Electronics • Commands • Networking • Technical Awareness • Skill Test • Quiz</p>
</header>
[4/13/2026 8:15 PM] Aakash SUI UXUY: <div class="tabs">
  <button class="tab-btn active" onclick="show('electronics',this)">⚡ Electronics</button>
  <button class="tab-btn" onclick="show('commands',this)">💻 CMD Commands</button>
  <button class="tab-btn" onclick="show('networking',this)">🌐 Networking</button>
  <button class="tab-btn" onclick="show('technical',this)">📚 Tech Awareness</button>
  <button class="tab-btn" onclick="show('skill',this)">🛠 Skill Test</button>
  <button class="tab-btn" onclick="show('quiz',this)">🧠 Quiz</button>
</div>

<!-- ═══════════ ELECTRONICS ═══════════ -->
<div class="section active" id="electronics">
<div class="sec-title">⚡ Basic Electronic Components – Detailed</div>

<!-- RESISTOR -->
<div class="topic-card">
  <div class="topic-header" onclick="toggle(this)">
    <div class="topic-header-left"><span class="topic-num">1</span><span class="topic-name">Resistor</span></div>
    <span class="arrow">▼</span>
  </div>
  <div class="topic-body">
    <div class="cb">
      <h4>Definition</h4>
      <p>A resistor is a passive electronic component that opposes or limits the flow of electric current in a circuit. Unit: <strong>Ohm (Ω)</strong>. Symbol: R</p>

      <h4>Ohm's Law</h4>
      <div class="cmd-box">V = I × R
<span class="comment"># V = Voltage (Volts), I = Current (Amperes), R = Resistance (Ohms)</span>
Power: P = V × I = I² × R = V²/R</div>

      <h4>Types of Resistors</h4>
      <ul>
        <li><strong>Fixed Resistors:</strong> Constant resistance value
          <ul>
            <li><strong>Carbon Composition:</strong> Carbon + insulating material. Cheap, less accurate. Usually 4 color bands.</li>
            <li><strong>Carbon Film:</strong> Carbon film on ceramic rod. Better accuracy than carbon composition.</li>
            <li><strong>Metal Film:</strong> Nickel chromium film on ceramic. High accuracy (±1%), 5 color bands. Low noise.</li>
            <li><strong>Wire-wound:</strong> Resistance wire wound on ceramic. High power handling. Used in power supplies.</li>
            <li><strong>Thin Film Resistor:</strong> 10–1000 nm resistive layer on glass/ceramic/silicon. Tolerance ±0.1% to ±1%. Very low noise, high stability. TCR: ±5 to ±50 ppm/°C. Used in precision and high-frequency circuits.</li>
            <li><strong>Fusible Resistor:</strong> Acts as resistor + fuse. Has 5 bands — last band is WHITE (unique identifier). Burns open to protect circuit.</li>
            <li><strong>SMD Resistor:</strong> Surface Mount Device. Very small. Used on PCBs. Identified by 3-digit code (e.g., 472 = 47×100 = 4700 Ω).</li>
          </ul>
        </li>
        <li><strong>Variable Resistors:</strong> Resistance can be changed manually
          <ul>
            <li><strong>Potentiometer (Pot):</strong> 3 terminals (2 ends + wiper). Works as voltage divider. Used in volume control, brightness control.</li>
            <li><strong>Rheostat:</strong> 2 terminals. Controls current. Used in series with load. High power rating. Used in lamp dimmers, motor speed control.</li>
            <li><strong>Trimmer (Preset):</strong> Small, adjusted with screwdriver. For calibration on PCBs. Infrequent adjustment. Also called preset resistor.</li>
          </ul>
        </li>
      </ul>

      <h4>Resistor Color Code (4-Band)</h4>
      <table class="tbl">
        <tr><th>Color</th><th>Digit</th><th>Multiplier</th><th>Tolerance</th></tr>
        <tr><td>Black</td><td>0</td><td>×1</td><td>—</td></tr>
        <tr><td>Brown</td><td>1</td><td>×10</td><td>±1%</td></tr>
        <tr><td>Red</td><td>2</td><td>×100</td><td>±2%</td></tr>
        <tr><td>Orange</td><td>3</td><td>×1K</td><td>—</td></tr>
        <tr><td>Yellow</td><td>4</td><td>×10K</td><td>—</td></tr>
        <tr><td>Green</td><td>5</td><td>×100K</td><td>±0.5%</td></tr>
        <tr><td>Blue</td><td>6</td><td>×1M</td><td>±0.25%</td></tr>
 <tr><td>Violet</td><td>7</td><td>×10M</td><td>±0.1%</td></tr>
        <tr><td>Grey</td><td>8</td><td>—</td><td>±0.05%</td></tr>
        <tr><td>White</td><td>9</td><td>—</td><td>Fusible</td></tr>
        <tr><td>Gold</td><td>—</td><td>×0.1</td><td>±5%</td></tr>
        <tr><td>Silver</td><td>—</td><td>×0.01</td><td>±10%</td></tr>
      </table>
      <p><strong>Memory Trick:</strong> BB ROY Great Britain Very Good Wife — Black Brown Red Orange Yellow Green Blue Violet Grey White</p>

      <h4>Rheostat vs Potentiometer</h4>
      <table class="tbl">
        <tr><th>Feature</th><th>Rheostat</th><th>Potentiometer</th></tr>
        <tr><td>Terminals</td><td>2</td><td>3</td></tr>
        <tr><td>Controls</td><td>Current</td><td>Voltage</td></tr>
        <tr><td>Connection</td><td>Series with load</td><td>Voltage divider</td></tr>
        <tr><td>Power Rating</td><td>High</td><td>Low</td></tr>
        <tr><td>Size</td><td>Large/bulky</td><td>Small/compact</td></tr>
        <tr><td>Uses</td><td>Motor speed, lamp dimmer</td><td>Volume control, brightness</td></tr>
      </table>

      <h4>Series &amp; Parallel Combinations</h4>
      <div class="cmd-box"><span class="comment"># Series: Total R = R1 + R2 + R3 (same current flows)</span>
<span class="comment"># Parallel: 1/RT = 1/R1 + 1/R2 + 1/R3 (same voltage)</span>
<span class="comment"># Two parallel resistors: RT = (R1 × R2) / (R1 + R2)</span></div>

      <div class="kp"><strong>📌 Key Fact:</strong> Fusible resistor has WHITE as its last (5th) band — the only resistor with a white band. It acts as both a resistor and a fuse, protecting circuits from overcurrent.</div>
      <div class="tag-row"><span class="tag">Ohm's Law</span><span class="tag">Color Code</span><span class="tag">Potentiometer</span><span class="tag">Rheostat</span><span class="tag">Thin Film</span></div>
    </div>
  </div>
</div>

<!-- CAPACITOR -->
<div class="topic-card">
  <div class="topic-header" onclick="toggle(this)">
    <div class="topic-header-left"><span class="topic-num">2</span><span class="topic-name">Capacitor</span></div>
    <span class="arrow">▼</span>
  </div>
  <div class="topic-body">
    <div class="cb">
      <h4>Definition</h4>
      <p>A capacitor is a passive component that stores electrical energy in the form of an electric field. It consists of two conducting plates separated by an insulating material called dielectric. Unit: <strong>Farad (F)</strong>. Practical units: µF, nF, pF.</p>

      <h4>Formula</h4>
      <div class="cmd-box">Q = C × V
<span class="comment"># Q = Charge (Coulombs), C = Capacitance (Farads), V = Voltage</span>
Energy stored: E = ½ × C × V²</div>

      <h4>Types of Capacitors</h4>

      <h4>1. Fixed Capacitors</h4>
      <ul>
        <li><strong>Mica Capacitor:</strong> Dielectric = Mica (silvered). Non-polarized. Very stable capacitance. Low dielectric loss. High Q-factor. High insulation resistance. Long life. Used in RF amplifiers, oscillators, tuned circuits, communication equipment. Frequency: up to GHz range.</li>
        <li><strong>Ceramic Capacitor:</strong> Dielectric = Ceramic material. Non-polarized. Most commonly used. Types: Disc ceramic &amp; MLCC (Multilayer Ceramic Capacitor). Used in decoupling, filtering, bypassing.</li>
        <li><strong>Paper Capacitor:</strong> Dielectric = Thin paper (oil-impregnated or waxed). Metal foil as plates. Non-polarized. Rolled into cylinder. Used in audio coupling (older equipment), AC signal coupling.</li>
        <li><strong>Film Capacitor (Plastic Capacitor):</strong> Dielectric = Plastic film (Polyester, Polypropylene, Polystyrene). Non-polarized. High stability, reliability. Used in audio circuits, timing circuits, filters, oscillators.</li>
        <li><strong>Electrolytic Capacitor:</strong> Polarized (has + and − terminals). Dielectric = thin oxide layer. Cathode = electrolyte (liquid/gel/solid). Very high capacitance (µF to mF range). Types: Aluminium (high capacitance, low cost) &amp; Tantalum (small size, stable, expensive). ⚠️ Reverse connection can BURST the capacitor.
 Used in power supply filters, audio amplifiers, DC smoothing.</li>
      </ul>

      <h4>2. Variable (Adjustable) Capacitors</h4>
      <ul>
        <li>Capacitance changes by varying overlapping area or distance between plates</li>
        <li>One plate fixed, other moves/rotates</li>
        <li>Used in radio tuning, RF circuits</li>
        <li><strong>Trimmer Capacitor:</strong> Small, adjusted with screwdriver. For fine-tuning circuits on PCB.</li>
      </ul>

      <h4>Capacitor Applications</h4>
      <ul>
        <li><strong>Energy Storage:</strong> Camera flash, power backup</li>
        <li><strong>Power Supply Filtering:</strong> Smooths DC ripples after rectification</li>
        <li><strong>Coupling:</strong> Passes AC, blocks DC (used in amplifiers)</li>
        <li><strong>Decoupling:</strong> Removes noise from power supply</li>
        <li><strong>Motor Starting:</strong> Creates phase shift to start AC motors (fans, pumps)</li>
        <li><strong>Tuning:</strong> Select frequency in radio/TV</li>
        <li><strong>Timing:</strong> RC circuits with 555 timer IC</li>
        <li><strong>Power Factor Correction:</strong> Industrial use</li>
        <li><strong>DRAM Memory:</strong> Each memory cell is a capacitor</li>
        <li><strong>Voltage Regulation</strong></li>
      </ul>

      <h4>Capacitor Comparison</h4>
      <table class="tbl">
        <tr><th>Type</th><th>Polarized</th><th>Capacitance</th><th>Best Use</th></tr>
        <tr><td>Mica</td><td>No</td><td>pF to nF</td><td>RF/High frequency</td></tr>
        <tr><td>Ceramic</td><td>No</td><td>pF to µF</td><td>General purpose</td></tr>
        <tr><td>Film</td><td>No</td><td>nF to µF</td><td>Audio, timing</td></tr>
        <tr><td>Electrolytic</td><td>Yes</td><td>µF to mF</td><td>Power supply</td></tr>
        <tr><td>Tantalum</td><td>Yes</td><td>µF range</td><td>Compact, stable DC</td></tr>
      </table>

      <div class="kp"><strong>📌 Key Fact:</strong> Electrolytic capacitors are polarized — always connect + to + and − to −. Reverse polarity causes the capacitor to burst due to internal gas buildup. The negative side is marked with a stripe (−) on the capacitor body.</div>
      <div class="tag-row"><span class="tag">Mica</span><span class="tag">Ceramic</span><span class="tag">Electrolytic</span><span class="tag">MLCC</span><span class="tag">Tantalum</span></div>
    </div>
  </div>
</div>

<!-- DIODE -->
<div class="topic-card">
  <div class="topic-header" onclick="toggle(this)">
    <div class="topic-header-left"><span class="topic-num">3</span><span class="topic-name">Diode – All Types</span></div>
    <span class="arrow">▼</span>
  </div>
  <div class="topic-body">
    <div class="cb">
      <h4>Definition</h4>
      <p>A diode is a semiconductor device with a PN junction that allows current to flow in only one direction (from Anode (+) to Cathode (−) when forward biased). Forward voltage drop: ~0.7V for Silicon, ~0.3V for Germanium.</p>

      <h4>Biasing</h4>
      <ul>
        <li><strong>Forward Biased:</strong> P-side connected to +, N-side to −. Current flows. Low resistance.</li>
        <li><strong>Reverse Biased:</strong> P-side connected to −, N-side to +. No current (except leakage). High resistance.</li>
      </ul>

      <h4>Types of Diodes</h4>
      <ul>
        <li><strong>PN Junction Diode:</strong> Basic diode. Used for rectification, signal clipping, clamping.</li>
        <li><strong>Zener Diode:</strong> Operates in reverse breakdown. Maintains constant voltage (voltage reference). Used in voltage regulators. Symbol: bent cathode.</li>
        <li><strong>LED (Light Emitting Diode):</strong> Emits light when forward biased. Heavily doped. Color depends on semiconductor material (GaAs=IR, GaP=Green, GaN=Blue/White). Used in displays, indicators, lighting.</li>
 <li><strong>Photodiode:</strong> Converts light to current. Works in reverse bias. Used in solar cells, optical sensors, cameras.</li>
        <li><strong>Schottky Diode:</strong> Metal-semiconductor junction. Very fast switching. Low forward voltage drop (~0.3V). Common part
