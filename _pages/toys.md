---
title: "Toys"
layout: textlay
description: "Interactive calculators and reference databases for low-temperature plasma physics: energy and spectroscopic unit converters, reduced electric field, plasma parameters, electron energy distributions, and Paschen curves, plus the databases and codes we use."
permalink: /toys/
---

# Toys

<div class="toys" markdown="0">

<style>
.toys-intro { font-size: 18px; line-height: 1.6; color: #444; margin: 10px 0 30px 0; max-width: 860px; }
.toy { background: #f8f9fa; border: 1px solid #e0e0e0; border-top: 4px solid #3498db; border-radius: 10px; padding: 22px 26px; margin: 0 0 28px 0; box-shadow: 0 2px 8px rgba(0,0,0,0.06); }
.toy h2 { margin: 0 0 6px 0; font-size: 24px; color: #2c3e50; border: none; padding: 0; }
.toy > p { font-size: 15px; line-height: 1.55; color: #555; margin: 0 0 16px 0; max-width: 900px; }
.toy-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(190px, 1fr)); gap: 12px 18px; margin: 0 0 14px 0; }
.toy label { display: block; font-size: 14px; font-weight: 700; color: #666; margin: 0 0 3px 0; }
.toy label sup, .toy label sub { line-height: 0; }
.toy input, .toy select { width: 100%; box-sizing: border-box; font-size: 16px; padding: 7px 10px; border: 1px solid #c8d2dc; border-radius: 6px; background: #fff; color: #2c3e50; font-family: inherit; }
.toy input:focus, .toy select:focus { outline: none; border-color: #337ab7; box-shadow: 0 0 0 2px rgba(51,122,183,0.15); }
.toy-out { display: grid; grid-template-columns: repeat(auto-fill, minmax(230px, 1fr)); gap: 8px 18px; margin: 10px 0 0 0; }
.toy-out div { background: #fff; border: 1px solid #e6ebf0; border-radius: 6px; padding: 8px 12px; font-size: 15px; color: #444; }
.toy-out span { display: block; font-size: 13px; color: #888; }
.toy-out b { font-size: 17px; color: #2c3e50; font-weight: 700; }
.toy-plot { background: #fff; border: 1px solid #e6ebf0; border-radius: 8px; margin: 14px 0 0 0; padding: 6px; overflow: hidden; }
.toy-plot svg { width: 100%; height: auto; display: block; }
.toy-note { font-size: 13px; color: #777; margin: 12px 0 0 0; }
.toy-btn { display: inline-block; padding: 6px 14px; font-size: 14px; border: 1px solid #337ab7; border-radius: 6px; color: #337ab7; background: #fff; cursor: pointer; font-family: inherit; }
.toy-btn:hover { background: #337ab7; color: #fff; }
.db-section h2 { font-size: 26px; color: #2c3e50; border-bottom: 2px solid #3498db; padding-bottom: 8px; margin: 40px 0 16px 0; }
.db-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(290px, 1fr)); gap: 16px; }
.db { background: #fff; border: 1px solid #e0e0e0; border-radius: 8px; padding: 16px 18px; }
.db h3 { margin: 0 0 10px 0; font-size: 17px; color: #2c3e50; }
.db ul { margin: 0; padding-left: 18px; font-size: 15px; line-height: 1.6; color: #444; }
.db ul li { margin: 0 0 4px 0; }
.db small { color: #777; }
</style>

<p class="toys-intro">
Small tools for quick estimates in low-temperature plasma physics, together with the databases and codes we use in our work. The calculators rely on textbook formulas and idealized assumptions, so treat the numbers as order-of-magnitude guides rather than as a substitute for a kinetic model.
</p>

<!-- ===================== Energy unit converter ===================== -->
<div class="toy" id="toy-energy">
<h2>Energy unit converter</h2>
<p>Type a value in any box and the others update. The kelvin value is the temperature with k<sub>B</sub>T equal to the energy.</p>
<div class="toy-grid" id="energy-grid"></div>
<div style="display:flex; gap:14px; align-items:center; flex-wrap:wrap;">
<button class="toy-btn" id="energy-reset">Reset to 1 eV</button>
<label style="margin:0; display:flex; align-items:center; gap:8px; font-size:14px;">Digits <select id="energy-digits" style="width:auto;"><option>3</option><option>4</option><option selected>5</option><option>6</option><option>8</option></select></label>
</div>
</div>

<!-- ===================== Spectroscopic unit converter ===================== -->
<div class="toy" id="toy-spec">
<h2>Spectroscopic unit converter</h2>
<p>Photon energy, wavenumber and vacuum wavelength of the same transition. Type a value in any box and the others update.</p>
<div class="toy-grid" id="spec-grid"></div>
<div style="display:flex; gap:14px; align-items:center; flex-wrap:wrap;">
<button class="toy-btn" id="spec-reset">Reset to 1 eV</button>
<label style="margin:0; display:flex; align-items:center; gap:8px; font-size:14px;">Digits <select id="spec-digits" style="width:auto;"><option>3</option><option>4</option><option selected>5</option><option>6</option><option>8</option></select></label>
</div>
</div>

<!-- ===================== Reduced electric field ===================== -->
<div class="toy" id="toy-field">
<h2>Reduced electric field</h2>
<p>Convert between the electric field, the reduced field E/N in townsend (1 Td = 10<sup>&minus;17</sup> V cm<sup>2</sup>) and E/p. Edit either E or E/N, the other follows.</p>
<div class="toy-grid">
<div><label>E (V/cm)</label><input id="f-E" type="number" step="any" value="100"></div>
<div><label>E/N (Td)</label><input id="f-EN" type="number" step="any"></div>
<div><label>Pressure</label><input id="f-p" type="number" step="any" value="1"></div>
<div><label>Pressure unit</label><select id="f-punit"><option value="torr" selected>Torr</option><option value="pa">Pa</option><option value="mbar">mbar</option><option value="atm">atm</option></select></div>
<div><label>Gas temperature (K)</label><input id="f-Tg" type="number" step="any" value="300"></div>
</div>
<div class="toy-out" id="f-out"></div>
</div>

<!-- ===================== Plasma parameters ===================== -->
<div class="toy" id="toy-plasma">
<h2>Plasma parameter calculator</h2>
<p>The three numbers that tell you whether something is a plasma: the Debye length, the electron plasma frequency, and the number of electrons in a Debye sphere, N<sub>D</sub>, which should be much larger than one for collective behavior.</p>
<div class="toy-grid">
<div><label>n<sub>e</sub> (cm<sup>&minus;3</sup>)</label><input id="p-ne" type="text" value="1e10"></div>
<div><label>T<sub>e</sub> (eV)</label><input id="p-Te" type="number" step="any" value="3"></div>
</div>
<div class="toy-out" id="p-out"></div>
<p class="toy-note">Formulas: &lambda;<sub>D</sub> = (&epsilon;<sub>0</sub> T<sub>e</sub>/e n<sub>e</sub>)<sup>1/2</sup>, &omega;<sub>pe</sub> = (e<sup>2</sup> n<sub>e</sub>/&epsilon;<sub>0</sub> m<sub>e</sub>)<sup>1/2</sup>, N<sub>D</sub> = (4&pi;/3) n<sub>e</sub> &lambda;<sub>D</sub><sup>3</sup>.</p>
</div>

<!-- ===================== EEDF ===================== -->
<div class="toy" id="toy-eedf">
<h2>Electron energy distribution function</h2>
<p>Generalized distribution f(&epsilon;) &prop; &epsilon;<sup>1/2</sup> exp[&minus;c (&epsilon;/&lang;&epsilon;&rang;)<sup>x</sup>], where x = 1 is Maxwellian and x = 2 is Druyvesteyn, normalized to a fixed mean energy. The plot shows the electron energy probability function f(&epsilon;)/&epsilon;<sup>1/2</sup>, which is a straight line for a Maxwellian on a semilog scale.</p>
<div class="toy-grid">
<div><label>Mean energy &lang;&epsilon;&rang; (eV)</label><input id="e-mean" type="number" step="any" value="4.5"></div>
<div><label>Shape x</label><select id="e-x"><option value="1" selected>1 (Maxwellian)</option><option value="1.5">1.5</option><option value="2">2 (Druyvesteyn)</option><option value="3">3</option></select></div>
<div><label>Plot up to (eV)</label><input id="e-max" type="number" step="any" value="30"></div>
</div>
<div class="toy-out" id="e-out"></div>
<div class="toy-plot" id="e-plot"></div>
<p class="toy-note">For a Maxwellian, T<sub>e</sub> = 2&lang;&epsilon;&rang;/3.</p>
</div>

<!-- ===================== Paschen ===================== -->
<div class="toy" id="toy-paschen">
<h2>Paschen curve</h2>
<p>Breakdown voltage of a uniform-field gap from the Townsend criterion, V<sub>B</sub> = B pd / [ln(A pd) &minus; ln ln(1 + 1/&gamma;)], with the empirical constants A and B of the first Townsend coefficient &alpha;/p = A exp(&minus;B p/E).</p>
<div class="toy-grid">
<div><label>Gas</label><select id="pa-gas"></select></div>
<div><label>A (1/cm Torr)</label><input id="pa-A" type="number" step="any"></div>
<div><label>B (V/cm Torr)</label><input id="pa-B" type="number" step="any"></div>
<div><label>&gamma; (secondary emission)</label><input id="pa-g" type="number" step="any" value="0.01"></div>
</div>
<div class="toy-out" id="pa-out"></div>
<div class="toy-plot" id="pa-plot"></div>
<p class="toy-note">Constants from Raizer, <i>Gas Discharge Physics</i> (1991), Table 4.1. They are fits over a limited E/p range and the curve is only indicative far from the minimum.</p>
</div>

<!-- ===================== Databases ===================== -->
<div class="db-section">
<h2>Databases and codes</h2>
<div class="db-grid">

<div class="db">
<h3>Data</h3>
<ul>
<li><a href="https://lxcat.net" target="_blank" rel="noopener">LXCat</a> <small>electron and ion scattering cross sections, swarm data</small></li>
<li><a href="https://physics.nist.gov/asd" target="_blank" rel="noopener">NIST Atomic Spectra Database</a> <small>levels, lines, transition probabilities</small></li>
<li><a href="https://physics.nist.gov/PhysRefData/Ionization/" target="_blank" rel="noopener">NIST Electron-Impact Cross Sections</a> <small>ionization and excitation</small></li>
<li><a href="https://library.psfc.mit.edu/catalog/online_pubs/NRL_FORMULARY_19.pdf" target="_blank" rel="noopener">NRL Plasma Formulary</a> <small>formulas and constants</small></li>
</ul>
</div>

<div class="db">
<h3>Electron and plasma kinetics</h3>
<ul>
<li><a href="https://www.bolsig.laplace.univ-tlse.fr/" target="_blank" rel="noopener">BOLSIG+</a> <small>two-term Boltzmann solver</small></li>
<li><a href="https://github.com/IST-Lisbon/LoKI" target="_blank" rel="noopener">LoKI-B</a> <small>open-source Boltzmann solver, IST Lisbon</small></li>
<li><a href="https://gitlab.com/LXCatThirdParty/MultiBolt" target="_blank" rel="noopener">MultiBolt</a> <small>multi-term Boltzmann solver, C++</small></li>
<li><a href="https://github.com/donkozoltan/eduPIC" target="_blank" rel="noopener">eduPIC</a> <small>introductory PIC/MCC code for RF plasmas</small></li>
<li><a href="https://jc-pic.org/" target="_blank" rel="noopener">JC-PIC</a> <small>interactive 1D3V PIC/MCC code with a graphical interface, J.-P. Boeuf</small></li>
</ul>
</div>

<div class="db">
<h3>Materials and plasma-surface interaction</h3>
<ul>
<li><a href="https://github.com/lcpp-org/RustBCA" target="_blank" rel="noopener">RustBCA</a> <small>binary collision approximation: sputtering, implantation, reflection</small></li>
<li><a href="https://www.lammps.org" target="_blank" rel="noopener">LAMMPS</a> <small>molecular dynamics</small></li>
<li><a href="https://www.quantum-espresso.org" target="_blank" rel="noopener">Quantum ESPRESSO</a> <small>density functional theory</small></li>
</ul>
</div>

</div>
</div>

<script>
(function () {
  "use strict";
  var kB = 8.617333262e-5;      // eV/K
  var e = 1.602176634e-19;      // C
  var me = 9.1093837015e-31;    // kg
  var eps0 = 8.8541878128e-12;  // F/m
  var kBJ = 1.380649e-23;       // J/K

  function $(id) { return document.getElementById(id); }
  function num(id) { var v = parseFloat($(id).value); return isFinite(v) ? v : NaN; }
  function fmt(x, d) {
    if (!isFinite(x)) return "&ndash;";
    d = d || 3;
    var a = Math.abs(x);
    if (a === 0) return "0";
    if (a >= 1e5 || a < 1e-3) {
      var s = x.toExponential(d - 1);
      var parts = s.split("e");
      var exp = parseInt(parts[1], 10);
      return parts[0] + " &times; 10<sup>" + exp + "</sup>";
    }
    return String(parseFloat(x.toPrecision(d)));
  }
  function out(id, items) {
    var h = "";
    items.forEach(function (it) { h += "<div><span>" + it[0] + "</span><b>" + it[1] + "</b> " + (it[2] || "") + "</div>"; });
    $(id).innerHTML = h;
  }
  function on(ids, fn) { ids.forEach(function (id) { $(id).addEventListener("input", fn); $(id).addEventListener("change", fn); }); fn(); }

  /* ---------- Unit converters ---------- */
  // Each unit: [label, factor in eV per unit] or [label, "inverse", constant] for E = constant / value.
  function converter(gridId, resetId, digitsId, prefix, units) {
    var grid = $(gridId);
    units.forEach(function (u, i) {
      var d = document.createElement("div");
      d.innerHTML = "<label>" + u[0] + "</label><input type=\"text\" id=\"" + prefix + i + "\">";
      grid.appendChild(d);
    });
    function toEV(u, v) { return u[1] === "inverse" ? (v > 0 ? u[2] / v : NaN) : v * u[1]; }
    function fromEV(u, eV) { return u[1] === "inverse" ? (eV > 0 ? u[2] / eV : NaN) : eV / u[1]; }
    function set(eV, skip) {
      var d = parseInt($(digitsId).value, 10);
      units.forEach(function (u, i) {
        if (i === skip) return;
        var v = fromEV(u, eV);
        $(prefix + i).value = isFinite(v) ? Number(v.toPrecision(d)).toString() : "";
      });
    }
    units.forEach(function (u, i) {
      $(prefix + i).addEventListener("input", function () {
        var v = parseFloat(this.value); if (!isFinite(v)) return;
        set(toEV(u, v), i);
      });
    });
    $(resetId).addEventListener("click", function () { set(1, -1); });
    $(digitsId).addEventListener("change", function () { var v = parseFloat($(prefix + "0").value); set(isFinite(v) ? v : 1, -1); });
    set(1, -1);
  }
  converter("energy-grid", "energy-reset", "energy-digits", "en-", [
    ["eV", 1], ["meV", 1e-3], ["Joule", 6.241509074e18], ["Kelvin", kB]
  ]);
  converter("spec-grid", "spec-reset", "spec-digits", "sp-", [
    ["eV", 1], ["Wavenumber (cm<sup>&minus;1</sup>)", 1.239841984e-4], ["Wavelength (nm)", "inverse", 1239.841984], ["Rydberg", 13.605693123]
  ]);

  /* ---------- Reduced field ---------- */
  function pTorr(v, unit) { return unit === "pa" ? v / 133.322368 : unit === "mbar" ? v / 1.33322368 : unit === "atm" ? v * 760 : v; }
  function Ncm3(pT, Tg) { return pT * 133.322368 / (kBJ * Tg) * 1e-6; }
  var lastField = "E";
  ["f-E", "f-EN"].forEach(function (id) { $(id).addEventListener("input", function () { lastField = id === "f-E" ? "E" : "EN"; field(); }); });
  on(["f-p", "f-punit", "f-Tg"], field);
  function field() {
    var p = pTorr(num("f-p"), $("f-punit").value), Tg = num("f-Tg"), N = Ncm3(p, Tg);
    var E, EN;
    if (lastField === "E") { E = num("f-E"); EN = E / N / 1e-17; $("f-EN").value = isFinite(EN) ? Number(EN.toPrecision(5)) : ""; }
    else { EN = num("f-EN"); E = EN * 1e-17 * N; $("f-E").value = isFinite(E) ? Number(E.toPrecision(5)) : ""; }
    out("f-out", [["Gas number density N", fmt(N, 4), "cm<sup>&minus;3</sup>"], ["E/p", fmt(E / p, 4), "V cm<sup>&minus;1</sup> Torr<sup>&minus;1</sup>"], ["E/N", fmt(EN, 4), "Td"], ["E", fmt(E, 4), "V/cm"]]);
  }

  /* ---------- Plasma parameters ---------- */
  on(["p-ne", "p-Te"], plasma);
  function plasma() {
    var ne = parseFloat($("p-ne").value), Te = num("p-Te");
    var lD = Math.sqrt(eps0 * Te / (e * ne * 1e6)) * 100;           // cm
    var wpe = Math.sqrt(e * e * ne * 1e6 / (eps0 * me));
    var ND = ne * 4 / 3 * Math.PI * lD * lD * lD;
    out("p-out", [
      ["Debye length &lambda;<sub>D</sub>", fmt(lD * 1e4, 3), "&micro;m"],
      ["Plasma frequency f<sub>pe</sub> = &omega;<sub>pe</sub>/2&pi;", fmt(wpe / 2 / Math.PI / 1e9, 3), "GHz"],
      ["Angular plasma frequency &omega;<sub>pe</sub>", fmt(wpe, 3), "rad/s"],
      ["Electrons in a Debye sphere N<sub>D</sub>", fmt(ND, 3), ""]
    ]);
  }

  /* ---------- SVG plot helper (matplotlib "tecplot-like" style) ---------- */
  function majorTicks(lo, hi, log) {
    var t = [];
    if (log) { for (var k = Math.ceil(lo - 1e-9); k <= Math.floor(hi + 1e-9); k++) t.push(k); if (t.length > 8) t = t.filter(function (v) { return v % 2 === 0; }); return t; }
    var span = hi - lo, step = Math.pow(10, Math.floor(Math.log10(span / 5))), r = span / step / 5;
    step *= r >= 4 ? 10 : r >= 2 ? 5 : r >= 1 ? 2 : 1;
    for (var v = Math.ceil(lo / step - 1e-9) * step; v <= hi + 1e-9; v += step) t.push(Number(v.toPrecision(10)));
    return t;
  }
  function minorTicks(maj, lo, hi, log) {
    var t = [];
    if (log) { for (var k = Math.floor(lo) - 1; k <= Math.ceil(hi); k++) for (var m = 2; m <= 9; m++) { var v = k + Math.log10(m); if (v > lo && v < hi) t.push(v); } return t; }
    if (maj.length < 2) return t;
    var step = maj[1] - maj[0], mant = step / Math.pow(10, Math.floor(Math.log10(step))), n = Math.abs(mant - 2) < 1e-9 ? 4 : 5, ds = step / n;
    for (var v2 = maj[0] - step; v2 <= hi; v2 += ds) if (v2 > lo && v2 < hi) t.push(v2);
    return t;
  }
  function pow10(t) { return "10<tspan dy=\"-8\" font-size=\"12\">" + String(t).replace("-", "&minus;") + "</tspan>"; }
  function plot(el, series, o) {
    var W = 720, H = 400, L = 90, R = 24, T = 24, Bm = 70, FS = 16;
    var xs = [], ys = [];
    series.forEach(function (s) { s.pts.forEach(function (p) { if (isFinite(p[0]) && isFinite(p[1]) && (!o.xlog || p[0] > 0) && (!o.ylog || p[1] > 0)) { xs.push(o.xlog ? Math.log10(p[0]) : p[0]); ys.push(o.ylog ? Math.log10(p[1]) : p[1]); } }); });
    var x0 = o.xmin !== undefined ? o.xmin : Math.min.apply(null, xs), x1 = o.xmax !== undefined ? o.xmax : Math.max.apply(null, xs);
    var y0 = o.ymin !== undefined ? o.ymin : Math.min.apply(null, ys), y1 = o.ymax !== undefined ? o.ymax : Math.max.apply(null, ys);
    if (y1 === y0) y1 = y0 + 1;
    var sx = function (x) { return L + (x - x0) / (x1 - x0) * (W - L - R); }, sy = function (y) { return H - Bm - (y - y0) / (y1 - y0) * (H - T - Bm); };
    var h = "<svg viewBox=\"0 0 " + W + " " + H + "\" xmlns=\"http://www.w3.org/2000/svg\" font-family=\"Arial, Helvetica, sans-serif\" font-size=\"" + FS + "\">";
    var xmaj = majorTicks(x0, x1, o.xlog), ymaj = majorTicks(y0, y1, o.ylog);
    var tick = function (X, Y, dx, dy, w) { return "<line x1=\"" + X + "\" y1=\"" + Y + "\" x2=\"" + (X + dx) + "\" y2=\"" + (Y + dy) + "\" stroke=\"#000\" stroke-width=\"" + w + "\"/>"; };
    minorTicks(xmaj, x0, x1, o.xlog).forEach(function (t) { h += tick(sx(t), H - Bm, 0, -3, 1.5); });
    minorTicks(ymaj, y0, y1, o.ylog).forEach(function (t) { h += tick(L, sy(t), 3, 0, 1.5); });
    xmaj.forEach(function (t) { var X = sx(t); h += tick(X, H - Bm, 0, -7, 2); h += "<text x=\"" + X + "\" y=\"" + (H - Bm + 22) + "\" text-anchor=\"middle\" fill=\"#000\">" + (o.xlog ? pow10(t) : t) + "</text>"; });
    ymaj.forEach(function (t) { var Y = sy(t); h += tick(L, Y, 7, 0, 2); h += "<text x=\"" + (L - 10) + "\" y=\"" + (Y + 6) + "\" text-anchor=\"end\" fill=\"#000\">" + (o.ylog ? pow10(t) : t) + "</text>"; });
    h += "<rect x=\"" + L + "\" y=\"" + T + "\" width=\"" + (W - L - R) + "\" height=\"" + (H - T - Bm) + "\" fill=\"none\" stroke=\"#000\" stroke-width=\"2\"/>";
    h += "<text x=\"" + (L + (W - L - R) / 2) + "\" y=\"" + (H - 14) + "\" text-anchor=\"middle\" fill=\"#000\" font-weight=\"700\">" + o.xlabel + "</text>";
    h += "<text transform=\"translate(22," + (T + (H - T - Bm) / 2) + ") rotate(-90)\" text-anchor=\"middle\" fill=\"#000\" font-weight=\"700\">" + o.ylabel + "</text>";
    series.forEach(function (s, i) {
      var d = "", pen = false;
      s.pts.forEach(function (p) {
        var ok = isFinite(p[0]) && isFinite(p[1]) && (!o.xlog || p[0] > 0) && (!o.ylog || p[1] > 0);
        if (!ok) { pen = false; return; }
        var X = sx(o.xlog ? Math.log10(p[0]) : p[0]), Y = sy(o.ylog ? Math.log10(p[1]) : p[1]);
        if (Y < T || Y > H - Bm || X < L || X > W - R) { pen = false; return; }
        d += (pen ? "L" : "M") + X.toFixed(1) + "," + Y.toFixed(1); pen = true;
      });
      h += "<path d=\"" + d + "\" fill=\"none\" stroke=\"" + s.color + "\" stroke-width=\"2.5\"" + (s.dash ? " stroke-dasharray=\"8,6\"" : "") + "/>";
      var ly = T + 24 + 22 * i, lx = W - R - 14;
      h += "<line x1=\"" + (lx - 150) + "\" y1=\"" + (ly - 5) + "\" x2=\"" + (lx - 112) + "\" y2=\"" + (ly - 5) + "\" stroke=\"" + s.color + "\" stroke-width=\"2.5\"" + (s.dash ? " stroke-dasharray=\"8,6\"" : "") + "/>";
      h += "<text x=\"" + (lx - 104) + "\" y=\"" + ly + "\" fill=\"#000\">" + s.name + "</text>";
    });
    el.innerHTML = h + "</svg>";
  }

  /* ---------- EEDF ---------- */
  function gamma(z) {
    var g = 7, c = [0.99999999999980993, 676.5203681218851, -1259.1392167224028, 771.32342877765313, -176.61502916214059, 12.507343278686905, -0.13857109526572012, 9.9843695780195716e-6, 1.5056327351493116e-7];
    if (z < 0.5) return Math.PI / (Math.sin(Math.PI * z) * gamma(1 - z));
    z -= 1; var x = c[0]; for (var i = 1; i < g + 2; i++) x += c[i] / (z + i);
    var t = z + g + 0.5; return Math.sqrt(2 * Math.PI) * Math.pow(t, z + 0.5) * Math.exp(-t) * x;
  }
  on(["e-mean", "e-x", "e-max"], eedf);
  function eedf() {
    var em = num("e-mean"), x = parseFloat($("e-x").value), emax = num("e-max");
    if (!(em > 0) || !(emax > 0)) return;
    var g3 = gamma(3 / (2 * x)), g5 = gamma(5 / (2 * x));
    var c1 = x * Math.pow(g5, 1.5) / Math.pow(g3, 2.5);
    var c2 = Math.pow(g5 / g3, x);
    var f = function (en) { return c1 / Math.pow(em, 1.5) * Math.sqrt(en) * Math.exp(-c2 * Math.pow(en / em, x)); };
    var Te = 2 * em / 3;
    var pts = [], ptsM = [];
    for (var j = 1; j <= 300; j++) { var ee = j / 300 * emax; pts.push([ee, f(ee) / Math.sqrt(ee)]); ptsM.push([ee, 2 / Math.sqrt(Math.PI) * Math.pow(Te, -1.5) * Math.exp(-ee / Te)]); }
    var series = [{ name: x === 1 ? "Maxwellian" : x === 2 ? "Druyvesteyn" : "x = " + x, pts: pts, color: "#1f4e79" }];
    if (x !== 1) series.push({ name: "Maxwellian", pts: ptsM, color: "#c0392b", dash: true });
    var top = Math.log10(Math.max(pts[0][1], ptsM[0][1]));
    plot($("e-plot"), series, { ylog: true, xlabel: "Electron energy (eV)", ylabel: "EEPF (eV<tspan dy=\"-7\" font-size=\"10\">&minus;3/2</tspan><tspan dy=\"7\">)</tspan>", ymin: Math.ceil(top) - 8, ymax: Math.ceil(top), xmin: 0, xmax: emax });
    out("e-out", [["Effective T<sub>e</sub> = 2&lang;&epsilon;&rang;/3", fmt(Te, 3), "eV"]]);
  }

  /* ---------- Paschen ---------- */
  var gases = [["Air", 15, 365], ["N<sub>2</sub>", 12, 342], ["Ar", 12, 180], ["He", 3, 34], ["Ne", 4, 100], ["Kr", 17, 240], ["Xe", 26, 350], ["H<sub>2</sub>", 5, 130], ["CO<sub>2</sub>", 20, 466], ["Hg", 20, 370], ["Custom", 12, 180]];
  gases.forEach(function (g, i) { var o = document.createElement("option"); o.value = i; o.innerHTML = g[0]; if (g[0] === "Ar") o.selected = true; $("pa-gas").appendChild(o); });
  function setGas() { var g = gases[parseInt($("pa-gas").value, 10)]; if (g[0] !== "Custom") { $("pa-A").value = g[1]; $("pa-B").value = g[2]; } }
  setGas();
  $("pa-gas").addEventListener("change", function () { setGas(); paschen(); });
  on(["pa-A", "pa-B", "pa-g"], paschen);
  function paschen() {
    var A = num("pa-A"), B = num("pa-B"), g = num("pa-g");
    if (!(A > 0) || !(B > 0) || !(g > 0)) return;
    var K = Math.log(Math.log(1 + 1 / g));
    var VB = function (pd) { var d = Math.log(A * pd) - K; return d > 0 ? B * pd / d : NaN; };
    var pdmin = Math.E * Math.log(1 + 1 / g) / A, Vmin = Math.E * B / A * Math.log(1 + 1 / g);
    var pts = [];
    for (var i = 0; i <= 400; i++) { var pd = Math.pow(10, -2 + 5 * i / 400); pts.push([pd, VB(pd)]); }
    plot($("pa-plot"), [{ name: gases[parseInt($("pa-gas").value, 10)][0].replace(/<[^>]+>/g, "") + ", &gamma; = " + g, pts: pts, color: "#1f4e79" }],
      { xlog: true, ylog: true, xlabel: "pd (Torr cm)", ylabel: "Breakdown voltage (V)", xmin: -2, xmax: 3, ymin: 2, ymax: 5 });
    out("pa-out", [["Minimum breakdown voltage", fmt(Vmin, 3), "V"], ["pd at the minimum", fmt(pdmin, 3), "Torr cm"]]);
  }

})();
</script>

</div>
