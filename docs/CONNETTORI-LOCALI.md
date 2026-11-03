[Italiano](CONNETTORI-LOCALI.md) · [English](en/GUIDE.md)

# Configurare i collegamenti di Rientro

Home Assistant è una scelta, non un requisito universale. La sorgente che rileva
il telefono e i connettori che azionano l'impianto si configurano separatamente.
Il programma Windows deve restare acceso e attivo nell'abitazione.

## 1. Scegli l'impianto

In **Connettori** scegli Home Assistant oppure integrazioni dirette. Con Home Assistant
inserisci URL locale e token e seleziona esplicitamente le entità. Il token è una
credenziale: non pubblicarlo nelle segnalazioni. L'entità della serratura deve essere
distinta da quella del cancello.

Per il cancello diretto puoi scegliere il videocitofono BTicino previsto dal
connettore esistente, un relè Shelly a contatto pulito supportato oppure un Sonoff
tramite iHost/eWeLink CUBE. Per Ajax resta il percorso account/2FA esistente.
BTicino e Ajax diretti dipendono dai rispettivi servizi cloud: diretti non significa
che funzionino senza Internet. Modello e firmware devono essere verificati.

## 2. Scegli come rilevare il ritorno

Apri **Impostazioni**, quindi la sezione rete/router. Scegli la sorgente:

| Sorgente | Cosa configurare |
| --- | --- |
| Tenda MX supportato | Accesso autenticato come nel percorso esistente |
| FRITZ!Box | IP locale, account autorizzato e TR-064 abilitato |
| OpenWrt | IP locale, credenziali ubus e lettura di tutti gli AP hostapd coinvolti |
| Home Assistant | Associazione esplicita di ogni telefono alla sua entità device_tracker |
| WINDTRE, Vodafone, Sky, TIM | Modello e firmware; solo se espongono realmente TR-064 o ubus compatibili |

Le famiglie degli operatori sono selezionabili, ma non rappresentano un supporto
universale ai loro modem. Non essendo ancora noti i modelli reali delle nuove case,
non è dichiarata la loro compatibilità. Se le API non esistono o la lettura fallisce,
il rientro rimane bloccato. ARP è diagnostico e non sostituisce una sorgente valida.

Premi la ricerca dei dispositivi online, identifica il telefono e associalo
esplicitamente alla persona. Puoi confrontare la lista prima e dopo una
riconnessione. Usa il MAC Wi-Fi effettivo di quella rete; se cambia il MAC privato,
aggiorna l'associazione. Non vengono scelti automaticamente dispositivi o persone.
Per Home Assistant ogni telefono registrato deve avere una propria associazione.

Una lettura incompleta di un access point o uno stato sconosciuto non significa
che tutti siano usciti. In una rete mesh devono essere coperti tutti gli AP.

## 3. Cancello a relè

Nel connettore cancello scegli Shelly RPC (Plus/Gen3/Pro supportati), Shelly Gen1
oppure Sonoff iHost. Inserisci l'indirizzo locale e le credenziali richieste,
cerca il dispositivo e seleziona esplicitamente il canale di apertura.
La ricerca legge i dispositivi: non aziona il relè.

Il modello deve offrire un vero contatto pulito: non basta che sia Shelly o Sonoff.
I modelli Shelly PM o non riconosciuti non sono accettati per questo comando.
Occorrono un ingresso di apertura dedicato e una durata impulso configurata.
Il comando di ritorno OFF deve avvenire sul dispositivo; per iHost viene verificata
la configurazione inching OFF prima del comando. Un Sonoff senza gateway iHost
compatibile non viene collegato automaticamente tramite questo percorso.

Non usare un ingresso passo-passo indistinto come se fosse sempre un'apertura.
Senza sensore, lo stato del relè non dimostra se il cancello sia aperto o chiuso:
Rientro mostra la disponibilità dell'impulso, non inventa la posizione fisica.

## 4. Serrature smart

| Percorso | Requisiti e limiti |
| --- | --- |
| Home Assistant | Entità lock scelta esplicitamente, diversa dal cancello |
| Nuki Bridge HTTP | Bridge e serratura compatibili, API locale abilitata e token autorizzato; non equivale a Nuki MQTT o a tutte le generazioni Nuki |
| Tedee Bridge | API locale abilitata e token; comandi in LAN, ma Internet necessario per il rinnovo periodico dei certificati del Bridge |
| SwitchBot BLE | Lock/Lock Pro supportata, Bluetooth Windows nel raggio della serratura e chiavi cifrate autorizzate; non tutte le generazioni SwitchBot |

Configura credenziali, avvia la ricerca e scegli la serratura. Non inviare le chiavi
Bluetooth o i token all'assistenza. Il salvataggio non sblocca la porta.
Il percorso SwitchBot non usa il cloud per il comando e non attiva tentativi
automatici di sblocco dopo un errore. L'apertura dello scrocco non è inclusa nel
normale sblocco locale dove il dispositivo distingue le due operazioni.

## 5. Telefono, tempi e prova

Imposta le soglie di assenza e riconnessione stabile, l'azione desiderata e la
condizione sull'allarme. Associa app Android o webapp dal codice della tua casa.
La sola presenza Wi-Fi non autorizza un'apertura: rimane la conferma autenticata
e monouso dal telefono. Il sistema non reinvia automaticamente un comando il cui
esito sia incerto. Le ricerche e i salvataggi non inviano aperture o disinserimenti.

I nuovi connettori hanno superato prove software con risposte simulate. I modelli
fisici vanno collaudati separatamente: inizia da letture e notifiche, poi segui
[il primo test](PRIMO-TEST.md). La gestione dei certificati HTTPS per Safari resta
necessaria per la webapp iPhone/iPad. GitHub distribuisce i file, non ospita la casa.
