# Software Requirements Specification (SRS) for "ImmoCamer" Real Estate Platform

**Case Study:** Cameroon Market  
**Standard Compliance:** IEEE 830 / ISO-24765  
**Version:** 1.0  

---

## 1. Introduction
### 1.1 Purpose
This document specifies the requirements for "ImmoCamer," an enterprise-grade real estate platform designed to address the unique challenges of the Cameroonian property market, including land title verification, mobile money payments, and multi-vendor/agent dynamics.

### 1.2 Scope
ImmoCamer is a mobile-first platform facilitating property sales, rentals, and management across Cameroon's 10 regions (focusing on Douala, Yaoundé, and Kribi). It integrates multi-vendor workflows, land registry checks (simulated), and secure localized payment systems.

---

## 2. Market Realities (Cameroon Case Study)
- **Land Tenure Complexity:** High prevalence of land disputes. Requirement for "Titre Foncier" (Land Title) verification status.
- **Payment Infrastructure:** Dominance of MTN Mobile Money and Orange Money over credit cards.
- **Agent Ecosystem:** Informal "demarcheurs" (brokers) need a formalized, tiered verification system.
- **Connectivity:** Optimization for low-bandwidth 3G/4G networks and offline caching.
- **Trust Factor:** Need for "Certified Agency" badges and escrow-like payment holds.

---

## 3. User Stories
| ID | User Role | Requirement | Goal |
|---|---|---|---|
| US1 | Property Seeker | Find a studio in Bastos, Yaoundé. | Quick rental within budget. |
| US2 | Owner/Landlord | Post an apartment in Akwa, Douala. | Reach verified tenants. |
| US3 | Agent | Manage multiple listings for different owners. | Centralized dashboard for commissions. |
| US4 | Admin | Verify the authenticity of a Land Title scan. | Prevent fraudulent listings. |

---

## 4. Use Cases
### UC1: Property Purchase Workflow
1. **Browse:** User filters by City (Douala) and Neighborhood (Bonapriso).
2. **Visit Request:** User schedules a site visit via the app (standard practice in Cameroon).
3. **Verification:** Agent uploads a copy of the "Certificat de Propriété."
4. **Offer:** User makes a formal offer.
5. **Payment:** Deposit paid via Mobile Money into an Escrow account.

---

## 5. System Requirements
### 5.1 Multi-Vendor/Agent Workflows
- **Onboarding:** Agents must provide a National ID Card (CNI) and business registration (RCCM).
- **Tiered Commissions:** Automated calculation of "frais de visite" and final brokerage fees.

### 5.2 Security Requirements
- **2FA:** mandatory via SMS (localized to +237).
- **Data Residency:** Encryption of user CNI scans and property deeds.

---

## 6. Database Schema (ERD Summary)
- **Users Table:** ID, Name, Role (Seeker, Agent, Admin), CNI_Hash.
- **Properties Table:** ID, Location (Region, Town, Quarter), Price, Status (Sale/Rent), Title_Status.
- **Transactions Table:** ID, Amount, Payment_Provider (MTN/Orange), Status, Escrow_Held.
- **Visits Table:** ID, Property_ID, User_ID, Date, Fee_Paid.

---

## 7. API Requirements
- **Endpoint:** `GET /v1/properties/search` (Filters: region, budget, type).
- **Endpoint:** `POST /v1/payments/momo` (Initiates Mobile Money push request).
- **Endpoint:** `POST /v1/verify/land-title` (Integration with Ministry of State Property/Land portal).

---

## 8. Admin & Analytics
- **Dashboard:** Heatmap of high-demand areas (e.g., Kribi seaside vs. Yaoundé residential).
- **Fraud Monitoring:** Flagging duplicate listings by different agents.

---

## 9. Acceptance Test Cases
| TC_ID | Scenario | Expected Result |
|---|---|---|
| TC1 | Pay visit fee via Orange Money. | Transaction success and visit confirmed in 'My Visits'. |
| TC2 | Upload 5MB property photo on 3G. | Image is compressed client-side before upload. |
| TC3 | Seeker filters by 'Titre Foncier Available'. | Only verified properties are displayed. |
