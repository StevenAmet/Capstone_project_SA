# Model Card  
**Iterative Heuristic Black Box Optimisation Strategy**  
Version 1.0  

---

## 1. Overview

**Name:** Iterative Heuristic Exploit–Explore Strategy  
**Type:** Sequential Black Box Optimisation  
**Version:** 1.0  

This optimisation strategy was developed for the Black Box Optimisation (BBO) Capstone Project.  

It selects query points sequentially across eight unknown objective functions and adapts over multiple rounds based on observed performance trends.

---

## 2. Intended Use

### Suitable for:

- Low-budget optimisation problems  
- Educational black box optimisation tasks  
- Sequential evaluation environments  

### Not suitable for:

- High-noise industrial optimisation  
- Safety-critical real-world deployment  
- Extremely high-dimensional optimisation requiring formal uncertainty modelling  

---

## 3. Strategy Details

The approach evolved across ten rounds:

### Rounds 1–3: Exploration Phase
- Broad coverage of the input space  
- Structured sampling to reduce uncertainty  

### Rounds 4–6: Mixed Strategy
- Balanced exploration and exploitation  
- Local refinement around promising regions  

### Rounds 7–10: Exploitation Phase
- Strong exploitation of monotonic improvement regions  
- Conservative perturbations for plateaued functions  
- Micro-adjustments for converged functions  

The strategy was inspired by exploration–exploitation principles in Bayesian optimisation literature.

---

## 4. Performance Summary

Performance was evaluated using:

- Maximum observed values for maximisation functions  
- Minimum observed values for minimisation functions  
- Convergence stability across iterations  

### Observed Outcomes:

- Strong convergence: Functions 1 and 5  
- Steady improvement: Functions 4 and 8  
- Instability or plateau: Functions 2 and 7  
- Gradual trend detection: Functions 3 and 6  

---

## 5. Assumptions and Limitations

### Key Assumptions

- Local smoothness of objective functions  
- Short-term trends indicate directional improvement  
- Limited noise in function evaluations  

### Limitations

- No explicit uncertainty quantification  
- Risk of convergence to local optima  
- Sparse sampling in high-dimensional spaces  
- Heuristic decision-making rather than formal acquisition functions  

---

## 6. Ethical and Transparency Considerations

Although this project involves synthetic objective functions, the documentation structure mirrors responsible AI reporting practices.

Transparency supports:

- Reproducibility  
- Clear communication of assumptions  
- Structured evaluation of strengths and weaknesses  

Clear documentation strengthens credibility and supports peer review.

---

## References

Mitchell, M. et al. (2019) *Model cards for model reporting*. Proceedings of the Conference on Fairness, Accountability, and Transparency, pp. 220–229.

Shahriari, B. et al. (2016) *Taking the human out of the loop: A review of Bayesian optimization*. Proceedings of the IEEE, 104(1), pp. 148–175.
