# 🚀 Black-Box Optimisation (BBO) Capstone Project

## 1. Project Overview
This repository documents my participation in the Black-Box Optimisation (BBO) capstone challenge.  
The project requires designing query strategies to optimise eight unknown functions where evaluations are costly and the underlying structure is hidden.  

The overall goal is to **maximise performance while minimising the number of queries**, balancing exploration of new regions with exploitation of promising areas (Shahriari et al., 2016).  
This challenge mirrors real-world ML tasks such as hyperparameter tuning and credit risk modelling, where optimisation must be performed under uncertainty (Jones, Schonlau and Welch, 1998).  

For my career in economic analysis and forecasting, this project strengthens my ability to design efficient search strategies, document decisions transparently, and apply optimisation methods to infrastructure planning.

---

## 2. 📊 Inputs and Outputs
**Inputs:**  
- Queries are submitted as vectors of values, each specified to six decimal places.  
- Dimensionality varies by function (2D–8D).  
- Example format:  
  - Function 1 (2D): `0.500000 0.500000`  
  - Function 3 (3D): `0.050000 0.500000 0.950000`

**Outputs:**  
- Each query returns a single numerical response value.  
- Outputs can be positive or negative, with magnitudes varying widely (Rasmussen and Williams, 2006).  

| Function | Example Input                          | Example Output |
|----------|----------------------------------------|----------------|
| 1 (2D)   | `0.500000 0.500000`                    | 2.675e-9       |
| 5 (4D)   | `0.450000 0.150000 0.850000 0.650000`  | 54.557         |

---

## 3. ⚖️ Challenge Objectives
- **Objective:** Maximise function values across all eight unknown functions.  
- **Constraints:**  
  - Limited number of queries per round.  
  - Response delay (outputs revealed only after submission).  
  - Unknown function structure, potentially noisy and high-dimensional.  

Success is measured by identifying high-performing regions quickly, avoiding wasted queries, and documenting a clear rationale for each decision.

---

## 4. 🧠 Technical Approach
My strategy has evolved across the first three rounds:

### Round 1 – Exploration
- Broad sampling across the domain.  
- Evenly spaced queries to reduce uncertainty.  

### Round 2 – Early Exploitation
- Focused on promising regions (Functions 5 and 8).  
- Small perturbations around high-performing points.  
- Continued exploration in weak regions.  

### Round 3 – Balanced Strategy
- Controlled perturbations (±0.05–0.10).  
- Adjusted sequences in higher-dimensional functions for interpretability.  
- Began considering surrogate modelling approaches.  

**Methods and Heuristics:**  
- **Bayesian Optimisation (BO):** Gaussian Processes and Tree-structured Parzen Estimators to approximate performance surfaces (Shahriari et al., 2016; Bergstra et al., 2011).  
- **Support Vector Machines (SVMs):** Soft-margin and kernel SVMs to classify high vs. low performance regions, reducing wasted queries (Cortes and Vapnik, 1995; Cristianini and Shawe-Taylor, 2000).  
- **Exploration vs. Exploitation:** Alternating between sampling near known high-performing regions and probing untested areas (Jones, Schonlau and Welch, 1998).  
- **Cross-validation mindset:** Ensuring strategies generalise by testing across multiple dimensions and avoiding overfitting (Guyon and Elisseeff, 2003).  

**Uniqueness of Approach:**  
My approach integrates classification (SVMs) with optimisation (BO). This hybrid strategy reduces the number of queries needed, enhances transparency, and mirrors governance practices in real-world modelling.

---

## 5. 🔜 Next Steps
- Refine surrogate models with growing data.  
- Experiment with kernel SVMs for non-linear boundaries.  
- Document trade-offs between efficiency and interpretability.  
- Prepare visualisations of optimisation traces and performance comparisons.

---

## 📚 References
- Bergstra, J., Bardenet, R., Bengio, Y. and Kégl, B., 2011. Algorithms for hyper-parameter optimization. *Advances in Neural Information Processing Systems*, 24, pp.2546–2554.  
- Cortes, C. and Vapnik, V., 1995. Support-vector networks. *Machine Learning*, 20(3), pp.273–297.  
- Cristianini, N. and Shawe-Taylor, J., 2000. *An Introduction to Support Vector Machines and Other Kernel-based Learning Methods*. Cambridge: Cambridge University Press.  
- Guyon, I. and Elisseeff, A., 2003. An introduction to variable and feature selection. *Journal of Machine Learning Research*, 3, pp.1157–1182.  
- Jones, D.R., Schonlau, M. and Welch, W.J., 1998. Efficient global optimization of expensive black-box functions. *Journal of Global Optimization*, 13(4), pp.455–492.  
- Rasmussen, C.E. and Williams, C.K.I., 2006. *Gaussian Processes for Machine Learning*. Cambridge, MA: MIT Press.  
- Shahriari, B., Swersky, K., Wang, Z., Adams, R.P. and de Freitas, N., 2016. Taking the human out of the loop: A review of Bayesian optimization. *Proceedings of the IEEE*, 104(1), pp.148–175.  
