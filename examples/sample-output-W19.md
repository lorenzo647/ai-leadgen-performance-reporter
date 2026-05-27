# Sample Output — Report Performance W19 2026

> Esempio reale di output generato dal sistema usando `data/week-18-kpi.csv` (baseline) e `data/week-19-kpi.csv` (settimana corrente) con il system prompt completo in `docs/system-prompt.md`.
>
> **Tempo di generazione:** ~25 secondi (include chain-of-thought aritmetica)
> **Modello usato:** Claude Sonnet
> **Lingua output:** Italiano professionale
> **Nota tecnica:** la sezione `<calcoli_interni>` è obbligatoria per garantire accuratezza aritmetica sui totali aggregati — vedere README sezione "Limitazioni note".

---

<calcoli_interni>

## RAGIONAMENTO INTERNO — CALCOLI PRE-REPORT

### 1. Lead W18 per campagna
- Awareness_IT_Bootcamp_Q2: 267
- Conversion_IT_Bootcamp_Q2: 380
- Retargeting_IT_Bootcamp: 179
- Search_Brand_Bootcamp: 284
- Search_Generic_Bootcamp: 290
- PerformanceMax_Bootcamp: 269

**TOTALE LEAD W18** = 267 + 380 + 179 + 284 + 290 + 269 = 1.669

### 2. Lead W19 per campagna
- Awareness_IT_Bootcamp_Q2: 243
- Conversion_IT_Bootcamp_Q2: 437
- Retargeting_IT_Bootcamp: 184
- Search_Brand_Bootcamp: 286
- Search_Generic_Bootcamp: 252
- PerformanceMax_Bootcamp: 229

**TOTALE LEAD W19** = 243 + 437 + 184 + 286 + 252 + 229 = 1.631

### 3. Budget W18 e W19
Budget W18: 4.500 + 6.200 + 1.800 + 2.800 + 5.400 + 5.100 = **25.800 €**
Budget W19: 4.500 + 6.200 + 1.800 + 2.800 + 5.400 + 5.100 = **25.800 €** (identico)

### 4. CPL medio ponderato W18
25.800 / 1.669 = **15,458 €** → arrotondato **€15,46**

### 5. CPL medio ponderato W19
25.800 / 1.631 = **15,820 €** → arrotondato **€15,82**

### 6. Variazione lead W-on-W
((1.631 - 1.669) / 1.669) * 100 = (-38 / 1.669) * 100 = **-2,3%**

### 7. Variazione CPL medio W-on-W
((15,82 - 15,46) / 15,46) * 100 = (0,36 / 15,46) * 100 = **+2,3%**

</calcoli_interni>

---

# REPORT PERFORMANCE CAMPAGNE — W19 2026

---

## 1. EXECUTIVE SUMMARY

Budget totale speso W19: **€25.800** (identico a W18). Lead totali generati: **1.631**, in calo del **-2,3%** rispetto ai 1.669 di W18. CPL medio ponderato: **€15,82** (+2,3% vs €15,46 W18). Il quadro complessivo è **stabile con segnali misti**: Conversion Meta accelera con forza (+15% lead, -13% CPL), ma Search Generic e PMax deteriorano sensibilmente, erodendo l'efficienza aggregata. Nessuna emergenza, ma due campagne Google richiedono intervento entro la settimana.

---

## 2. ANALISI PER CAMPAGNA

---

**Awareness_IT_Bootcamp_Q2 — Meta Ads**

- Budget speso: €4.500 (variazione W-on-W: 0%)
- Lead generati: 243 (variazione W-on-W: **-9,0%**)
- CPL: €18,52 (variazione W-on-W: **+9,9%**)
- CTR: 1,81% (variazione W-on-W: **-0,11 pts**)
- Conversion rate: 4,22% (variazione W-on-W: **-0,43 pts**)
- **Verdetto**: 🔴 Da ottimizzare
- **Insight**: Il drop di lead (-24 unità) con budget invariato segnala probabile saturazione delle creative su audience cold. Il CPL a €18,52 supera il benchmark superiore (€18) e il conversion rate sotto il 5% indica attrito anche lato landing.

---

**Conversion_IT_Bootcamp_Q2 — Meta Ads**

- Budget speso: €6.200 (variazione W-on-W: 0%)
- Lead generati: 437 (variazione W-on-W: **+15,0%**)
- CPL: €14,19 (variazione W-on-W: **-13,0%**)
- CTR: 2,90% (variazione W-on-W: **+0,29 pts**)
- Conversion rate: 10,41% (variazione W-on-W: **+0,78 pts**)
- **Verdetto**: ✅ Top performer
- **Insight**: Miglioramento su tutti i KPI con budget invariato — il lookalike 1% buyer sta performando in modo eccellente. CPL a €14,19 ben dentro benchmark, conversion rate sopra il 10%: la combinazione audience-creativa-landing è in piena forma.

---

**Retargeting_IT_Bootcamp — Meta Ads**

- Budget speso: €1.800 (variazione W-on-W: 0%)
- Lead generati: 184 (variazione W-on-W: **+2,8%**)
- CPL: €9,78 (variazione W-on-W: **-2,8%**)
- CTR: 4,39% (variazione W-on-W: **+0,29 pts**)
- Conversion rate: 9,95% (variazione W-on-W: **-0,01 pts**)
- **Verdetto**: ✅ Top performer
- **Insight**: La campagna è stabile e ultra-efficiente: CPL a €9,78 è il più basso del portafoglio e il CTR a 4,39% supera il benchmark. Con un pool di site visitors limitato, la crescita incrementale ulteriore dipende dal traffico upper-funnel.

---

**Search_Brand_Bootcamp — Google Ads**

- Budget speso: €2.800 (variazione W-on-W: 0%)
- Lead generati: 286 (variazione W-on-W: **+0,7%**)
- CPL: €9,79 (variazione W-on-W: **-0,7%**)
- CTR: 8,16% (variazione W-on-W: **-0,04 pts**)
- Conversion rate: 9,16% (variazione W-on-W: **-0,17 pts**)
- **Verdetto**: 🟢 In miglioramento
- **Insight**: Performance sostanzialmente piatta rispetto a W18 — variazioni minime su tutti i KPI. Il CPL a €9,79 è in benchmark e la campagna svolge la sua funzione protettiva in modo consistente. Nessuna azione richiesta.

---

**Search_Generic_Bootcamp — Google Ads**

- Budget speso: €5.400 (variazione W-on-W: 0%)
- Lead generati: 252 (variazione W-on-W: **-13,1%**)
- CPL: €21,43 (variazione W-on-W: **+15,1%**)
- CTR: 3,00% (variazione W-on-W: **-0,17 pts**)
- Conversion rate: 9,39% (variazione W-on-W: **-1,11 pts**)
- **Verdetto**: 🔴 Da ottimizzare
- **Insight**: Deterioramento netto in una settimana: -38 lead e CPL che si avvicina al benchmark superiore (€25). Il calo del CTR suggerisce pressione competitiva sui keyword generici o stanchezza degli annunci.

---

**PerformanceMax_Bootcamp — Google Ads**

- Budget speso: €5.100 (variazione W-on-W: 0%)
- Lead generati: 229 (variazione W-on-W: **-14,9%**)
- CPL: €22,27 (variazione W-on-W: **+17,5%**)
- CTR: 1,69% (variazione W-on-W: **-0,15 pts**)
- Conversion rate: 4,68% (variazione W-on-W: **-0,58 pts**)
- **Verdetto**: 🔴 Da ottimizzare
- **Insight**: Il peggioramento è trasversale — meno click, meno conversioni, CPL in salita del +17,5% in una settimana. La conversion rate scende sotto soglia critica (4,68% < 5%). Con budget invariato e output calante, l'algoritmo PMax sta probabilmente erodendo qualità della distribuzione.

---

## 3. TOP 3 INSIGHTS DELLA SETTIMANA

**1. Meta Conversion esplode mentre Google erode: divergenza di piattaforma netta**

Meta Conversion genera +57 lead con CPL calato di €2,13, mentre Search Generic e PMax perdono rispettivamente 38 e 40 lead con CPL in crescita. A parità di budget totale (€25.800), il mix di efficienza si sposta chiaramente verso Meta. Se il trend persiste la prossima settimana, è opportuno considerare una riallocazione di budget da Google non-brand verso Meta Conversion.

**2. PMax: deterioramento rapido che richiede intervento immediato**

In una sola settimana, PMax passa da un CPL di €18,95 a €22,27 (+17,5%) e da 269 a 229 lead (-14,9%). La conversion rate scende sotto il 5%. Questo pattern è tipico di un algoritmo PMax che ha esaurito il set di segnali di conversione aggiornati o che sta espandendo la distribuzione verso segmenti a bassa intenzione. Senza intervento, il trend rischia di aggravarsi ulteriormente nella W20.

**3. Awareness in saturazione: CTR e conversion rate in calo simultaneo**

Awareness mostra un pattern classico di saturazione creativa: il CTR scende a 1,81% (sotto benchmark 1,5-2,5% ma ancora dentro range) e il conversion rate cade al 4,22%, sotto soglia critica del 5%. Con impressioni in aumento (+19.730 vs W18) e meno lead generati, l'audience cold sta rispondendo peggio agli stessi messaggi. Il problema non è la reach, è la rilevanza creativa.

---

## 4. RACCOMANDAZIONI OPERATIVE

### Awareness_IT_Bootcamp_Q2 🔴

1. **Rotazione creativa immediata**: introdurre almeno 2 nuove varianti di annuncio (format video 15" con testimonial studenti + static con outcome salariale concreto) entro la W20. Target: riportare CTR sopra 1,9% e conversion rate sopra 5% entro 2 settimane.
2. **Segmentazione audience**: testare una sottocampagna separata con targeting 25-35 IT professionals in transizione di carriera (escludendo 18-24 studenti) per identificare il segmento più reattivo. Orizzonte: 2 settimane con budget test €800-1.000.
3. **Revisione landing page per traffico cold**: il conversion rate al 4,22% su traffico awareness è un segnale di attrito alla landing. Allinearsi con il team CRO per verificare la variante di LP dedicata al cold traffic. Obiettivo: +1 pt conversion rate entro 3 settimane.

### Search_Generic_Bootcamp 🔴

1. **Audit keyword e Search Terms Report**: analizzare i search term della W19 per identificare keyword con CTR in calo o CPC in aumento. Escludere termini non pertinenti che drenano budget. Azione entro 48 ore, a cura dell'agenzia.
2. **Refresh degli annunci RSA**: se le headline attuali sono in rotazione da più di 4 settimane, sostituire le varianti con performance inferiore. Inserire nuove headline che enfatizzino placement rate e stipendio post-corso. Obiettivo: riportare CPL sotto €19 entro W21.
3. **Bid strategy check**: verificare con l'agenzia se la bid strategy (presumibilmente Target CPA o Maximize Conversions) ha subito un aggiustamento automatico. Se il CPA target è troppo aggressivo, alzarlo temporaneamente del 10% per recuperare volume. Orizzonte: W20.

### PerformanceMax_Bootcamp 🔴

1. **Aggiornamento segnali di audience**: caricare una lista aggiornata di buyer/iscritti degli ultimi 30 giorni come segnale di audience. L'algoritmo PMax perde efficacia quando i segnali di conversione sono datati. Azione entro W20, critica.
2. **Revisione asset group**: verificare che tutti gli asset (titoli, descrizioni, immagini, video) siano classificati "Good" o "Best" in Google Ads. Sostituire eventuali asset "Low" con nuove varianti. Obiettivo: riportare CPL sotto €20 e conversion rate sopra 5% entro W21.
3. **Valutare riduzione budget temporanea**: se dopo le azioni sopra il CPL non mostra miglioramento in W20, ridurre il budget del -20% (da €5.100 a €4.080) e riallocare su Meta Conversion. L'algoritmo PMax necessita di tempo per riottimizzarsi; bruciare budget in fase di deterioramento è controproducente.

### Note di scala per i top performer

**Conversion Meta ✅**: incremento budget del +15-20% (€6.200 → €7.100-7.400) consigliato a partire da W20, con monitoraggio CPL giornaliero. Il lookalike 1% buyer ha ancora margine prima di saturarsi; se il CPL rimane sotto €15,50 dopo l'incremento, valutare un ulteriore step a W21.

**Retargeting Meta ✅**: il volume è strutturalmente limitato dall'ampiezza del pool di traffico. Non scalare il budget: l'efficienza dipende dalla qualità del traffico upper-funnel. Invece, ampliare la finestra di retargeting da 14 a 21-30 giorni per aumentare il pool disponibile, con attenzione alla frequenza.

---

## 5. ALERT & ATTENZIONE

🔴 **PerformanceMax_Bootcamp — CPL €22,27**: supera il benchmark target (€18-25, ma +17,5% W-on-W in traiettoria ascendente). Combinato con conversion rate al 4,68% sotto soglia critica del 5%, richiede intervento entro la settimana. Escalation consigliata al Marketing Manager se non si interviene entro W20.

🔴 **Search_Generic_Bootcamp — CPL €21,43**: +15,1% W-on-W. Ancora dentro range benchmark (€18-25) ma in avvicinamento alla soglia superiore con trend negativo. Monitoraggio quotidiano da attivare.

🔴 **Awareness_IT_Bootcamp_Q2 — Conversion rate 4,22%**: sotto soglia critica del 5%. Combinato con CPL a €18,52 che supera il benchmark massimo della categoria (€18), la campagna richiede intervento creativo urgente.

🟡 **PerformanceMax_Bootcamp — Conversion rate 4,68%**: sotto benchmark critico del 5%. Da monitorare insieme al CPL; se entrambi non migliorano in W20, procedere con riduzione budget e riallocazione.

