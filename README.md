# India-Stocks-841-870-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 841 to 870)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-841-870-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (841 to 870)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 841 | `CAMLINFINE` | Camlin Fine Sciences Limited | `CAMLINFINE.NS` |
| 842 | `CAMPUS` | Campus Activewear Limited | `CAMPUS.NS` |
| 843 | `CANTABIL` | Cantabil Retail India Limited | `CANTABIL.NS` |
| 844 | `CAPACITE` | Capacit'e Infraprojects Limited | `CAPACITE.NS` |
| 845 | `CAPILLARY` | Capillary Technologies India Limited | `CAPILLARY.NS` |
| 846 | `CAPITALSFB` | Capital Small Finance Bank Limited | `CAPITALSFB.NS` |
| 847 | `CAPTRUST` | Capital Trust Limited | `CAPTRUST.NS` |
| 848 | `CARERATING` | CARE Ratings Limited | `CARERATING.NS` |
| 849 | `CARRARO` | Carraro India Limited | `CARRARO.NS` |
| 850 | `CARYSIL` | CARYSIL LIMITED | `CARYSIL.NS` |
| 851 | `CCCL` | Consolidated Construction Consortium Limited | `CCCL.NS` |
| 852 | `CCHHL` | Country Club Hospitality & Holidays Limited | `CCHHL.NS` |
| 853 | `CEIGALL` | Ceigall India Limited | `CEIGALL.NS` |
| 854 | `CEINSYS` | Ceinsys Tech Limited | `CEINSYS.NS` |
| 855 | `CELEBRITY` | Celebrity Fashions Limited | `CELEBRITY.NS` |
| 856 | `CELLO` | Cello World Limited | `CELLO.NS` |
| 857 | `CENTENKA` | Century Enka Limited | `CENTENKA.NS` |
| 858 | `CENTEXT` | Century Extrusions Limited | `CENTEXT.NS` |
| 859 | `CENTRUM` | Centrum Capital Limited | `CENTRUM.NS` |
| 860 | `CENTUM` | Centum Electronics Limited | `CENTUM.NS` |
| 861 | `CENTURYPLY` | Century Plyboards (India) Limited | `CENTURYPLY.NS` |
| 862 | `CERA` | Cera Sanitaryware Limited | `CERA.NS` |
| 863 | `CEWATER` | Concord Enviro Systems Limited | `CEWATER.NS` |
| 864 | `CFEL` | Confidence Futuristic Energetech Limited | `CFEL.NS` |
| 865 | `CGVAK` | CG Vak Software & Exports Limited | `CGVAK.NS` |
| 866 | `CHALET` | Chalet Hotels Limited | `CHALET.NS` |
| 867 | `CHEMBOND` | Chembond Material Technologies Limited | `CHEMBOND.NS` |
| 868 | `CHEMBONDCH` | Chembond Chemicals Limited | `CHEMBONDCH.NS` |
| 869 | `CHEMCON` | Chemcon Speciality Chemicals Limited | `CHEMCON.NS` |
| 870 | `CHEMCRUX` | Chemcrux Enterprises Limited | `CHEMCRUX.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream CAMLINFINE 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-841-870-Historical-Data/main/CAMLINFINE/1m/2026/10/CAMLINFINE_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
