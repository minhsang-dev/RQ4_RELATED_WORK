# RQ4 gap check

**Coverage:** 33 works, pages opened this session; web search only, so absence is not proof. Malware-detector poisoning was not searched.

**Source tier + row tier for context/ICL models?** Not found. Row-level only: Jhuma 2025 (spectral signature on LLM demonstrations), ICLShield (abstract only), PriorPoison (oof, dedup; one dataset, unreviewed). Source-level only: WeiDetect, FLTrust (FL updates), Ma–Olshevsky, Fang et al. (crowdsourcing). No tabular in-context model appears with either.

**Bound like Proposition 2?** Not found. Nearest: kNN certification (Jia et al.: prediction stable if poisoned rows ≤ ⌈(s_a−s_b+I)/2⌉−1), Levine–Feizi and Rosenfeld certificates (abstract only). None uses a per-source cap or an audit detection probability. Ma–Olshevsky bounds tolerated adversary fraction ~1/[(2+ε)log log n], a different quantity.

**Adaptive attackers who know the defence?** Yes, but never against this pairing: Koh et al. (kNN, loss, SVD sanitizers broken at 3% poison), Miao et al. (disguise against Dawid–Skene audit), FLTrust and Fang et al. (adaptive/full-knowledge). TabFM poisoning papers (Bilos, PriorPoison) evaluate no adaptive attacker.

**Threats to H4a/H4b raised by the literature**
1. Defence-aware poison evades row filters; Koh et al. use influence functions on the attacker side, so a defender-aware attacker can optimise against I_i.
2. Peer audits can be disguised (Miao) or beaten by coordination through a shared cheap signal (Zhang et al., abstract-level).
3. RONI fails on focused attacks (Nelson); targeted family flips are focused, so V_t must contain the target families.
4. Real and adversarial drift look alike to detectors (Korycki); a stale V_t may misprice influence under drift (my inference).
5. Honest-but-different sources look like outliers (WeiDetect motivation); kNN cleaning relabels genuine points (Paudice).
6. Source peer methods need overlap (Ma–Olshevsky); K sources labelling different subnets may share no items.
7. Confident learning assumes class-conditional noise; feature-targeted flips violate it.
8. Copy injection reached ASR 1.00 on TabPFN with oof filtering failing (PriorPoison, single dataset): duplicates across colluding sources bypass a per-source cap.
9. Trusted references (V_t, AD, root set) are assumed clean everywhere; none addresses a compromised reference.
10. Measured TabFM damage from hub poisoning is small (−3.7/−3.3 pp, Bilos), so H4a's 50% reduction needs a strong attack to be meaningful.

**GAP_NARROW** — the combination of a same-day peer source audit plus a row-influence filter plus a per-source cap, for tabular in-context models under targeted label flips with honest-but-different sources, and a bound tying cap and audit power to poison share, was not found; each component exists separately.
