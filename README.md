# FRANCE CREATOR V4.1

Revisione della V4.0 che mantiene il motore parametrico V4 ma ripristina il colpo d'occhio operativo della V3.3: il piano di taglio è organizzato per misura di pacco, con bordino verde, materiale, quantità da prelevare, sequenza dei tagli e sfrido.

## Regole principali
- Tavole: lunghezza + larghezza opzionale + spessore.
- Se tutte le tavole attive di uno spessore hanno la larghezza dichiarata, il conteggio è esatto e il piano indica quante tavole prelevare.
- Se almeno una larghezza attiva manca, per quello spessore il piano resta a pannelli: numero pannelli + TAGLIO + SVILUPPO, senza inventare il numero di tavole.
- Travetti: lunghezza + due lati della sezione obbligatori.
- Compatibilità delle sezioni verificata prima del piano.
- Kerf prudenziale: 0,5 cm per taglio.
- Rifilatura pannelli: 0,5 cm per pannello sullo sviluppo cumulativo.
- Nessuna sovrapproduzione volontaria: una misura esce dal problema quando il suo fabbisogno è esaurito.
- Gli scarti archivio possono essere combinati in più pezzi sullo stesso residuo; lo sfrido morto è mostrato per pezzo e totale.
- Un solo piano operativo; nessuna sezione Alternative/Consigliato.
- Le distinte restano separate per elemento; eliminato il riepilogo finale ridondante.
- Prezzo €/m³ sul volume geometrico netto, senza kerf/rifili/sfridi.

## Nota
Le tavolette del gabbione e gli altri componenti con sezione non ancora formalizzata restano fuori dall'ottimizzatore. I rinforzi restano esclusi dal volume.
