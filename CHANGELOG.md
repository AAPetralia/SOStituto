# SOStituto — registro delle versioni

Formato versione: `GG.MM.AAAA` + lettera (a, b, c… se più consegne nello stesso giorno) + numero progressivo delle consegne (`n. 90`).
Si legge in alto nell'app, sotto il titolo. Da qui in avanti si aggiorna a ogni consegna. La 16.10.2026c era la n. 89.

## Da qui in avanti (dettaglio certo)

### 05.11.2026a — n. 108
- **Ricevimento dei maestri di strumento musicale associato al docente.** In Altro → Cambio e aggiunta docente → «Docente senza orario del mattino» ogni docente ha ora i campi del ricevimento: giorno, ora (un numero come «6», un intervallo «3-4» oppure un orario scritto «12:05 - 13:05»), materia e classi. Sono i dati che finiscono nel PDF dei ricevimenti per la segreteria, che li legge da qui; sparisce l'elenco dei maestri nella schermata del PDF. Arima, Nardi, Organtini e Sette sono già precompilati (ricevimenti concordati), modificabili. I dati restano nell'orario e viaggiano con la condivisione e il backup.

### 04.11.2026d — n. 107
- **Gruppi di seconda lingua: l'elenco mostra tutti i sostegni con la lingua**, non solo quelli indicati a mano. Per ognuno: docente, lingua, giorno, ora, classe e origine («orario» se la cella lo dice già, «a mano» se l'hai indicato qui, con ✕). Ordine per giorno e ora. Con ⚠ le celle la cui classe non è in articolata di lingua in quell'ora secondo i docenti di francese/spagnolo (di solito un'ora sbagliata nell'orario importato).

### 04.11.2026c — n. 106
- PDF ricevimenti: Pucci Erika (supplente temporanea di Pacetti) compare con il nome della titolare, «Pacetti Elisa».

### 04.11.2026b — n. 105
- PDF ricevimenti: i docenti che non sono nell'elenco della scuola (es. un supplente nuovo) compaiono con il nome dell'orario «Cognome Nome» invece che in maiuscolo.

### 04.11.2026a — n. 104
- **Nuovo: «Ricevimenti per la segreteria (PDF)»** (Orario → pulsante sotto «Importa ricevimenti»). Genera il PDF «RICEVIMENTO GENITORI» nel formato della scuola: **A3 verticale, tutto in una pagina**, DOCENTE · MATERIA · CLASSE · GIORNO · ORARIO, ordine alfabetico, ore consecutive unite (es. 8:05 - 10:00).
- È **indipendente dalla webapp**: dalla webapp serve solo il file dei ricevimenti (già importato). Ore R e classi si leggono sempre dall'orario di SOStituto: se sposti o togli un'ora R, ristampi e il PDF esce aggiornato.
- Nome per esteso e materia sono quelli della cattedra 2026/27 (Allegato 3, già inseriti nel programma, compreso «Approfondimento»); i quattro maestri di strumento musicale (Arima, Nardi, Organtini, Sette) sono già inseriti con giorno e ora. Tutto correggibile in «Correzioni a mano» (anche orari delle ore e intestazione); salvato con i dati e nel backup.
- Le librerie PDF (jsPDF) si caricano al momento del download: serve internet.

### 03.11.2026d — n. 103
- **Uscita con delegazione: tolta del tutto l'esclusione dei docenti delle classi coinvolte.** Con la n. 102 era tornato disponibile solo il sostegno; ora vale anche per il **potenziamento assegnato** alla classe in delegazione: la classe resta a scuola con una parte degli alunni e con il suo curricolare, quindi non ha bisogno del potenziatore, che può essere usato per le sostituzioni come in un giorno normale. Cambia solo la delegazione («solo una parte della classe esce»); se la classe è tutta fuori sede resta com'era.

### 03.11.2026c — n. 102
- **Uscita con delegazione: il sostegno delle classi coinvolte torna disponibile come «sostegno spostato».** Prima i sostegni delle classi da cui parte una delegazione erano esclusi del tutto. Ma la classe resta a scuola con una parte degli alunni e con il suo curricolare, quindi il sostegno (che non accompagna) può essere spostato, come in un giorno normale (criterio H, via residuale, in fondo all'elenco). Restano esclusi nelle classi in delegazione i docenti non di sostegno (es. potenziamento assegnato alla classe).
- Caso: Clementi (sostegno 3A) per la 4ª ora di mercoledì 4/11, con la 3A in delegazione (ore 2-5): ora compare come «⚠ unico sostegno di 3A».

### 03.11.2026b — n. 101
- **«Perché manca un docente?»** Nell'elenco delle alternative di una cella (tocca la riga della sostituzione) in fondo c'è un menù con i docenti che NON compaiono fra le alternative: sceglierne uno mostra il motivo (incompatibile, assente o accompagnatore, già impegnato alla stessa ora, classe in uscita con delegazione, flag «non toccare», criterio disattivato, ora fuori servizio non attaccata al suo orario…).
- Caso di partenza (backup del 03/11): Clementi non proposta per la 4ª ora di mercoledì 4/11 perché la 3A è in uscita **con delegazione** (ore 2-5): il sostegno resta con gli alunni che non escono. Era il comportamento previsto, non un errore.

### 03.11.2026a — n. 100
- **Correzione: sostegno in un gruppo di seconda lingua mai proposto come «sostegno spostato».** Se un sostegno era in un'ora assegnata a un gruppo lingua (es. 3A·SP, 2B·FR — anche solo con l'assegnazione in «Gruppi di seconda lingua», che nella griglia dell'orario continua a mostrarsi come classe), il motore non lo considerava affatto: non compariva nemmeno in «mostra tutte» come ultima spiaggia. Ora vale come un sostegno in classe: «sostegno spostato da 3A» o «⚠ unico sostegno di 3A», con le stesse tutele (flag «non toccare», altri sostegni nella classe, curricolare assente in classe).
- Caso di partenza: Clementi (sostegno 3A) non proposta per la 4ª ora di mercoledì.

### 02.11.2026a — n. 99
- **Ricevimento (R) e supplenze a pagamento.** Il ricevimento mattutino c'è solo nella **1ª e 3ª settimana del mese** (giorni 1-7 e 15-21: la 1ª e la 3ª volta che quel giorno ricorre nel mese). In quelle settimane l'ora R **non viene più usata per le supplenze**, nemmeno a pagamento: il docente risulta non disponibile (nella griglia resta «R»). Nelle altre settimane il ricevimento non c'è e l'ora vale come una normale ora libera (buca, o «entra prima / esce dopo» se è ai margini del servizio), quindi può essere proposta a pagamento come le altre.
- Se scegli a mano un docente in ora di ricevimento (1ª/3ª settimana) resta l'avviso «è la sua ora di ricevimento».
- Verificato con prove su date di tutte e quattro le settimane (nov 2026).

### 31.10.2026a — n. 98
- **Aggiungi supplenza** (Altro → Cambio e aggiunta docente, nuova sezione): per un periodo (astensione, malattia lunga…) scegli il titolare, scrivi il supplente e le date «dal» e «fino al» (la fine si può lasciare vuota). Nel periodo il titolare esce dall'orario e il supplente **subentra in automatico con le sue classi**: ore in classe, sostegni intoccabili, gruppi lingua, potenziamento assegnato, Pno. Finito il periodo il titolare rientra com'era.
- L'orario segue la **data su cui lavori** (quella scelta in Sostituzioni): preparando il prospetto di domani si vede già lo stato di domani; le previsioni dei giorni futuri usano l'orario giusto per ciascun giorno.
- Le supplenze sono in elenco (programmata / in corso / conclusa): si cambiano le date o si tolgono, con ripristino immediato. Non si possono sovrapporre due supplenze sullo stesso titolare, ma una può dare il cambio a un'altra.
- Restano alla persona e **non** passano al supplente: storico del registro, recuperi, incompatibilità, assenze note, uscite. Se avevi segnato il titolare assente per quel periodo in Assenze note, vanno tolte.
- «Scarica l'orario» esporta sempre l'orario di base, con il titolare; dopo una reimportazione dell'orario le supplenze restano e si riattivano secondo le date.

### 29.10.2026a — n. 97
- **Correzione: sostegno assente nelle ore di gruppo lingua.** Le ore di un sostegno assente segnate come gruppo di seconda lingua (es. 3B·SP, 2B·FR) venivano ignorate: non comparivano né fra le sostituzioni né fra i «sostegni non sostituiti». Ora seguono la stessa regola delle altre ore di sostegno: con il flag sulla classe si sostituiscono (affiancamento), senza flag compaiono fra i non sostituiti (con l'indicazione del gruppo, es. «2ª B·FR») e si possono sostituire a mano.
- Caso di partenza: Pacetti assente di venerdì, con il flag su 3B, aveva la 1ª in 3B·SP scoperta senza avviso.

### 28.10.2026e — n. 96
- **Importa ricevimenti (R)** (scheda Orario, sotto «Scarica l'orario»): legge il file `.json` scaricato dalla webapp «Ricevimento Mestica» (o un orario Excel con le R) e aggiorna **solo** le ore di ricevimento: le ore libere segnate R diventano R, le R non più presenti nel file tornano libere; le ore già occupate in SOStituto non si toccano e vengono elencate come «non applicabili». Prima di applicare mostra il riepilogo e salva un'istantanea (Altro → Backup); se c'è un prospetto in corso lo ricalcola.
- Verificato con prove su JSON ed Excel (aggiunte, rimozioni, conflitti, docenti non trovati, reimportazione identica = nessuna modifica).

### 28.10.2026d — n. 95
- **Scarica l'orario** (scheda Orario, in fondo): file Excel nello stesso formato di quello che si importa (foglio «orario», con le modifiche fatte a mano già dentro), pronto da ripubblicare o da reimportare; verificato che reimportandolo si ritrovano tutte le celle identiche. Se ci sono modifiche a mano, un secondo foglio «modifiche» le elenca (data, docente, ora, prima → dopo).
- Non entrano nel file le sovrapposizioni temporanee dell'app (Pno, sospensioni e spostamenti del potenziamento, assegnazioni del potenziamento alle classi).

### 28.10.2026c — n. 94
- **Modifica dell'orario di un docente**, in Altro → Cambio e aggiunta docente (nuova sezione «Modifica l'orario di un docente»): scegli il docente, tocca l'ora nella griglia e la fai diventare *In una classe* (con la classe), *Libera*, *Ricevimento* o *Potenziamento* (con classe facoltativa). Vale subito per le sostituzioni, senza reimportare l'orario; se c'è un prospetto in corso viene rigenerato.
- Ogni modifica è registrata in elenco, con prima → dopo: si può **annullare**; dopo un nuovo import dell'orario (che le cancella) restano in elenco segnate «non applicata» e si possono **riapplicare**. Prima di ogni modifica l'app salva un'istantanea (Altro → Backup).
- Cambiando un'ora di potenziamento si aggiorna anche la classe assegnata; sui gruppi lingua/AIRC l'app chiede conferma.

### 28.10.2026b — n. 93
- **Banca ore.** Un'ora fatta a pagamento (buca o ora attaccata al servizio) si può segnare «a credito»: nel prospetto tocca la riga → «🏦 Segna a credito». L'ora non conta più tra quelle a pagamento (prospetto, stampa, registro, WhatsApp «BANCA ORE») e va nel credito del docente. Si può togliere dallo stesso punto.
- **Scheda Recuperi → «Banca ore»**: crediti per docente, con data, ora e classe. Sui debiti aperti di chi ha credito compare «Compensa 1 ora con la banca ore»: usa il credito più vecchio e chiude un'ora del debito; «Annulla uso» rimette tutto com'era.
- Il credito segue il prospetto: se rigenerando l'ora non è più a pagamento (altro sostituto, assenza tolta) il credito non ancora usato decade. Fa parte di backup, condivisione, reset d'anno e cambio nome docente.

### 28.10.2026a — n. 92
- **Ore attaccate al servizio, a pagamento.** Oltre alle buche, diventa candidato a pagamento anche chi ha libera l'ora subito prima del primo turno o subito dopo l'ultimo: entra prima / esce dopo. Nella graduatoria sta dopo le buche vere (stessa posizione del criterio «pagamento», sottordine successivo); si vede con «mostra tutte» o scegliendo a mano. Vale anche per le ore di sostegno assente da coprire a mano.
- La riga indica «⚠ pagamento · entra prima» / «esce dopo», con l'avviso «a pagamento, fuori orario»; l'ora entra nel conteggio delle ore a pagamento e nel testo WhatsApp (PAG).
- **Scelta manuale e pagamento:** se la scelta a mano cade su un'ora a pagamento (buca o ora attaccata) l'ora è ora conteggiata e segnata come tale; prima una scelta manuale non risultava mai a pagamento.

### 26.10.2026a — n. 91
- **Uscita con sola delegazione.** Un'uscita può essere segnata «solo una delegazione»: dalla classe esce solo una parte degli alunni, gli altri restano a scuola. In questo caso la classe **non è fuori sede**: l'accompagnatore si sostituisce anche nelle ore che avrebbe avuto in quella classe, e i docenti della classe (sostegno e potenziamento assegnato compresi) **non diventano una risorsa** per le altre classi, perché restano con gli alunni che non escono.
- Spunta nel form delle uscite a mano e, per le uscite del foglio viaggi, nuova colonna «Delegazione» (x) e casella nel modulo della FS: serve la nuova versione dello script del foglio (v5, «Nuova versione» del deployment). Senza aggiornare lo script tutto funziona come prima.
- Nelle uscite, nei prospetti (schermo, stampa) e nel diario delle modifiche la delegazione è indicata a parte.

### 16.10.2026d — n. 90
- Accanto alla versione compare il numero progressivo delle consegne («v 16.10.2026d · n. 90»).

(numerazione retroattiva: 16.10.2026c = n. 89, b = 88, a = 87)

### 16.10.2026c
- Un permesso breve non genera più due debiti di recupero (assenze note + pagina «Oggi»): resta quello delle assenze note; i doppioni già presenti vengono tolti da soli.

### 16.10.2026b
- Recuperi anche nelle ore attaccate al servizio (ora subito prima del primo turno / subito dopo l'ultimo), con precedenza a chi è già a scuola.
- Nel prospetto, stampa e WhatsApp compare l'avviso «entra prima / esce dopo».

### 16.10.2026a
- Flag «sostegno intoccabile»: blocca solo chi è già in quella classe (non può lasciarla), non chi la raggiunge da un'altra. Es.: Bidini (flag su 3ªB) ora è selezionabile per 3ªB quando è altrove.

### 15.10.2026a
- Docenti senza orario del mattino (es. musicale, servizio pomeridiano) aggiungibili da «Cambio e aggiunta docente»; utilizzabili come accompagnatori/riserve.
- Docenti di riserva e subentro per le uscite; link alle impostazioni di importazione dal modulo uscita.

## Ricostruzione dalle copie di sicurezza (indicativa)

Le voci sotto sono dedotte dai nomi delle copie `index_prima_*.html` rimaste nella cartella di lavoro: la funzione indicata è quella introdotta *dopo* la versione citata. Le versioni tra il 20/09 e il 06/10 e tra il 10/10 e il 14/10 non hanno copie.

| Dopo la versione | Modifica (dal nome della copia) |
|---|---|
| 20.09.2026l | (ultima del 20/09; esistono almeno le versioni a…l) |
| 06.10.2026 | «lascia» (cosa lascia scoperto chi viene spostato) |
| 07.10.2026 | tema |
| 07.10.2026b | controllo |
| 07.10.2026c | «in classe» |
| 07.10.2026d | cambio docente |
| 07.10.2026e | correzione dati non aggiornati («stale») |
| 09.10.2026a | uscite |
| 09.10.2026b | aggiornamento automatico |
| 09.10.2026c | riserve |
| 09.10.2026d | (intermedia) |
| 09.10.2026e | docenti extra |

Modulo viaggi (Apps Script, serie separata): ultima versione 15.10.2026d.
