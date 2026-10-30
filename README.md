# The Feasibility Stress Test — Case Study #3: Base Case vs. Monte Carlo Mean, Segilola Gold Mine

A Monte Carlo simulation reconstruction demonstrating that a single-point "base case" NPV can be wrong in either direction, not just optimistically — built around a real published case study.

## The real case study

**Ugwuegbu, C. (2013).** *Segilola gold mine valuation using Monte Carlo simulation approach.* Mineral Economics, 26, 39–46.

A base-case discounted cash flow analysis on Nigeria's Segilola gold project returned a **negative** NPV of $7.46 million — on a strict single-point basis, a rejection. Sensitivity analysis identified four real value drivers (gold price, gold grade, strip ratio, operating costs). Running those through Monte Carlo simulation instead of one guess each told a different story.

### Confirmed findings (from the published abstract)

| Metric | Value |
|---|---|
| Base-case NPV | −$7.46 million |
| Monte Carlo mean NPV | +$30.79 million |
| Monte Carlo standard deviation | $58.26 million |
| Probability of a positive NPV | 69.2% |
| Value drivers (sensitivity analysis) | Gold price, gold grade, strip ratio, operating costs |
| Gap: base case to mean | ~$38 million |

**The lesson:** a base case is one combination of point estimates, not the most likely outcome and not automatically the conservative one. It can make a genuinely good project look like a reject just as easily as it can overstate a bad one.

## What's in this repo

- `notebook.ipynb` — an **illustrative reconstruction**: a representative gold project calibrated around the four confirmed value drivers, comparing a base-case NPV against a full Monte Carlo mean
- `data/confirmed_facts.csv` — every number above, structured
- `data/notebook_reconstruction_output.json` — this repo's own simulation output, for comparison against the published figures
- `docs/` — GitHub Pages site (landing page + rendered notebook)

## Important: what this notebook is and isn't

The full paper is not open-access. This project worked from the public abstract only. The notebook uses invented but plausible distributions for the four confirmed value drivers, tuned so its four headline outputs (base case, mean, std. dev., probability of profit) land close to the published figures — not to reproduce them exactly.

**Do not cite this notebook's specific dollar figures as the paper's numbers.**

## Running it

```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

## License

MIT — see `LICENSE`. Code and structure are freely reusable; the underlying research belongs to its original authors and should always be cited.

---
Built as part of [The Feasibility Stress Test](#) — real Monte Carlo and financial-engineering case studies for capex decisions, published as a LinkedIn newsletter by Eka Krisna Santoso.
