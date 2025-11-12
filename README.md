This dataset provides a comprehensive view of dynamic supplier disruption risk scoring, combining multi-source indicators and intelligent modeling outputs for multiple suppliers across a simulated 60-day time horizon. It has been designed to support research and experimentation in risk & context-aware supplier selection, digital twin-driven supply chain resilience, and hybrid decision-support systems that blend knowledge graphs (KGs), semantic embeddings, and simulation-based risk-mitigation policies. The dataset contains daily records from January 1 to March 1, 2025, for 10 suppliers. Each row includes temporal disruption signals and pre-computed disruption risk outputs based on a fused analytical model. This model integrates a knowledge graph (KG) based supplier assessment criteria score (kg_score),  NLP based (natural language processing) semantic embedding score (Em_Score), and five external disruption indicators: Twitter alert presence (twitter_alert), weather disruptions (weather_risk), economic risk (economic_risk), geopolitical signal (geo_risk), and technology disruption (tech_risk). Additionally, the daily supplier downtime (downtime_hours) is logged as an operational impact measure. The final column, high_disruption_p, represents the daily probability of high disruption, calculated using la ogistic regression equation.

File Format:

The main dataset is presented in CSV format, compatible with Python, R, MATLAB, and Excel. Each column is clearly labeled, and date stamps are included for anomaly detection studies.

Intended Use:

•	Academic Research: Users can analyze disruption propagation, model resilience strategies, and evaluate multi-objective trade-offs in supplier selection.
•	Simulation Input: These records can serve as input scenarios for discrete-event or agent-based simulations in AnyLogic, Simio, or FlexSim for digital twin supply chains.
•	ML Training/Benchmarking: The dataset may be used to train or benchmark models for disruption classification, predictive maintenance scheduling, or RL-based supplier switching strategies.
•	Multi-Criteria Decision Making (MCDM): Decision-makers can explore trade-offs among cost, risk, downtime, and sustainability dimensions.

Tools Required:

•	Basic Analysis: Any spreadsheet tool (MS Excel, Google Sheets).
•	Advanced Analysis: Python (Pandas, NumPy, Scikit-learn), Jupyter Notebook, or RStudio.
•	Simulation Integration: AnyLogic or FlexSim with Java/Python (Pycommunicator) input connectors for real-time score injection.

Recommended Preprocessing:

•	Normalize kg_score and Em_Score if used for comparative model training.
•	Convert binary indicators (twitter_alert, geo_risk, etc.) to categorical strings (“Yes”/ “No”) for dashboarding purposes.
•	Apply rolling average or exponential smoothing on high_disruption_p for volatility analysis.
