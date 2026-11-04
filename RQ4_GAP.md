# RQ4 gap check (v2)

**Coverage:** 38 works, pages opened this session; web search only, so absence is not proof. Outline refs [34] Vejling and [35] Xu are not yet covered (not identified).

**Source tier + row tier for context/ICL models?** Not found. Row-level only: Jhuma 2025 (spectral signature on LLM demonstrations), Dolejš 2026 (pre-ingestion LightGBM consensus), PriorPoison (oof, dedup; unreviewed). ICLShield dilutes with clean rows rather than filtering. Source-level only: WeiDetect, FLTrust, Ma–Olshevsky, Fang et al. No tabular in-context model appears with any.

**Bound like Proposition 2?** Not found. Nearest: kNN certification (Jia et al.: stable if poisoned rows ≤ ⌈(s_a−s_b+I)/2⌉−1); DPA and Rosenfeld certificates (abstract only); ICLShield's concept-ratio bound (LLM backdoors). None uses a per-source cap or audit detection probability.

**Adaptive attackers who know the defence?** Koh et al. (kNN, loss, SVD sanitizers broken at 3%), Miao et al. (disguise against Dawid–Skene), FLTrust and Fang et al. Never against a source+row pairing; TabFM papers evaluate none.

**Threats to H4a/H4b**
1. Defence-aware poison evades row filters; Koh et al. build attacks with influence functions, which is the defender's I_i.
2. Peer audits can be disguised (Miao) or beaten by cheap-signal coordination (Zhang et al., abstract-level).
3. RONI misses focused attacks (Nelson); V_t must contain target families.
4. Real and adversarial drift look alike (Korycki); stale V_t may misprice influence (my inference).
5. Honest-but-different sources look like outliers (WeiDetect); kNN cleaning relabels genuine points (Paudice).
6. Peer methods need item overlap (Ma–Olshevsky).
7. Confident learning assumes class-conditional noise.
8. Copy injection reached ASR 1.00 on TabPFN while oof failed (PriorPoison, one dataset): colluding duplicates may bypass a per-source cap.
9. Trusted references (V_t, oracle partition, root set) are assumed clean everywhere.
10. Real label sources can be manipulated upstream: AndroVenom flips VirusTotal-derived labels via the AV engines; Deep k-NN then helped some models, hurt GBT (~−20% TPR) and left the targeted attack standing, with drift suspected.
11. Hub-poison damage to TabFMs is small (−3.7/−3.3 pp), so H4a's 50% reduction needs a strong attack.

**GAP_NARROW** — a same-day peer source audit plus row-influence filter plus per-source cap for tabular in-context models under targeted flips with honest-but-different sources, and a bound linking cap and audit power to poison share, was not found; components exist separately.
