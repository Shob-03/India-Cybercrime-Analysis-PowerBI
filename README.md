# 🔐 India Cybercrime Analysis — Power BI
Cybercrime analysis across Indian states built with Power BI — analyzing crime motives, fraud patterns and sexual exploitation cases using real government data from data.gov.in

## 📌 Objective
Analyzed cybercrime data across Indian states to identify the most 
prevalent crime motives, highest affected states, and breakdown of 
fraud, extortion and sexual exploitation cases.

## 📂 Dataset
- **Source:** data.gov.in — National Crime Records Bureau (NCRB)
- **Records:** 191 city/state level cybercrime records
- **Coverage:** 74 States/UTs
- **Crime Motives:** 14 categories including Fraud, Sexual 
  Exploitation, Extortion, Personal Revenge, Prank and more
- **Tools Used:** Power BI, DAX

## 📊 Dashboard Pages

### Page 1 — Crime Overview
- Total States: 74 | Total Crimes: 146K
- Total Fraud Cases: 86K | Total Sexual Exploitation: 9K
- Geographic distribution map of cybercrime across India
- Crime breakdown donut — Fraud, Others, Extortion, Sexual Exploitation
- Total crimes by state — top 6 most affected states
- Total crime by motive — all 14 motive categories ranked

### Page 2 — Motive Deep Dive
- Fraud Rate: 58.73%
- Total Extortion: 6K | Total Personal Revenge: 4K
- Total Prank Cases: 2K | Total Sexual Exploitation: 9K
- Top 6 states by Fraud cases
- Top 6 states by Sexual Exploitation cases
- Top 6 states by Extortion cases
- Comparative table — Fraud, Extortion and Sexual Exploitation by state

## 🧮 DAX Measures

```dax
-- Total crimes
Total Crimes = SUM('Dataset_CyberCrime_Sean'[Total])

-- Fraud rate as percentage of total crimes
Fraud Rate % = 
DIVIDE(
    SUM('Dataset_CyberCrime_Sean'[Fraud]),
    SUM('Dataset_CyberCrime_Sean'[Total])
) * 100

-- Sexual exploitation rate
Sexual Exploitation Rate % = 
DIVIDE(
    SUM('Dataset_CyberCrime_Sean'[Sexual Exploitation]),
    SUM('Dataset_CyberCrime_Sean'[Total])
) * 100

-- Distinct counts
Total Cities = DISTINCTCOUNT('Dataset_CyberCrime_Sean'[City])
Total Fraud = SUM('Dataset_CyberCrime_Sean'[Fraud])
Total Sexual Exploitation Cases = 
    SUM('Dataset_CyberCrime_Sean'[Sexual Exploitation])
```

## 🔍 Key Insights
- **Fraud is the dominant cybercrime motive** accounting for 
  67.68% of all cases with 85,615 total fraud cases nationally
- **Uttar Pradesh and Karnataka are the most affected states** 
  with 33,764 and 31,774 total cybercrime cases respectively
- **Karnataka leads in fraud cases** with 29,266 cases — 
  significantly higher than any other state
- **Uttar Pradesh has the highest extortion cases** at 2,217 
  followed by Assam at 1,183
- **Maharashtra records the most sexual exploitation cases** 
  at 2,355 — highest among all states
- **Abetment to Suicide is the rarest cybercrime motive** 
  with only 7 cases nationally
- **Fraud accounts for 58.73% of all cybercrime** making it 
  the single biggest cybercrime challenge in India

## 🛠️ Tools
- Power BI — dashboard and visualizations
- DAX — calculated measures
- Data Source — data.gov.in (Government of India open data portal)
