# 🥗 LazyLean
### The Science-Backed Weight Loss Guide for Lazy, Smart People

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Type](https://img.shields.io/badge/Type-Capstone%20Project-blue)
![Field](https://img.shields.io/badge/Field-Data%20Science%20%2F%20Analytics-9cf)
![Sources](https://img.shields.io/badge/Sources-NIH%20%7C%20OMA%20%7C%20FDA-orange)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-lightgrey)

> An interactive, evidence-based weight loss dashboard for people who love eating and hate suffering.  
> Built with vanilla HTML/CSS/JS · Monte Carlo simulations · NIH-grounded evidence ratings · GLP-1 clinical data.

**Author:** Alexia Le  
**Year:** 2026  
**Live Demo:** Open `index.html` directly in any browser — no server, no install needed.

---

## 📸 Preview

| Section | Description |
|---------|-------------|
| 📊 Evidence | NIH ratings for 9 major OTC supplements |
| 🎯 Simulator | Personal weight loss simulator with 200-trial Monte Carlo + confidence bands |
| 🎲 Monte Carlo | 5-scenario probability analysis across 500 simulated people |
| 🌿 Fiber Guide | Psyllium & glucomannan exact dosing protocols |
| 🛒 Shopping | Budget guide — ~$1.30/day full stack |
| 📋 Lazy Stack | 12-week phased protocol with no gym required |
| 💉 Saxenda | GLP-1 mechanism, injection protocol, vitamin combinations, drug comparison |
| 📚 Sources | 8 cited peer-reviewed and institutional sources |

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/alexia-le/lazylean.git
cd lazylean

# Open directly in browser — no build step required
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

Or simply **drag `index.html` into any browser tab** — it works fully offline.

---

## 📁 Repository Structure

```
lazylean/
├── index.html          # Full interactive dashboard (self-contained)
├── README.md           # This file
├── LICENSE             # MIT License
├── data/
│   └── evidence.json   # Structured evidence database (supplements, drugs, protocols)
└── assets/
    ├── css/            # (reserved for future modularization)
    └── js/             # (reserved for future modularization)
```

---

## 🔑 Key Findings

### Finding 1 — OTC Supplements: Almost All Are Hype
- **Only one FDA-approved OTC weight-loss product exists:** Orlistat (Alli, 60mg) — ~5% body weight loss
- All other major OTC supplements produce **< 1 kg weight loss** on average vs. placebo over 12 weeks
- The FDA issued **36+ adulteration warnings** for weight-loss supplements in a single year
- NIH ODS verdict: *"Evidence supporting dietary supplements to reduce body weight is inconclusive and unconvincing"*

### Finding 2 — The Only OTC Tools With Real Evidence
| Tool | Mechanism | Cost/Day | Evidence |
|------|-----------|----------|----------|
| Psyllium husk (7–10g/day) | Gel formation → satiety, slows gastric emptying | ~$0.15 | ★★★★☆ |
| Glucomannan capsules (1–3g/day) | Absorbs 50× water → fullness | ~$0.22 | ★★★☆☆ |
| Whey protein (1.5g/kg/day) | Highest satiety per calorie, preserves muscle | ~$0.90 | ★★★★★ |

### Finding 3 — The Only Proven Fat Loss Mechanism
```
7,700 kcal deficit = 1 kg fat lost
Diet ≈ 70% of deficit | Exercise ≈ 30%
Safe rate: 0.5–1 kg/week (500–1,000 kcal/day deficit)
```

### Finding 4 — Monte Carlo Results (500 trials, 24 weeks, 70% adherence, 75kg)
| Strategy Stack | P(≥5% weight loss) |
|---------------|---------------------|
| No strategy | ~5% |
| Fiber only | ~28% |
| Fiber + protein shake | ~61% |
| Fiber + shake + walks | ~74% |
| **Full Lazy Stack (all 5)** | **~88%** |

> 💡 Key insight: Raising adherence 50% → 70% increases success probability **more** than adding an extra strategy.

### Finding 5 — Prescription GLP-1 Efficacy Ranking (OMA 2026)
| Drug | Avg. Weight Loss | Frequency | Monthly Cost (US) |
|------|-----------------|-----------|-------------------|
| Zepbound (tirzepatide) | ~20–22% | Weekly | ~$1,060–1,300 |
| Wegovy (semaglutide) | ~15.8% | Weekly | ~$1,300+ |
| Saxenda (liraglutide) | ~8% | **Daily** | ~$1,000 |
| Orlistat Rx | ~5% | 3× daily oral | ~$75 |

STEP-8 head-to-head trial: Wegovy 15.8% vs. Saxenda 6.4% at 68 weeks.

### Finding 6 — Saxenda Clinical Protocol (FDA Prescribing Data)
```
Titration: 0.6 → 1.2 → 1.8 → 2.4 → 3.0 mg (1 new dose/week, 5 weeks total)
Injection: Subcutaneous, once daily, rotate sites (abdomen / thigh / upper arm)
Checkpoint: If <4% weight loss at week 16 on full dose → discontinue per FDA guideline
```

### Finding 7 — Vitamin Protocol for GLP-1 Users
Based on meta-analysis of **480,825 GLP-1 users** — deficiencies documented in:

| Supplement | Priority | Form | Dose |
|------------|----------|------|------|
| Vitamin B12 | 🔴 Critical | Methylcobalamin | 500–1,000 mcg/day |
| Vitamin D3 + K2 | 🔴 Critical | Cholecalciferol + MK-7 | 1,000–2,000 IU/day |
| Magnesium | 🟡 Important | Glycinate | 200–400 mg/day |
| Protein | 🟡 Important | Whey/pea isolate | 1.2–2.0 g/kg/day |
| Calcium Citrate | 🟡 Important | Citrate (split doses) | 500–1,000 mg/day |
| Zinc | 🟢 Supportive | Gluconate | 8–11 mg/day |

> ⚠️ **Absorption warning:** Saxenda slows gastric emptying. Take all supplements **1–2 hours** before or after injection.

### Finding 8 — Weight Regain After Stopping GLP-1
- Most patients regain 60–100% of lost weight within 1–2 years of stopping
- Hunger hormones return to baseline within 2–4 weeks
- **Conclusion:** Obesity must be treated as a chronic condition — the strategy that loses the weight must become the permanent lifestyle.

---

## 🧮 Simulation Methodology

The weight loss simulator uses a **Monte Carlo approach**:

```
for each trial (n = 200 personal / 500 scenario):
    for each week:
        effective_deficit = daily_deficit × (1 if random() < adherence else 0.15)
        kg_loss = effective_deficit × 7 / 7700
        noise = gaussian(0, 0.2) × kg_loss
        weight -= (kg_loss + noise)

output: median trajectory + 10th/25th/75th/90th percentile bands
```

Parameters sourced from clinical literature:
- `7,700 kcal = 1 kg fat` (standard clinical model)
- Strategy deficit values from RCT averages (psyllium −200 kcal/day, protein shake −250 kcal/day, etc.)
- Adherence noise: ±20% weekly variance

---

## 📚 Sources

1. **NIH Office of Dietary Supplements** — Dietary Supplements for Weight Loss (May 2022)
2. **Obesity Medicine Association** — Top Weight Loss Medications (January 2026)
3. **GoodRx Health** — Prescription Weight Loss Pills Guide (2025), reviewed by Patricia Pinto-Garcia MD MPH
4. **Quora Community** — Healthcare professionals: Amy Chai MD, Susan Swan, Bart B. Van Bockstaele
5. **Mumsnet** — Weight Loss Injection Community Thread (2025) — real-world GLP-1 stop/regain accounts
6. **Mayo Clinic Connect** — Ozempic and Saxenda non-diabetic use discussions
7. **FAIR Health Study** (May 2025) via OMA — GLP-1 usage prevalence data
8. **FDA Prescribing Information** — Saxenda (liraglutide injection) official label

---

## ⚕️ Disclaimer

This project is for **educational and research purposes only**. It does not constitute medical advice. All prescription weight-loss medications require physician evaluation, blood work, and ongoing monitoring. Consult a licensed healthcare provider before beginning any weight-loss program.

---

## 📄 License

MIT © 2026 [Alexia Le](https://github.com/alexia-le)
