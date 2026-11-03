[Italiano](WEBAPP-IOS.md) · [English](en/GUIDE.md)

# Webapp su iPhone e iPad

La webapp viene servita dal programma della tua abitazione. **Non esiste un link
pubblico unico che colleghi automaticamente tutte le case.** GitHub non esegue
il backend domestico; lo ZIP della webapp contiene soltanto l'interfaccia.

## Preparazione
Configura sul PC l'accesso mobile e un indirizzo HTTPS attendibile dal dispositivo.
Il certificato LAN usato dall'APK Android non viene automaticamente considerato
attendibile da Safari. Finché HTTPS non è correttamente configurato non promettiamo
installazione PWA o notifiche iOS pronte all'uso.

## Sul dispositivo
1. Collegati alla rete domestica, oppure al percorso Tailscale configurato per la tua casa.
2. Apri in Safari il link della tua installazione e usa il codice monouso per quel dispositivo.
3. Premi **Condividi → Aggiungi alla schermata Home → Aggiungi**.
4. Riapri dall'icona salvata e abilita le notifiche dove supportate.
5. Verifica la ricezione della notifica e il ritorno alla webapp prima di provare i comandi.

Il solo invio di link e codice a un dispositivo sui dati mobili non rende
raggiungibile un servizio che è disponibile soltanto sulla rete domestica.
L'accesso da fuori e la condizione di presenza che permette un rientro sono due
aspetti distinti: poter visualizzare la webapp non autorizza un'apertura da fuori casa.

**Stato:** percorso webapp previsto, prove fisiche iPhone/iPad e notifiche ancora
da completare per questa distribuzione. Non viene distribuita un'app iOS nativa.
