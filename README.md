# SOStituto

App web per la gestione delle sostituzioni dei docenti, pensata per il lavoro quotidiano del responsabile di plesso di una scuola italiana. Un solo file HTML, nessuna installazione, funziona anche offline una volta caricata; i dati restano sul dispositivo salvo che si attivi la condivisione.

**Versione corrente:** vedi la costante `VERSIONE` in cima a `index.html` (si legge anche in alto nell'app, sotto il titolo).

## Cosa fa

A partire dall'orario della scuola (importato da Excel) e dalle assenze dei docenti segnalate giorno per giorno, propone automaticamente chi sostituisce chi, seguendo una gerarchia di criteri conforme alla circolare sulle sostituzioni e configurabile dal dirigente. Tiene il registro di ogni giornata, i debiti da permesso breve, le uscite didattiche, il potenziamento e i vincoli particolari (sostegni non derogabili, incompatibilità). Può essere usata da un dispositivo solo o condivisa fra più persone (responsabile di plesso, vicepreside) tramite un foglio Google.

## Schede principali

**Sostituzioni** — la schermata del giorno. Si segnano gli assenti (anche solo per alcune ore), si genera il prospetto, si corregge a mano dove serve. Il prospetto resta visibile finché non si cambia giorno o lo si elimina esplicitamente — chiudere l'app non lo perde.

**Registro** — l'archivio di tutte le giornate generate: sostituzioni, ore scoperte, ore coperte dal potenziamento, export in PDF e WhatsApp. Una singola sostituzione registrata per errore si può segnare come "non avvenuta" senza perdere la traccia storica del giorno.

**Orario** — consultazione dell'orario importato, docente per docente o classe per classe.

**Altro** — tutte le schede di configurazione e le funzioni accessorie, elencate sotto.

## Il motore delle sostituzioni

Per ogni ora scoperta, propone un sostituto seguendo la gerarchia della circolare (criteri a–h): privi di alunni per gita, recupero permessi brevi, sostegno della classe, flessibilità oraria, potenziamento, sostegno col proprio alunno assente, ora eccedente a pagamento, sostegno di altra classe. La **Configurazione criteri** permette di disattivare un criterio o cambiarne l'ordine, perché la circolare è soggetta a interpretazione del dirigente e non è detto valga identica in ogni scuola.

La scelta automatica si può sempre correggere a mano: la cella toccata prende la scelta manuale, e se questo "ruba" qualcuno già assegnato altrove, quella seconda cella ricade da sola sul prossimo candidato migliore — non resta mai vuota senza motivo.

## Assenze e permessi

**Assenze note** — si registrano in anticipo (anche per periodi lunghi, es. un congedo) e si caricano da sole nel giorno giusto. L'app riconosce dall'orario in quali giorni della settimana un docente è davvero in servizio in quella scuola, ed esclude gli altri: un'assenza plurigiornaliera non "suona" nei giorni in cui comunque non ci sarebbe.

**Permessi brevi e recuperi** — un'assenza breve può generare un debito da recuperare entro due mesi, con precedenza data a chi lo ha aperto quando viene scelto un sostituto. Non tutti i permessi brevi vanno recuperati: lo si indica caso per caso. Il **plafond annuo** mostra il consumato per ogni docente rispetto al proprio orario settimanale, con il dettaglio di ogni voce (apribile per correggerla).

## Potenziamento

Le ore di potenziamento si possono assegnare a una classe — a mano o in automatico, con il pulsante che riempie le ore scoperte rispettando chi le classi già conoscono e bilanciando il carico. Un'ora assegnata, se il curricolare è assente, copre la classe senza generare una sostituzione.

Un'ora di potenziamento può anche essere **sospesa** (il docente diventa indisponibile per un periodo) o **spostata** (stesso docente, altra ora, stesso periodo) per esigenze funzionali — entrambe tracciate con data di inizio/fine e motivo, revocabili in ogni momento.

## Sostegno

**Sostegni non derogabili** — segnala gli abbinamenti sostegno-classe che non vanno mai spostati (un alunno grave con assistenza continua).

**Gruppi di seconda lingua** — quando un sostegno copre un'ora di articolata (francese/spagnolo) e l'orario non specifica il gruppo, lo si indica qui — importabile da file o a mano — così il motore sa a quale gruppo appartiene.

**Incompatibilità** — un docente che non può mai fare supplenza in una data classe (tipicamente un parente stretto di un alunno). Esclusione assoluta, vale per le sostituzioni dirette e per il potenziamento, automatico o a mano.

## Uscite didattiche

Si registrano a mano, oppure si importano da un foglio Google aggiornato dalla funzione strumentale viaggi — con le classi e gli accompagnatori già nel formato giusto, verificati contro l'orario prima di essere accettati.

## Coperture

Vista settimanale di dove c'è una seconda presenza in aula (doppio sostegno, sostegno singolo, solo curricolare, nessuna riserva) e dove no — utile per programmare, non solo per l'emergenza del giorno. Include gli assistenti comunali all'autonomia (orario importato a parte, mai usati come sostituti) e si stampa in PDF A3, tutta la settimana su un foglio solo.

## Condivisione fra più dispositivi

Tramite un foglio Google e uno script collegato, più persone possono lavorare sugli stessi dati. Un conflitto (due invii basati su dati diversi) viene segnalato prima di sovrascrivere. Dopo ogni sincronizzazione si può condividere su WhatsApp un riepilogo leggibile di cosa è cambiato, nome per nome.

## Backup e sicurezza dei dati

Backup manuale completo in un file scaricabile. Prima di ogni Scarica dal foglio condiviso, l'app salva da sola un'istantanea dello stato precedente (le ultime tre), recuperabile con un tocco anche senza backup manuale aggiornato — e se il foglio scaricato risulta sospettosamente più povero di quanto si ha già, lo segnala invece di sovrascrivere alla cieca.

## Fine anno scolastico

Una scheda dedicata azzera in blocco i dati dell'anno concluso (registro, assenze, uscite, recuperi, potenziamento) mantenendo la configurazione dei criteri, il ruolo del dispositivo e le impostazioni di condivisione — con riepilogo di cosa verrà tolto prima di confermare.

## Note tecniche

- Un solo file `index.html`, autosufficiente; ospitabile gratuitamente su GitHub Pages.
- Dati salvati nel `localStorage` del browser; nessun server proprio, salvo lo script Google per la condivisione (facoltativa).
- L'orario si importa da un file Excel con un formato di intestazione flessibile (righe/colonne riconosciute per nome, non per posizione fissa).
- Font caricati online al primo avvio; il resto funziona offline.
