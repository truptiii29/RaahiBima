# RaahiBima
### AI-Powered Parametric Income Protection for India’s Q-Commerce Gig Workers

<p align="center">
  <img src="https://img.shields.io/badge/Hackathon-Guidewire_DEVTrails_2026-blue?style=for-the-badge" alt="Hackathon">
  <img src="https://img.shields.io/badge/Sector-InsurTech-green?style=for-the-badge" alt="Sector">
  <img src="https://img.shields.io/badge/Status-Phase_1_Complete-orange?style=for-the-badge" alt="Status">
</p>

**RahiBima** is a specialized parametric insurance platform built for the backbone of India's 10-minute delivery ecosystem (**Zepto, Blinkit, Swiggy Instamart**). We protect riders from the one thing traditional insurance ignores: **lost opportunity cost due to external disruptions.**

---

## 📌 The Problem
For a delivery partner, a sudden monsoon downpour or a 43°C heatwave isn't just an inconvenience—it’s a financial wipeout. 
* **The Gap:** Traditional insurance covers accidents or vehicles. No one covers the **₹400–₹600 loss** incurred when a rider is forced off the road for 4 hours.
* **The Friction:** Manual claims take weeks. For someone living on weekly pay cycles, "weeks" is too long.

## 💡 The RaahiBima Solution
RahiBima eliminates the "Claims Department." Payouts are triggered by **objective third-party data**, not manual reports.

* **Target Persona:** Q-Commerce riders in Indian metros earning ₹800–₹1,200/day.
* **Coverage:** Pure Income Loss (No health/life/accident coverage).
* **Payout Speed:** Instant UPI disbursement within seconds of event confirmation.
* **Premium Model:** Dynamic weekly micro-payments (₹19 – ₹79) adjusted by AI-driven zone risk scores.

---

## ⛈️ Parametric Triggers (Multi-Oracle Consensus)
We utilize a **2-of-3 Consensus Model**. No single data source can trigger a payout, ensuring high-fidelity disruption events.

| Trigger Type | Threshold | Data Sources |
| :--- | :--- | :--- |
| **Sustained Rain** | ≥15mm/hr for ≥45 mins | Open-Meteo + IMD |
| **Heat Index** | "Feels like" ≥42°C (11AM–4PM) | Open-Meteo Apparent Temp |
| **Severe AQI** | PM2.5 AQI ≥300 for ≥3hrs | OpenAQ API |
| **Flood Zone Lock** | IMD Watch + Dark Store Inactivity | IMD RSS + Platform Signal |
| **Civic Disorder** | Section 144 / Curfew orders | NDMA RSS + NLP Classifier |

---

## 🛡️ 5-Layer Fraud Defense Architecture
To maintain a sustainable **70% Loss Ratio**, RahiBima employs a rigorous defense stack:

1. **Parametric Lock:** Disruption must be confirmed by external APIs. You can't spoof a rainstorm.
2. **Sensor Fingerprinting:** Cross-verifying GPS variance (detecting <0.5m spoofed jitters) with Accelerometer/Gyroscope data.
3. **GigTrust Score:** A pre-computed legitimacy engine (0.00–1.00) gating every payout based on account age and delivery history.
4. **Zone Saturation Circuit Breaker:** If claims > 2.5x expected rate, payouts are frozen for manual spot-checks.
5. **Social Graph Detection:** Identifying Sybil attacks by clustering shared hardware IDs and UPI handles.

---

## ⚙️ Technical Stack
* **Backend:** `FastAPI` (Python) — Async event processing.
* **Mobile:** `React Native` (Expo) — Native iOS/Android experience.
* **Database:** `PostgreSQL` (Supabase) — Real-time disruption triggers.
* **ML Engine:** `LightGBM` (Risk Scoring) & `Scikit-learn` (Fraud Detection).

---

## 📈 GigTrust Scoring Model
Payouts are gated by a per-rider score:
* **0.75 – 1.00 (Trusted):** Instant Auto-approve.
* **0.50 – 0.74 (Review):** Soft hold (4-hour window).
* **Below 0.50:** Manual review or rejection.

---

## 📅 Hackathon Roadmap
- [x] **Phase 1:** Concept Design & Parametric Architecture
- [ ] **Phase 2:** Registration Flow & Dynamic Premium Calculation
- [ ] **Phase 3:** GigTrust Engine & Instant UPI Payout Integration
- [ ] **Final:** Intelligent Dashboard & Pitch Video

---

**Developed for Guidewire DEVTrails 2026**
*Built by Team MARVELS*
