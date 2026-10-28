# SOStituto — registro delle versioni

Formato versione: `GG.MM.AAAA` + lettera (a, b, c… se più consegne nello stesso giorno) + numero progressivo delle consegne (`n. 90`).
Si legge in alto nell'app, sotto il titolo. Da qui in avanti si aggiorna a ogni consegna. La 16.10.2026c era la n. 89.

## Da qui in avanti (dettaglio certo)

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
