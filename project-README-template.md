# FEDERATED-TUBERCULOSIS-CLASSIFICATION-FROM-CHEST-X-RAYS

This project provides a PDPA 2010-compliant federated learning framework for healthcare providers that prevents active Tuberculosis sensitivity collapse caused by client-side Non-IID label skew across decentralized clinic nodes.

## Problem statement
Healthcare facilities cannot centralize Chest X-rays on cloud servers for AI training due to strict data privacy regulations under Malaysia's Personal Data Protection Act (PDPA 2010). Although Federated Learning (FedAvg) preserves privacy by keeping patient data local, real-world variations in clinic demographics create severe Non-IID label distribution skew (8.3% to 25.0% TB prevalence). This imbalance forces client models to generate opposing local gradient signals during training, which suffer from destructive gradient cancellation when averaged at the central server. Consequently, the global model experiences sensitivity collapse defaulting to "Normal" predictions and failing to diagnose contagious active TB cases in early screening environments.

## Documents
- [Problem statement](problem-statement.md)
- [Requirements](requirements.md)
- [User stories](user-stories.md)

## Status
Planning (CSC649, Week 2)

## Author
izzat fahmi 

