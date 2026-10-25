# Requirements

## Functional requirements 
- **FR1:** The system shall partition the training dataset across 3 simulated client nodes to emulate Non-IID label distribution skew (Clinic A: 8.3%, Clinic B: 16.7%, Clinic C: 25.0% active TB prevalence).
- **FR2:** The system shall apply Client-Side Localized Weighted Cross-Entropy Loss during local client training loops prior to model parameter transmission.
- **FR3:** The system shall aggregate local client parameter weight updates at the central server using standard Federated Averaging (FedAvg) without transferring raw images.
- **FR4:** The system shall perform binary classification (Normal vs. Active TB) on an unseen central evaluation dataset of 600 Chest X-ray images.
- **FR5:** The system shall calculate and display key diagnostic metrics: Active TB Sensitivity (Recall), False Negative Rate (FNR), Specificity, and AUROC after each federation round.

## Non-functional requirements
- **NFR1 (Privacy/Security):** The system shall maintain 100% compliance with statutory regulations under PDPA 2010 by ensuring zero raw patient Chest X-rays or personal identifiers leave local client nodes.
- **NFR2 (Performance/Accuracy):** The system shall achieve an Active TB Sensitivity (Recall) score of at least 85.0% on the central test set under severe Non-IID label skew.
- **NFR3 (Efficiency):** The system shall complete a full 20-round federated training and evaluation cycle in under 60 minutes on a single GPU workstation environment.
