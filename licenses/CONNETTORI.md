# Componenti dei connettori

- pybticino 1.9.0, MIT, https://github.com/k-the-hidden-hero/pybticino
  Installato come dipendenza, licenza nella distribuzione del pacchetto.
- Aegis for Ajax, tag v1.28.0, commit 08167ebfb761b2927370cafde7dde7b360084b12,
  https://github.com/bvis/aegis-hass, MIT. Licenza e attribuzione conservate in
  vendor/rientro_aegis/LICENSE e SOURCE.json. Include definizioni protobuf
  distribuite dall'autore per interoperabilita.
- grpcio, protobuf, aiohttp, websockets, cryptography e dipendenze mantengono
  le rispettive licenze nelle distribuzioni installate.

Adattamenti Aegis: estrazione del solo nucleo API; namespace riscritto con AST;
esclusione dei wrapper HA, panic, logout e gestione compagnie. Il disinserimento
Rientro costruisce gli stessi messaggi protobuf ma non replica i retry automatici
di comando del wrapper HA. TLS resta attivo; le letture non divulgano risposte
grezze, token o password all'interfaccia.

I prodotti e marchi appartengono ai rispettivi proprietari. Questi connettori non
sono ufficiali e non implicano approvazione dei produttori. Verificare condizioni,
licenze e avvertenze upstream prima di ridistribuzioni, soprattutto commerciali.

Connettori Bluetooth locali: PySwitchbot 3.1.0, bleak 3.0.2 e
bleak-retry-connector 4.7.1, distribuiti con licenza MIT. Le dipendenze
WinRT e i relativi metadati/licenze sono conservati nel runtime Windows.
L'inventario di release è tecnico e non sostituisce la revisione legale complessiva.
