# 🧠 AI Data & Business Analyst — Roadmap de Proiect

**Obiectiv final:** un tool (Python + LLM) căruia îi dai un dataset (CSV/Excel) și îți scoate automat:
- insight-uri de business relevante
- typos / inconsistențe în date categorice
- outliers și anomalii
- calitate generală a datelor (missing values, duplicate, tipuri greșite)
- recomandări de decizie, în limbaj natural

**Format:** documentat integral pe GitHub, un branch/folder per săptămână, cu README explicativ la fiecare etapă.

**Punct de plecare:** ai deja Data Analytics, Advanced Data Analytics și IBM Business Analysis (Coursera) — deci sărim peste noțiunile de bază de analiză și mergem direct pe partea tehnică + aplicată.

---

## 📁 Structura recomandată a repo-ului GitHub

```
ai-data-analyst/
├── README.md                 <- prezentare generală proiect + demo GIF/screenshot
├── ROADMAP.md                <- acest fișier
├── 01_sql/
├── 02_python_pandas/
├── 03_statistics/
├── 04_dataviz/
├── 05_powerbi/
├── 06_apis/
├── 07_machine_learning/
├── 08_finance/
├── 09_capstone_ai_tool/       <- produsul final
│   ├── app.py
│   ├── modules/
│   ├── notebooks/
│   └── README.md
└── datasets/
```

Fiecare folder = un README scurt cu: ce ai învățat, ce exerciții ai făcut, link la resurse, screenshot-uri.

---

## 🗓️ Faza 0 — Setup (2-3 zile)

- Cont GitHub + Git instalat local (sau folosești GitHub Codespaces, gratuit).
- Instalezi: Python 3.11+, VS Code, extensii Python/Jupyter.
- Creezi structura de mai sus, faci primul commit ("project skeleton").
- Alegi 2-3 dataseturi „prietenoase" de pe Kaggle sau data.gov pentru exersat pe tot parcursul (ex: retail sales, HR attrition, e-commerce orders) — le refolosești constant, asta creează coerență în portofoliu.

---

## Săptămâna 1-2 — SQL

**De ce:** e coloana vertebrală a oricărei analize de business reale.

**Resurse gratuite:**
- SQLZoo (interactiv, exerciții progresive)
- Mode Analytics SQL Tutorial (gratuit, orientat business)
- W3Schools SQL (referință rapidă)
- Kaggle Learn → „Intro to SQL" + „Advanced SQL" (gratuit)

**Ce înveți:** SELECT/WHERE/JOIN/GROUP BY → subqueries, window functions (RANK, LAG/LEAD, PARTITION BY), CTEs.

**Proiect mini:** rulezi SQLite local pe unul din dataseturile alese, scrii 15-20 query-uri de business (top clienți, retenție, trend vânzări lunar) → le pui în `01_sql/queries.sql` cu explicații.

---

## Săptămâna 2-4 — Python pentru Data Analysis (pandas/numpy)

**Resurse gratuite:**
- Kaggle Learn → „Pandas", „Python"
- Corey Schafer (YouTube) — seria de Pandas, foarte clară
- freeCodeCamp — „Data Analysis with Python" (curs complet gratuit pe YouTube)
- Documentația oficială pandas (are un „10 minutes to pandas" excelent)

**Ce înveți:** citire/curățare date, missing values, groupby, merge, pivot, funcții custom, `apply`/`map`.

**Proiect mini:** curățare completă a unui dataset „murdar" (poți lua unul intenționat neîngrijit de pe Kaggle — „messy dataset") → documentezi fiecare decizie de curățare într-un notebook.

---

## Săptămâna 4-5 — Statistică aplicată

**Resurse gratuite:**
- StatQuest with Josh Starmer (YouTube) — cel mai bun canal pentru intuiție statistică
- Khan Academy — Statistics & Probability (gratuit, structurat)
- Kaggle Learn → nu are curs dedicat, dar poți aplica direct în pandas/scipy

**Ce înveți:** medie/mediană/deviație standard, distribuții, corelație vs cauzalitate, testare ipoteze (t-test, chi-square), z-score, IQR (esențial pentru outliers).

**Proiect mini:** analiză statistică descriptivă + testare de ipoteză pe un dataset de business (ex: „campania A a crescut semnificativ vânzările față de campania B?").

---

## Săptămâna 5-6 — Data Visualization

**Resurse gratuite:**
- Kaggle Learn → „Data Visualization"
- Documentația matplotlib/seaborn (galerii cu exemple)
- Plotly Python — pentru grafice interactive (foarte util pentru tool-ul final)

**Ce înveți:** matplotlib (bază), seaborn (statistic viz), plotly (interactiv, dashboards).

**Proiect mini:** un notebook „storytelling" — 5-6 grafice care spun o poveste de business completă dintr-un dataset, cu narativ scris.

---

## Săptămâna 6-7 — Power BI

**Resurse gratuite:**
- Microsoft Learn — „Power BI" learning path (gratuit, oficial)
- Guy in a Cube (YouTube) — cel mai popular canal Power BI
- Power BI Desktop e gratuit de instalat (Windows; dacă ești pe Mac, poți folosi o VM gratuită sau te concentrezi mai mult pe Python/Plotly pentru dashboards)

**Ce înveți:** Power Query (ETL), modelare de date, DAX de bază, dashboard design.

**Proiect mini:** un dashboard interactiv pe unul din dataseturile tale, publicat ca screenshot/video în portofoliu (Power BI publish e gratuit dar public).

---

## Săptămâna 7-8 — APIs

**Resurse gratuite:**
- Documentația `requests` (Python) — simplă și suficientă
- FastAPI — tutorial oficial (excelent, gratuit) — îl vei folosi pentru tool-ul final
- Public APIs gratuite pentru exersat (ex: exchange rates, weather, alpha vantage pentru date financiare)

**Ce înveți:** consum de API extern (GET/POST, JSON, autentificare cu API key), și construire de API proprie cu FastAPI (esențial pentru capstone).

**Proiect mini:** un script care extrage date financiare/economice live printr-un API public și le salvează structurat.

---

## Săptămâna 8-10 — Machine Learning

**Resurse gratuite:**
- Kaggle Learn → „Intro to Machine Learning" + „Intermediate ML"
- Andrew Ng — Machine Learning Specialization (Coursera, poți face audit gratuit fără certificat)
- scikit-learn — documentație + exemple (foarte bine scrisă)

**Ce înveți:** regresie, clasificare, train/test split, cross-validation, feature engineering, și — important pentru tool-ul tău — **algoritmi de detectare outliers** (Isolation Forest, Local Outlier Factor, DBSCAN pentru clustering anomalii).

**Proiect mini:** model simplu de predicție (ex: churn prediction) + un notebook dedicat outlier detection cu 2-3 metode comparate.

---

## Săptămâna 10-11 — Finance pentru analiști

**Resurse gratuite:**
- Corporate Finance Institute (CFI) — au module gratuite introductive
- Investopedia — referință excelentă pentru concepte (gratuit)
- Aswath Damodaran (NYU) — cursuri complete de corporate finance/valuation, gratuite pe YouTube — nivel foarte avansat dar excelent

**Ce înveți:** citire situații financiare (P&L, balance sheet, cash flow), KPI-uri de business (CAC, LTV, churn, margin), noțiuni de bază de valuation.

**Proiect mini:** analiză financiară a unei companii publice (folosind date reale, ex de pe SEC EDGAR — gratuit) → interpretare KPI-uri.

---

## Săptămâna 11-13+ — Capstone: Tool-ul de AI Data Analysis

Aici pui tot cap la cap. Arhitectura recomandată:

### 1. Ingestion
- Upload CSV/Excel (pandas `read_csv`/`read_excel`)

### 2. Data Quality & Profiling
- Missing values, duplicate rows, tipuri de date greșite
- Detectare typos în coloane categorice (ex: „Bucuresti" vs „București" vs „buc") — folosind `rapidfuzz` (fuzzy string matching) pentru a grupa variații ale aceleiași valori
- Librărie utilă: `ydata-profiling` (fost pandas-profiling) — generează automat un raport de profiling, pe care apoi îl interpretezi/rafinezi

### 3. Outlier Detection
- Metode statistice simple: Z-score, IQR (rapid, transparent)
- Metode ML: Isolation Forest / LOF (pentru anomalii multivariate)
- Afișezi outlierii vizual (boxplots, scatter cu highlight)

### 4. Statistical Summary
- Distribuții, corelații, trenduri temporale (dacă există coloană de dată)

### 5. Vizualizare automată
- Plotly — generezi automat grafice relevante în funcție de tipul coloanelor (numerice → histograme/boxplot, categorice → bar charts, date → time series)

### 6. Stratul de AI (LLM) — partea „inteligentă"
- Iei rezultatele structurate din pașii 2-5 (statistici, outliers, typos găsite) și le trimiți ca prompt către un model LLM (poți folosi Claude API — ai deja acces la Anthropic API, e cel mai natural fit)
- Modelul primește un „sumar de date" structurat (JSON) și generează insight-uri de business în limbaj natural, prioritizate după impact
- **Foarte important pentru portofoliu:** documentezi clar prompt-ul folosit și de ce — arată maturitate în „prompt engineering", nu doar „am apelat un API"

### 7. Interfață
- Streamlit (cel mai rapid mod de a face un frontend funcțional în Python, gratuit)
- Upload dataset → vezi profiling + outliers + typos + grafice + insight-uri AI, totul într-un singur dashboard

### 8. Deployment (gratuit)
- Streamlit Community Cloud — deploy gratuit direct din GitHub repo
- Astfel ai și un link live de arătat în CV/portofoliu, nu doar cod

---

## 📝 Cum documentezi pe GitHub (foarte important pentru portofoliu)

Pentru fiecare săptămână/folder:
1. **Ce am învățat** (2-3 fraze)
2. **Resursele folosite** (linkuri)
3. **Ce am construit** (notebook/query/dashboard)
4. **Decizii + raționament** — nu doar cod, ci *de ce* ai ales acea abordare (asta arată gândire de analist, nu doar execuție)
5. **Ce aș face diferit** — arată reflecție critică, apreciat de recruiteri

README-ul principal al repo-ului ar trebui să aibă: descrierea proiectului, un GIF/screenshot al tool-ului final, tech stack, cum se rulează local, link la deployment live.

---

## ⏱️ Timeline sumar

| Săptămâni | Temă |
|---|---|
| 0 | Setup |
| 1-2 | SQL |
| 2-4 | Python (pandas/numpy) |
| 4-5 | Statistică |
| 5-6 | Data Viz |
| 6-7 | Power BI |
| 7-8 | APIs |
| 8-10 | Machine Learning |
| 10-11 | Finance |
| 11-13+ | Capstone: AI Data Analyst Tool |

Total: ~12-14 săptămâni, dar flexibil — dacă unele teme îți vin mai ușor (ai deja bază din Coursera), poți comprima SQL/Python și avansa mai repede spre ML/capstone.

---

## 💡 Notă despre costuri

Tot ce e listat mai sus e **gratuit**. Singurul cost posibil ar fi apelurile către Claude API în faza de capstone (dar sunt foarte ieftine la volum mic de testare — câțiva dolari cel mult pentru tot proiectul). Streamlit Cloud, GitHub, toate cursurile menționate sunt gratuite.
