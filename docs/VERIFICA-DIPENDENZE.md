[Italiano](VERIFICA-DIPENDENZE.md) · [English](en/GUIDE.md)

# Verifica tecnica delle dipendenze — 3 novembre 2026

Inventariati 61 metadati di distribuzione Python nel runtime effettivo,
69 file di licenza/avvisi raccolti e 65 binari runtime elencati.
Metadati senza campo licenza completo: clr_loader, colorama, pybticino; consultati i testi
inclusi in dist-info anziché dedurre l'assenza di licenza dal campo vuoto.
Nel runtime della nuova release è stato conservato solo il metadato cryptography
corrispondente al modulo importato (50.0.2), eliminando la precedente duplicazione.

Componenti MPL: pywebpush, py-vapid, certifi. Sorgenti e avvisi inclusi nel runtime
e nel separato archivio Licenze-terze-parti/Sorgenti-MPL-2.0.zip, senza restrizioni
proprietarie. Mozilla documenta la combinazione MPL con componenti proprietari:
https://www.mozilla.org/en-US/MPL/2.0/FAQ/

Python mantiene PSF e licenze incorporate: https://docs.python.org/3/license.html
Lucide e Aegis mantengono avvisi upstream. AndroidX e dipendenze sono verificate
dal grafo Gradle risolto; licenze incluse negli asset dell'APK e nel fascicolo.
Il bootstrap Microsoft WebView2 mantiene le condizioni Microsoft ed è separato
dal codice originale. Tailscale non è redistribuito come parte del programma.

Nessun obbligo di canone per copia rilevato nei testi delle librerie esaminate.
L'inventario non autorizza uso di marchi, servizi cloud o API dei produttori e
non è una certificazione legale di ogni binario o contratto hardware. Per queste
parti valgono condizioni ufficiali proprie e requisiti della matrice connettori.
