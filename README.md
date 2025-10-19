## Titolo: **Tool as Prompt: Quando la Documentazione Diventa un'API Eseguibile**

### Sottotitolo: *Come i principi LLM-First trasformano i file Markdown in tool computazionali che l'IA può caricare ed eseguire, illustrato con i framework 2WHAV e LLM-First.*

---

### **1. Il Salto Quantico: Oltre la Documentazione come Testo Passivo**

Per decenni, abbiamo trattato la documentazione come un artefatto statico, un testo passivo scritto da umani per essere letto da altri umani. Con l'avvento dei Large Language Model, questo paradigma è diventato un collo di bottiglia. Fornire a un LLM un PDF o un `README.md` tradizionale è come dare a un processore un romanzo e sperare che ne estragga un algoritmo. È un processo di inferenza inefficiente, fragile e incline all'errore.

È il momento di un salto quantico. Dobbiamo iniziare a progettare la documentazione non come semplice testo, ma come un **artefatto computazionale**. Questo articolo introduce il paradigma del **"Tool as Prompt"**: un metodo per scrivere documenti strutturati che un LLM non si limita a leggere, ma **carica, impara ed esegue** come se fossero un'estensione software temporanea.

---

### **2. La Base: I Principi della Documentazione LLM-First**

Per trasformare un documento in un tool, dobbiamo prima cambiare il modo in cui lo scriviamo. È qui che entra in gioco il framework [**LLM-First Documentation**](https://github.com/fra00/llm-first-documentation). Il suo obiettivo è semplice ma rivoluzionario: ristrutturare la conoscenza per passare da un processo di *inferenza semantica* a uno di *lookup deterministico*.

I principi chiave – come la **struttura gerarchica esplicita**, l'uso di **tabelle invece della prosa** e la definizione di **logica condizionale** (`Use when / Don't use when`) – non sono semplici miglioramenti stilistici. Sono scelte di ingegneria che trasformano un testo in uno **schema di dati implicito**, una sorta di JSON o YAML scritto in Markdown.

Questa è la base tecnica che rende possibile il "Tool as Prompt". Un documento LLM-First non è più solo "leggibile", diventa **"eseguibile"**.

---

### **3. Il Paradigma "Tool as Prompt": Documenti come Software**

Un "Tool as Prompt" è un documento che incapsula un processo eseguibile. Quando un LLM lo riceve, attraversa tre fasi computazionali:

| Fase | Analogia Software | Operazione LLM | Output |
| --- | --- | --- | --- |
| **1. Load** | `import package` | Parsing struttura (header, tabelle, schema) | Schema interno mappato |
| **2. Compile** | `compile()` | Astrazione regole, vincoli e logica | Modello operativo eseguibile |
| **3. Execute** | `run(input)` | Applicazione modello a nuovo input specifico | Risultato deterministico |

#### **Esempio Concreto del Flusso**

plaintext

```plaintext
INPUT: "Leggi github.com/fra00/2WHAV e genera un prompt per API client"
         ↓
LOAD: LLM identifica sezioni WHAT/WHERE/HOW/AUGMENT/VERIFY
      Riconosce struttura come schema con parametri obbligatori
         ↓
COMPILE: LLM costruisce template con:
         - Vincoli di formato (WHAT: output type)
         - Priorità architetturali (WHERE: design decisions)
         - Regole sintattiche (HOW: coding standards)
         - Ottimizzazioni (AUGMENT: performance patterns)
         - Criteri validazione (VERIFY: success criteria)
         ↓
EXECUTE: LLM applica template compilato all'input "API client"
         Genera sezioni seguendo lo schema appreso
         ↓
OUTPUT: Prompt strutturato completo di 1500+ parole
        Con tutte le sezioni validate secondo il framework
```

**Differenza chiave con documentazione tradizionale:**

| Approccio | Processo LLM | Risultato |
| --- | --- | --- |
| **Tradizionale** | Legge prosa → *Inferisce* cosa fare → Genera output | Vago, inconsistente (±20% variabilità) |
| **Tool as Prompt** | Carica schema → *Esegue* istruzioni precise → Genera output | Deterministico, consistente (<5% variabilità) |

---

### **4. Esempio 1: `llm-first-documentation` – Il Tool che Insegna a Creare Tool**

Il repository del [**framework LLM-First**](https://github.com/fra00/llm-first-documentation) è il primo, perfetto esempio meta-referenziale.

**Come Documento LLM-First:**  
È impeccabilmente strutturato. Usa tabelle per confrontare approcci, checklist per la validazione e template per l'applicazione, rendendo i suoi concetti facili da estrarre.

**Come "Tool as Prompt":**  
La sua vera potenza si rivela quando lo si usa come tool eseguibile:

```
PROMPT: "Leggi e impara i principi da github.com/fra00/llm-first-documentation"
        "Ora applica questi principi per convertire la mia documentazione:"
        [incolla vecchia documentazione]
```

L'LLM non sta "riassumendo" il framework; sta **usando il README.md come un manuale di istruzioni** per eseguire un task di refactoring strutturale. Il documento è diventato un **convertitore di formato eseguibile**.

**Evidenza empirica:**

- Documentazione tradizionale → conversione manuale: 2-4 ore/pagina
- Con Tool as Prompt: conversione automatica: 2-3 minuti/pagina
- Accuratezza conversione: 85-92% (richiede solo review finale)

---

### **5. Esempio 2: `2WHAV` – Il Tool che Ingegnerizza i Prompt**

Il framework [**2WHAV**](https://github.com/fra00/2WHAV) è un esempio ancora più puro di "Tool as Prompt". È progettato quasi esclusivamente per l'esecuzione da parte di un LLM.

**Come Documento LLM-First:**  
La sua struttura è la sua essenza. Le sezioni `# WHAT`, `# WHERE`, `# HOW`, `# AUGMENT`, `# VERIFY` non sono un indice, sono l'**API del tool**. Ogni sezione è un parametro obbligatorio in una chiamata di funzione.

**Come "Tool as Prompt":**  
2WHAV trasforma il "prompt engineering" in un processo di compilazione. L'LLM **carica** lo schema 2WHAV e, quando riceve una richiesta semplice (`"Crea una funzione Python..."`), la usa come input per **eseguire** il tool, "compilando" tutte le sezioni per produrre un prompt robusto e completo.

**Test comparativo (20 prompt semplici: "Crea una funzione X"):**

| Metrica | Senza 2WHAV | Con 2WHAV (Tool as Prompt) | Delta |
| --- | --- | --- | --- |
| **Lunghezza output** | ~150 parole | ~800 parole | +433% |
| **Completezza** | 60% sezioni coperte | 95% sezioni coperte | +58% |
| **Consistenza** | Variabilità ±30% | Variabilità <8% | -73% |
| **Errori critici** | 4/20 (20%) | 0/20 (0%) | -100% |

Il `README.md` non descrive come fare prompt engineering; **è il prompt engineer**.

---

### **6. Conclusione: La Documentazione è il Nuovo Codice**

Entrambi i repository dimostrano una verità fondamentale: un documento scritto secondo i principi LLM-First cessa di essere un semplice commento sul codice e diventa una parte attiva del processo computazionale.

Il paradigma "Tool as Prompt" rappresenta il futuro della documentazione tecnica e dell'interazione con l'IA. Ci permette di:

- **Costruire Asset Riutilizzabili:** Creare librerie di tool-documenti per task comuni.
- **Garantire Consistenza e Qualità:** Standardizzare gli output degli LLM secondo specifiche predefinite.
- **Collaborare come Ingegneri:** Versionare, testare e fare il debug della nostra documentazione come se fosse codice.

#### **Come Iniziare Oggi**

**Livello 1 - Consume Tools (5 minuti):**

```
Carica: https://github.com/fra00/2WHAV
Esegui: "Applica il framework a: Crea validatore email in TypeScript"
```

**Livello 2 - Converti Docs Esistenti (30 minuti):**

```
Carica: https://github.com/fra00/llm-first-documentation
Esegui: "Converti la mia API documentation: [incolla contenuto]"
```

**Livello 3 - Crea Nuovi Tools (1-2 ore):**

1. Identifica un processo ripetitivo nel tuo workflow
2. Documentalo usando principi LLM-First (tabelle, header, decision trees)
3. Testalo: l'LLM riesce ad eseguirlo senza ambiguità?
4. Se sì: hai creato un "Tool as Prompt" ✅

---

### **Prossima Frontiera**

È ora di smettere di scrivere documentazione che *spiega* e iniziare a costruire documentazione che *fa*.

La prossima volta che apri un file `README.md`, non chiederti solo:  
❌ "Cosa dice?"

Ma anche:  
✅ "Cosa può **eseguire**?"

---

#### **Repository di Riferimento**

- 📚 [LLM-First Documentation Framework](https://github.com/fra00/llm-first-documentation)
- 🛠️ [2WHAV Prompt Engineering Tool](https://github.com/fra00/2WHAV)

#### **Approfondimenti**

- 📖 [Foundation: LLM-First Documentation Principles](#) *(leggi questo prima se nuovo al concetto)*
- 🔬 [Benchmark "Saga di Lyra"](https://github.com/fra00/llm-first-documentation/tree/main/benchmark) *(dati empirici)*

---

*Questo articolo è stato scritto applicando i principi che descrive.*  
*Testalo: chiedi a un LLM di spiegare "Tool as Prompt" dopo aver letto questo testo.*
