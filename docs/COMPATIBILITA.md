[Italiano](COMPATIBILITA.md) · [English](en/GUIDE.md)

# Compatibilità e stato delle prove

La selezione di una famiglia non certifica ogni modello. Questi pacchetti includono
i nuovi percorsi software; nessun nuovo connettore è dichiarato collaudato su hardware
fisico solo perché compare nel menu.

| Componente | Percorso | Stato |
| --- | --- | --- |
| Windows x64 | Setup e portable 2.0.2 | Compilati; test software e interfaccia verificati |
| Android | APK firmata 2.0.2 | Build, lint e firma verificati; installazione fisica da verificare |
| Home Assistant | Entità e presenza device_tracker | Opzionale; prove software, flusso della casa di sviluppo già provato |
| Tenda MX | Lista client autenticata | Percorso esistente conservato; verificare modello/firmware |
| FRITZ!Box | TR-064 Hosts | Implementato e verificato con risposte simulate; prova del modello reale necessaria |
| OpenWrt | ubus/hostapd | Implementato e verificato con risposte simulate; autorizzazioni e tutti gli AP necessari |
| WINDTRE / Vodafone / Sky / TIM | Modello + TR-064 o ubus effettivo | Famiglie configurabili; modelli non forniti e compatibilità non dichiarata |
| ARP | Diagnostica | Non abilita il rientro operativo |
| BTicino / Ajax | Cloud diretto non ufficiale | Percorsi esistenti; account, 2FA e firmware da collaudare |
| Shelly contatto pulito | Gen1 / RPC su modelli riconosciuti | Lettura e impulso software verificati; cablaggio e modello reali da collaudare |
| Sonoff contatto pulito | Gateway iHost/eWeLink CUBE API v2 + inching OFF | Implementato con prove simulate; gateway e dispositivo compatibili necessari |
| Nuki | Bridge HTTP compatibile | Implementato con prove simulate; non supporto generico a tutte le Nuki |
| Tedee | Bridge API locale | Implementato con prove simulate; Internet richiesto dal Bridge per certificati |
| SwitchBot | Lock/Lock Pro BLE cifrato | Implementato con prove simulate; chiavi e Bluetooth necessari; altre generazioni non dichiarate |
| iPhone / iPad | Webapp su HTTPS attendibile | Dispositivi e notifiche reali da collaudare |
| macOS | Nessun binario incluso | Compilazione e prova su Mac separate |

Per un relè senza sensore non è disponibile la posizione fisica del cancello.
Un errore di lettura non viene trasformato in un'assenza certa dei telefoni.
Le API cloud non ufficiali possono cambiare. Segnala modello e firmware senza
allegare credenziali; le conferme fisiche saranno documentate con versione e data.
