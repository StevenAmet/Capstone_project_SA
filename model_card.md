# Model Card – Black-Box Optimisation Strategy

## Model Description

**Input:**  
Numerical parameter vectors submitted to the black-box function.

**Output:**  
A scalar performance score representing the quality of the input.

**Model Architecture:**  
This project does not use a traditional machine learning model. Instead, the “model” is an iterative optimisation strategy.

The approach involves:
- Exploring the input space in early iterations  
- Identifying promising regions  
- Refining inputs based on previous results  

This process is similar to heuristic optimisation and adaptive search strategies.

---

## Performance

Performance is measured based on improvement in output scores over time.

Observed behaviour:
- Early iterations: high variability  
- Middle iterations: emerging patterns  
- Final iterations: stabilisation and incremental improvement  

This reflects typical convergence behaviour in optimisation problems.

---

## Limitations

- The underlying function is unknown, limiting interpretability  
- Small number of observations  
- Results may be sensitive to initial exploration choices  
- Risk of converging to local optima  

---

## Trade-offs

- Exploration vs exploitation:  
  Early exploration provides information but yields lower scores  
  Later exploitation improves results but risks missing better regions  

- Precision vs coverage:  
  Fine-tuning improves performance but reduces search diversity  

The strategy balances these trade-offs over time.