[Italiano](CONFIGURAZIONE.md) · [English](en/GUIDE.md)

# Configurazione dell'abitazione

1. In **Connettori** scegli Home Assistant oppure integrazioni dirette.
2. Configura cancello, allarme e/o serratura scegliendo i dispositivi in modo esplicito.
3. In **Impostazioni** scegli la sorgente di presenza e associa il telefono alla persona.
4. Imposta tempi di assenza/riconnessione, azioni e condizione sull'allarme.
5. Abilita il collegamento mobile e associa app o webapp dal link/codice della casa.
6. Verifica prima gli stati e le notifiche, poi esegui il primo test controllato.

Home Assistant è opzionale: rilevamento presenza e comandi hanno requisiti distinti.
La configurazione guidata completa, inclusi router e connettori diretti, è nella
[guida ai collegamenti](CONNETTORI-LOCALI.md). Leggi anche la
[matrice di compatibilità](COMPATIBILITA.md).

La regola firewall LAN non apre porte Internet sul router. La webapp richiede
HTTPS attendibile, in particolare su iPhone/iPad. I salvataggi non azionano i dispositivi.
