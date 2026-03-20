RaahiBima 

🚀AI-Powered Parametric Income Protection for India’s Q-Commerce Gig WorkersRahiBima is a specialized parametric insurance platform designed for the backbone of India's 10-minute delivery ecosystem (Zepto, Blinkit, Swiggy Instamart). We protect riders from the one thing traditional insurance ignores: lost opportunity cost due to external disruptions.

📌 Problem Statement
  For a delivery partner like Ravi (26, Bangalore), a sudden monsoon downpour or a 43°C heatwave isn't just an inconvenience — it’s a financial wipeout.
  The Gap: 
    Traditional insurance covers accidents (Health/Life) or vehicles (Motor). No one covers the ₹400–₹600 loss incurred when a rider is forced off the road for 4 hours.
  The Friction: 
    Manual claims take weeks. For someone living on weekly pay cycles, "weeks" is too long.

💡 The RahiBima Solution: 
  Parametric "Non-Claim" InsuranceRahiBima eliminates the "Claims Department." Payouts are triggered by objective data, not manual reports.
  Target Persona:
    Q-Commerce riders in Indian metros.
  Coverage: 
    Income loss only (No health/life/accident).
  Payout Speed:
    Seconds via UPI, triggered automatically by API consensus.
  Premium Model:
    Dynamic weekly micro-payments (₹19 – ₹79) adjusted by zone-specific risk AI.

⛈️ Parametric Triggers (The "Ground Truth" Engine)
  We use a Multi-Oracle Consensus model. A payout is initiated only when ≥2 independent sources verify a disruption.TriggerThresholdData SourcesSustained Rain≥15mm/hr for ≥45 minsOpen-Meteo, IMDHeat IndexApparent temp ≥42°C (11AM–4PM)Open-MeteoSevere AQIPM2.5 AQI ≥300 for ≥3hrsOpenAQ APIFlood LockIMD Watch + Dark Store inactivityIMD RSS, Platform SignalCivic DisorderSection 144 / Curfew ordersNDMA RSS, NLP Classifier

🛡️ 5-Layer Fraud Defense Architecture
  To prevent "Flash Mob" attacks (coordinated GPS spoofing), RahiBima employs a proprietary defense stack:
    Parametric Lock: 
      Cannot spoof a rainstorm. If the API says it’s sunny, no payout occurs regardless of user reports.
    Sensor Fingerprinting: 
      Cross-verifying GPS variance (≥3m/5min) with Accelerometer/Gyroscope data to detect stationary "ghost" riders.
    GigTrust Score: 
      A 0.00–1.00 legitimacy rating based on account age, delivery history, and device stability.
    Zone Saturation Circuit Breaker: 
      If claims in a zone exceed 2.5x the historical expected rate, payouts are paused for manual batch-verification.
    Social Graph Analysis:
      Identifying "Sybil attacks" by detecting clusters of accounts sharing hardware IDs or UPI handles.

⚙️ Technical StackBackend: 
  FastAPI (Python): for high-concurrency async processing.
  Database: PostgreSQL (Supabase) for real-time disruption subscriptions.
  AI/ML: LightGBM: Weekly dynamic premium calculation based on rolling 12-week risk.
        Scikit-learn: Fraud detection and GigTrust scoring.
  Infrastructure: Celery + Redis for polling environmental APIs every 15 minutes.

📈 Economic ModelWeekly Cycle: 
  Premiums collected on Mondays; 
  Payouts disbursed instantly upon events.
  Dynamic Pricing: Low (₹19) to Surge (₹79) risk bands.
  Target Loss Ratio: 68–72%.
  Break-even: 77%.

📅 Roadmap (Guidewire DEVTrails 2026)
  [x] Phase 1: Concept Validation & Architecture Design (Current)
  [ ] Phase 2: Policy Management & Dynamic Premium Engine
  [ ] Phase 3: GigTrust Score Implementation & Instant UPI Payout Integration
  [ ] Final: Live Dashboard & Pitch Presentation


                                                                                                                                                                                      Built by Team MARVELS for GuideWire 2026
