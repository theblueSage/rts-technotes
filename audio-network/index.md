---
title: Audio network & signal chain
description: How audio routes from stage to Pro Tools, monitoring, and the mastering chain — the studio-wide network (same for every band).
tags: [signal-chain, madi, routing, network]
status: confirmed
updated: 2026-10-20
---

The studio-wide audio network — **the same for every band**. Stage sources run
over snakes and AES50 into the M32C, across MADI to Pro Tools and the converters,
out to monitoring, with the analog mastering chain patched through Patch XT and
the Flock Patch. (Generated from the master draw.io *"New Audio Channel Network"*.)

<figure class="diagram">
<svg class="audio-net" viewBox="0 0 940 790" role="img" xmlns="http://www.w3.org/2000/svg" aria-labelledby="an-title an-desc">
<title id="an-title">Right Take Studio audio network</title>
<desc id="an-desc">Signal flow from stage snakes and in-ear monitors through the MIDAS M32C and stagebox over AES50, across MADI to the Pro Tools PCIe card and AD/DA converters and FerroFish, out to Grace M905 monitoring, with the mastering outboard patched through Patch XT and Flock Patch.</desc>
<style>
  .audio-net{width:100%;height:auto}
  .audio-net text{font-family:'Raleway',sans-serif}
  .audio-net .zone{font-family:'Bebas Neue',sans-serif;fill:var(--gold);font-size:12px;letter-spacing:2.5px}
  .audio-net .node{fill:var(--brick-dark);stroke:var(--gold-dim);stroke-width:1.5}
  .audio-net .node.accent{stroke:var(--gold);stroke-width:2}
  .audio-net .nlabel{fill:var(--cream);font-size:12.5px;font-weight:600;text-anchor:middle}
  .audio-net .nsub{fill:var(--gold-pale);font-size:10px;text-anchor:middle;font-style:italic}
  .audio-net .cluster{fill:rgba(26,8,8,.55);stroke:var(--gold-dim);stroke-width:1.5}
  .audio-net .chead{fill:var(--gold-light);font-family:'Bebas Neue',sans-serif;font-size:12px;letter-spacing:1.5px}
  .audio-net .cline{fill:rgba(249,243,232,.82);font-size:10.5px}
  .audio-net .edge{fill:none;stroke:var(--gold-dim);stroke-width:1.6;marker-end:url(#ah)}
  .audio-net .edge.bi{marker-start:url(#ah)}
  .audio-net .elabel{fill:var(--gold-light);font-size:9.5px;font-style:italic;text-anchor:middle}
</style>
<defs><marker id="ah" markerWidth="9" markerHeight="9" refX="6" refY="3" orient="auto"><path d="M0,0 L6,3 L0,6 z" fill="var(--gold)"/></marker></defs>
<path class="edge" d="M125,92 C 140,190 330,266 470,266"/>
<path class="edge" d="M445,92 L445,150"/>
<path class="edge" d="M667,92 L667,150"/>
<path class="edge" d="M425,92 C 400,180 455,255 505,265"/>
<path class="edge" d="M648,92 C 625,185 600,250 580,265"/>
<path class="edge" d="M445,198 C 460,228 490,252 512,265"/>
<path class="edge" d="M660,198 C 635,228 600,252 582,266"/>
<path class="edge bi" d="M440,290 L310,290"/>
<text class="elabel" x="375" y="283">AES50 A</text>
<path class="edge" d="M200,319 C 198,350 197,368 197,390"/>
<path class="edge" d="M310,300 C 350,330 375,360 400,384"/>
<path class="edge bi" d="M305,410 L360,407"/>
<path class="edge" d="M360,474 C 320,466 280,456 262,446"/>
<path class="edge bi" d="M305,428 C 450,432 520,436 600,440"/>
<text class="elabel" x="455" y="424">MADI OPT</text>
<path class="edge" d="M525,405 C 560,412 580,424 600,434"/>
<path class="edge" d="M600,460 C 560,468 540,472 527,474"/>
<path class="edge" d="M190,446 C 183,490 179,515 177,545"/>
<text class="elabel" x="163" y="500">× 2</text>
<path class="edge" d="M265,569 L300,569"/>
<path class="edge" d="M265,576 C 360,600 440,588 478,576"/>
<path class="edge" d="M400,692 C 418,688 430,684 440,680"/>
<path class="edge" d="M625,679 L655,679"/>
<path class="edge" d="M745,655 C 748,545 705,500 692,468"/>
<text class="zone" x="40" y="30">STAGE</text>
<text class="zone" x="355" y="140">PRE-AMPS</text>
<text class="zone" x="120" y="256">DESK / I-O</text>
<text class="zone" x="90" y="382">MADI CORE</text>
<text class="zone" x="90" y="537">MONITORING</text>
<text class="zone" x="40" y="640">MASTERING</text>
<g><rect class="node" x="40" y="40" width="170" height="52" rx="4"/><text class="nlabel" x="125" y="62">In-Ear Monitors</text><text class="nsub" x="125" y="78">× 4 mixes</text></g>
<g><rect class="node" x="355" y="40" width="180" height="52" rx="4"/><text class="nlabel" x="445" y="62">Front Stage Snake</text><text class="nsub" x="445" y="78">12 out</text></g>
<g><rect class="node" x="575" y="40" width="185" height="52" rx="4"/><text class="nlabel" x="667" y="62">Rear Stage Snake</text><text class="nsub" x="667" y="78">16 out / 4 in</text></g>
<g><rect class="node" x="800" y="40" width="120" height="52" rx="4"/><text class="nlabel" x="860" y="62">Spare Stereo</text><text class="nsub" x="860" y="78">out</text></g>
<g><rect class="node" x="355" y="150" width="180" height="48" rx="4"/><text class="nlabel" x="445" y="170">Grace M801 mk2</text><text class="nsub" x="445" y="185">mic pre</text></g>
<g><rect class="node" x="575" y="150" width="185" height="48" rx="4"/><text class="nlabel" x="667" y="170">Phoenix DRS8 MKII</text><text class="nsub" x="667" y="185">mic pre</text></g>
<g><rect class="node accent" x="120" y="265" width="190" height="54" rx="4"/><text class="nlabel" x="215" y="289">MIDAS M32C</text><text class="nsub" x="215" y="305">digital desk</text></g>
<g><rect class="node accent" x="440" y="265" width="220" height="54" rx="4"/><text class="nlabel" x="550" y="289">Stagebox</text><text class="nsub" x="550" y="305">32 in / 16 out</text></g>
<g><rect class="node accent" x="90" y="390" width="215" height="56" rx="4"/><text class="nlabel" x="197" y="414">PCIe Card 3 MADI</text><text class="nsub" x="197" y="430">Pro Tools</text></g>
<g><rect class="node" x="360" y="384" width="165" height="46" rx="4"/><text class="nlabel" x="442" y="404">DA Converter</text><text class="nsub" x="442" y="419">32 ch</text></g>
<g><rect class="node" x="360" y="452" width="165" height="46" rx="4"/><text class="nlabel" x="442" y="472">AD Converter</text><text class="nsub" x="442" y="487">32 ch</text></g>
<g><rect class="node accent" x="600" y="414" width="180" height="54" rx="4"/><text class="nlabel" x="690" y="438">FerroFish A32 Pro</text><text class="nsub" x="690" y="453">MADI hub</text></g>
<g><rect class="node" x="90" y="545" width="175" height="48" rx="4"/><text class="nlabel" x="177" y="565">Grace M905</text><text class="nsub" x="177" y="580">monitor control</text></g>
<g><rect class="node" x="300" y="545" width="140" height="48" rx="4"/><text class="nlabel" x="370" y="573">Cue Mix (¼")</text></g>
<g><rect class="node" x="475" y="545" width="120" height="48" rx="4"/><text class="nlabel" x="535" y="573">AES OUT</text></g>
<g><rect class="cluster" x="40" y="648" width="360" height="122" rx="5"/><text class="chead" x="58" y="670">MASTERING OUTBOARD</text><text class="cline" x="58" y="692">Shelford Channel</text><text class="cline" x="58" y="710">Manley Core · Manley Force (×4)</text><text class="cline" x="58" y="728">Heritage 1073 (×2)</text><text class="cline" x="58" y="750" style="fill:var(--gold-pale);font-style:italic">→ XLR patch →</text></g>
<g><rect class="node accent" x="440" y="655" width="185" height="48" rx="4"/><text class="nlabel" x="532" y="675">Patch XT</text><text class="nsub" x="532" y="690">analog routing</text></g>
<g><rect class="node" x="655" y="655" width="180" height="48" rx="4"/><text class="nlabel" x="745" y="675">Flock Patch</text><text class="nsub" x="745" y="690">mastering</text></g>
</svg>
</figure>

## How it flows

- **Stage → desk.** In-ear monitors, the Front Stage Snake (12 out) and Rear
  Stage Snake (16 out / 4 in) feed the **Stagebox (32 in / 16 out)**, which links
  to the **MIDAS M32C** over **AES50 A**. Snakes also feed the **Grace M801 mk2**
  and **Phoenix DRS8 MKII** mic pres.
- **MADI core.** The M32C crosses to the **PCIe Card 3 MADI** (Pro Tools) and the
  **32-channel AD/DA converters**, hubbed through the **FerroFish A32 Pro** over
  MADI optical.
- **Monitoring.** The MADI card feeds the **Grace M905** monitor controller → Cue
  Mix and AES OUT.
- **Mastering.** The analog outboard (Shelford, Manley Core/Force, Heritage 1073)
  patches through **Patch XT** and the **Flock Patch** back into the FerroFish.

> The per-channel D-sub patch assignments behind Patch XT and the Flock Patch are
> mapped separately (rack + DB25/D-sub mapping).
