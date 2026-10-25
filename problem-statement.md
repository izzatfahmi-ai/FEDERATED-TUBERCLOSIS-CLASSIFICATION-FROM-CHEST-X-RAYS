# Problem Statement

## Who is affected?
Radiologists and doctors in rural clinics, hospital IT administrators, and Data Protection Officers (DPOs) trying to build collaborative AI tools safely.

## What exactly is going wrong?
Under Malaysia's Personal Data Protection Act (PDPA 2010), healthcare facilities cannot dump raw patient X-rays onto a shared cloud server. Federated learning solves this privacy issue by keeping images local, but real-world clinics see vastly different patient populations (ranging from 8.3% to 25.0% TB prevalence). This uneven data split forces each clinic's AI to learn conflicting diagnostic rules. When the central server averages these conflicting updates together, the mathematical signals cancel each other out.

## Why does it matter?
When client updates cancel out at the server, the global AI model suffers from sensitivity collapse—it starts playing it safe by predicting "Normal" for almost every patient. As a result, contagious active TB cases get missed in early screening clinics, leading to delayed treatment and community transmission.

## Problem statement (3 to 5 sentences)
Healthcare facilities cannot pool patient Chest X-rays on central cloud servers due to strict privacy rules under Malaysia's Personal Data Protection Act (PDPA 2010). Although Federated Learning keeps data safely inside clinic firewalls, facilities naturally handle very different disease rates (8.3% to 25.0% TB prevalence). This imbalance causes local client models to send conflicting mathematical updates that cancel each other out when averaged at the central server. Consequently, the final global model suffers from sensitivity collapse, defaulting to "Normal" predictions and missing dangerous active TB cases during routine screenings.