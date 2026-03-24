# Black-Box Optimisation Capstone Project

## NON-TECHNICAL EXPLANATION

This project explores how to solve problems where the underlying system is unknown, often referred to as a “black box”. Instead of knowing how the function works, different inputs are tested and the outputs are observed.

Over multiple iterations, I refined my inputs based on previous results to improve performance. This process demonstrates how optimisation can be achieved through experimentation, pattern recognition and gradual improvement, even without access to the internal workings of the system.

---

## PROBLEM

The objective was to maximise the output of several unknown functions by submitting input vectors over multiple weeks. Each query returned a score, and the goal was to iteratively improve these scores.

---

## APPROACH

My strategy evolved over time:

- Early stage: broad exploration of the input space  
- Middle stage: identifying promising regions  
- Final stage: refining inputs around strong-performing areas  

This reflects the exploration–exploitation trade-off commonly seen in optimisation and reinforcement learning.

---

## RESULTS

- Initial performance: highly variable  
- Final performance: more stable and consistently higher scores  
- Key insight: small, structured refinements produced better results than random inputs  

---

## INTERPRETATION

The results show that optimisation is not about random guessing, but about learning from previous outcomes and adapting strategy over time.

---

## FILES

- `notebook.ipynb` → full workflow and analysis  
- `data_sheet.md` → dataset description  
- `model_card.md` → optimisation strategy description  

---

## REAL-WORLD CONNECTION

This type of optimisation approach is similar to:
- hyperparameter tuning in machine learning  
- reinforcement learning decision-making  
- industrial optimisation problems  

---
