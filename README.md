# AI LeadGen Performance Reporter

> **Sistema AI per il reporting settimanale di campagne lead generation Meta Ads + Google Ads in contesto EdTech.**
> Trasforma Claude in un Marketing Analyst senior che legge i KPI delle campagne, calcola le variazioni settimana-su-settimana, identifica top e worst performer, genera un executive report in italiano con raccomandazioni operative concrete.

![Status](https://img.shields.io/badge/status-POC-yellow) ![Built with](https://img.shields.io/badge/built%20with-Claude%20Code-orange) ![Use case](https://img.shields.io/badge/use%20case-EdTech%20LeadGen-blue) ![License](https://img.shields.io/badge/license-MIT-green)

---

## 🇮🇹 Executive Summary (italiano)

**Cosa fa.** Un Marketing Manager apre Claude.ai, incolla un system prompt strutturato (questo repo) e i dati settimanali delle campagne ads (CSV). In 15-20 secondi ottiene un report executive in italiano pronto da girare al C-level: variazioni W-on-W per campagna, top 3 insight strategici, raccomandazioni operative attuabili e alert su anomalie.

**Perché esiste.** Nelle scale-up EdTech il media buying è quasi sempre esternalizzato ad agenzie. Il team marketing interno passa ore ogni settimana a leggere dashboard Meta + Google Ads, confrontarle, scrivere brief per il management e raccomandazioni per le agenzie. Questo tool comprime quel ciclo da 2-3 ore a 5 minuti, mantenendo il giudizio umano sul brief finale ma automatizzando la parte di analisi strutturata.

**Per chi è pensato.** Marketing Manager e Marketing Operations Specialist di scale-up EdTech italiane che coordinano agenzie media esterne e devono produrre reporting settimanale verso il top management.

**Stato attuale.** POC con dati simulati (vedi sezione *Roadmap*). Il prompt è progettato per essere immediatamente adattabile a dati reali sostituendo i due CSV di esempio.

---

## 🎯 Il problema che risolve

In una scale-up EdTech italiana tipica:

- **6-10 campagne attive** in parallelo tra Meta Ads e Google Ads (Awareness, Conversion, Retargeting, Search Brand, Search Generic, Performance Max)
- **Agenzie esterne** che gestiscono il buying e mandano report ogni venerdì
- **Marketing Manager interno** che deve aggregare quei dati, calcolare variazioni W-on-W, identificare anomalie, produrre un riassunto leggibile dal C-level entro lunedì mattina
- **2-3 ore** di lavoro ripetitivo per settimana che potrebbero diventare 30 minuti di review + decisioni

Questo tool gestisce la parte ripetitiva: calcoli, alert, struttura del report, raccomandazioni standard. Il Marketing Manager mantiene il controllo sul giudizio strategico finale.

---

## ⚙️ Come funziona

```
┌─────────────────────┐     ┌────────────────────┐     ┌──────────────────────┐
│  CSV settimanali    │ ──▶ │  Claude (Sonnet)   │ ──▶ │  Executive Report    │
│  W-corrente + W-1   │     │  + System Prompt   │     │  IT, 5 blocchi       │
│  Meta + Google Ads  │     │  + Benchmark KPI   │     │  Pronto per C-level  │
└─────────────────────┘     └────────────────────┘     └──────────────────────┘
```

Il sistema si basa su 4 componenti:

1. **System prompt strutturato** (`docs/system-prompt.md`) — definisce il ruolo (senior marketing analyst), il contesto (EdTech bootcamp italiano), lo schema input, l'output obbligatorio in 5 blocchi, e regole di calcolo esplicite (variazioni W-on-W).
2. **Benchmark KPI di settore** (`docs/benchmark-edtech.md`) — 11 soglie di riferimento calibrate per platform × campaign objective sul mercato italiano EdTech bootcamp 2026.
3. **Glossario KPI** (`docs/kpi-glossary.md`) — definizioni operative per allineamento terminologico.
4. **Dati CSV** (`data/week-XX-kpi.csv`) — schema a 12 colonne tipizzate, due settimane (corrente e baseline).

L'output è strutturato in 5 blocchi obbligatori:

1. **Executive Summary** (3-4 righe) — budget, lead, CPL medio, trend
2. **Analisi per Campagna** — scheda compatta per ciascuna delle 6 campagne con verdetto a semaforo (✅ 🟢 🟡 🔴)
3. **Top 3 Insights della Settimana** — pattern strategici emersi dai dati
4. **Raccomandazioni Operative** — azioni specifiche, misurabili, time-bound per campagne sotto target
5. **Alert & Attenzione** — anomalie da escalare al Marketing Manager

---

## 🚀 Quickstart (3 minuti)

**Requisiti:** un account Claude.ai (anche piano free è sufficiente).

1. Apri [https://claude.ai](https://claude.ai) e inizia una nuova conversazione
2. Copia il contenuto di [`docs/system-prompt.md`](docs/system-prompt.md) e incollalo come primo messaggio
3. Copia il contenuto di [`data/week-18-kpi.csv`](data/week-18-kpi.csv) (baseline) e poi [`data/week-19-kpi.csv`](data/week-19-kpi.csv) (settimana corrente) e incollali come secondo messaggio
4. Claude genera l'executive report in 15-20 secondi

Vedi screenshot in [`examples/`](examples/) per il flusso completo.

---

## 📂 Struttura del repository

```
ai-leadgen-performance-reporter/
├── docs/
│   ├── system-prompt.md         # System prompt completo (role, context, task, benchmark)
│   ├── benchmark-edtech.md      # Tabella benchmark KPI EdTech Italia 2026
│   └── kpi-glossary.md          # Definizioni operative KPI in italiano
├── data/
│   ├── week-19-kpi.csv          # Dati settimana corrente (6 campagne)
│   └── week-18-kpi.csv          # Dati settimana baseline per confronto W-on-W
├── examples/
│   ├── 01-claude-system-prompt-loaded.png    # Setup: prompt caricato
│   ├── 02-input-data-csv.png                 # Input: CSV incollati
│   ├── 03-executive-report-output.png        # Output: report generato
│   └── 04-recommendations-detail.png         # Output: dettaglio raccomandazioni
├── README.md
└── LICENSE
```

---

## 🧠 Scelte di design (per chi vuole capire il "perché")

Alcune decisioni di prodotto che ho preso durante la costruzione, e perché:

**Perché Claude e non altri LLM.** Claude (Sonnet 4) è particolarmente forte nell'analisi strutturata di tabelle numeriche e nell'output professionale in italiano. Per workflow di reporting executive, la consistenza dello stile e l'accuratezza dei calcoli pesano più della creatività generativa.

**Perché variazioni W-on-W in % per metriche assolute, in punti percentuali per CTR e conversion rate.** Quando un CTR passa da 2% a 3%, l'aumento è di +50% o di +1 punto percentuale? Entrambi, ma per un Marketing Manager il punto percentuale è più leggibile. Per metriche assolute (€, lead) la % è invece l'unità naturale. Il prompt forza questa convenzione esplicitamente.

**Perché 11 benchmark distinti per platform × objective.** Un CPL di €15 è eccellente per una campagna Search Generic ma deludente per una Search Brand. I benchmark generici (es. "il CPL medio è X") generano insight inutili. Servono soglie contestuali.

**Perché 5 blocchi di output fissi.** I report executive devono essere prevedibili nella struttura. Un Marketing Manager che li riceve ogni lunedì deve sapere dove guardare per trovare le 3 informazioni critiche. La struttura fissa è un feature, non un limite.

**Perché un sistema di verdetto a semaforo (✅ 🟢 🟡 🔴).** Permette al C-level di skimmare il report in 30 secondi e fermarsi solo sulle campagne che richiedono attenzione.

---

## 🗺️ Roadmap

**Lo stato attuale è un POC funzionante con dati simulati.** Le evoluzioni naturali in versione 2.0:

- **v1.1 — Connessione dati reali.** Sostituire il flusso copia-incolla con integrazione API Meta Ads + Google Ads Reports. Tecnicamente: un wrapper Python che pulla i dati settimanali e li passa a Claude via Anthropic API.
- **v1.2 — Output PDF auto-formattato.** Generare un PDF brandizzato pronto da condividere via email, invece di output testuale.
- **v1.3 — Multi-cliente.** Supporto a più account in parallelo (utile per agenzie che gestiscono N clienti EdTech).
- **v1.4 — Confronto su finestra mobile.** Estendere il confronto da W-on-W a window mobili (4-settimane, trimestre) per identificare trend strutturali oltre alle oscillazioni settimanali.
- **v1.5 — Trigger automatici.** Workflow n8n/Zapier che esegue il report ogni lunedì alle 8:00 e lo invia direttamente al Marketing Manager.

---

## ⚠️ Limitazioni note

- **POC con dati simulati**: i CSV di esempio sono dati realistici ma fittizi. Non posso usare dati reali per ragioni di confidenzialità dei progetti su cui lavoro attualmente.
- **Calcoli numerici**: Claude è affidabile su calcoli percentuali e variazioni di base, ma per analisi statistiche più complesse (regressioni, attribution modeling) servirebbe un layer di analisi dedicato.
- **Benchmark calibrati su EdTech bootcamp Italia 2026**: vanno ricalibrati per altri verticali (es. EdTech B2B, scale-up SaaS) o altri mercati.
- **Lingua output**: ottimizzato per italiano professionale. L'output in altre lingue richiede aggiustamenti al prompt.

---

## 🔌 Nota sull'integrazione con le piattaforme

Lo schema CSV di esempio (12 colonne) è progettato come **standard intermedio** tra il Marketing Manager e Claude. I CSV esportati direttamente da Meta Ads Manager, Google Ads e Looker Studio hanno colonne con nomi diversi (es. "Amount Spent (EUR)" vs `budget_spent_eur`, "Cost" vs `budget_spent_eur`), formato settimana non ISO (es. "May 13 - May 19, 2026" vs `2026-W19`), e separatori currency variabili.

**Conseguenza operativa:** prima di incollare i dati in Claude, è necessario un **mapping una tantum** (rinomina colonne + normalizzazione settimana) che richiede 2-3 minuti la prima volta e poi può essere automatizzato con:

- Un foglio Sheets template con formule di pulizia
- Uno script bash/Python di normalizzazione
- L'integrazione API diretta prevista in **v1.1** della roadmap (wrapper Python con Meta Ads + Google Ads Reports API)

Questa frizione è **voluta nel POC**: tenere il mapping fuori dal sistema mantiene il prompt portabile e adattabile a schemi diversi (es. CRM proprietari, dashboard interne). In versione production il mapping è invisibile all'utente finale.

---

## 👤 Built by

**Lorenzo Ricci** — Project Manager & Communications Specialist

Costruito come showcase di product design AI-assistito per ruoli Marketing Operations / Marketing Specialist in scale-up EdTech. Le scelte di prodotto (KPI, benchmark, struttura output, anti-pattern) riflettono anni di esperienza in coordinamento agenzie media e reporting client-facing.

## 📄 License

MIT
