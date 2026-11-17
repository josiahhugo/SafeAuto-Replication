# SafeAuto-Replication
Final Project for Intro to AI Class (CSCE 4201): Reproducing results from top-tier AI conferences 
Using the same datasets, hyperparameters, and experimental setup, evaluate how reproducible the reported results are and document any inconsistencies or obstacles that were encountered. Optionally, extend or modify the original approach. 

OG Repo: https://github.com/AI-secure/SafeAuto

# Motivation
Selected this paper as it aligns with my academic interests and long term career goals in AI, cybersecurity, and the security cyber-physical systems.

# Roadmap
| Experiment | Goal                               | 
| ---------- | ---------------------------------- | 
| PDCE       | Evaluate numerical prediction loss | 
| PGM/MLN    | Evaluate traffic-rule verification | 
| BDD-X      | Test available evaluation data     |

With this we can measure:
- Traffic-rule violations before and after verfication
- Accuracy of corrected driving actions
- False corrections of originally valid actions
- Processing overhead introduced by verification

# OG Repo Notes
- PDCE loss (llava/model/language_model/llava_llama.py)-- improves numerical prediction 
- Safety verification (pgm/) -- evaluate actions against traffic rules
- Multimodal RAG (retrieval/) -- retrieves relevant driving experiences
- Model evaluation (evaluate.bddx.py) -- evaluates predicitons on BDD-x

# First Experiment: Reproducing PDCE
Can test its mathematical implementation independently of the full multimodal model --> investigating whether it improves numerical prediction accuracy.  

Research Question: Does Position-Dependent Cross-Entropy provide a more informative training signal for numerical predictions than standard cross-entropy?


