# Requirements

## Functional requirements (what the system must DO)
1. The system shall split the training dataset across 3 simulated clinic nodes to mirror real-world class imbalance (8.3%, 16.7%, and 25.0% TB prevalence).
2. The system shall adjust the local loss function directly on the client side before sending model updates to the server.
3. The system shall aggregate local model weights at the central server using standard FedAvg without transferring any raw X-ray files.
4. The system shall evaluate the trained global model on a separate, unseen test set of 600 Chest X-rays.
5. The system shall calculate and display key diagnostic metrics: Active TB Sensitivity (Recall), False Negative Rate (FNR), Specificity, and AUROC.

## Non-functional requirements (how the system must PERFORM)
1. The system shall maintain 100% compliance with PDPA 2010 by ensuring no raw patient images or personal identifiers ever leave local clinic nodes.
2. The system shall achieve at least 85% Active TB Sensitivity on the global test set despite severe class imbalance across local nodes.
3. The system shall complete a full federated training and evaluation run within 60 minutes on a standard GPU workstation.