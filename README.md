# AI-Assisted Mental Health Support Platform 🧠🛡️

## 🔒 Project Status: Private Commercial Repository
This repository serves as a **technical demonstration and documentation hub** for my Final Year Project. 

The full source code is currently maintained in a private repository as it is being prepared for commercial licensing and further development. This public README outlines the system architecture, engineering decisions, and security protocols implemented.

---

## 📌 Project Overview
This platform is a cross-platform solution designed to bridge the gap between AI-driven emotional support and professional human intervention. It provides users with immediate, empathetic AI interaction while ensuring a secure, consent-based escalation path to licensed therapists when high-risk situations are detected.

### 🎯 Key Objectives
* **Empathetic AI Interaction:** Utilizing instruction-tuned LLMs for supportive dialogue.
* **Risk Detection:** Real-time monitoring of user input for crisis indicators.
* **Secure Escalation:** Seamless, consent-mandatory handoff from AI to Human professionals.
* **Privacy-First Design:** Strict adherence to data isolation and role-based access.

---

## 🏗️ System Architecture & Engineering
The platform is built on a distributed **Client-Server-Inference** architecture to ensure high availability and data integrity.

### 1. Flutter Mobile Client
* Cross-platform UI for users and therapists.
* Secure state management and real-time UI updates via Firebase streams.

### 2. Secure Node.js Backend (The Control Layer)
* **Centralized Gateway:** All database operations are proxied through a Node.js API to prevent direct client-side DB access.
* **Token Verification:** Implements JWT-based authentication via Firebase Admin SDK.
* **Safety Logic:** Orchestrates the logic that disables AI and enables human chat during sensitive escalations.

### 3. AI Inference Layer
* **Model:** FLAN-T5 (via Hugging Face Space).
* **Fine Tuning:** Custom instruction-tuning on therapy data to prevent clinical diagnosis and maintain supportive, non-medical boundaries.

### 4. Hybrid Data Strategy
* **NoSQL (Firestore):** Optimized for real-time messaging and user profile metadata.
* **Object Storage (Supabase):** Dedicated storage for high-resolution media and voice notes to reduce database payload.

---

## 🛡️ Security & Privacy Engineering
Since this app handles sensitive mental health data, I implemented a **Defense-in-Depth** strategy:

* **Role-Based Access Control (RBAC):** Distinct permissions for Users, Therapists, and Admins enforced at both the API and Database levels.
* **Consent Protocol:** A cryptographic-like handoff where a therapist cannot view user logs until the user explicitly triggers a "Consent Grant" in the UI.
* **Data Isolation:** Personal Identifiable Information (PII) is logically separated from chat logs to ensure privacy.

---

## 🛠️ Technology Stack
| Layer | Technology |
| :--- | :--- |
| **Frontend** | Flutter |
| **Backend** | Node.js / Express |
| **Authentication** | Firebase Auth |
| **Primary Database** | Google Firestore |
| **Media Storage** | Supabase Storage |
| **AI Inference** | Hugging Face Space / FLAN-T5 |
| **Deployment** | Render (Backend), Firebase (Hosting) |

---

## 📺 Demonstration
> [!TIP]
> **[Link to YouTube/Loom Demo Video]** > *Watch a 3-minute walkthrough of the app's core features, including the AI-to-Therapist handoff workflow.*

---

## 👨‍🎓 Author & Evaluation
**Muhammad Usman** *BS Computer Science – Final Year Project*

**For Recruiters:** I am available to perform a live code walkthrough of the private repository to demonstrate my coding standards, API design, and security implementations.

---
*Disclaimer: This project is for academic and research purposes. It is not a substitute for professional medical advice, diagnosis, or treatment.*
