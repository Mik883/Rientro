[Italiano](RISOLUZIONE-PROBLEMI.md) · [English](en/GUIDE.md)

# Risoluzione dei problemi

## Il telefono non raggiunge il servizio
Controlla che PC e Rientro siano attivi, che l'IP del PC sia corretto e che telefono
e PC possano comunicare. Reti ospiti e isolamento Wi-Fi possono impedirlo.
Verifica la regola firewall per la sola rete domestica; non disattivare tutto il firewall.
Fuori dalla rete serve il percorso Tailscale configurato, non il solo link LAN.

## Nessuna richiesta al rientro
Controlla MAC effettivo, sorgente di presenza configurata e autenticata, tempi di assenza e riconnessione,
stati dell'impianto e opzione “solo con allarme inserito”. Con ARP diagnostico il
rientro operativo non è abilitato. Consulta gli avvisi in Diagnostica.

## Nessuna notifica Android
Controlla autorizzazione notifiche, collegamento in background e risparmio energetico.
Dopo un arresto forzato riapri l'app. Prova la notifica prima di ripetere il rientro.

## La notifica apre il browser
Verifica di aver associato l'APK corretta e di usare la prova dall'app installata.
Evita una seconda sottoscrizione browser sullo stesso telefono se vuoi ricevere
soltanto le notifiche native. Indica nella segnalazione quale icona/app ha generato la notifica.

## Codice scaduto
Generane uno nuovo per il dispositivo corretto e usalo prima della scadenza.
Non pubblicare il codice per chiedere aiuto.

## Certificato non attendibile su Safari
Consulta [la guida webapp](WEBAPP-IOS.md). Il comportamento dell'APK Android non
dimostra che Safari si fidi dello stesso certificato.

## Stato incerto dopo un comando
Verifica fisicamente l'impianto e leggi il registro. Un timeout non dimostra che il
comando non sia arrivato. Non inviare sequenze ripetute per tentativi.

## Segnalare
Usa versione, sistema operativo, modello/firmware, passaggi e messaggio visualizzato.
Oscura nomi, IP pubblici, MAC, codici, token e altri dati personali negli allegati.
