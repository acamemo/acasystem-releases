# Acasystem

Acasystem è l'interfaccia di MeMo Srl per Home Assistant. Questa app installa sul mini PC il server di Acasystem; si usa dai client **Acasystem** per Windows e Android oppure dal browser sulla stessa rete locale.

## Come si usa

1. Con HAOS già installato sul mini PC, installa e avvia questa app. La release 0.9.33 comprende uno script di bootstrap per la console host di HAOS 18.4 e le relative istruzioni; non installa HAOS sul disco.
2. Sul tablet o sul PC apri il nuovo client Acasystem e scrivi l'indirizzo IP del mini PC, porta 3002. In alternativa apri `http://IP:3002/` nel browser.
3. Se la casa è nuova, crea il primo proprietario dalla webapp ACA, accedi e completa il nome della casa. Per una casa esistente usa l'account Home Assistant; la registrazione iniziale non viene ripetuta.
4. In **Sistema → QR Code** mostra il QR di collegamento per un altro dispositivo. Android può scansionarlo dal client; su iPhone o senza app si apre il browser. Il QR contiene soltanto l'indirizzo della centrale: l'accesso rimane necessario.

Gli inviti **Collega account** e **Importa layout** sono separati dal QR di collegamento: il primo collega la stessa casa/account, il secondo copia il layout. Durano cinque minuti e sono monouso.

La versione 0.9.33 è stata verificata su banco Windows e HA Container; installazione HAOS su mini PC fisico, scanner Android e Safari/iPhone fisici restano da collaudare.

## Dettagli

- **Porta:** 3002 sulla rete locale. Non serve aprirla verso Internet.
- **Dati:** layout, profili e Casa 3D sono nella cartella dell'app ed entrano nei backup di Home Assistant (backup a freddo).
- **Home Assistant:** l'app lo raggiunge sulla rete interna di HA OS e legge da sola la porta.
- **Aggiornamenti:** quando esce una versione nuova, Home Assistant la mostra tra gli aggiornamenti.
- **Rete:** il collegamento IP/QR è locale; non abilita l'accesso remoto da Internet.

## Licenza

GPL-3.0. I sorgenti di ogni versione sono allegati alla release corrispondente in <https://github.com/acamemo/acasystem-releases/releases>.
