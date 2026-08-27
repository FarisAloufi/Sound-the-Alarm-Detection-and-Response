# PASTA Threat Model — Sneaker Marketplace App

## 📌 Project Overview
This project applies the **PASTA (Process for Attack Simulation and Threat Analysis)** framework to threat model a new mobile app that lets users buy and sell sneakers. The goal was to evaluate whether the app was ready to launch securely by working through all seven stages of PASTA — from business objectives to concrete security controls.

## 🎯 Objectives
- Define the business and security objectives driving the app's development.
- Identify and prioritize the app's key technologies from a security standpoint.
- Decompose how the app processes and moves data.
- Identify realistic threats and vulnerabilities, and model how they could be exploited.
- Recommend security controls to reduce the app's risk before launch.

## 🛠️ Skills & Concepts Demonstrated
- PASTA threat modeling framework (all 7 stages)
- Data flow diagram analysis
- Attack tree analysis
- Application security concepts: PKI (AES/RSA), SHA-256 hashing, SQL injection, session hijacking
- Translating technical risk into launch-readiness recommendations

## 🧭 PASTA Stages Covered
| Stage | Focus |
|---|---|
| I. Business & Security Objectives | Secure transactions, data privacy, payment/legal compliance |
| II. Technical Scope | Prioritized PKI due to sensitive payment/personal data |
| III. Decompose Application | Traced the product search data flow (user → process → database) |
| IV. Threat Analysis | External (SQL injection) and internal (social engineering) threats |
| V. Vulnerability Analysis | Missing prepared statements; weak login credential requirements |
| VI. Attack Modeling | Attack tree showing paths to user data via SQL injection and session hijacking |
| VII. Risk Analysis & Impact | 4 security controls: prepared statements, MFA, strong password policy, AES/RSA + SHA-256 |

## ✅ Key Recommendation
Both major attack paths identified — SQL injection and session hijacking — trace back to two fixable root causes: unprepared SQL statements and weak login requirements. Addressing these with prepared statements and MFA closes off the most realistic routes to compromising user data before launch.

## 📂 Files in This Repository
- `PASTA-Threat-Model.pdf` — Full threat model covering all 7 PASTA stages, including the data flow diagram and attack tree used in the analysis.

## 📎 Note
This is a training/portfolio project based on a fictional company scenario, intended to demonstrate threat modeling skills using the PASTA framework.
