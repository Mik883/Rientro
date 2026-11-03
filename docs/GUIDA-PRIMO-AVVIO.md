[Italiano](GUIDA-PRIMO-AVVIO.md) · [English](en/GUIDE.md)

# Primo avvio

1. Installa il setup Windows oppure estrai completamente il portable. Avvia Rientro.
2. In Connettori scegli Home Assistant (URL locale e token) oppure integrazioni
   dirette. Configura router e dispositivi secondo la matrice di compatibilità.
3. Associa esplicitamente il telefono rilevato alla persona. Usa il MAC Wi-Fi
   effettivo della rete domestica, anche quando il telefono usa un MAC privato.
4. Configura cancello, allarme e/o serratura. Verifica prima le letture. Scegli
   azioni e attese in Rientro. Salvataggio e ricerca non inviano comandi.
5. In Impostazioni abilita il collegamento mobile HTTPS e l'accesso LAN. Per
   Android configura il proxy LAN previsto dalla guida tecnica del pacchetto.
6. Per collegarti da fuori installa Tailscale su PC e telefono con accessi
   autorizzati alla stessa rete Tailscale; configura Tailscale Serve HTTPS verso
   il servizio locale previsto dalla guida MOBILE.md. Non aprire porte sul router
   e non pubblicare il servizio con Tailscale Funnel.
7. Genera il codice di associazione dal programma: è un codice del telefono,
   non una licenza commerciale. Nell'app inserisci il tuo URL HTTPS e il codice.
8. Per iPhone/iPad apri quell'URL in Safari, Condividi → Aggiungi alla schermata
   Home. HTTPS deve essere attendibile. Per notifiche web serve un dispositivo
   compatibile e il consenso dall'app salvata nella schermata Home; non basta
   distribuire lo ZIP statico su GitHub. Il PC deve essere acceso e raggiungibile.
9. Concedi il ruolo amministratore solo ai telefoni che possono configurare la
   casa; gli altri utenti confermano soltanto le richieste autorizzate.
10. Prova prima notifiche e presenza. Prova i comandi fisici solo sorvegliando
    l'impianto. Una richiesta di rientro richiede la conferma monouso e presenza
    domestica verificata; essere raggiungibili da remoto non autorizza l'apertura.

Tailscale ha termini e limiti propri; Rientro non include un servizio VPN o VPS.
