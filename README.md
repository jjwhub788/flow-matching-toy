# Flow Matching on 2D Toy Distributions (MoG)

## Project question (1-liner)
Can conditional flow matching with a simple straight-line schedule learn mode-preserving transport in 2D mixtures (bimodal↔bimodal) without collapsing modes?

## Scope (Step 0)
- Domain: 2D toy data (Mixture of Gaussians)
- Time: t ∈ [0, 1]
- Baseline schedule: straight-line conditional vector field
- Datasets:
  1) Unimodal → Unimodal (baseline)
  2) Bimodal → Unimodal (mode-collapse observation)
  3) Bimodal → Bimodal (mode-matching observation)

## Repo structure
- `configs/` experiment configs (yaml)
- `src/` training code
- `notebooks/` plotting & figure generation
- `results/figures/` key figures (6–10)
- `docs/summary.pdf` 2–4 page interview summary
- `docs/slides.pdf` 5-slide mini deck

## Metrics (fixed to 3)
1) Sample quality: sliced-W2 (approx Wasserstein)
2) Mode coverage: recovered modes / assignment accuracy
3) Training stability: loss curve + diagnostics

## Progress
- [x] Step 0: scope fixed + repo scaffold + 3 configs
- [ ] Step 1: implement MoG sampler + FM baseline training
- [ ] Step 2: run 3 settings + generate 6–10 key figures
- [ ] Step 3: write 2–4 page summary PDF + (optional) 5-slide deck