# FRANCE CREATOR V3.1 — Cut Optimizer

Add-on integrato per l'ottimizzazione delle tavole da 2,2 cm.

## Parametri fissi
- Pacchi: 401,5 cm · 450 cm · 504 cm
- Perdita lama prudenziale: 0,5 cm per ogni taglio
- Anche il rifilo finale dello scarto consuma 0,5 cm

## Archivio scarti
- De Martini: 185, 180, 170, 155, 150, 125, 110, 95 cm
- Leani: 187, 157, 142, 105, 103, 100, 95, 88 cm
- Slate&Marble: 172, 157, 142, 105, 103, 100, 95, 88 cm

## Logica operativa
- Confronto dei tre pacchi per ogni misura di taglio.
- Ricerca di 1..N tagli uguali + miglior scarto archivio.
- Proposta di combinazioni miste tra misure del progetto.
- Le combinazioni miste sono eseguite per lotti: prima una misura su tutte le tavole, residui accantonati, poi la misura successiva.
- OSB/Binder, legni sotto, travetti e piantoni sono esclusi dal motore tavole 2,2 cm.
- I pannelli assemblati possono essere ottimizzati come schema di lunghezza; il numero di tavole necessario dipende dallo sviluppo del pannello, perché la V3 non contiene una larghezza utile standard della tavola.
