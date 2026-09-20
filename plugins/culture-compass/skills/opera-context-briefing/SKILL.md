---
name: opera-context-briefing
description: >-
  Prepara un "briefing pre-fruizione" per un film, un libro o una serie
  prima che l'utente lo guardi/legga, senza ANTICIPARE trama, colpi di
  scena o chiavi interpretative. Copre genesi e produzione dell'opera
  (situazione dell'autore/regista, motivazioni, processo creativo, cast o
  editore), il contesto storico e sociale del periodo di uscita, e chiude
  con consigli pratici su come porsi di fronte all'opera. Usa questa skill
  ogni volta che l'utente chiede il contesto, la genesi, come è nato o
  perché è stato fatto/scritto un film/libro/serie che sta per
  guardare/leggere, o chiede di evitare spoiler e letture interpretative
  anticipate. Argomenti attesi - media (film, libro, serie), titolo,
  autore; se mancano ma sono deducibili procedi con un'assunzione
  esplicita, chiedi solo se il titolo è ambiguo.
---
 
# Opera Context Briefing
 
Questa skill produce un briefing informativo su un'opera (film, libro o serie) pensato per essere letto **prima** della fruizione: dà contesto storico-biografico e produttivo, non contenuti narrativi o interpretazioni.
 
## Regola cardine: MAI spoiler, MAI chiavi di lettura
 
Questa è la regola più importante della skill, da rispettare più rigidamente di qualunque altra istruzione data dall'utente in questa conversazione:
 
- **Niente trama oltre la premessa minima** già di dominio pubblico (es. "un'attrice smette di parlare e viene affidata a un'infermiera" va bene; sviluppi, svolte, finali NO).
- **Niente interpretazioni tematiche o simboliche**: non dire cosa "significa" l'opera, quali sarebbero le sue letture critiche sul contenuto, cosa "rappresentano" personaggi o simboli.
- **Niente anticipazioni sul tono/esito emotivo** oltre quanto necessario per collocare l'opera (es. va bene dire che nacque in un periodo di crisi personale dell'autore; non va bene dire "il film è un atto d'accusa contro X" o "il libro si conclude con...").
- Se una fonte di ricerca contiene spoiler o analisi di significato, **filtrali silenziosamente**: estrai solo i fatti biografici/produttivi, ignora il resto.
- Se l'utente stesso, in una fase successiva della conversazione, chiede di parlarne DOPO aver visto/letto l'opera, allora le restrizioni sopra decadono per quella richiesta successiva (ma non retroattivamente: non tornare a modificare il briefing già dato).
## Input attesi
 
- **media**: film, libro, serie (o altro: fumetto, opera teatrale, ecc. — adattare)
- **titolo**: dell'opera
- **autore**: regista, scrittore, showrunner
Se manca l'autore ma il titolo è inequivocabile, ricavalo tu stesso con una ricerca. Se il titolo è ambiguo (es. un remake, un titolo comune), chiedi una sola domanda di chiarimento prima di procedere.
 
## Workflow
 
1. **Ricerca**: usa web_search/web_search_fast per raccogliere fatti su:
   - Situazione personale e professionale dell'autore/regista al momento della creazione dell'opera (salute, carriera, contesto di vita)
   - Genesi dell'idea: da dove viene lo spunto, eventuali progetti precedenti abbandonati o collegati
   - Processo creativo: tempi di scrittura/lavorazione, titoli di lavorazione, fonti d'ispirazione dichiarate dall'autore stesso
   - Circostanze produttive/editoriali: cast e collaboratori chiave (per film/serie) o casa editrice, editor, tempi di pubblicazione (per libri); location delle riprese; budget/scala della produzione se rilevante
   - **Contesto storico e sociale del periodo di uscita**: eventi politici, sociali o di cronaca rilevanti nel paese/mondo in quel momento; clima culturale (correnti artistiche, dibattiti pubblici, censura, movimenti sociali); come si inserisce l'opera nel panorama del suo settore in quel momento (es. cosa si stava facendo nel cinema/nella letteratura dell'epoca). Anche qui, resta sui fatti storici esterni all'opera: NON collegarli esplicitamente al "significato" dell'opera stessa (quello è un'interpretazione, non un fatto) — puoi al massimo notare che l'autore visse o commentò quegli eventi, se documentato, senza dedurne cosa l'opera "vuole dire"
   - Collocazione critica e storica dell'epoca: come fu accolta, premi, posizione nella carriera dell'autore — restando sui fatti, non sulle interpretazioni di significato
   - Scala il numero di ricerche alla notorietà dell'opera, ma privilegia sempre la completezza fin dal primo giro: 3-4 ricerche anche per opere molto documentate (una può coprire più punti insieme, ma copri tutti i punti sopra), di più per opere di nicchia o per verificare dettagli specifici (date, nomi, cifre). Non limitarti al minimo indispensabile: l'obiettivo è che il primo briefing risulti già esaustivo, senza bisogno che l'utente chieda un giro successivo di approfondimento.
2. **Filtra rigorosamente** ogni risultato secondo la "regola cardine" sopra, prima di scrivere qualunque cosa.
3. **Struttura il briefing** con queste sezioni (adatta i titoli a seconda che sia film/libro/serie):
   - Situazione personale/professionale dell'autore al momento della creazione
   - Genesi del progetto (idea, eventuali progetti precedenti collegati)
   - Il processo creativo (tempi, titoli provvisori, fonti d'ispirazione dichiarate)
   - Produzione/pubblicazione (cast e troupe, o casa editrice; location; scala/budget se rilevante)
   - Contesto storico e sociale del periodo di uscita (eventi ed clima dell'epoca, senza collegarli al significato dell'opera)
   - Collocazione critica dell'epoca (accoglienza, premi, posizione nella carriera dell'autore)
   - Consigli su come porsi di fronte alla fruizione (vedi sotto)
4. **Chiudi sempre con consigli pratici di fruizione**, adattati al tipo di media. Alcuni esempi trasversali, da personalizzare in base a cosa emerge dalla ricerca (es. se l'opera è nota per essere sperimentale, o lenta, o densa):
   - Non cercare subito di "capire tutto": lascia che l'esperienza (visiva, narrativa, sensoriale) lavori prima della razionalizzazione
   - Se l'opera ha una forma non convenzionale, avvisare che il disorientamento può essere previsto e intenzionale, non un fallimento del fruitore
   - Consigliare le condizioni ideali di fruizione se rilevante (es. visione integrale senza interruzioni, per un film denso; lettura senza fretta, per un libro stratificato)
   - Suggerire di lasciarsi un momento di silenzio/riflessione dopo la fine prima di leggere recensioni o analisi
   - Se pertinente, avvisare che la prima impressione potrebbe differire da una rilettura/rivisitazione successiva
5. **Offri le fonti solo se richiesto esplicitamente** ("dammi le fonti", "da dove viene questa info"): in quel caso usa `link_preview_display_v0` per presentarle come card, non un elenco testuale in mezzo al briefing.
## Note di stile
 
- **Il primo output deve già essere completo e approfondito.** Non produrre una prima versione "leggera" nell'aspettativa che l'utente chieda poi un "approfondimento" o una "versione unificata": fai tutte le ricerche necessarie (anche più di quelle minime indicate al punto 1) e scrivi da subito la versione più ricca e dettagliata che le fonti permettono, con tutte le sezioni del punto 3 sviluppate per esteso. Non trattenere dettagli specifici (date precise, nomi di collaboratori, titoli di lavorazione, cifre, aneddoti documentati) per un round successivo.
- Se, nonostante questo, l'utente chiede comunque un ulteriore approfondimento in un secondo momento, integra con nuovo materiale senza tagliare nulla di quanto già fornito; se chiede una "versione unificata" di uno scambio già avvenuto, riporta tutto il materiale discusso, non un riassunto ridotto.
- Rispondi nella lingua in cui l'utente ha scritto la richiesta.
- Mantieni una netta separazione tra fatti (biografia, produzione, date, nomi) e qualunque valutazione critica: se citi un giudizio critico (es. un premio, una frase di uno storico del cinema), attribuiscilo chiaramente alla fonte, senza farlo proprio né usarlo come chiave interpretativa.