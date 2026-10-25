# User Stories

Format: As a [type of user], I want [goal], so that [reason or benefit].

### User Story 1
**As a** primary care clinician at a low-prevalence screening clinic,  
**I want** an AI screening assistant with high active-TB sensitivity,  
**so that** early active TB cases are not missed due to regional sample imbalance.  
* **Linked Requirements:** `FR2`, `NFR2`  
* **Acceptance Criteria:**  
  1. Given local training data with only 8.3% TB prevalence, when local updates are trained using Client-Side Localized Weighted Loss, then the evaluated model achieves $\ge 85.0\%$ active TB sensitivity on test data.  
  2. The system flags suspected active TB X-rays with a clear probability score without generating excessive false negatives.

### User Story 2
**As a** Hospital Data Protection Officer (DPO),  
**I want** a privacy-preserving federated architecture that shares only abstract model parameters,  
**so that** patient diagnostic data strictly complies with PDPA 2010 privacy regulations.  
* **Linked Requirements:** `FR3`, `NFR1`  
* **Acceptance Criteria:**  
  1. During network transmission, 0 raw images or DICOM patient metadata files leave the simulated local client firewall.  
  2. Only encrypted or sanitized model weight tensors ($\theta_k$) are transmitted between client nodes and the central aggregation server.

### User Story 3
**As a** healthcare AI developer,  
**I want** a lightweight client-side loss function adjustment,  
**so that** I can eliminate Non-IID gradient cancellation without incurring heavy server-side computational overhead or extra communication rounds.  
* **Linked Requirements:** `FR2`, `NFR3`  
* **Acceptance Criteria:**  
  1. The client loss adjustment integrates directly into standard local training loops (e.g., PyTorch) without modifying standard FedAvg server aggregation logic.  
  2. Total federated execution time across 20 communication rounds stays under 60 minutes on standard GPU infrastructure.
