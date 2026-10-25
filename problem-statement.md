# Problem Statement

## Who is affected?
Radiologists, doctors in rural clinics, hospital IT administrators, and Data Protection Officers attempting to deploy joint AI diagnostic systems.

## What exactly is going wrong?
Under Malaysia's Personal Data Protection Act (PDPA 2010), healthcare facilities cannot transfer raw patient Chest X-rays to central cloud servers. While Federated Learning (FedAvg) keeps patient data local. Real-world clinics handle diverse populations, creating severe Non-IID label distribution skew (8.3% to 25.0% active TB prevalence). This imbalance forces client models to generate conflicting gradient updates that cancel each other out when averaged at the central server.

## Why does it matter?
Destructive gradient cancellation causes global model sensitivity collapse. The resulting global AI model defaults to predicting Normal majority cases and misses active Tuberculosis (high False Negative Rate), risking delayed treatment and continued community transmission of contagious TB.

## Problem statement 
Healthcare facilities cannot pool patient Chest X-rays on central cloud servers due to strict privacy rules under Malaysia's Personal Data Protection Act (PDPA 2010). Although Federated Learning keeps data safely inside local clinic firewalls, facilities naturally handle highly skewed disease distributions (8.3% to 25.0% TB prevalence). This imbalance forces client models to send conflicting mathematical updates that cancel each other out when averaged at the central server. Consequently, the global model experiences sensitivity collapse, defaulting to Normal predictions and failing to diagnose dangerous active TB cases during routine screenings.
