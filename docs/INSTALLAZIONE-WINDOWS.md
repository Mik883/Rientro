[Italiano](INSTALLAZIONE-WINDOWS.md) · [English](en/GUIDE.md)

# Installazione Windows

Richiesti Windows 10/11 x64, collegamento alla rete domestica e Microsoft Edge WebView2 Runtime.

## Setup
1. Scarica il setup dalla sezione Releases ufficiale e, se desideri, confrontane il SHA-256.
2. Avvia l'installer e leggi la licenza. Gli eseguibili non sono firmati con Authenticode:
   verifica provenienza e impronta prima di decidere se procedere a un eventuale avviso Windows.
3. Installa WebView2 se manca; segui le indicazioni/prerequisiti del pacchetto.
4. Apri Rientro e completa [la configurazione](CONFIGURAZIONE.md).

## Portable
1. Scarica lo ZIP e usa **Estrai tutto** in una cartella scrivibile.
2. Avvia `Rientro.exe` dalla cartella estratta. Non avviarlo dentro lo ZIP.
3. Il profilo utente pubblico è `%USERPROFILE%/RientroData/Public`:
   “portable” non significa che tutte le credenziali siano trasferibili su un altro PC.

## Esecuzione e riavvio
Il PC deve rimanere acceso, collegato e con il servizio Rientro avviato; la sospensione
interrompe il funzionamento. La finestra di configurazione non deve necessariamente
essere in primo piano. Verifica l'avvio effettivo dopo un riavvio prima di affidarti al flusso.
Non presumere che un'installazione nuova erediti l'avvio automatico di un altro impianto.

## Aggiornamenti
Conserva una copia protetta del profilo prima di un aggiornamento e chiudi Rientro.
Usa l'installer dello stesso canale oppure sostituisci l'intera cartella applicativa
del portable, preservando il profilo. Non cancellare i dati per un normale aggiornamento.
Le credenziali protette da Windows DPAPI restano legate al contesto Windows:
copiare il profilo su un PC diverso non garantisce il ripristino degli accessi.
