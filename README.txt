DELMET — Showroom AR "POSEIDON 3x2"
=====================================

Struttura della cartella
-------------------------
index.html          → la pagina pubblica AR (quella da testare da smartphone)
assets/              → qui va messo il modello 3D esportato (poseidon.glb + poseidon.usdz)
exporter/index.html  → lo strumento per esportare il modello dal vostro Showroom


PASSO 1 — Esportare il modello 3D
-----------------------------------
1. Aprite nel browser (Chrome, su computer):
   exporter/index.html?export=1
2. In alto a sinistra compare un pannello con un bottone per ogni impianto.
3. Cliccate "POSEIDON 3x2" → il browser scarica "poseidon.glb"
4. Spostate il file scaricato dentro la cartella "assets/" di questo pacchetto,
   così: assets/poseidon.glb

Nota: questo passaggio va rifatto solo se in futuro modificate il modello 3D
della Poseidon nel Showroom (es. colori, dettagli). Il file .glb resta valido
finché il modello non cambia.


PASSO 2 (opzionale ma consigliato) — Versione per iPhone
-----------------------------------------------------------
Apple non legge i file .glb: su iPhone/iPad serve un file .usdz.
Per ottenerlo dal poseidon.glb:
  - su Mac: aprite il file con "Reality Converter" (gratuito, Apple) ed esportate in .usdz
  - oppure: usate un convertitore online glb → usdz (es. https://products.aspose.app/3d/conversion/glb-to-usdz)
Mettete il risultato in: assets/poseidon.usdz
(Se questo file manca, su iPhone l'AR semplicemente non parte; su Android funziona comunque.)


PASSO 3 — Pubblicare online
------------------------------
Caricate TUTTA questa cartella (index.html + assets/) su un hosting con HTTPS.
L'AR da smartphone richiede una connessione sicura (https://), non funziona da file locali o da http semplice.

Opzioni rapide per un primo test, gratuite e senza configurazione:
  - https://app.netlify.com/drop  → trascinate la cartella, ottenete subito un link pubblico
  - Vercel, GitHub Pages, o una sottocartella del sito Delmet (es. delmet.it/ar/poseidon/)

IMPORTANTE: non è necessario (anzi, meglio evitare) pubblicare la cartella "exporter/"
sull'hosting definitivo — è uno strumento di lavoro interno, non serve ai clienti.
Per i test potete anche caricarla, ma per la versione finale destinata ai clienti
basta pubblicare solo: index.html + assets/


PASSO 4 — Provarla
---------------------
Aprite il link pubblico da smartphone (Android o iPhone), toccate
"Visualizza nella tua officina": la fotocamera si apre e potete
posizionare la Poseidon sul pavimento in scala reale, ruotarla e
guardarla da tutti i lati.


Estendere ad altri impianti
------------------------------
Lo stesso "exporter/index.html?export=1" funziona per QUALSIASI impianto del
catalogo Showroom (TGL, ELPOL CUBE, OYSTER, TP 250, SCRUBBER, ecc.): basta
cliccare il bottone corrispondente ed esportare, poi duplicare index.html
cambiando il nome del file .glb caricato.
