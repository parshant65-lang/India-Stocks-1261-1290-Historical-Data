# India-Stocks-1261-1290-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1261 to 1290)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1261-1290-Historical-Data/
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

## 📦 Constituents (1261 to 1290)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1261 | `HINDADH` | Hindustan Adhesives Limited | `HINDADH.NS` |
| 1262 | `HINDALUMI` | Hind Aluminium Industries Limited | `HINDALUMI.NS` |
| 1263 | `HINDCOMPOS` | Hindustan Composites Limited | `HINDCOMPOS.NS` |
| 1264 | `HINDCON` | Hindcon Chemicals Limited | `HINDCON.NS` |
| 1265 | `HINDOILEXP` | Hindustan Oil Exploration Company Limited | `HINDOILEXP.NS` |
| 1266 | `HINDWAREAP` | Hindware Home Innovation Limited | `HINDWAREAP.NS` |
| 1267 | `HIRECT` | Hirect Limited | `HIRECT.NS` |
| 1268 | `HISARMETAL` | Hisar Metal Industries Limited | `HISARMETAL.NS` |
| 1269 | `HITECH` | Hi-Tech Pipes Limited | `HITECH.NS` |
| 1270 | `HITECHCORP` | Hitech Corporation Limited | `HITECHCORP.NS` |
| 1271 | `HITECHGEAR` | The Hi-Tech Gears Limited | `HITECHGEAR.NS` |
| 1272 | `HLEGLAS` | HLE Glascoat Limited | `HLEGLAS.NS` |
| 1273 | `HLVLTD` | HLV LIMITED | `HLVLTD.NS` |
| 1274 | `HMAAGRO` | HMA Agro Industries Limited | `HMAAGRO.NS` |
| 1275 | `HMT` | HMT Limited | `HMT.NS` |
| 1276 | `HMVL` | Hindustan Media Ventures Limited | `HMVL.NS` |
| 1277 | `HNDFDS` | Hindustan Foods Limited | `HNDFDS.NS` |
| 1278 | `HONDAPOWER` | Honda India Power Products Limited | `HONDAPOWER.NS` |
| 1279 | `HORIZONIND` | Horizon Industrial Parks Limited | `HORIZONIND.NS` |
| 1280 | `HPAL` | HP Adhesives Limited | `HPAL.NS` |
| 1281 | `HPIL` | Hindprakash Industries Limited | `HPIL.NS` |
| 1282 | `HPL` | HPL Electric & Power Limited | `HPL.NS` |
| 1283 | `HRYNSHP` | Hariyana Ship Breakers Limited | `HRYNSHP.NS` |
| 1284 | `HTEL` | Hy-Tech Engineers Limited | `HTEL.NS` |
| 1285 | `HTMEDIA` | HT Media Limited | `HTMEDIA.NS` |
| 1286 | `HUBTOWN` | Hubtown Limited | `HUBTOWN.NS` |
| 1287 | `HUHTAMAKI` | Huhtamaki India Limited | `HUHTAMAKI.NS` |
| 1288 | `HYBRIDFIN` | Hybrid Financial Services Limited | `HYBRIDFIN.NS` |
| 1289 | `IBULLSLTD` | Indiabulls Limited | `IBULLSLTD.NS` |
| 1290 | `ICDSLTD` | ICDS Limited | `ICDSLTD.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream HINDADH 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1261-1290-Historical-Data/main/HINDADH/1m/2026/10/HINDADH_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
